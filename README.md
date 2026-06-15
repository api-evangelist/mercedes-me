# Mercedes-Benz Mercedes me (mercedes-me)

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/mercedes-me/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/mercedes-me/refs/heads/main/apis.yml)

## Scope

- **Access:** 3rd-Party

## Tags

- Automotive
- Connected Car
- Connected Vehicle
- Daimler
- Fleet Management
- Mercedes me
- Mercedes-Benz
- OEM
- Telematics
- Vehicle Data

## APIs

### Mercedes-Benz Car Configurator API

The Car Configurator API offers programmatic access to Mercedes-Benz vehicle configuration functions. It exposes reference data (markets, classes, bodies, models) and the configuration engine so apps can build interactive configurators, retrieve images for any configuration state, and save/share configurations via an online code.

- **Human URL:** [https://developer.mercedes-benz.com/products/configurator](https://developer.mercedes-benz.com/products/configurator)
- **Base URL:** `https://api.mercedes-benz.com/configurator/v1`

#### Tags

- Automotive
- Configurator
- Connected Vehicle
- Mercedes-Benz
- Vehicle Reference Data

#### Properties

- [Documentation](https://developer.mercedes-benz.com/products/configurator)
- [Documentation](https://developer.mercedes-benz.com/products/configurator/docs)
- [OpenAPI](openapi/mercedes-me-configurator-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/mercedes-me-configurator-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-configurator-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/mercedes-me-vehicle-configuration-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/mercedes-me-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Mercedes-Benz Dealer API

The Dealer API exposes Mercedes-Benz authorized dealer locations worldwide with filtering by country, geo radius, services offered, opening hours, and dealer brand. It powers dealer-locator widgets, service-booking flows, and OEM marketing surfaces.

- **Human URL:** [https://developer.mercedes-benz.com/products/dealer](https://developer.mercedes-benz.com/products/dealer)
- **Base URL:** `https://api.mercedes-benz.com/dealer/v1`

#### Tags

- Automotive
- Dealer Locator
- Mercedes-Benz
- Retail

#### Properties

- [Documentation](https://developer.mercedes-benz.com/products/dealer)
- [OpenAPI](openapi/mercedes-me-dealer-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/mercedes-me-dealer-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-dealer-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Mercedes-Benz Vehicle Images API

The Vehicle Images API provides original Mercedes-Benz exterior, interior, and component imagery keyed by FIN/VIN. It supports perspective and day/night modifiers and exposes component-level images for engine, paint, rim, trim, upholstery, and individual equipments.

- **Human URL:** [https://developer.mercedes-benz.com/products/vehicle_images](https://developer.mercedes-benz.com/products/vehicle_images)
- **Base URL:** `https://api.mercedes-benz.com/vehicle_images/v1/vehicles`

#### Tags

- Automotive
- Imagery
- Mercedes-Benz
- Vehicle Reference Data

#### Properties

- [Documentation](https://developer.mercedes-benz.com/products/vehicle_images)
- [OpenAPI](openapi/mercedes-me-vehicle-images-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/mercedes-me-vehicle-images-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-vehicle-images-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Mercedes-Benz Remote Diagnostic Support API

The Remote Diagnostic Support API lets authorized third parties (e.g. roadside assistance, fleet operators, dealerships) read Diagnostic Trouble Codes, ECU inventories, DTC snapshots, and available resource readouts from a Mercedes-Benz vehicle on behalf of the customer. All endpoints take a VIN/FIN as the vehicle identifier and support async polling.

- **Human URL:** [https://developer.mercedes-benz.com/products/remote_diagnostic_support](https://developer.mercedes-benz.com/products/remote_diagnostic_support)
- **Base URL:** `https://api.mercedes-benz.com/remotediagnostic/v1`

#### Tags

- Automotive
- Connected Vehicle
- Diagnostics
- DTC
- ECU
- Mercedes-Benz
- Telematics

#### Properties

- [Documentation](https://developer.mercedes-benz.com/products/remote_diagnostic_support)
- [OpenAPI](openapi/mercedes-me-remote-diagnostic-support-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/mercedes-me-remote-diagnostic-support-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-remote-diagnostic-support-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/mercedes-me-dtc-readout-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Mercedes-Benz Vehicle Status API

The Vehicle Status API delivers real-time vehicle state — doors, windows, deck lid, sunroof, tire pressure, and overall lock state — for a customer-consented Mercedes-Benz vehicle by VIN. Returns last-known timestamps and uses the standard Mercedes-Benz OAuth 2.0 customer-consent flow.

- **Human URL:** [https://developer.mercedes-benz.com/products/vehicle_status](https://developer.mercedes-benz.com/products/vehicle_status)

#### Tags

- Automotive
- Connected Vehicle
- Mercedes me
- Mercedes-Benz
- Telematics
- Vehicle Status

#### Properties

- [Documentation](https://developer.mercedes-benz.com/products/vehicle_status)
- [Documentation](https://developer.mercedes-benz.com/products/vehicle_status/docs)
- [Postman Collection](collections/mercedes-me-configurator-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-configurator-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/mercedes-me-dealer-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-dealer-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/mercedes-me-remote-diagnostic-support-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-remote-diagnostic-support-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/mercedes-me-vehicle-images-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-vehicle-images-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Mercedes-Benz Vehicle Lock Status API

The Vehicle Lock Status API returns the current door-lock, deck-lid, and position-lock state of a Mercedes-Benz vehicle by VIN. Designed for parking, insurance, and security-monitoring use cases that need a minimal lock-only surface separate from full Vehicle Status.

- **Human URL:** [https://developer.mercedes-benz.com/products/vehicle_lock_status](https://developer.mercedes-benz.com/products/vehicle_lock_status)

#### Tags

- Automotive
- Connected Vehicle
- Lock Status
- Mercedes me
- Mercedes-Benz
- Telematics

#### Properties

- [Documentation](https://developer.mercedes-benz.com/products/vehicle_lock_status)
- [Documentation](https://developer.mercedes-benz.com/products/vehicle_lock_status/docs)
- [Postman Collection](collections/mercedes-me-configurator-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-configurator-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/mercedes-me-dealer-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-dealer-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/mercedes-me-remote-diagnostic-support-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-remote-diagnostic-support-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/mercedes-me-vehicle-images-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-vehicle-images-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Mercedes-Benz Fuel Status API

The Fuel Status API exposes a Mercedes-Benz combustion vehicle's current tank level, remaining fuel range in km, and last-update timestamp by VIN. Targeted at fueling, fleet, and concierge integrations.

- **Human URL:** [https://developer.mercedes-benz.com/products/fuel_status](https://developer.mercedes-benz.com/products/fuel_status)

#### Tags

- Automotive
- Connected Vehicle
- Fuel
- Mercedes me
- Mercedes-Benz
- Telematics

#### Properties

- [Documentation](https://developer.mercedes-benz.com/products/fuel_status)
- [Documentation](https://developer.mercedes-benz.com/products/fuel_status/docs)
- [Postman Collection](collections/mercedes-me-configurator-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-configurator-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/mercedes-me-dealer-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-dealer-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/mercedes-me-remote-diagnostic-support-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-remote-diagnostic-support-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/mercedes-me-vehicle-images-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-vehicle-images-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Mercedes-Benz Electric Vehicle Status API

The Electric Vehicle Status API (currently at v3) provides charge state, state-of-charge percent, remaining electric range in km, charging-active flag, and time-to-full estimates for Mercedes-EQ and EV-mode plug-in hybrid vehicles. v2 also adds remote charge start/stop commands.

- **Human URL:** [https://developer.mercedes-benz.com/products/electric_vehicle_status_3](https://developer.mercedes-benz.com/products/electric_vehicle_status_3)

#### Tags

- Automotive
- Charging
- Connected Vehicle
- Electric Vehicle
- EV
- Mercedes me
- Mercedes-Benz
- Telematics

#### Properties

- [Documentation](https://developer.mercedes-benz.com/products/electric_vehicle_status_3)
- [Documentation](https://developer.mercedes-benz.com/products/electric_vehicle_status_2/docs)
- [Postman Collection](collections/mercedes-me-configurator-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-configurator-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/mercedes-me-dealer-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-dealer-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/mercedes-me-remote-diagnostic-support-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-remote-diagnostic-support-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/mercedes-me-vehicle-images-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-vehicle-images-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Mercedes-Benz Pay As You Drive 2.0 API

The Pay As You Drive 2.0 API supplies precise odometer readings and geographical position for a consented Mercedes-Benz vehicle, designed for usage-based insurance, mileage-based subscriptions, and PAYD underwriting workflows.

- **Human URL:** [https://developer.mercedes-benz.com/products/pay_as_you_drive_insurance_2](https://developer.mercedes-benz.com/products/pay_as_you_drive_insurance_2)

#### Tags

- Automotive
- Connected Vehicle
- Geolocation
- Insurance
- Mercedes me
- Mercedes-Benz
- Odometer
- Telematics
- Usage-Based Insurance

#### Properties

- [Documentation](https://developer.mercedes-benz.com/products/pay_as_you_drive_insurance_2)
- [Documentation](https://developer.mercedes-benz.com/products/pay_as_you_drive_insurance_2/docs)
- [Postman Collection](collections/mercedes-me-configurator-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-configurator-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/mercedes-me-dealer-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-dealer-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/mercedes-me-remote-diagnostic-support-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-remote-diagnostic-support-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/mercedes-me-vehicle-images-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-vehicle-images-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Mercedes-Benz Fleet API

The Mercedes-Benz Fleet API integrates vehicle data into fleet management systems without retrofit hardware. It splits into a REST Management API (add vehicles, activate/deactivate per-vehicle data packages, issue remote commands) and a Kafka Push API that streams location, mileage, fuel/charge, vehicle health, tires, door/window status, driving behavior, and anti-theft events. Packages are activated individually at vehicle level.

- **Human URL:** [https://developer.mercedes-benz.com/products/mercedes-benz_fleet_api](https://developer.mercedes-benz.com/products/mercedes-benz_fleet_api)

#### Tags

- Automotive
- Connected Vehicle
- Fleet Management
- Kafka
- Mercedes-Benz
- Streaming
- Telematics

#### Properties

- [Documentation](https://developer.mercedes-benz.com/products/mercedes-benz_fleet_api)
- [Documentation](https://connectivity.mercedes-benz.com/products/mercedes-benz-fleet-api)
- [SDK](https://github.com/mercedes-benz/kafka-integration-samples)
- [Postman Collection](collections/mercedes-me-configurator-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-configurator-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/mercedes-me-dealer-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-dealer-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/mercedes-me-remote-diagnostic-support-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-remote-diagnostic-support-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/mercedes-me-vehicle-images-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mercedes-me-vehicle-images-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Portal](https://developer.mercedes-benz.com/)
- [Documentation](https://developer.mercedes-benz.com/products)
- [SDK](https://developer.mercedes-benz.com/sdks)
- [SDK](https://github.com/mercedes-benz/MBSDK-Mobile-Android)
- [SDK](https://github.com/mercedes-benz/MBSDK-Mobile-iOS)
- [SDK](https://github.com/mercedes-benz/MBSDK-community-support)
- [SDK](https://github.com/mercedes-benz/kafka-integration-samples)
- [Git Hub](https://github.com/mercedes-benz)
- [Git Hub](https://github.com/mercedes-benz/foss)
- [Git Hub](https://github.com/mercedes-benz/mercedes-benz-foss-manifesto)
- [Postman](https://www.postman.com/mbdevelopers/mercedes-benz/overview) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Connectivity](https://connectivity.mercedes-benz.com/)
- [Connectivity](https://data.mercedes-benz.com/)
- [LinkedIn](https://www.linkedin.com/company/mercedes-benz-ag/)
- [Twitter](https://twitter.com/MercedesBenz)
- [Consumer App](https://www.mbusa.com/en/mercedes-benz-app)
- [Payments](https://group.mercedes-benz.com/innovations/digitalisation/connectivity/mercedes-pay.html)
- [Payments](https://www.mercedes-benz-mobility.com/en/what-we-do/payment-services/)
- [Vocabulary](vocabulary/mercedes-me-vocabulary.yml)
- [Spectral Rules](rules/mercedes-me-rules.yml)
- [Plans](plans/mercedes-me-plans-pricing.yml)
- [Rate Limits](rate-limits/mercedes-me-rate-limits.yml)
- [Fin Ops](finops/mercedes-me-finops.yml)
