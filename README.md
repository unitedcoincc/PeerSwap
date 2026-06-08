# PeerSwap Protocol

PeerSwap is a non-custodial coordination protocol for multi-party value conversion between fiat-linked digital assets and cryptocurrencies.

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
- facilitate creation of user-controlled multi-signature wallets

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

## Architecture

- Discovery Layer (intent visibility)
- Allocation Layer (math engine)
- Settlement Layer (user-controlled multisig)

---

## License

MIT (or TBD)
