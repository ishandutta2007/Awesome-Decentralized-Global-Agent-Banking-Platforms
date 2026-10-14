# Awesome-Decentralized-Global-Agent-Banking-Platforms

## Top Decentralized Global Agent Banking Platforms Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Agent Identity, Scoped Spend Authorization & Stablecoin Settlement*  

**Last updated: March 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Decentralized Global Agent Banking**. These tools enable autonomous AI agents to hold identity, receive funds, spend within policy-defined boundaries, and settle transactions across fiat and crypto rails—without exposing permanent payment credentials.



**Examples** include Skyfire Systems, Sphere, Helio (MoonPay Commerce), Rain Cards, Crossmint, Conduit, BVNK, Bridge (Stripe), Lightspark, and Meso (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, scoped spend governance, and open payment rails—ideal for agent developers, fintech engineers, and platforms seeking transparent, vendor-independent agent banking infrastructure.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Skyfire Systems](https://skyfire.xyz/)**  

  Verified identity and payment credentials for agents across the open internet. Three token types: **kya** (Know Your Agent—proves identity), **pay** (authorizes payment to a seller), and **kya-pay** (identity and payment combined). Tokens are JWTs conforming to the open **KYAPay protocol**—an industry specification for identity-linked payment credentials purpose-built for autonomous systems. Every interaction follows four steps: Present, Verify, Deliver, Settle .



- **[Sphere (Unicity)](https://sphere.xyz/)**  

  Autonomous economic agent SDK providing identity, wallet, and ability to find, negotiate with, and settle with other agents—peer-to-peer, with perfect privacy and ultra-fast finality. SDK available for Node.js with multi-wallet support, Nostr relay transport, and wallet API providers. A community MCP server (`@purplesquirrel/sphere-mcp`) exposes 13 tools covering stablecoin contractor payouts, treasury sweeps, on-ramp/off-ramp virtual accounts, customer onboarding, KYC, and webhooks .



- **[Helio (MoonPay Commerce)](https://hel.io/)**  

  Agent-payable checkout and deposit platform for merchants. Agents settle payments on-chain in **mainnet USDC** via **x402** (HTTP 402-based payment protocol)—no human checkout required. Merchant integration unchanged: paylinks, charges, deposits, and webhooks work identically for agent and human payers. Per-payer deposit wallets pre-allocated; rate limits 10 requests/60s per payer IP. Audited by Ackee Blockchain; non-custodial—funds never held by Helio .



- **[Rain Cards](https://www.rain.xyz/)**  

  Scoped virtual card infrastructure for programmable payments. Cards created in **milliseconds** against defined spend parameters and **auto-retired** after intended use. **Agent Control Layer** (beta) enforces controls at card issuance and transfer initiation—not after the fact. Agent-level controls: transaction amounts, merchant/category allowlists, spend intervals, card expiry. Program-level controls: caps on active cards, aggregate spend limits. Sponge (YC-backed) issues agent-usable cards funded by stablecoin balance, transacting anywhere Visa is accepted online across **175M+ merchant locations** .



- **[Crossmint](https://www.crossmint.com/)**  

  Payment infrastructure for AI agents with three composable products: **Agent Cards** (one-time or encrypted credentials—real card never exposed, PCI scope stays with Crossmint, limits enforced at Visa/Mastercard), **Agent Wallets** (non-custodial smart wallets for x402, MPP, and onchain actions—spend cap, allowed counterparties, time window enforced onchain), and **Agent Checkouts** (accept payments from agentic commerce protocols or optimized browser). User stays in control; every allowance scoped, explicit, revocable .



- **[Conduit](https://conduit.financial/)**  

  Banking infrastructure for AI customer service and agent operations. **Clients** (business entities/subsidiaries) get named **Virtual Accounts** for true banking-like functionality—hold USD balances, send/receive payments, manage multiple entities independently. Onboarding 1-3 business days. API for client balances, deposit instructions, and payment execution. While positioned for AI customer service, the virtual account architecture provides the banking layer for agent-initiated corporate payments .



- **[BVNK](https://bvnk.com/)**  

  Enterprise stablecoin payments infrastructure bridging banks and blockchains. **Embedded Wallets** (launched March 2025) unify fiat and stablecoins in a single platform—Swift, SEPA, ACH, and blockchains. 25+ licenses and regulatory approvals, ISO 27001 and SOC 2 Type II certified, 99.9% uptime. 130+ countries supported for onboarding. Send, receive, convert, store, and embed wallets in your brand .



- **[Bridge (Stripe)](https://bridge.xyz/)**  

  Stablecoin infrastructure platform acquired by Stripe. Integration with XDC Tech enables autonomous AI agents to access **fiat payments, securely hold stablecoins, and execute cross-border financial services through a fully regulated pipeline**. **Virtual accounts** assign dedicated ACH or IBAN endpoints to AI systems—agents receive fiat, settle as stablecoins, convert back to fiat. Bridge manages KYC, KYB, sanctions screening, and regulated asset custody. XDC Tech processes 2,000+ transactions per second with two-second finality .



- **[Lightspark (Grid Global Accounts)](https://www.lightspark.com/)**  

  Global financial accounts with native AI agent support. Users create **scoped, revocable, auditable operating pockets** for agents—spending limits, approved payees, approval thresholds defined by user. Grid evaluates policy **before any agent-initiated action executes**. Permissions granular: view balances, send payments, create external accounts, execute withdrawals—each explicitly allowed/denied. Connection flows: CLI install, MCP with OAuth, or agent-initiated device flow. Real-time revocation; every action fully traceable .



- **[Meso](https://meso.network/)**  

  Developer-focused platform bridging traditional banking and card payments with crypto applications. Stablecoin and crypto APIs supporting ETH, SOL, MATIC, ARB, OP, BASE, and BTC. Built-in tools for KYC, AML, and fraud prevention. Instant transfers between banks and crypto wallets. Global coverage: US and Europe .



## Open-Source GitHub Projects



- **[PayGraph](https://pypi.org/project/paygraph/)**  

  **Open-source spend governance for AI agents**—the most directly applicable open-source agent banking layer available. Issue **single-use virtual cards** or pay **x402-enabled APIs with USDC**—with policy enforcement, audit logging, and human-in-the-loop approval. Policy engine enforces `max_transaction`, `daily_budget`, `blocked_vendors`, and custom rules. Gateways: **StripeCardGateway** (real virtual cards), **StripeMPPGateway** (scoped Shared Payment Tokens for Stripe machine payments), **X402Gateway** (EVM + Solana USDC payments). Framework integrations: LangGraph, CrewAI, or any agent framework. `pip install paygraph` .



- **[sphere-sdk](https://github.com/unicity-sphere/sphere-sdk)**  

  SDK for autonomous economic agents—give an agent an identity, a wallet, and the ability to find, negotiate with, and settle with other agents. Peer-to-peer, with perfect privacy and ultra-fast finality. Node.js implementation with multi-wallet support (each wallet file under one `dataDir`), Nostr relay transport for decentralized communication, wallet API providers, and oracle trust base configuration. `npm install @unicitylabs/sphere-sdk` .



- **[sphere-mcp](https://www.npmjs.com/package/@purplesquirrel/sphere-mcp)**  

  MCP server for Sphere Pay—**13 tools** covering stablecoin contractor payouts, treasury sweeps, on-ramp/off-ramp virtual accounts, customer onboarding, KYC, and webhooks. Designed primarily for contractor stablecoin payouts + treasury sweep (USDC → fiat bank, wallet → wallet). Any MCP-compatible AI agent (Claude Code, Cursor, ChatGPT) gets native access to Sphere's full payments stack. Webhook signature verification (HMAC-SHA256) included .



### Additional Strong Open-Source Options



- **x402 Protocol** — HTTP 402-based payment protocol for machine-to-machine payments. Emerging standard for agent-paid APIs. Integrated in PayGraph, Crossmint, Helio, and Sphere. Open specification .

- **KYAPay Protocol** — Open industry specification for identity-linked payment credentials purpose-built for autonomous systems. Standardizes how identity and value are packaged and transmitted across agents, services, and platforms .

- Community **n8n** workflows for agent spend alerting and policy violation routing.



**Frameworks for building custom systems**: Combine **PayGraph** for scoped spend governance with **sphere-sdk** for agent identity and wallet management, **sphere-mcp** for MCP-native payments, and **x402** for machine-to-machine API payments—creating a fully self-hosted, enterprise-grade agent banking platform.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Agent banking platforms handling financial transactions must comply with payment regulations (PSD2, SOC 2, AML/KYC requirements, money transmission laws) and applicable financial services law.

- **Open-source agent banking is emerging, not mature.** PayGraph provides scoped spend governance with Stripe and x402 gateways . sphere-sdk provides agent identity and wallet primitives . **No open-source project provides the full regulated banking stack of Bridge, BVNK, or Lightspark.** Integration with regulated partners is required for production deployment.

- **Scoped spend authorization is the core primitive.** Skyfire (kya/pay/kya-pay tokens), Rain (scoped cards), Crossmint (Agent Cards/Wallets), and Lightspark (operating pockets) all enforce policy before money moves. PayGraph implements the same pattern open-source: `SpendPolicy(max_transaction, daily_budget, blocked_vendors)` . Never deploy agent spend without deterministic policy enforcement.

- **Stablecoin settlement is the common denominator.** Helio (USDC via x402), Crossmint (USDC), Bridge (USDC), and Sphere (USDC) all settle in stablecoins. This provides 24/7/365 settlement without correspondent banking delays—critical for autonomous agents operating continuously.

- Self-hosted open-source solutions require proper security hardening, key management, and ongoing maintenance. Agent banking infrastructure is financially critical—audit trails and revocation mechanisms are essential.



---



**Made for agent developers, fintech engineers, and platform teams building transparent autonomous banking infrastructure.**

Let's make Decentralized Global Agent Banking more open, policy-governed, and verifiable.
