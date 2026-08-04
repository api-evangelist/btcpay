# BTCPay Server

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

BTCPay Server is a self-hosted, open-source Bitcoin and cryptocurrency payment processor. It provides merchants and developers a censorship-resistant, zero-fee, privacy-preserving alternative to hosted payment processors. The platform supports on-chain Bitcoin payments as well as Lightning Network transactions.

## API

BTCPay Server exposes the **Greenfield API v1**, a full-featured REST API served at `/api/v1` on any BTCPay Server instance. The API is documented with an OpenAPI 3.0 specification available at `/swagger/v1/swagger.json` on each deployment.

### Key Resource Areas

| Controller | Description |
|---|---|
| Stores | Create and manage payment stores |
| Invoices | Create, query, update, and archive invoices |
| Wallets | On-chain Bitcoin wallet operations |
| Lightning Network | Node management, channels, payments, and addresses |
| Payment Requests | Reusable payment request links |
| Pull Payments | Batch payouts and refunds |
| Payouts | Manage and approve payout batches |
| Payout Processors | Automated on-chain and Lightning payout processing |
| Webhooks | Event-driven HTTP callbacks |
| Notifications | In-app notification management |
| Users | User account creation and management |
| API Keys | Programmatic API key management |
| Server Info | Server health, version, and configuration |
| Apps | Point-of-sale, crowdfunding, and payment button apps |
| Files | File upload and management |
| Reports | Payment and sales reporting |
| Rates | Exchange rate queries and configuration |
| Email | Store and server-level email configuration |
| Roles | Server and store role/permission management |

### Authentication

- **API Keys** (recommended): Generated via `Account > Manage account > API keys` or programmatically via the Create API Key endpoint. Supports granular permissions (e.g., `btcpay.store.cancreateinvoice`, `btcpay.store.canviewinvoices`).
- **HTTP Basic Auth**: Username and password; suitable for server-level operations.
- **Interactive Authorization Flow**: OAuth-like redirect flow allowing third-party applications to request scoped API keys from users.

### Base URL

```
https://{your-btcpay-host}/api/v1
```

## Pricing

BTCPay Server is **free and open-source** (MIT license). There are no transaction fees, no API call fees, and no licensing costs. Infrastructure costs (hosting a VPS) are the only operational expense for self-hosted deployments.

## Resources

- **Website**: https://btcpayserver.org
- **Documentation**: https://docs.btcpayserver.org
- **API Reference**: https://docs.btcpayserver.org/API/Greenfield/v1/
- **GitHub**: https://github.com/btcpayserver/btcpayserver
- **Community Chat**: https://chat.btcpayserver.org/
- **Releases / Changelog**: https://github.com/btcpayserver/btcpayserver/releases
- **Third-Party Hosts**: https://btcpayserver.org/third-party-hosts/

## License

MIT — see https://github.com/btcpayserver/btcpayserver/blob/master/LICENSE
