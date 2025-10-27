# 🧱 Cube Ecosystem – Public Assets & Documentation

Welcome to the official asset and documentation repository for **CubeCoin**, a meaning-driven token ecosystem built on the Polygon (MATIC) network.

This repository contains verified public resources for Cube, including:

- ✅ Logos and branding files (`cube.svg`)
- ✅ Contract architecture and specifications
- ✅ Governance and rollout documentation
- ✅ Deployment and usage guides
- ✅ Security and operational notes

---

## 🌐 Network Information

- **Network**: Polygon (MATIC)  
- **Chain ID**: 137  
- **RPC URL**: https://polygon-rpc.com  
- **Block Explorer**: [Polygonscan – CubeCoin](https://polygonscan.com/address/0x966c3E5c3225af9ABdEbE8Db52D65f51E63037C6)

---

## 📜 Core Contracts

| Contract             | Address                                      | Purpose                                           |
|----------------------|----------------------------------------------|---------------------------------------------------|
| `CubeCoin`           | `0x966c3E5c3225af9ABdEbE8Db52D65f51E63037C6` | ERC20 token with mint/burn, cooldown, and pause  |
| `CubeCoinUnified`    | `0x084C6970e4Efb2f72b55caCEf2b6Afa7AD5A524C` | Distribution, airdrop, and supply management     |
| `TimelockController` | `0x3cF2a1F7Ff3A2bFfB9f6c6B9c7f2E6c2F3F3F3F3` | Governance and delayed execution                 |

All contracts are verified and publicly accessible on Polygonscan.

---

## 🛡️ Security & Governance

Cube implements multi-tiered access control and timelock governance:

- Role-based permissions (`MINTER_ROLE`, `PAUSER_ROLE`, `PROPOSER_ROLE`)  
- Transfer limits and cooldown protection  
- Emergency pause functionality  
- Delayed execution for critical operations  
- DAO-ready architecture with operational stewards onboarded

📄 [Governance Setup](https://github.com/cubecoinproject-ops/cube-assets/blob/main/rollout/governance-setup.md)  
📄 [Transaction Log](https://github.com/cubecoinproject-ops/cube-assets/blob/main/rollout/tx-hashes.md)

---

## 💰 Tokenomics

- **Token Name**: CubeCoin  
- **Symbol**: CUBE  
- **Total Supply**: `30,000,000,000 CUBE`  

| Allocation Type        | Amount (CUBE)       | Purpose                                           |
|------------------------|---------------------|---------------------------------------------------|
| Private & Public Sale  | 15,000,000,000       | Strategic fundraising and ecosystem onboarding    |
| Airdrop                | 5,000,000,000        | Community growth and incentives                   |
| Treasury Reserve       | 10,000,000,000       | Sustainability and deflationary burns             |

All tokens are distributed via the `Unified` contract.  
📄 [Whitepaper](https://github.com/cubecoinproject-ops/cube-assets/blob/main/docs/whitepaper.md)
📄 [Tokenomics](https://github.com/cubecoinproject-ops/cube-assets/blob/main/docs/tokenomics.md)
📄 [Governance Roles](https://github.com/cubecoinproject-ops/cube-assets/blob/main/docs/roles.md)


---

## 📁 Repository Structure
cube-assets/
├── cube.svg
├── README.md
├── LICENSE
├── docs/
│   ├── whitepaper.md
│   ├── architecture.md
│   ├── investor-brief.md
├── rollout/
│   ├── distribution-log.md
│   ├── tx-hashes.md
│   └── governance-setup.md


---

## 🧠 Philosophy

Cube is more than a token—it’s a system of meaning, resilience, and trust. Every contract, role, and transfer is designed to preserve autonomy and prepare for gradual decentralization. The ecosystem is stewarded by family, documented for community, and protected for the future.

---

## 👤 Founder

Cube was founded by **Cyrus EF**, a meaning-driven architect focused on ethical systems and resilient infrastructure. Stewardship is shared with two trusted brothers, each holding operational roles and participating in governance.

---

## 📬 Contact & Updates

- GitHub: [github.com/cubecoinproject-ops](https://github.com/cubecoinproject-ops)  
- GitHub Pages: [cubecoinproject.github.io/cube](https://cubecoinproject.github.io/cube/)  
- X (Twitter) – Cyrus EF: [@cyruscbf](https://x.com/cyruscbf)  
- Email – Cyrus EF: [cyrus.cbf@gmail.com](mailto:cyrus.cbf@gmail.com)  
- Medium: [Coming Soon]
- [Download Whitepaper (PDF)](docs/whitepaper.pdf)

---

**⚠️ Note**: All assets and documentation are proprietary. Redistribution or reuse without written permission is prohibited.  
_Last updated: October 2025_


