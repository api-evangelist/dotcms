# dotCMS (dotcms)

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

dotCMS is a Java-based visual headless content management system aimed at compliance-led enterprises, deployable as SaaS (dotCMS Cloud), on premise, or as a managed service. It covers content modelling, authoring, workflow, multi-site management, personalization, experiments and content analytics, and pairs headless delivery with a Universal Visual Editor so authors can edit content in place inside a React, Angular or Next.js front end.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/dotcms/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/dotcms/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- CMS
- Content
- Content Management
- Headless CMS
- Digital Experience
- Content Delivery
- Workflows
- GraphQL
- MCP
- Java

## Timestamps

- **Created:** 2025-01-08
- **Modified:** 2026-09-06

## APIs

### dotCMS REST API

Every dotCMS instance serves its own first-party OpenAPI 3.0.1 document at `/api/openapi.json` — **592 paths, 754 operations, 606 component schemas, 71 tags**, covering content and content types, workflow, search, publishing, sites, folders, templates, containers, roles, permissions, experiments, jobs and dotAI. The copy in `openapi/` was harvested verbatim from dotCMS's own demo instance.

- **Human URL:** [https://dev.dotcms.com/docs/build/apis/api-basics/rest-apis](https://dev.dotcms.com/docs/build/apis/api-basics/rest-apis)
- **Base URL:** `https://demo.dotcms.com/api`
- **Spec source:** `https://demo.dotcms.com/api/openapi.json` (HTTP 200, harvested 2026-09-06)

#### Properties

- [OpenAPI](openapi/dotcms-rest-api-openapi.json) — [OpenAPI 3.0.1](https://spec.openapis.org/oas/latest.html)
- [Documentation](https://dev.dotcms.com/docs/build/apis/api-basics/rest-apis)
- [API Reference](https://dev.dotcms.com/docs/build/apis/rest-apis/api-playground)
- [Developer Portal](https://dev.dotcms.com/)
- [Overlay](overlays/dotcms-rest-api-overlay.yaml)
- [Error Catalog](errors/dotcms-problem-types.yml)
- [Data Model](data-model/dotcms-data-model.yml)
- [Conventions](conventions/dotcms-conventions.yml)

### dotCMS GraphQL API

A single endpoint for querying content across all content types. The endpoint answers anonymously on the demo instance, but `__schema` introspection is disabled server-side, so no SDL could be captured and none was fabricated.

- **Human URL:** [https://dev.dotcms.com/docs/graphql](https://dev.dotcms.com/docs/graphql)
- **Base URL:** `https://demo.dotcms.com/api/v1/graphql`

#### Properties

- [Documentation](https://dev.dotcms.com/docs/graphql)
- [GraphQL](graphql/dotcms-graphql.md)

## Agent surface

dotCMS ships an early and unusually complete agent surface, all of it first-party:

- **MCP server** — `@dotcms/mcp-server` (stdio), source in `dotCMS/core`, documented at [dev.dotcms.com/docs/mcp-server](https://dev.dotcms.com/docs/mcp-server). Four tools, two of which are sandboxes over the whole REST spec. See `mcp/`.
- **Agent Skills** — two provider-authored skills published at [dotCMS/agent-toolkit](https://github.com/dotCMS/agent-toolkit) (MIT), mirrored verbatim in `skills/`.
- **RFC 9727 API catalog** — served at [`/.well-known/api-catalog`](https://www.dotcms.com/.well-known/api-catalog) as `application/linkset+json`, declaring markdown content negotiation across the site.
- **RFC 9116 security.txt** — served at [`/.well-known/security.txt`](https://www.dotcms.com/.well-known/security.txt).
- **llms.txt** — published at [dev.dotcms.com/llms.txt](https://dev.dotcms.com/llms.txt).

## Compliance

ISO/IEC 27001:2022 · ISO/IEC 42001:2023 (AI management) · SOC 2 Type II · TX-RAMP Level II · CSA CAIQ — trust center at [security.dotcms.com](https://security.dotcms.com/).

## Common Properties

- [GitHub Organization](https://github.com/dotCMS)
- [LinkedIn](https://www.linkedin.com/company/dotcms)
- [llms.txt](llms/dotcms-llms.txt)
- [Packages / SDKs](packages/dotcms-packages.yml)
- [CLI](cli/dotcms-cli.yml)
- [Components](components/dotcms-components.yml)
- [Well-Known](well-known/dotcms-well-known.yml)
- [MCP Server](mcp/dotcms-mcp.yml)
- [Tool Crosswalk](mcp/dotcms-tool-crosswalk.yml)
- [Agent Skills](skills/_index.yml)
- [Conformance](conformance/dotcms-conformance.yml)
- [Compliance](https://www.dotcms.com/product/security-compliance)
- [Trust Center](security/dotcms-trust-center.yml)
- [Security / Responsible Disclosure](https://dev.dotcms.com/docs/manage/access-and-security/security-and-privacy/responsible-disclosure-policy)
- [Lifecycle](lifecycle/dotcms-lifecycle.yml)
- [Changelog](changelog/dotcms-changelog.yml)
- [Sandbox](sandbox/dotcms-sandbox.yml)
- [Webhooks / Event surface](asyncapi/dotcms-event-surface.yml)
- [Plans](plans/dotcms-plans-pricing.yml)
- [Rate Limits](rate-limits/dotcms-rate-limits.yml)
- [Roadmap](https://www.dotcms.com/roadmap)
- [Pricing](https://www.dotcms.com/pricing)
- [Support](https://community.dotcms.com/)

## Superseded artifacts

`openapi/_superseded/` and `collections/_superseded/` hold the documentation-derived scaffold specs (19 paths) and the collections generated from them, retired on 2026-09-06 when the real 754-operation contract was harvested. They are kept for audit; nothing points at them. See the README in each directory.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
