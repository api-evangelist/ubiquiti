# Ubiquiti (ubiquiti)

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

Ubiquiti Inc. (NYSE&#58; UI) is an American networking technology company that designs and sells wireless and wired network products for enterprises, service providers, and consumers under the UniFi, UISP, AmpliFi, airMAX, airFiber, and EdgeMax brands. UniFi is a full-stack platform spanning WiFi, switching, routing, identity, surveillance (Protect), access control (Access), and VoIP (Talk), managed locally by the UniFi Network Controller and globally via the UniFi Site Manager cloud at unifi.ui.com. UISP is Ubiquiti's ISP platform combining a Network Management System (NMS) and a Customer Relationship Management (CRM) module for wireless and fiber service providers. The official UniFi Site Manager API exposes hosts, sites, devices, ISP metrics, and SD-WAN configurations at api.ui.com/v1 with X-API-KEY authentication; UISP NMS and CRM APIs are hosted on each customer instance under /nms/api/v2.1/ and /crm/api/v1.0/ respectively.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/ubiquiti/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/ubiquiti/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Networking
- WiFi
- Switching
- Routing
- Surveillance
- Access Control
- ISP
- WISP
- UniFi
- UISP
- AmpliFi

## Timestamps

- **Created:** 2026-05-25T00:00:00.000Z
- **Modified:** 2026-05-25

## APIs

### UniFi Site Manager API

The UniFi Site Manager API is Ubiquiti's official cloud API at api.ui.com for programmatic access to UniFi deployments across all sites linked to a UI account. Endpoints expose hosts (UniFi OS consoles), sites (UniFi Network applications), devices, ISP metrics (latency, packet loss, uptime, bandwidth), and SD-WAN configurations. Authentication uses an `X-API-KEY` header generated at unifi.ui.com/settings/api-keys. Read-only at GA; write scope (adopt, configure) is being rolled out through 2026. GA rate limit is 10,000 requests per minute; Early Access endpoints under `/ea/` are limited to 100 requests per minute.

- **Human URL:** [https://developer.ui.com/site-manager-api/](https://developer.ui.com/site-manager-api/)
- **Base URL:** `https://api.ui.com/v1`

#### Tags

- Networking
- UniFi
- Site Manager
- Cloud

#### Properties

- [Documentation](https://developer.ui.com/site-manager-api/)
- [Getting Started](https://developer.ui.com/site-manager/v1.0.0/gettingstarted)
- [Documentation](https://help.ui.com/hc/en-us/articles/30076656117655-Getting-Started-with-the-Official-UniFi-API)
- [Versioning](https://developer.ui.com/site-manager-api/versioncontrol)
- [Documentation](https://developer.ui.com/site-manager-api/responseformat/)
- [OpenAPI](openapi/ubiquiti-unifi-site-manager-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ubiquiti-unifi-site-manager-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ubiquiti-unifi-site-manager-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### UniFi Network Controller API

The UniFi Network Controller API is the local HTTP API exposed by every UniFi Network controller (UDM, UDM Pro, UDR, Cloud Key, self-hosted controller, UniFi OS consoles). Endpoints are prefixed with `/api/s/{site}/` on a standalone controller, or `/proxy/network/api/s/{site}/` on UniFi OS devices. It covers sites, devices, clients, stats (`stat/health`, `stat/sta`, `stat/device`), settings, wireless networks, firewall, port forwards, vouchers, hotspot, alerts, and events. Authentication is via `/api/auth/login` on UniFi OS. Responses follow the `{ "meta": { "rc": "ok" }, "data": [...] }` shape. Not formally documented by Ubiquiti; reverse-engineered conventions captured in community wikis and third-party SDKs.

- **Human URL:** [https://ubntwiki.com/products/software/unifi-controller/api](https://ubntwiki.com/products/software/unifi-controller/api)

#### Tags

- Networking
- UniFi
- Controller
- Local API

#### Properties

- [Documentation](https://ubntwiki.com/products/software/unifi-controller/api)
- [Documentation](https://help.ui.com/hc/en-us/articles/30076656117655-Getting-Started-with-the-Official-UniFi-API)
- [SDK](https://github.com/Art-of-WiFi/UniFi-API-client)
- [Documentation](https://github.com/ubiquiti-community/unifi-api)
- [Postman Collection](collections/ubiquiti-unifi-site-manager-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ubiquiti-unifi-site-manager-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### UISP Network (NMS) API

The UISP Network (NMS) API is the per-instance REST API for the network-management half of UISP — Ubiquiti's purpose-built ISP platform for wireless and fiber service providers. Endpoints are served from each UISP instance under `/nms/api/v2.1/` (e.g. `/nms/api/v2.1/devices`, `/nms/api/v2.1/devices/{id}/detail`, sites, outages, alerts, statistics). Authentication uses an `x-auth-token` header carrying an API token generated in the UISP console; tokens can be issued in read-only or read/write mode. A live Swagger UI is hosted at `https://{your-host}/nms/api-docs/` on every UISP installation.

- **Human URL:** [https://uisp.ui.com/nms/api-docs/](https://uisp.ui.com/nms/api-docs/)

#### Tags

- ISP
- UISP
- WISP
- Network Management

#### Properties

- [Documentation](https://help.uisp.com/hc/en-us/sections/22589678457879-UISP-Network)
- [Documentation](https://help.uisp.com/hc/en-us/articles/22590956856087-UISP-CRM-API-Usage)
- [Postman Collection](collections/ubiquiti-unifi-site-manager-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ubiquiti-unifi-site-manager-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### UISP CRM API

The UISP CRM API is the per-instance REST API for the customer-relationship-management half of UISP, covering clients, services (subscriptions), invoices, payments, quotes, tickets, jobs, taxes, and product/service plans. Endpoints are served from each UISP instance under `/crm/api/v1.0/`. Authentication uses an `X-Auth-App-Key` header carrying an App Key generated under Settings → Security → App keys. The full reference is mirrored on Apiary at unmscrm.docs.apiary.io.

- **Human URL:** [https://unmscrm.docs.apiary.io/](https://unmscrm.docs.apiary.io/)

#### Tags

- ISP
- UISP
- WISP
- CRM
- Billing

#### Properties

- [Documentation](https://unmscrm.docs.apiary.io/)
- [Documentation](https://help.uisp.com/hc/en-us/articles/22590956856087-UISP-CRM-API-Usage)
- [Postman Collection](collections/ubiquiti-unifi-site-manager-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ubiquiti-unifi-site-manager-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Portal](https://www.ui.com)
- [Portal](https://developer.ui.com)
- [Documentation](https://developer.ui.com/site-manager-api/)
- [Getting Started](https://help.ui.com/hc/en-us/articles/30076656117655-Getting-Started-with-the-Official-UniFi-API)
- [Documentation](https://ubntwiki.com/products/software/unifi-controller/api)
- [Documentation](https://help.uisp.com/)
- [Documentation](https://unmscrm.docs.apiary.io/)
- [Portal](https://amplifi.com)
- [Sign Up](https://account.ui.com)
- [Authentication](https://unifi.ui.com/settings/api-keys)
- [Rate Limits](https://developer.ui.com/site-manager-api/)
- [Versioning](https://developer.ui.com/site-manager-api/versioncontrol)
- [Status Page](https://status.ui.com)
- [Blog](https://www.ui.com/blog)
- [Forum](https://community.ui.com)
- [Support](https://help.ui.com)
- [Terms of Service](https://www.ui.com/legal/termsofservice/)
- [Privacy Policy](https://www.ui.com/legal/privacypolicy/)
- [Investors](https://ir.ui.com/)
- [GitHub Organization](https://github.com/ubiquiti)
- [GitHub Organization](https://github.com/ubiquiti-community)
- [SDK](https://github.com/Art-of-WiFi/UniFi-API-client)
- [SDK](https://github.com/ubiquiti-community/go-unifi)
- [SDK](https://github.com/ubiquiti-community/py-unifi)
- [SDK](https://github.com/DiegoMax/uisp)
- [Tool](https://github.com/ubiquiti-community/terraform-provider-unifi)
- [Tool](https://github.com/ubiquiti-community/external-dns-unifi-webhook)
- [Plans](plans/ubiquiti-plans-pricing.yml)
- [Rate Limits](rate-limits/ubiquiti-rate-limits.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
