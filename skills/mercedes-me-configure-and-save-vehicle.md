---
name: mercedes-me-configure-and-save-vehicle
description: Configure a Mercedes-Benz vehicle from market reference data and persist it as a shareable online code, using the Car Configurator API.
api: Mercedes-Benz Mercedes me Configurations API
generated: '2026-08-26'
method: generated
source: openapi/mercedes-me-references-api-openapi.yml, openapi/mercedes-me-configurations-api-openapi.yml, openapi/mercedes-me-saved-configurations-api-openapi.yml
operations:
  - marketsGET
  - modelsGET
  - modelGET
  - modelConfigurationsGET
  - modelConfigurationSelectablesGET
  - modelConfigurationAlternativesGET
  - modelConfigurationGET
  - onlineCodePOST
  - onlineCodeGET
---

# Configure a Mercedes-Benz vehicle and save it

Base host `https://api.mercedes-benz.com`. Sandbox base path `/configurator_tryout/v1`; production
`/configurator/v1`. Auth: developer-portal API key as a query parameter — the parameter name is documented
only on developer.mercedes-benz.com, so obtain it from the product page before running this skill.

Everything below is keyed by a `marketId`. There is no global model list.

## Steps

1. **Pick a market.** `marketsGET` → `GET /markets`. Returns every market the configurator supports.
   Take the `marketId` you need. There is no pagination — the full list comes back.
2. **List models in that market.** `modelsGET` → `GET /markets/{marketId}/models`. Optionally narrow
   first with `classesGET` (`/markets/{marketId}/classes`), `bodiesGET` (`/markets/{marketId}/bodies`)
   or `productGroupsGET` (`/markets/{marketId}/productgroups`).
3. **Read the model.** `modelGET` → `GET /markets/{marketId}/models/{modelId}`. The response carries
   `vehicleClass`, `vehicleBody`, `productGroup` and `priceInformation`.
4. **Get the starting configuration.** `modelConfigurationsGET` →
   `GET /markets/{marketId}/models/{modelId}/configurations/initial`. This is the default build. Keep the
   `configurationId`.
5. **See what can still be changed.** `modelConfigurationSelectablesGET` →
   `GET /markets/{marketId}/models/{modelId}/configurations/{configurationId}/selectables`.
6. **Apply a change.** `modelConfigurationAlternativesGET` →
   `GET /markets/{marketId}/models/{modelId}/configurations/{configurationId}/alternatives/{componentList}`.
   Note the shape: changing the build is a **GET**, and it returns a NEW `configurationId`. Nothing is
   mutated server-side. Repeat this step, carrying the new id forward, until the build is what you want.
7. **Read the final build.** `modelConfigurationGET` →
   `GET /markets/{marketId}/models/{modelId}/configurations/{configurationId}`. Carries
   `initialPrice`, `configurationPrice`, `technicalInformation` and `vehicleComponents[]`.
8. **Persist it.** `onlineCodePOST` → `POST /markets/{marketId}/onlinecode`. Returns an `onlineCode`.
9. **Reload it later.** `onlineCodeGET` → `GET /markets/{marketId}/onlinecode/{onlineCode}`.

## Rules an agent must follow

- **Step 8 is the only write, and it is not idempotent.** There is no `Idempotency-Key` header on this
  API. If the POST times out and you retry, you will create a **second** online code. Treat a timeout as
  ambiguous, not as a failure.
- **There is no delete and no published expiry for an online code.** Mercedes-Benz does not state how long
  a saved configuration lives or whether it can be revoked. Do not tell a user it can be undone.
- **Validate ids before you call.** A bad `marketId` or `modelId` returns `400` with
  `"Invalid parameter was specified: * MarketId is not valid * ModelId is not valid"`. Resolve ids from
  steps 1–2 rather than guessing.
- **On `429`** the body reads `"Rate limit is exceeded. Try again in NN seconds."` There is **no**
  `Retry-After` header and **no** `RateLimit-*` headers — parse the interval out of the message and sleep.
- **On `500`** the message conflates an upstream failure with a server fault. Retry with backoff; do not
  report it to the user as a bad request.
- Errors are **not** RFC 9457. Expect `{"errorMessage", "statusCode", "message"}`, and note that
  `statusCode` is a string on 401 and an integer on 429.
- Responses are HAL-shaped (`_links`, `SelfLink`, `DefaultLinks`) but served as `application/json`, not
  `application/hal+json`. Do not rely on HAL content negotiation.

See `conventions/mercedes-me-conventions.yml` and `errors/mercedes-me-problem-types.yml`.
