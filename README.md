# Mercedes-Benz Mercedes me

API Evangelist profile of the [Mercedes-Benz /developers](https://developer.mercedes-benz.com/) API platform — the public developer portal that exposes Mercedes-Benz vehicle reference data, the Car Configurator, the Dealer Locator, the Vehicle Images service, the Remote Diagnostic Support API, the Mercedes me connected-vehicle product family (Vehicle Status, Vehicle Lock Status, Fuel Status, Electric Vehicle Status, Pay As You Drive 2.0), and the Mercedes-Benz Fleet API (Management REST + Kafka Push) from Mercedes-Benz Connectivity Services.

This repo follows the [api-evangelist](https://github.com/api-evangelist) profiling convention.

- Provider: Mercedes-Benz Group AG
- Portal: https://developer.mercedes-benz.com/
- Fleet portal: https://connectivity.mercedes-benz.com/products/mercedes-benz-fleet-api
- GitHub org: https://github.com/mercedes-benz
- FOSS landing: https://github.com/mercedes-benz/foss

## Repo Layout

| Folder | Contents |
|---|---|
| [`apis.yml`](apis.yml) | APIs.json catalog entry — 10 APIs across reference data, imagery, diagnostics, connected vehicle, and fleet |
| [`openapi/`](openapi/) | OpenAPI / Swagger 2.0 specs for the four publicly-documented APIs (Configurator, Dealer, Vehicle Images, Remote Diagnostic Support) |
| [`capabilities/`](capabilities/) | Naftiko capability definitions — one per logical business surface across the four spec'd APIs |
| [`json-schema/`](json-schema/) | JSON Schemas for the Vehicle Configuration and DTC Readout entities |
| [`json-structure/`](json-structure/) | Capability-oriented JSON Structure describing the Mercedes me entity model |
| [`json-ld/`](json-ld/) | JSON-LD context mapping Mercedes me concepts to schema.org + a Mercedes-Benz vocabulary namespace |
| [`examples/`](examples/) | Concrete request/response examples for representative operations |
| [`rules/`](rules/) | Spectral ruleset enforcing Mercedes-Benz's host, HTTPS, error-code, and operationId conventions |
| [`vocabulary/`](vocabulary/) | Operational + capability vocabulary for the Mercedes me surface |
| [`plans/`](plans/) | API Commons Plans 0.1 view of Mercedes-Benz commercial tiers |
| [`rate-limits/`](rate-limits/) | API Commons Rate Limits 0.1 view of Mercedes-Benz quota policies |
| [`finops/`](finops/) | FOCUS-aligned FinOps view of the Mercedes-Benz billing surface |

## APIs Profiled

| ID | Name | OpenAPI |
|---|---|---|
| `mercedes-me-car-configurator-api` | Car Configurator API | [yes](openapi/mercedes-me-configurator-api-openapi.yml) |
| `mercedes-me-dealer-api` | Dealer API | [yes](openapi/mercedes-me-dealer-api-openapi.yml) |
| `mercedes-me-vehicle-images-api` | Vehicle Images API | [yes](openapi/mercedes-me-vehicle-images-api-openapi.yml) |
| `mercedes-me-remote-diagnostic-support-api` | Remote Diagnostic Support API | [yes](openapi/mercedes-me-remote-diagnostic-support-api-openapi.yml) |
| `mercedes-me-vehicle-status-api` | Vehicle Status API | docs only |
| `mercedes-me-vehicle-lock-status-api` | Vehicle Lock Status API | docs only |
| `mercedes-me-fuel-status-api` | Fuel Status API | docs only |
| `mercedes-me-electric-vehicle-status-api` | Electric Vehicle Status 3.0 API | docs only |
| `mercedes-me-pay-as-you-drive-insurance-api` | Pay As You Drive 2.0 API | docs only |
| `mercedes-benz-fleet-api` | Mercedes-Benz Fleet API (REST + Kafka) | docs only |

The four "yes" specs are real Swagger 2.0 definitions mirrored from the APIs-guru/openapi-directory (originally published by Mercedes-Benz under the `_tryout` sandbox basePaths). Connected-vehicle products are documented via `humanURL` only because the Mercedes developer portal renders specifications behind a JavaScript SPA — no machine-readable spec is exposed at a public URL.

## Capabilities

The Naftiko capabilities cover the spec'd APIs as a set of business surfaces:

- `configurator-references` — markets, classes, bodies, models
- `configurator-configurations` — initial state, by-id, alternatives, selectables, product groups
- `configurator-images` — vehicle + component renders for a configuration
- `configurator-saved-configurations` — online-code save/restore
- `dealer-dealers` — dealer locator (countries + search + by-id)
- `vehicle-images-vehicle` — full vehicle imagery by VIN/FIN
- `vehicle-images-components` — component imagery by VIN/FIN
- `remote-diagnostic-support-readouts` — DTC, DTC snapshot, ECU, and resource readouts

Each capability exposes both a REST adapter and an MCP adapter so consumers can call Mercedes-Benz operations via traditional HTTP or as agent tools.

## Notes On The Mercedes-Benz Developer Surface

1. **Product-style API platform.** Every API is a "product" with its own docs, specs, details, console, and pricing — a clean OEM API platform pattern.
2. **OAuth 2.0 customer consent.** Connected-vehicle APIs use a Mercedes-Benz-hosted OAuth flow where the vehicle owner explicitly grants per-resource consent (lock, fuel, charge, odometer, position, tires).
3. **VIN/FIN-keyed.** All vehicle-facing operations use VIN/FIN as the vehicle identifier.
4. **Async-polling diagnostics.** Remote Diagnostic Support returns 202 + readoutId with a polling URL, recognising that ECU reads aren't immediate.
5. **Sandbox-by-basePath.** Every spec ships with a `*_tryout` basePath for free sandbox use against synthetic data.
6. **Quota-by-API-key.** Every operation documents 429 "Quota limit is exceeded" — quota is per API key, per product, with exact limits set by subscription contract.
7. **Fleet via Kafka.** The Fleet API splits into REST (Management) and Kafka (Push); Mercedes-Benz publishes an OAuth-aware [Kafka samples repo](https://github.com/mercedes-benz/kafka-integration-samples).
8. **Mobile SDKs archived.** The native [iOS](https://github.com/mercedes-benz/MBSDK-Mobile-iOS) and [Android](https://github.com/mercedes-benz/MBSDK-Mobile-Android) Mobile SDK modules and the [community-support](https://github.com/mercedes-benz/MBSDK-community-support) repo were archived in 2021; Mercedes-Benz now directs SDK users back to the developer portal.

## License

This profile aggregates public information about Mercedes-Benz's developer surface for the API Evangelist research project. All Mercedes-Benz trademarks, API names, and specification text remain the property of Mercedes-Benz Group AG. Specs in `openapi/` originate from the Apache-2.0-licensed [APIs-guru/openapi-directory](https://github.com/APIs-guru/openapi-directory).
