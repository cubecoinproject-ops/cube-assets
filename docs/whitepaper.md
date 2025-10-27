# 🧱 Cube Ecosystem – Whitepaper

## 1. Vision & Philosophy

Cube is a modular Web3 infrastructure built on meaning-centric stewardship. It prioritizes ethical governance, creative autonomy, and resilient decentralization. Every contract, role, and process is designed to reflect Cube’s philosophical foundation: control must be earned, delayed, and documented.

---

## 2. Architecture & Smart Contracts

Cube operates through three core contracts on Polygon Mainnet:

- **CubeCoin**: ERC20 token with minting and pausing capabilities  
- **Unified Distributor**: Manages initial token allocation and operational transfers  
- **TimelockController**: Enforces delayed execution and decentralized governance

All contracts are verified on Polygonscan and publicly accessible.

---

## 3. Governance & Role Management

Cube uses `TimelockController` to manage all sensitive roles:

| Role                | Assigned To          |
|---------------------|----------------------|
| `DEFAULT_ADMIN_ROLE` | TimelockController   |
| `MINTER_ROLE`        | TimelockController   |
| `PAUSER_ROLE`        | TimelockController   |
| `PROPOSER_ROLE`      | Multisig (planned)   |
| `EXECUTOR_ROLE`      | Trusted executors    |

All EOA-based roles have been revoked. Governance actions are scheduled, executed, and monitored via Timelock.

---

## 4. Tokenomics & Distribution

- **Token Name**: CubeCoin  
- **Symbol**: CUBE  
- **Total Supply**: `30,000,000,000 CUBE`  

### 🔹 Allocation Breakdown

| Allocation Type        | Amount (CUBE)       | Purpose                                           |
|------------------------|---------------------|---------------------------------------------------|
| Private & Public Sale  | 15,000,000,000       | Strategic fundraising and ecosystem onboarding    |
| Airdrop                | 5,000,000,000        | Community growth, early supporters, and incentives|
| Treasury Reserve       | 10,000,000,000       | Long-term sustainability and deflationary burns   |

- All tokens are distributed via the **Unified** contract  
- Treasury tokens are subject to **scheduled burns** and **DAO-controlled spending**  
- All transfers are logged in `distribution-log.md` and verifiable on-chain

---

## 5. Legal & Licensing

Cube is protected under the **Cube Proprietary License v1.0**, which prohibits unauthorized use of its code, brand, and creative assets. All visual files (e.g. `cube.svg`) are validated for authenticity and platform compatibility.

---

## 6. Roadmap to DAO

Cube is designed for gradual decentralization:

- Phase 1: Founder-led stewardship with Timelock control  
- Phase 2: Role modularization and multisig onboarding  
- Phase 3: Community proposals and DAO activation  
- Phase 4: Full DAO governance with treasury automation

Each phase is documented and executed with presence and caution.

---

## 7. Founder & Stewardship

Cube was founded by **Cyrus EF**, a meaning-driven architect focused on ethical systems and resilient infrastructure. Stewardship is shared with two trusted brothers, each holding operational roles and participating in governance.

Cube is not just a token—it is a philosophy encoded in smart contracts.

---

## 8. Resources

- [GitHub Repository](https://github.com/cubecoinproject-ops/cube-assets)  
- [Governance Setup](https://github.com/cubecoinproject-ops/cube-assets/blob/main/rollout/governance-setup.md)
- [Governance Roles](https://github.com/cubecoinproject-ops/cube-assets/blob/main/docs/roles.md)

- [Transaction Log](https://github.com/cubecoinproject-ops/cube-assets/blob/main/rollout/tx-hashes.md)  
- [Logo](https://raw.githubusercontent.com/cubecoinproject-ops/cube-assets/main/cube.svg)  
- [Official Page](https://cubecoinproject.github.io/cube/)  
- [X (Twitter) – Cyrus EF](https://x.com/cyruscbf)  
- [Email – Cyrus EF](mailto:cyrus.cbf@gmail.com)
 
---

© 2025 Cube Ecosystem. All rights reserved.
