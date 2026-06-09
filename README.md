# PeerSwap Protocol

PeerSwap is a non-custodial coordination protocol for multi-party value conversion between fiat-linked digital assets and cryptocurrencies. An open-source, non-custodial peer-to-peer (P2P) protocol designed to enable large-scale asset conversions by aggregating multiple counterparties into a single shared atomic swap.

PeerSwap does NOT:
- hold user funds
- act as a custodian
- operate a matching engine
- set or guarantee pricing
- execute transactions

PeerSwap DOES:
- display real-time counterparty intent
- compute allocation breakdowns
- enable user-selected multi-party conversions
- facilitate creation of user-controlled multi-signature atomic wallets

---

## Core Idea

PeerSwap is a **coordination layer**, not an exchange.

Users maintain full control of assets at all times. PeerSwap only provides:
- visibility
- arithmetic allocation
- workflow coordination

---

## Example Flow

1. User A wants to convert BTC → CAD
2. Users B, C, D want CAD → BTC
3. PeerSwap shows available counterparties
4. User A selects multiple counterparties
5. Allocation is computed in real time
6. A shared multisig wallet is created
7. Users independently sign and settle

---

## 📱 Protocol Interface Preview

Here is a visual breakdown of how PeerSwap handles multi-party liquidity matching:

![PeerSwap Interface](https://raw.githubusercontent.com/unitedcoincc/PeerSwap/dd972fdde33cfce61cf3ff29a3f7c04475d5d339/SwapUI.png)

---

## 💡 How PeerSwap Solves P2P Liquidity

Traditional P2P platforms fail when a user wants to convert a large amount of currency, because it is rare to find a single individual who perfectly matches that exact volume. PeerSwap changes this by introducing two core concepts:

### 🧩 1. Multi-Party Allocation Engine
Instead of waiting for a single counterparty, PeerSwap fragments your order and fills it across multiple independent swappers simultaneously. As shown in the preview above:
* To convert **1.00 BTC (~$88,508 CAD)**, the engine dynamically groups `@MapleInvestor` (contributing 45.20%) and `@TorontoBuilder` (contributing 54.80%).
* This achieves **100% order coverage** instantly, minimizing slippage and maximizing speed.

### 🔐 2. Non-Custodial Co-Signed Escrow
PeerSwap never holds user funds or private keys. 
* Once swappers are selected, the protocol instantiates a secure, multi-signature shared atomic wallet.
* All selected counterparties must collectively co-sign to release the funds, ensuring trustless execution where users maintain joint control throughout the lifecycle of the swap.

---

## 🛠️ Project Structure

The project is structured as a TypeScript monorepo designed for rapid open-source development:

* **`packages/core`**: Core math engines handling allocation algorithms and real-time pricing adapters.
* **`packages/discovery`**: P2P intent feeds and counterparty rating/filtering mechanics.
* **`packages/wallet`**: Multi-sig factory infrastructure and cryptographic signing flows.
* **`apps/web`**: The web frontend interface and API integration layers.

---

## 🤝 Contributor Warmup (Help Wanted!)

We want to build a truly decentralized alternative to custodial exchanges, and we need your help to make it a reality. We are actively looking for contributors across these domains:

* **Frontend Developers:** Build out the UI components corresponding to the mockup using React/Next.js (`packages/ui`).
* **Protocol & Cryptography Engineers:** Design and implement the multi-sig factories (`packages/wallet`) and trustless coordination schemes.
* **Backend/Distributed Systems Engineers:** Optimize the real-time intent routing feed (`packages/discovery`).

### How to Get Started
1. Review our open [Issues](https://github.com) tagged with `good first issue` or `help wanted`.
2. Fork the repository and create your feature branch (`git checkout -b feature/amazing-feature`).
3. Open a Pull Request detailing your changes!

## Architecture

- Discovery Layer (intent visibility)
- Allocation Layer (math engine)
- Settlement Layer (user-controlled multisig)

---

## License

MIT (or TBD)
