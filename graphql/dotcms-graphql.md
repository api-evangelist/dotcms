# dotCMS GraphQL API

The dotCMS GraphQL API provides a single endpoint for querying content across all content types using a self-documenting schema. It supports Lucene-style query strings, pagination, sorting, and content-type collections, and exposes base types for File, Form, Key/Value, Page, Persona, Vanity URL, and Widget content. The API accepts the same authentication methods as the dotCMS REST API and includes a built-in GraphQL Playground for exploring the schema.

**Endpoint:** https://demo.dotcms.com/api/v1/graphql

**Documentation:** https://dev.dotcms.com/docs/graphql

## Introspection status

*Probed 2026-09-06.* The endpoint is live and answers **anonymously**:

```
POST https://demo.dotcms.com/api/v1/graphql
{"query":"{__typename}"}
→ 200 {"data":{"__typename":"Query"}}
```

Schema introspection, however, is **disabled server-side** — not auth-gated, stripped:

```
POST https://demo.dotcms.com/api/v1/graphql
{"query":"{__schema{types{name}}}"}
→ 200 {"errors":[{"message":"Validation error of type FieldUndefined:
        Field 'types' in type '__Schema' is undefined ..."}],"data":null}
```

The `__Schema` fields (`types`, `queryType`) are removed from the executable schema, so a client
cannot discover the content-type collections without prior knowledge of the instance's content
model. **No SDL is stored in this repository, because none could be fetched and none was
fabricated.**

This matters because a dotCMS GraphQL schema is *per-instance* by construction — it is generated
from the content types a given deployment defines. There is no single "dotCMS GraphQL schema" to
publish; the schema is whatever the customer modelled. With introspection off, the only way to
learn it is the dotCMS admin UI's GraphQL Playground on that instance, or reading the content-type
definitions through the REST API (`/api/v1/contenttype`, operationId `getContentTypes`).

## Relationship to the REST surface

REST and GraphQL are overlapping but non-identical projections of the same content core. The REST
contract (`openapi/dotcms-rest-api-openapi.json`, 754 operations) covers the whole platform —
administration, workflow, publishing, permissions — while GraphQL covers content *delivery*:
querying contentlets, pages and collections for a front end. See
`mcp/dotcms-tool-crosswalk.yml` for the recorded divergence across all three surfaces (REST,
GraphQL, MCP).

**References:**

- Documentation: https://dev.dotcms.com/docs/graphql
- REST contract: openapi/dotcms-rest-api-openapi.json
- Surface crosswalk: mcp/dotcms-tool-crosswalk.yml
