---
name: mercedes-me-render-vehicle-imagery
description: Retrieve Mercedes-Benz vehicle and component imagery, either for a configuration under construction or for a built vehicle by FIN/VIN.
api: Mercedes-Benz Mercedes me Images API
generated: '2026-08-26'
method: generated
source: openapi/mercedes-me-images-api-openapi.yml, openapi/mercedes-me-components-api-openapi.yml, openapi/mercedes-me-perspectives-api-openapi.yml
operations:
  - imageVehicleGET
  - imageComponentsGET
  - imageComponentsEngineGET
  - imageComponentsEquipmentsGET
  - imageComponentsEquipmentsByCodeGET
  - imageComponentsPaintGET
  - imageComponentsRimGET
  - imageComponentsTrimGET
  - imageComponentsUpholsteryGET
---

# Render Mercedes-Benz vehicle imagery

There are **two different image surfaces** and they are keyed differently. Pick the right one first.

| Surface | Key | Base path (sandbox) | Use when |
|---|---|---|---|
| Configurator imagery | `marketId` + `modelId` + `configurationId` | `/configurator_tryout/v1` | The vehicle is a build in progress |
| Vehicle Images API | `finorvin` | `/image_tryout/v1/vehicles` | The vehicle physically exists |

Auth: developer-portal API key as a query parameter.

## A. Imagery for a configuration

1. `imageVehicleGET` →
   `GET /markets/{marketId}/models/{modelId}/configurations/{configurationId}/images/vehicle`
   — the whole-vehicle render.
2. `imageComponentsGET` → `.../images/components` — every component image at once.
3. Narrow to one component family with `imageComponentsEngineGET`, `imageComponentsPaintGET`,
   `imageComponentsRimGET`, `imageComponentsTrimGET`, `imageComponentsUpholsteryGET` or
   `imageComponentsEquipmentsGET` (`.../images/components/engine`, `/paint`, `/rim`, `/trim`,
   `/upholstery`, `/equipments`).
4. For one specific equipment code, `imageComponentsEquipmentsByCodeGET` →
   `.../images/components/equipments/{componentCode}`.

Get the `configurationId` from the `mercedes-me-configure-and-save-vehicle` skill.

## B. Imagery for a built vehicle

1. `imageVehicleGET` → `GET /{finorvin}/vehicle` — whole-vehicle render for a real car.
2. `imageComponentsGET` → `GET /{finorvin}/components` — all component images.
3. Narrow with `GET /{finorvin}/components/engine`, `/equipments`, `/paint`, `/rim`, `/trim`,
   `/upholstery`.

## Rules an agent must follow

- **`204` is a success, not a failure.** The contract states: *"No content could be found for your
  request. The FIN/VIN belongs to a vehicle for which no images are available."* The VIN is valid; there
  is simply no imagery. Report that, do not retry, and do not fall back to guessing another VIN.
- **`404` means the FIN/VIN could not be resolved** — *"Please verify that your FIN/VIN is correct."*
  That is a different condition from `204` and needs a different message to the user.
- Every operation is read-only. Nothing here mutates anything.
- The two surfaces share the `imageVehicleGET` and `imageComponentsGET` **operationIds** but sit at
  different paths under different base paths. Bind by path, not by operationId alone.
- No pagination anywhere; responses return the whole set.
- `429` carries its retry interval in prose in the body only.

See `data-model/mercedes-me-data-model.yml` for why `finorvin` and `configurationId` never resolve to
one another.
