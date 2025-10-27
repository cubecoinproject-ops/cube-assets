# 🧱 Governance Setup – Cube Ecosystem

This document outlines the governance architecture of the CubeCoin ecosystem, including role assignments, contract ownership, and operational safeguards. Cube uses `TimelockController` to ensure all sensitive actions are delayed, auditable, and executed only by authorized entities.

---

## 🔐 Governance Architecture

| Component            | Address                                      |
|---------------------|----------------------------------------------|
| CubeCoin Contract    | `0x966c3E5c3225af9ABdEbE8Db52D65f51E63037C6` |
| Unified Distributor  | `0x084C6970e4Efb2f72b55caCEf2b6Afa7AD5A524C` |
| TimelockController   | `0x3cF2a1F7Ff3A2bFfB9f6c6B9c7f2E6c2F3F3F3F3` |

---

## 🧩 Role Assignments

| Role                | Assigned To                                  |
|---------------------|----------------------------------------------|
| `DEFAULT_ADMIN_ROLE` | `TimelockController`                         |
| `PROPOSER_ROLE`      | Multisig wallets (to be defined)             |
| `EXECUTOR_ROLE`      | Trusted executors (to be defined)            |
| `MINTER_ROLE`        | TimelockController                           |
| `PAUSER_ROLE`        | TimelockController                           |

All roles previously held by EOAs have been revoked to minimize risk.

---

## ⏱ Timelock Parameters

- Minimum Delay: `172800` seconds (48 hours)  
- Chain: Polygon Mainnet (`Chain ID: 137`)  
- Governance actions must be scheduled and executed via Timelock

---

## 🛠 Setup Script Summary

Cube uses Hardhat scripts to automate governance setup:

- `governance-setup.js`: Grants roles and transfers admin rights to Timelock  
- `schedule-update-max.js`: Schedules a sample operation (e.g. update transfer cap)  
- `execute-update-max.js`: Executes scheduled operation after delay  
- `cancel-operation.js`: Cancels a pending operation if needed

Scripts rely on `.env` configuration for addresses and private keys.  
**Private keys are never stored in the repository.**

---

## 📡 Monitoring & Recovery

Cube recommends monitoring the following Timelock events:

- `CallScheduled`  
- `CallExecuted`  
- `CallCanceled`

Emergency actions (e.g. `pause`) must be proposed and executed via Timelock.  
Recovery procedures include role reassignment and contract migration—also governed by Timelock.

---

## 🧠 Best Practices

- Use multisig wallets for `PROPOSER_ROLE` and `EXECUTOR_ROLE`  
- Avoid assigning `DEFAULT_ADMIN_ROLE` to EOAs  
- Document all governance actions in `tx-hashes.md`  
- Maintain public transparency for all role changes and contract upgrades

---

© 2025 Cube Ecosystem. All governance actions are subject to delay, auditability, and meaning-centric stewardship.
