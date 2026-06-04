# University of Florida (university-of-florida)

The University of Florida (UF) is a public land-grant research university in Gainesville, Florida, United States, ranked #215 in the QS World University Rankings 2025. This repository catalogs UF's public developer and API footprint as an [APIs.json](https://apisjson.org) provider profile. UF has no single centralized public developer portal; this profile aggregates the public and community-documented data endpoints that could be verified.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/university-of-florida/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=university-of-florida-api-evangelist&utm_content=repo

## Type

- Index / Consumer / 3rd-Party

## Tags

Education, Higher Education, University, Courses, Digital Collections, Open Data, United States

## APIs

- **UF Schedule of Courses (SOC) API** — public JSON course schedule, filterable by term, category, course code, instructor and day. Docs: https://github.com/Rolstenhouse/uf_api (base: `https://one.ufl.edu/apix/soc/schedule/`)
- **UF Campus Map JSON Data** — JSON datasets for buildings, bus stops, dining, parking and housing. Docs: https://github.com/Rolstenhouse/uf_api (base: `https://campusmap.ufl.edu/library/cmapjson/`)
- **UF Digital Collections (UFDC) Metadata Feeds** — OAI-PMH and RSS metadata feeds over 18M+ digital objects; OpenAPI API forthcoming. Docs: https://lts.uflib.ufl.edu/supported-systems/uf-digital-collections/

## Plans

- [plans/university-of-florida-plans-pricing.yml](plans/university-of-florida-plans-pricing.yml)

## Rate Limits

- [rate-limits/university-of-florida-rate-limits.yml](rate-limits/university-of-florida-rate-limits.yml)

## FinOps

- [finops/university-of-florida-finops.yml](finops/university-of-florida-finops.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-06-03

## Common Properties

- Website: https://www.ufl.edu/
- GitHub: https://github.com/UniversityofFlorida
- LinkedIn: https://www.linkedin.com/school/university-of-florida/
- Plans, Rate Limits, FinOps, and Review pointers (see files above)

## Notes

All endpoints were probed on 2026-06-03. The SOC API returns live course JSON (HTTP 200) when called with a term parameter; the campus map JSON host responds but blocks automated/non-browser clients (HTTP 403); UFDC OAI-PMH/RSS feeds are documented by UF Library Technology Services with an OpenAPI (Swagger) API noted as forthcoming. The SOC and campus map APIs are community documented (Rolstenhouse/uf_api), not officially published by UF. Gated identity, SIS and enterprise integration APIs behind UFIT authentication are excluded. No endpoints were fabricated.

## Maintainers

- Kin Lane — kin@apievangelist.com
