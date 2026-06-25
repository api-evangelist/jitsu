# Jitsu (jitsu)

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
