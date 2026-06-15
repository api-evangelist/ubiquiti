# Ubiquiti (ubiquiti)

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
