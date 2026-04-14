<div align="center">

<img src="../assets/banner.svg" alt="Donut Me — Crypto Payment Infrastructure for the Next Web" width="100%" />

<br />

<img src="../assets/logo.png" alt="Donut Me Logo" width="80" />

<br />

<img src="https://img.shields.io/badge/Web3-Payment_Infrastructure-blueviolet?style=for-the-badge" />
<img src="https://img.shields.io/badge/Built_with-TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
<img src="https://img.shields.io/badge/Solidity-0.8.24-363636?style=for-the-badge&logo=solidity&logoColor=white" />

Empowering any developer to build Web3 payment experiences in minutes.

[Website](#) · [Documentation](#) · [Contact Us](#)

</div>

---

## What is Donut Me?

Donut Me is a **Web3 crypto payment infrastructure** that provides developers and merchants with a simple, secure, and cross-chain payment solution.

We believe Web3 payments shouldn't be complicated. Whether it's subscriptions, one-time payments, or custom payment plans, Donut Me lets you collect payments with a single link — as easy as buying someone a donut.

## Why Donut Me?

| Pain Point | Our Solution |
| --- | --- |
| High barrier to accept crypto payments | **Developer-friendly API** — integrate in just a few lines of code |
| Single-chain limitations & fragmented assets | **Multi-chain support** — Ethereum, Polygon, Arbitrum, Base, BSC all in one |
| Opaque transaction fees | **On-chain transparent fee splitting** — smart contract auto-splits, fees publicly verifiable |
| Broken payment experience | **Checkout Link** — one link from wallet connection to payment completion |
| Lack of operational data | **Real-time Dashboard** — transactions, customers, and revenue visualized instantly |

## Quick Start

Create a checkout session with just a few lines of code:

```typescript
import { DonutMe } from '@donutme/sdk';

const donutme = new DonutMe({ apiKey: 'your-api-key' });

// Create a checkout session
const session = await donutme.checkout.create({
  amount: '10.00',
  token: 'USDC',
  chain: 'polygon',
  merchant: '0xYourWalletAddress',
  successUrl: 'https://yoursite.com/success',
});

// Share the payment link
console.log(session.paymentUrl);
// → https://pay.donutme.io/cs_live_abc123
```

That's it. Your customer clicks the link, connects their wallet, and pays — the smart contract handles the rest.

## Supported Chains & Tokens

| Chain | Network | Tokens |
| :---: | --- | --- |
| <img src="https://img.shields.io/badge/-Ethereum-3C3C3D?logo=ethereum&logoColor=white&style=flat-square" /> | Ethereum Mainnet | USDT · USDC · DAI |
| <img src="https://img.shields.io/badge/-Polygon-8247E5?logo=polygon&logoColor=white&style=flat-square" /> | Polygon PoS | USDT · USDC · DAI |
| <img src="https://img.shields.io/badge/-Arbitrum-28A0F0?logo=arbitrum&logoColor=white&style=flat-square" /> | Arbitrum One | USDT · USDC |
| <img src="https://img.shields.io/badge/-Base-0052FF?logo=coinbase&logoColor=white&style=flat-square" /> | Base | USDC |
| <img src="https://img.shields.io/badge/-BSC-F0B90B?logo=binance&logoColor=black&style=flat-square" /> | BNB Smart Chain | USDT · USDC · BUSD |

> More chains and tokens are on the way. See our [Roadmap](#roadmap) below.

## Core Features

- 🔗 **Payment Links** — Generate one-time or reusable crypto payment links
- 🏦 **Multi-chain ERC-20** — Support USDT, USDC and other stablecoins across 5+ chains
- 🔐 **Secure Auth** — Email, Social Login, Passkey, and 2FA authentication
- 📊 **Real-time Dashboard** — Socket.IO-powered live transaction and revenue panels
- 🔑 **API Keys** — Integrate payments into your own product via API
- 🧾 **Invoice & Billing** — Automatic receipt generation and billing management
- 👥 **Team Management** — Multi-user collaboration with role-based access control
- 🌐 **i18n** — English / Traditional Chinese bilingual support
- 🛡️ **On-chain Security** — ReentrancyGuard, Pausable, two-step ownership transfer

## Security & Audit

Security is at the core of everything we build. Our smart contracts follow industry best practices:

| Measure | Details |
| --- | --- |
| **OpenZeppelin v5** | Battle-tested contract libraries for access control, reentrancy guards, and safe token transfers |
| **ReentrancyGuard** | Protection against reentrancy attacks on all payment functions |
| **Pausable** | Emergency circuit breaker to halt operations if an exploit is detected |
| **Ownable2Step** | Two-step ownership transfer to prevent accidental loss of admin control |
| **SafeERC20** | Safe token transfer wrappers to handle non-standard ERC-20 implementations |
| **Token Allowlist** | Only whitelisted tokens can be used for payments |
| **Session Replay Protection** | Each payment is tagged with a unique session ID to prevent double-spending |

> 🔍 **Third-party audit** is planned for an upcoming milestone. Stay tuned for the full audit report.

## Get Involved

We're a fast-growing Web3 startup team. If you're interested in decentralized payment infrastructure, feel free to follow our repos or reach out to us directly.

---

<div align="center">

**Built with 🍩 by the Donut Me team**

*Making crypto payments as easy as buying a donut.*

</div>
