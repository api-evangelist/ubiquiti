# Ubiquiti (ubiquiti)
Ubiquiti Inc. (NYSE: UI) is an American networking technology company that designs and sells wireless and wired network products for enterprises, service providers, and consumers under the UniFi, UISP, AmpliFi, airMAX, airFiber, and EdgeMax brands. UniFi is a full-stack platform spanning WiFi, switching, routing, identity, surveillance (Protect), access control (Access), and VoIP (Talk), managed locally by the UniFi Network Controller and globally via the UniFi Site Manager cloud at unifi.ui.com. UISP is Ubiquiti's ISP platform combining a Network Management System (NMS) and a Customer Relationship Management (CRM) module for wireless and fiber service providers.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/ubiquiti/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - Networking, WiFi, Switching, Routing, Surveillance, Access Control, ISP, WISP, UniFi, UISP, AmpliFi

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### UniFi Site Manager API
Ubiquiti's official cloud API at `https://api.ui.com/v1` for multi-site UniFi management. Exposes hosts (UniFi OS consoles), sites, devices, ISP metrics, and SD-WAN configurations. Authentication via `X-API-KEY` header (keys issued at https://unifi.ui.com/settings/api-keys). Read-only at GA; write scope rolling out through 2026. GA rate limit: 10,000 req/min. Early Access (`/ea/`) endpoints: 100 req/min.

**Human URL:** [https://developer.ui.com/site-manager-api/](https://developer.ui.com/site-manager-api/)

- [Documentation](https://developer.ui.com/site-manager-api/)
- [Getting Started](https://developer.ui.com/site-manager/v1.0.0/gettingstarted)
- [Help Center walkthrough](https://help.ui.com/hc/en-us/articles/30076656117655-Getting-Started-with-the-Official-UniFi-API)
- [Versioning](https://developer.ui.com/site-manager-api/versioncontrol)
- [OpenAPI](openapi/ubiquiti-unifi-site-manager-api-openapi.yml)

### UniFi Network Controller API
The local HTTP API exposed by every UniFi Network controller (UDM, UDM Pro, UDR, Cloud Key, self-hosted controller). Endpoints prefixed with `/api/s/{site}/` on standalone controllers or `/proxy/network/api/s/{site}/` on UniFi OS. Covers sites, devices, clients, stats, wireless networks, firewall, port forwards, vouchers, hotspot, alerts, and events. Authentication via `/api/auth/login` on UniFi OS. Not formally documented by Ubiquiti; conventions captured in community wikis and third-party SDKs.

**Human URL:** [https://ubntwiki.com/products/software/unifi-controller/api](https://ubntwiki.com/products/software/unifi-controller/api)

- [Community Wiki — UniFi Controller API](https://ubntwiki.com/products/software/unifi-controller/api)
- [Help Center — Official UniFi API](https://help.ui.com/hc/en-us/articles/30076656117655-Getting-Started-with-the-Official-UniFi-API)
- [SDK — Art-of-WiFi UniFi PHP client](https://github.com/Art-of-WiFi/UniFi-API-client)
- [Community OpenAPI definition](https://github.com/ubiquiti-community/unifi-api)

### UISP Network (NMS) API
Per-instance REST API for the network-management half of UISP. Endpoints under `/nms/api/v2.1/` on every UISP installation — devices, sites, outages, alerts, statistics. Authentication via `x-auth-token` header. Live Swagger UI at `https://{your-host}/nms/api-docs/` per instance.

**Human URL:** [https://uisp.ui.com/nms/api-docs/](https://uisp.ui.com/nms/api-docs/)

- [UISP Network Help Center](https://help.uisp.com/hc/en-us/sections/22589678457879-UISP-Network)
- [UISP API Usage docs](https://help.uisp.com/hc/en-us/articles/22590956856087-UISP-CRM-API-Usage)

### UISP CRM API
Per-instance REST API for the CRM half of UISP — clients, services, invoices, payments, quotes, tickets, jobs, taxes, product/service plans. Endpoints under `/crm/api/v1.0/`. Authentication via `X-Auth-App-Key` header (App Keys issued in Settings → Security → App keys). Full reference mirrored on Apiary.

**Human URL:** [https://unmscrm.docs.apiary.io/](https://unmscrm.docs.apiary.io/)

- [UISP CRM API on Apiary](https://unmscrm.docs.apiary.io/)
- [UISP CRM API Usage docs](https://help.uisp.com/hc/en-us/articles/22590956856087-UISP-CRM-API-Usage)

## Common Properties

- [Portal — ui.com](https://www.ui.com)
- [Portal — developer.ui.com](https://developer.ui.com)
- [Portal — AmpliFi](https://amplifi.com)
- [Documentation — UniFi Site Manager API](https://developer.ui.com/site-manager-api/)
- [Documentation — UniFi Controller API (Community Wiki)](https://ubntwiki.com/products/software/unifi-controller/api)
- [Documentation — UISP Help Center](https://help.uisp.com/)
- [Documentation — UISP CRM API on Apiary](https://unmscrm.docs.apiary.io/)
- [Getting Started — Official UniFi API](https://help.ui.com/hc/en-us/articles/30076656117655-Getting-Started-with-the-Official-UniFi-API)
- [Authentication — UniFi Site Manager API Keys](https://unifi.ui.com/settings/api-keys)
- [SignUp — UI Account](https://account.ui.com)
- [StatusPage](https://status.ui.com)
- [Blog — ui.com/blog](https://www.ui.com/blog)
- [Forum — Ubiquiti Community](https://community.ui.com)
- [Support — Help Center](https://help.ui.com)
- [Investors](https://ir.ui.com/)
- [TermsOfService](https://www.ui.com/legal/termsofservice/)
- [PrivacyPolicy](https://www.ui.com/legal/privacypolicy/)
- [GitHubOrganization — github.com/ubiquiti](https://github.com/ubiquiti)
- [GitHubOrganization — github.com/ubiquiti-community](https://github.com/ubiquiti-community)
- [SDK — UniFi PHP API client (Art-of-WiFi)](https://github.com/Art-of-WiFi/UniFi-API-client)
- [SDK — go-unifi (Go)](https://github.com/ubiquiti-community/go-unifi)
- [SDK — py-unifi (Python)](https://github.com/ubiquiti-community/py-unifi)
- [SDK — UISP CRM (TypeScript)](https://github.com/DiegoMax/uisp)
- [Tool — Terraform provider for UniFi](https://github.com/ubiquiti-community/terraform-provider-unifi)
- [Tool — External-DNS Webhook for UniFi DNS](https://github.com/ubiquiti-community/external-dns-unifi-webhook)

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [UniFi Site Manager API](openapi/ubiquiti-unifi-site-manager-api-openapi.yml)

### Commercial artifacts

- [Plans / Pricing](plans/ubiquiti-plans-pricing.yml)
- [Rate Limits](rate-limits/ubiquiti-rate-limits.yml)

## Maintainers

**FN:** Kin Lane

**Email:** info@apievangelist.com
