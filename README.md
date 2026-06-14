# BTCPay Server

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
