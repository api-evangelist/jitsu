# Jitsu (jitsu)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Jitsu is an open-source, real-time event data pipeline and customer data platform (a Segment alternative). It collects events from websites, apps, and servers and streams them to data warehouses and other destinations. Jitsu is available as MIT-licensed self-hosted software (github.com/jitsucom/jitsu) and as a managed Jitsu Cloud (use.jitsu.com); both expose the same HTTP event ingestion API authenticated with a Write Key.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/jitsu/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/jitsu/refs/heads/main/apis.yml)

## Tags

- Event Data
- CDP
- Data Pipeline
- Analytics
- Open Source
- Ingestion

## Timestamps

- **Created:** 2026-06-21
- **Modified:** 2026-06-21

## APIs

### Jitsu Event Ingestion API (Track / Identify / Page)

Real-time event ingestion endpoint at POST /api/s/{type} (and the server-to-server variant /api/s/s2s/{type}) for page, track, identify, and group events. Payloads follow the Segment-style event shape (type, event, properties, userId, anonymousId, context). Authenticated with a Write Key passed via the X-Write-Key header, HTTP Basic auth, or a writeKey query parameter.

- **Human URL:** [https://jitsu.com/docs/sending-data/http](https://jitsu.com/docs/sending-data/http)
- **Base URL:** `https://use.jitsu.com`

#### Tags

- Event Data
- Ingestion
- Track
- Identify
- Page

#### Properties

- [Documentation](https://jitsu.com/docs/sending-data/http)
- [API Reference](https://jitsu.com/docs/sending-data/http)
- [OpenAPI](openapi/jitsu-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/jitsu.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/jitsu.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Jitsu Bulk / Batch API

Batch ingestion via POST /v1/batch using the Segment-compatible batch envelope (a batch array of events), plus a bulk archive endpoint POST /api/s/bulk that accepts large multipart uploads of events for synchronous loading. Useful for server-side backfills and high-volume sends in a single request.

- **Human URL:** [https://jitsu.com/docs/sending-data/http](https://jitsu.com/docs/sending-data/http)
- **Base URL:** `https://use.jitsu.com`

#### Tags

- Event Data
- Bulk
- Batch
- Ingestion

#### Properties

- [Documentation](https://jitsu.com/docs/sending-data/http)
- [OpenAPI](openapi/jitsu-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/jitsu.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/jitsu.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Jitsu Configuration / Management

Configuration surface for managing workspaces, sites/streams, write keys, destinations, and connections. In self-hosted Jitsu this is backed by the Console application and its configuration store; in Jitsu Cloud it is managed through the use.jitsu.com console. Programmatic management is not a stable, broadly published public REST contract, so it is documented here at the platform level.

- **Human URL:** [https://jitsu.com/docs](https://jitsu.com/docs)
- **Base URL:** `https://use.jitsu.com`

#### Tags

- Configuration
- Management
- Sources
- Destinations
- Connections

#### Properties

- [Documentation](https://jitsu.com/docs)
- [OpenAPI](openapi/jitsu-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [GitHub Organization](https://github.com/jitsucom)
- [LinkedIn](https://www.linkedin.com/company/jitsu-com)
- [Website](https://jitsu.com/)
- [Documentation](https://jitsu.com/docs)
- [Plans](plans/jitsu-plans-pricing.yml)
- [Rate Limits](rate-limits/jitsu-rate-limits.yml)
- [Fin Ops](finops/jitsu-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
