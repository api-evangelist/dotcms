# Superseded scaffold OpenAPIs

The files in this directory were written from the dotCMS **documentation**, not harvested from a
dotCMS server. Their own `info.description` said so: *"Endpoints derived from public dotCMS
documentation at https://dev.dotcms.com/docs — best-effort, not exhaustive."* They carried 19 paths
across seven per-tag splits.

On 2026-09-06 the enrichment pipeline's STEP 0b contract discovery found the **real, first-party
OpenAPI** that every dotCMS instance serves at `/api/openapi.json` — harvested verbatim from
dotCMS's own demo instance to `openapi/dotcms-rest-api-openapi.json`:

- OpenAPI 3.0.1, `info.title: dotCMS REST API`, version `3`
- **592 paths / 754 operations / 606 component schemas / 76 tags**
- source: https://demo.dotcms.com/api/openapi.json (HTTP 200, `application/json`)

The scaffolds are retained here for audit only. Nothing points at them.
