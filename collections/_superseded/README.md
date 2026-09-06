# Superseded collections

Every file here was **derived from the scaffold OpenAPIs** now retired to `openapi/_superseded/` —
documentation-shaped specs of 19 paths total, not harvested from a dotCMS server. They describe a
dotCMS API that does not match the one dotCMS actually serves.

On 2026-09-06 the real first-party contract was harvested to
`openapi/dotcms-rest-api-openapi.json` (592 paths / 754 operations, from
`https://demo.dotcms.com/api/openapi.json`). These collections were not regenerated against it in
that pass; they are kept for audit only and nothing points at them.

Regenerating Postman/OpenCollection artifacts from the real spec is the obvious follow-up.
