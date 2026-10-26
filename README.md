# University of Florida (university-of-florida)

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

The University of Florida (UF) is a public land-grant research university in Gainesville, Florida, United States, and a member of the Association of American Universities. This repository catalogs UF's public API footprint as an [APIs.json](https://apisjson.org) provider profile, re-profiled on 2026-09-01 under the API Evangelist **university pipeline**, whose first question is never "is there a spec" but **who operates the thing the spec describes**.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/university-of-florida/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=university-of-florida-api-evangelist&utm_content=repo

## Type

- University / Public Research University / Provider / Public

## What UF actually operates

UF is unusual in this cohort. Most universities' apparent APIs turn out to be a vendor's contract running under an institution hostname. UF has two that are genuinely its own, verified by ARIN whois on the resolved address and by TLS issuer rather than by hostname — both inside `128.227.0.0/16` (ARIN NetName **UFNET**, OrgName "University of Florida"), both under Internet2/InCommon certificates UF procures itself, neither with a vendor CNAME.

| Surface | Operator | What it is |
|---|---|---|
| **Schedule of Courses API** — `one.ufl.edu/apix/soc` | `institution` | The JSON backend of ONE.UF. 49 terms, 203 departments, filters for General Education area, meeting day, online delivery, course level — and UF's **AI curriculum designation** as a first-class query parameter (138 of 4,624 Fall 2026 courses). Unauthenticated. Undocumented by UF. |
| **Libraries Patron API** — `api.patron.uflib.ufl.edu` | `institution` | The Smathers Libraries read API behind UF Digital Collections, dLOC and the Florida Digital Newspaper Library. 17 resources: faceted search, OCR page search, geospatial search, MODS citation, serial hierarchy, view statistics, three RSS feeds, and a conformant **OAI-PMH 2.0** repository. Self-documenting — the root returns a machine-readable resource index. |
| **Shibboleth IdP** — `login.ufl.edu/idp/shibboleth` | `federation` | UF's own SAML 2.0 identity provider, registered in InCommon, interfederated into eduGAIN, carrying REFEDS Research & Scholarship and Sirtfi commitments. Self-hosted: no CNAME, UF address space, InCommon certificate. |
| **Campus map JSON** — `campusmap.ufl.edu` | `institution` | Live host, but the WAF returns 403 to every non-browser client. Recorded as blocked, not dead, and not as an available API. |
| **Crossref membership 17357** | `registry` | UF Smathers Libraries, DOI prefix `10.32473`, 14,724 DOIs. A fact about UF, not an API UF runs. |
| **ROR `02y3ad647`** | `registry` | UF's Research Organization Registry entry. |
| **Canvas** — `ufl.instructure.com` | `tenant` | UF's LMS. The teaching data is UF's; the contract is Instructure's and is deliberately not saved here. |
| **CourseLeaf catalog** — `catalog.ufl.edu` | `tenant` | CNAMEs to `ufl-public.courseleaf.com`. Leepfrog's contract. |
| **LiveWhale calendar** — `calendar.ufl.edu` | `tenant` | CNAMEs to `ufl-prod.lwcal.com`. Live iCal feed of real UF events; the contract is the vendor's. |

## Corrections made in the 2026-09-01 re-profile

1. **The OAI-PMH endpoint this profile pointed at was a soft-404.** `ufdc.ufl.edu/sobekcm_oai.aspx` returns **HTTP 200 carrying the UFDC React app shell** — a status-code-only liveness check grades it live, and any harvester aimed at it has been silently collecting nothing since UF migrated off SobekCM. The working OAI-PMH 2.0 repository is on a different host, `api.patron.uflib.ufl.edu/oai`, found by reading the UFDC client's build-time environment module. UF published no 301, no 410, no `Sunset` header and no notice.
2. **`one.ufl.edu/llms.txt` returns 200 and is not an llms.txt** — it is the ONE.UF SPA shell. Not credited.
3. **Two CNAME tenancies the cohort DNS pass had recorded as none** — `catalog.ufl.edu` → CourseLeaf and `calendar.ufl.edu` → LiveWhale. Recorded as tenant relationships rather than deleted; neither vendor's contract is saved here.

## Domain standard conformance (Kin Score `education` regime)

Reward-only, evidenced, institution-operated only:

- **oai-pmh** — conformant. `Identify` names repository "University of Florida Digital Collections", repositoryIdentifier `UFDC`, protocolVersion 2.0, earliest datestamp 2007-08-07; formats `oai_dc` **and MODS 3.7**.
- **shibboleth** — conformant. Shibboleth 1.0 profile endpoint and `shibmd:Scope = ufl.edu` in signed InCommon metadata.
- **saml** — conformant. SAML 2.0 POST/Redirect SSO, artifact resolution, attribute authority; REFEDS R&S and Sirtfi entity categories.
- **crossref** — registered (member 17357).
- **Not found, probed:** datacite (zero results — UF is not a DataCite member), orcid, oneroster, caliper, qti, ed-fi, scim.
- **lti** — vendor only. Canvas is LTI-certified; that is Instructure's engineering and is not credited to UF.

## Artifacts

- `openapi/` (+ `openapi/_original/`) — two derived contracts, every parameter individually verified against live responses
- `json-schema/` — response schemas derived from those contracts
- `examples/` — verbatim live responses, truncated and with the caller-IP field the libraries API echoes back removed
- `errors/` — the probed error envelopes, and the **silent-failure modes**: an unrecognised `term` returns 200 with an empty result set, and unknown parameters are ignored rather than rejected
- `rules/` — consumption rules an agent needs so those silent failures do not become confidently wrong answers
- `vocabulary/` — term codes, department codes, General Education letters, bibid/vid identifier forms, OAI metadata prefixes
- `authentication/`, `lifecycle/`, `conformance/`, `identity-federation/` (with the signed InCommon metadata archived locally)

## What UF does not publish

No developer portal. No API documentation for either API it runs. No versioning of any kind — no URL segment, no header, no payload field. No changelog, no deprecation policy, no status page, no rate-limit signal, no `429`, no terms of use, no licence and no attribution requirement. No open data portal: `data.ufl.edu` redirects an unauthenticated caller straight to GatorLink SSO. No `security.txt`. The `UniversityofFlorida` GitHub organization holds three repositories, none touched since 2018.

## Plans, Rate Limits, FinOps

- [plans/university-of-florida-plans-pricing.yml](plans/university-of-florida-plans-pricing.yml)
- [rate-limits/university-of-florida-rate-limits.yml](rate-limits/university-of-florida-rate-limits.yml)
- [finops/university-of-florida-finops.yml](finops/university-of-florida-finops.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-09-01

## Notes

Every URL in this profile was probed on 2026-09-01 and every pointer was checked live. Bodies were read, not just status codes — which is how both soft-404s above were caught. Gated identity, SIS and enterprise integration APIs behind UFIT authentication are excluded. Nothing was fabricated, and no vendor contract is saved under UF's name.

## Maintainers

- Kin Lane — kin@apievangelist.com
