---
name: mercedes-me-find-dealer
description: Find Mercedes-Benz dealers, garages and retailers by attribute and read their services, opening hours and location.
api: Mercedes-Benz Mercedes me Dealer search API
generated: '2026-08-26'
method: generated
source: openapi/mercedes-me-dealer-search-api-openapi.yml, openapi/mercedes-me-references-api-openapi.yml
operations:
  - countriesGET
  - dealersGET
  - dealerGET
---

# Find a Mercedes-Benz dealer

Base host `https://api.mercedes-benz.com`. Sandbox base path `/dealer_tryout/v1`; production
`/dealer/v1`. Auth: developer-portal API key as a query parameter.

## Steps

1. **Scope by country.** `countriesGET` → `GET /countries`. Returns the countries the dealer network
   covers. Use this to validate a country before searching — do not assume an ISO code is supported.
2. **Search.** `dealersGET` → `GET /dealers`, narrowed by the search attributes the operation accepts.
   This endpoint has **no page/limit/offset parameter**: you narrow with the query, not with paging. A
   broad search returns a broad result set in one response, so filter deliberately.
3. **Read one dealer.** `dealerGET` → `GET /dealers/{dealerId}`. The `Dealer` object carries:
   - `address` (`Address`) and `geoCoordinates` (`GeoCoordinates`)
   - `functions[]` (`Function`) — what the site actually does: sales, service, parts. A "dealer" in this
     API is not necessarily a showroom.
   - `openingHours[]` (`FunctionOpeningHours`) — hours are attached **per function**, not per dealer.
     A site can sell on Saturday and service only on weekdays. Read the hours for the function you care
     about, never the first entry in the array.
   - `communication` (`CommunicationChannels`), `brandCodes[]`, `region`, and `distance` when the search
     was geographic.

## Rules an agent must follow

- Read-only. Nothing here writes.
- Opening hours are per function. Answering "is this dealer open" without naming the function is wrong.
- `brandCodes[]` matters: Mercedes-Benz sites can carry more than one Mercedes-Benz Group brand. Check it
  before telling a user a site handles their vehicle.
- No pagination. If the result set is unusably large, add search attributes; do not attempt to page.
- `429` carries its retry interval in prose in the body; there is no `Retry-After` header.
- There is no request id in any response or error, so nothing can be quoted in a support ticket.
