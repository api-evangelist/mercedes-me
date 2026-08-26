---
name: mercedes-me-remote-diagnostic-readout
description: Run an asynchronous remote diagnostic readout against a Mercedes-Benz vehicle — ECU inventory, diagnostic trouble codes, DTC snapshots and resource data.
api: Mercedes-Benz Mercedes me Resources API
generated: '2026-08-26'
method: generated
source: openapi/mercedes-me-electronical-control-units-ecu-s-api-openapi.yml, openapi/mercedes-me-diagnostic-trouble-codes-dtc-s-api-openapi.yml, openapi/mercedes-me-diagnostic-trouble-code-dtc-snapshots-api-openapi.yml, openapi/mercedes-me-resources-api-openapi.yml
operations:
  - getEcuDataListByVehicleIdUsingPOST
  - getDtcDataListByEcuUsingPOST
  - getDtcSnapshotReadoutsUsingPOST
  - getResourceReadoutsUsingPOST
---

# Run a Mercedes-Benz remote diagnostic readout

Base host `https://api.mercedes-benz.com`. Sandbox base path `/remotediagnostic_tryout/v1`; production
`/remotediagnostic/v1`. Auth: developer-portal API key; the connected-vehicle scope for this product is
`mb:vehicle:rds:reader`.

**Read this before calling anything.** Every operation in this skill is a `POST` that starts a job
against a **real vehicle**. They are named "readouts" and they return data, but they are writes: they
create work, they are asynchronous, they are **not idempotent**, and Mercedes-Benz publishes **no
operation to cancel one**.

## Steps

1. **Inventory the control units.** `getEcuDataListByVehicleIdUsingPOST` →
   `POST /vehicles/{vehicleId}/ecuReadouts`. Returns `EcuDataItem` entries. Keep the `ecuId` values.
2. **Read the trouble codes.** `getDtcDataListByEcuUsingPOST` →
   `POST /vehicles/{vehicleId}/dtcReadouts`. Returns `DtcDataItem` entries. The `dtcStatus` parameter
   narrows the result.
3. **Pull a snapshot for one code.** `getDtcSnapshotReadoutsUsingPOST` →
   `POST /vehicles/{vehicleId}/ecuId/{ecuId}/dtcId/{dtcId}/dtcSnapshotReadouts`. This is the freeze-frame
   data captured when the fault occurred. It needs the `ecuId` from step 1 and the `dtcId` from step 2 —
   you cannot skip to it.
4. **Read resource data.** `getResourceReadoutsUsingPOST` →
   `POST /vehicles/{vehicleId}/resourceReadouts`.

## Rules an agent must follow

- **`202 Accepted` means the job is not finished.** Do not treat a 202 body as the result. Poll.
- **Never retry a `POST` blindly.** No idempotency key exists. A retry starts a second readout against
  the car. On a timeout, poll for the existing job rather than re-posting.
- **There is no cancel.** Once started, a readout cannot be called back through the API. Confirm intent
  with the human before step 1 if the vehicle belongs to a customer.
- **`vehicleId` is not documented as being the same value as `finorvin`.** The Vehicle Images API keys on
  `finorvin`; this API keys on `vehicleId`. Mercedes-Benz does not state in the contract that they are
  interchangeable. Do not pass one where the other is expected on the assumption they match.
- **`402 Payment required` is a real response here.** It means the subscription covering Remote Diagnostic
  Support is not active — an entitlement problem, not a request problem. Do not retry it.
- **`403`** means the credential is valid but not entitled to this vehicle. **`501`** means the capability
  is not available for this vehicle. Neither is retryable.
- `429` carries its retry interval in prose in the body only. `500` conflates a vehicle-offline condition
  with a platform fault — retry with backoff.
- Diagnostic data is personal vehicle data. Handle it under the consent the vehicle owner granted and
  nothing wider. See `scopes/mercedes-me-scopes.yml`.
