<div align="center">

<img src="https://img.shields.io/badge/Web3-Payment_Infrastructure-blueviolet?style=for-the-badge" />
<img src="https://img.shields.io/badge/Built_with-TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
<img src="https://img.shields.io/badge/Solidity-0.8.24-363636?style=for-the-badge&logo=solidity&logoColor=white" />

# 🍩 Donut Me

**Crypto Payment Infrastructure for the Next Web**

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

## Architecture

```
┌──────────────────────────────────────────────────────┐
│                    Donut Me Platform                  │
├─────────────────┬──────────────────┬─────────────────┤
│   Frontend Core │  Backend Core    │ Contract Core   │
│                 │                  │                 │
│  Next.js 16     │  NestJS 11       │ Solidity 0.8    │
│  React 19       │  PostgreSQL      │ OpenZeppelin v5 │
│  RainbowKit     │  BullMQ + Redis  │ Hardhat 3       │
│  wagmi + viem   │  Socket.IO       │ Multi-chain     │
│  shadcn/ui      │  better-auth     │ ERC-20 Router   │
│  TanStack Query │  Prometheus      │ SafeERC20       │
└─────────────────┴──────────────────┴─────────────────┘
         │                  │                 │
         └──────────────────┴─────────────────┘
                          │
              ┌───────────┴───────────┐
              │  Supported Chains     │
              │  Ethereum · Polygon   │
              │  Arbitrum · Base      │
              │  BSC                  │
              └───────────────────────┘
```

## Repositories

| Repo | Description | Stack |
| --- | --- | --- |
| **DonutMe-Frontend-Core** | Payment platform frontend — Checkout, Dashboard, Docs | Next.js 16 · React 19 · Tailwind v4 · shadcn/ui |
| **DonutMe-Backend-Core** | Core API service — Auth, transaction processing, notifications | NestJS 11 · PostgreSQL · Redis · BullMQ |
| **DonutMe-Contract-Core** | On-chain payment contracts — ERC-20 router, auto fee splitting | Solidity 0.8.24 · OpenZeppelin · Hardhat 3 |

## Payment Flow

```
 Developer                    Payer                     Smart Contract
    │                           │                            │
    │  1. Create Checkout       │                            │
    │     Session (API)         │                            │
    │──────────────────►        │                            │
    │                           │                            │
    │  2. Share Payment Link    │                            │
    │──────────────────────────►│                            │
    │                           │                            │
    │                           │ 3. Connect Wallet          │
    │                           │    & Approve ERC-20        │
    │                           │───────────────────────────►│
    │                           │                            │
    │                           │ 4. pay(session, token,     │
    │                           │    amount, merchant)       │
    │                           │───────────────────────────►│
    │                           │                            │
    │                           │         5. Auto Split      │
    │                           │    ┌──────────────────────►│ → Merchant
    │                           │    │     (amount - fee)    │
    │                           │    │                       │ → Treasury
    │                           │    │       (fee)           │
    │                           │                            │
    │  6. Webhook / Real-time   │                            │
    │◄──────────────────────────│                            │
    │     Payment Confirmed ✓   │                            │
```

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

## Tech Stack

**Frontend:** Next.js 16 · React 19 · TypeScript · Tailwind CSS v4 · shadcn/ui · wagmi · viem · RainbowKit · Zustand · TanStack Query · Recharts

**Backend:** NestJS 11 · Fastify · TypeORM · PostgreSQL · Redis · BullMQ · Socket.IO · Pino · Prometheus · better-auth

**Smart Contract:** Solidity 0.8.24 · Hardhat 3 · OpenZeppelin v5 · TypeChain · ethers.js v6

**DevOps & QA:** Docker · Vitest · Playwright · Jest · ESLint · Prettier · Solhint

## Get Involved

We're a fast-growing Web3 startup team. If you're interested in decentralized payment infrastructure, feel free to follow our repos or reach out to us directly.

---

<div align="center">

**Built with 🍩 by the Donut Me team**

*Making crypto payments as easy as buying a donut.*

</div>
