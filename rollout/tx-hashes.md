# 🔐 Governance Transaction Log – Cube Ecosystem

This document records critical transaction hashes related to CubeCoin governance setup, role assignments, and Timelock operations. All actions are executed on Polygon Mainnet (`Chain ID: 137`) and verified via Polygonscan.

---

## 🧩 Role Assignments

| Action                            | Contract         | Role              | Target Address                                 | Tx Hash                                      |
|----------------------------------|------------------|-------------------|------------------------------------------------|----------------------------------------------|
| Grant `DEFAULT_ADMIN_ROLE`       | CubeCoin         | Admin             | TimelockController                             | `0x...`                                       |
| Revoke `DEFAULT_ADMIN_ROLE`      | CubeCoin         | Admin             | Deployer EOA                                   | `0x...`                                       |
| Grant `DEFAULT_ADMIN_ROLE`       | Unified          | Admin             | TimelockController                             | `0x...`                                       |
| Revoke `DEFAULT_ADMIN_ROLE`      | Unified          | Admin             | Deployer EOA                                   | `0x...`                                       |
| Grant `MINTER_ROLE`              | CubeCoin         | Minter            | TimelockController                             | `0x...`                                       |
| Grant `PAUSER_ROLE`              | CubeCoin         | Pauser            | TimelockController                             | `0x...`                                       |

---

## ⏱ Timelock Operations

| Operation                        | Target Contract   | Function                 
