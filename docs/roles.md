# 🛡️ Cube Governance Roles & Structure

CubeCoin is governed through a modular, meaning-driven structure designed to ensure autonomy, resilience, and gradual decentralization.

All sensitive roles are assigned to contracts or trusted operational stewards—not externally owned accounts (EOAs) with unilateral control.

---

## 🔑 Key Roles & Contracts

| Role              | Assigned To | Address | Purpose |
|-------------------|-------------|---------|---------|
| Minter            | Operational Steward A | `0x...` | Authorized to mint CUBE tokens  
| Pauser            | Operational Steward B | `0x...` | Authorized to pause/unpause token transfers  
| Admin             | TimelockController | `0x...` | Controls role changes, governance actions, and treasury  
| Treasury Receiver | Unified Contract | `0x084C6970e4Efb2f72b55caCEf2b6Afa7AD5A524C` | Receives initial allocations and manages distribution  

> Note: All role assignments are visible on-chain via Polygonscan and verified through deployment artifacts.

---

## ⏱️ Timelock Governance

Cube uses a `TimelockController` contract to enforce delayed execution of sensitive actions.  
This ensures that no immediate changes can be made without community visibility and time for review.

- Minimum Delay: 48 hours  
- Proposers: Governance contracts or multisig (future)  
- Executors: Timelock itself

---

## 🧱 Philosophy of Role Design

Cube’s role structure reflects its core values:

- **No central control**: No EOA holds admin or treasury roles  
- **Trust-based modularity**: Operational roles are assigned to trusted stewards with documented on-chain permissions  
- **Future-proofing**: Roles are designed to be transferable to DAO or multisig structures  
- **Transparency-first**: All role changes are documented and visible on-chain

---

## 📬 References

- [CubeCoin Contract](https://polygonscan.com/address/0x966c3E5c3225af9ABdEbE8Db52D65f51E63037C6)  
- [Unified Allocation Contract](https://polygonscan.com/address/0x084C6970e4Efb2f72b55caCEf2b6Afa7AD5A524C)  
- [TimelockController](https://polygonscan.com/address/0x...)  
- [Deployment Artifacts](https://github.com/cubecoinproject-ops/cube-assets/tree/main/artifacts)

---

© 2025 Cube Ecosystem. All rights reserved.
