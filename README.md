# Mercedes-Benz Mercedes me

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Mercedes-Benz operates one of the few genuinely public OEM API platforms. Its /developers portal at developer.mercedes-benz.com sells connected-vehicle data as individually-subscribable products — Vehicle Status, Vehicle Lock Status, Fuel Status, Electric Vehicle Status and Pay As You Drive — each gated by its own OAuth 2.0 scope and each requiring the vehicle owner's explicit per-signal consent, granted through the Mercedes-Benz identity provider at id.mercedes-benz.com. Alongside them sit four content and service APIs with published Swagger 2.0 contracts: the Car Configurator, the Dealer API, the Vehicle Images API and Remote Diagnostic Support. Mercedes-Benz Connectivity Services GmbH sells the Fleet API separately, pairing a REST management surface with a managed Apache Kafka push channel that streams nineteen activatable telemetry packages plus five remote-command packages, including remote door lock and unlock. Every API is versioned by URI path and shipped with a *_tryout sandbox base path on the same host.

**Areas:** Automotive · Connected Vehicles · Daimler · Fleet Management · Mercedes me · Mercedes-Benz · OEM · Telematics · Vehicle Data

## Mercedes-Benz Mercedes me on APIs.io

Everything profiled for Mercedes-Benz Mercedes me is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/mercedes-me/](https://apis.io/providers/mercedes-me/)** — or go straight to one of the APIs or properties below.

### APIs (17)

- [Mercedes-Benz Vehicle Status API](https://apis.io/apis/mercedes-me/mercedes-me-vehicle-status-api/) — The Vehicle Status API delivers real-time vehicle state — doors, windows, deck lid, sunroof, tire pressure, and overall lock state — for a…
- [Mercedes-Benz Vehicle Lock Status API](https://apis.io/apis/mercedes-me/mercedes-me-vehicle-lock-status-api/) — The Vehicle Lock Status API returns the current door-lock, deck-lid, and position-lock state of a Mercedes-Benz vehicle by VIN. Designed for parking,…
- [Mercedes-Benz Fuel Status API](https://apis.io/apis/mercedes-me/mercedes-me-fuel-status-api/) — The Fuel Status API exposes a Mercedes-Benz combustion vehicle's current tank level, remaining fuel range in km, and last-update timestamp by VIN. Targeted…
- [Mercedes-Benz Electric Vehicle Status API](https://apis.io/apis/mercedes-me/mercedes-me-electric-vehicle-status-api/) — The Electric Vehicle Status API (currently at v3) provides charge state, state-of-charge percent, remaining electric range in km, charging-active flag, and…
- [Mercedes-Benz Pay As You Drive 2.0 API](https://apis.io/apis/mercedes-me/mercedes-me-pay-as-you-drive-insurance-api/) — The Pay As You Drive 2.0 API supplies precise odometer readings and geographical position for a consented Mercedes-Benz vehicle, designed for usage-based…
- [Mercedes-Benz Fleet API](https://apis.io/apis/mercedes-me/mercedes-benz-fleet-api/) — The Mercedes-Benz Fleet API integrates vehicle data into fleet management systems without retrofit hardware. It splits into a REST Management API (add…
- [Mercedes-Benz Mercedes me Components API](https://apis.io/apis/mercedes-me/mercedes-me-components-api/) — The Components API from Mercedes-Benz Mercedes me — 7 operation(s) for components.
- [Mercedes-Benz Mercedes me Configurations API](https://apis.io/apis/mercedes-me/mercedes-me-configurations-api/) — Select equipment and configure a car
- [Mercedes-Benz Mercedes me Dealer search API](https://apis.io/apis/mercedes-me/mercedes-me-dealer-search-api/) — Resources that provide search functions for dealers (dealer, garage, retailer, etc.) based on given attributes.
- [Mercedes-Benz Mercedes me Diagnostic Trouble Code (DTC) Snapshots API](https://apis.io/apis/mercedes-me/mercedes-me-diagnostic-trouble-code-dtc-snapshots-api/) — Remote Diagnostic Support service for view dtc snapshot List.
- [Mercedes-Benz Mercedes me Diagnostic Trouble Codes (DTC's) API](https://apis.io/apis/mercedes-me/mercedes-me-diagnostic-trouble-codes-dtc-s-api/) — Remote Diagnostic Support service for view dtc List.
- [Mercedes-Benz Mercedes me Electronical Control Units (ECU's) API](https://apis.io/apis/mercedes-me/mercedes-me-electronical-control-units-ecu-s-api/) — Remote Diagnostic Support services for view ecu List.
- [Mercedes-Benz Mercedes me Images API](https://apis.io/apis/mercedes-me/mercedes-me-images-api/) — Get images for the vehicle configuration and its components
- [Mercedes-Benz Mercedes me Perspectives API](https://apis.io/apis/mercedes-me/mercedes-me-perspectives-api/) — The Perspectives API from Mercedes-Benz Mercedes me — 1 operation(s) for perspectives.
- [Mercedes-Benz Mercedes me References API](https://apis.io/apis/mercedes-me/mercedes-me-references-api/) — Provide static reference data about cars like markets, bodies, classes, etc.
- [Mercedes-Benz Mercedes me Resources API](https://apis.io/apis/mercedes-me/mercedes-me-resources-api/) — Remote Diagnostic Support service for view all resources.
- [Mercedes-Benz Mercedes me Saved configurations API](https://apis.io/apis/mercedes-me/mercedes-me-saved-configurations-api/) — Store and load configurations with an onlinecode

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Mercedes Me Fleet Event Catalog](https://apis.io/asyncapis/mercedes-me/mercedes-me-fleet-event-catalog/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Mercedes Me Agentic Access](https://apis.io/agentic-access/mercedes-me/mercedes-me-agentic-access/)

#### JSON Schema (2)

The data models the API reads and writes.

- [Mercedes-Benz DTC Readout](https://apis.io/schemas/mercedes-me/mercedes-me-dtc-readout/)
- [Mercedes-Benz Vehicle Configuration](https://apis.io/schemas/mercedes-me/mercedes-me-vehicle-configuration/)

#### JSON Structure (1)

Data models expressed in JSON Structure.

- [Mercedes Me Vehicle Configuration Structure](https://apis.io/json-structure/mercedes-me/mercedes-me-vehicle-configuration-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Mercedes Me Context](https://apis.io/jsonld/mercedes-me/mercedes-me-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Mercedes-Benz Mercedes me Vocabulary](https://apis.io/vocabularies/mercedes-me/mercedes-me-vocabulary/)

#### Examples (3)

Example requests and responses.

- [Mercedes Me Create Dtc Readout Example](https://apis.io/examples/mercedes-me/mercedes-me-create-dtc-readout-example/)
- [Mercedes Me List Dealers Example](https://apis.io/examples/mercedes-me/mercedes-me-list-dealers-example/)
- [Mercedes Me List Markets Example](https://apis.io/examples/mercedes-me/mercedes-me-list-markets-example/)

#### Collections (15)

Postman and Open Collection request collections.

- [Car Configurator Components API](https://apis.io/collections/mercedes-me/open-mercedes-me-components-api/)
- [Car Configurator Components Configurations API](https://apis.io/collections/mercedes-me/open-mercedes-me-configurations-api/)
- [Car Configurator](https://apis.io/collections/mercedes-me/open-mercedes-me-configurator-api/)
- [Dealer](https://apis.io/collections/mercedes-me/open-mercedes-me-dealer-api/)
- [Car Configurator Components Dealer search API](https://apis.io/collections/mercedes-me/open-mercedes-me-dealer-search-api/)
- [Car Configurator Components Diagnostic Trouble Code (DTC) Snapshots API](https://apis.io/collections/mercedes-me/open-mercedes-me-diagnostic-trouble-code-dtc-snapshots-api/)
- [Car Configurator Components Diagnostic Trouble Codes (DTC's) API](https://apis.io/collections/mercedes-me/open-mercedes-me-diagnostic-trouble-codes-dtc-s-api/)
- [Car Configurator Components Electronical Control Units (ECU's) API](https://apis.io/collections/mercedes-me/open-mercedes-me-electronical-control-units-ecu-s-api/)
- [Car Configurator Components Images API](https://apis.io/collections/mercedes-me/open-mercedes-me-images-api/)
- [Car Configurator Components Perspectives API](https://apis.io/collections/mercedes-me/open-mercedes-me-perspectives-api/)
- [Car Configurator Components References API](https://apis.io/collections/mercedes-me/open-mercedes-me-references-api/)
- [Remote Diagnostic Support](https://apis.io/collections/mercedes-me/open-mercedes-me-remote-diagnostic-support-api/)
- [Car Configurator Components Resources API](https://apis.io/collections/mercedes-me/open-mercedes-me-resources-api/)
- [Car Configurator Components Saved configurations API](https://apis.io/collections/mercedes-me/open-mercedes-me-saved-configurations-api/)
- [Vehicle Image](https://apis.io/collections/mercedes-me/open-mercedes-me-vehicle-images-api/)

#### Overlays (11)

OpenAPI overlays, including conversational phrasing for each operation.

- [Mercedes Me Components Overlay](https://apis.io/overlays/mercedes-me/mercedes-me-components-overlay/)
- [Mercedes Me Configurations Overlay](https://apis.io/overlays/mercedes-me/mercedes-me-configurations-overlay/)
- [Mercedes Me Dealer Search Overlay](https://apis.io/overlays/mercedes-me/mercedes-me-dealer-search-overlay/)
- [Mercedes Me Diagnostic Trouble Code Dtc Snapshots Overlay](https://apis.io/overlays/mercedes-me/mercedes-me-diagnostic-trouble-code-dtc-snapshots-overlay/)
- [Mercedes Me Diagnostic Trouble Codes Dtc S Overlay](https://apis.io/overlays/mercedes-me/mercedes-me-diagnostic-trouble-codes-dtc-s-overlay/)
- [Mercedes Me Electronical Control Units Ecu S Overlay](https://apis.io/overlays/mercedes-me/mercedes-me-electronical-control-units-ecu-s-overlay/)
- [Mercedes Me Images Overlay](https://apis.io/overlays/mercedes-me/mercedes-me-images-overlay/)
- [Mercedes Me Perspectives Overlay](https://apis.io/overlays/mercedes-me/mercedes-me-perspectives-overlay/)
- [Mercedes Me References Overlay](https://apis.io/overlays/mercedes-me/mercedes-me-references-overlay/)
- [Mercedes Me Resources Overlay](https://apis.io/overlays/mercedes-me/mercedes-me-resources-overlay/)
- [Mercedes Me Saved Configurations Overlay](https://apis.io/overlays/mercedes-me/mercedes-me-saved-configurations-overlay/)

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [Mercedes-Benz Mercedes me — jsonschema rules](https://apis.io/rules/mercedes-me/mercedes-me-jsonschema-spectral-rules/)
- [Mercedes-Benz Mercedes me API Rules](https://apis.io/rules/mercedes-me/mercedes-me-rules/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Mercedes Me Authentication](https://apis.io/security/mercedes-me/mercedes-me-authentication/)
- [Mercedes Me Domain Security](https://apis.io/security/mercedes-me/mercedes-me-domain-security/)
- [Mercedes Me Vulnerability Disclosure](https://apis.io/security/mercedes-me/mercedes-me-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Mercedes Me Scopes](https://apis.io/scopes/mercedes-me/mercedes-me-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Mercedes Me Plans Pricing](https://apis.io/plans/mercedes-me/mercedes-me-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Mercedes Me Rate Limits](https://apis.io/rate-limits/mercedes-me/mercedes-me-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Mercedes Me Finops](https://apis.io/finops/mercedes-me/mercedes-me-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Documentation](https://developer.mercedes-benz.com/products)

## API Evangelist rating

**Unrated** — no public website could be reached for this company, so there was almost nothing to measure and nothing a reader could check.

This is not a score of zero. No rating is published for this company. If that is wrong because something public exists that we missed, say so on this repository or email [info@apievangelist.com](mailto:info@apievangelist.com) and it will be re-run — free, and no justification needed.

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Mercedes-Benz Mercedes me: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/mercedes-me/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
