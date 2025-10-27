# 📦 CubeCoin Distribution Log

This file documents all token transfers executed for CubeCoin distribution on the Polygon network. It includes recipient summaries, transaction metadata, and verification links via Polygonscan.

---

## 🔍 Distribution Summary

- **Network**: Polygon (Chain ID: 137)  
- **Token Contract**: `0x966c3E5c3225af9ABdEbE8Db52D65f51E63037C6`  
- **Recipients**:
  - Recipient 1: `0x67AaCEdE646fB245047C37017A42A893bb07BF73` — Total received: `1,500,000,000.0 CUBE`
  - Recipient 2: `0x6FB802e8Acf78B3243E94aaeaF2315049ad54DdC` — Total received: `1,000,000,000.0 CUBE`
- **Total Distributed**: `2,500,000,000.0 CUBE`

---

## 📊 Transfer Table

| # | Date (UTC) | Network | Token Contract | From (Sender) | To (Recipient) | Amount (CUBE) | Tx Hash | Status | Block | Gas Used (MATIC) | Gas Price (Gwei) | Gas Limit |
|---|------------|---------|----------------|----------------|----------------|----------------|---------|--------|--------|-------------------|------------------|-----------|
| 1 | —          | Polygon (137) | `0x966c3E5c...37C6` | Admin (PRIVATE_KEY) | `0x67AaCEdE...BF73` | `500,000,000.0` | `0x921d110391bed58fd4e86cb8679e7f4abe7f020203aad0358b057c2f31359c25` | Success | — | — | — | — |
| 2 | —          | Polygon (137) | `0x966c3E5c...37C6` | Admin (PRIVATE_KEY) | `0x67AaCEdE...BF73` | `500,000,000.0` | — | Success | — | — | 30 | 250,000 |
| 3 | —          | Polygon (137) | `0x966c3E5c...37C6` | Admin (PRIVATE_KEY) | `0x67AaCEdE...BF73` | `500,000,000.0` | — | Success | — | — | 30 | 250,000 |
| 4 | —          | Polygon (137) | `0x966c3E5c...37C6` | Admin (PRIVATE_KEY) | `0x6FB802e8...4DdC` | `500,000,000.0` | — | Success | — | — | 30 | 250,000 |
| 5 | —          | Polygon (137) | `0x966c3E5c...37C6` | Admin (PRIVATE_KEY) | `0x6FB802e8...4DdC` | `500,000,000.0` | — | Success | — | — | 30 | 250,000 |

---

## 📝 Notes

- Row 1 reflects the initial 500M transfer executed before explicit gas settings were applied.  
- Rows 2–5 reflect transfers with explicit gas parameters (`gasPrice = 30 gwei`, `gasLimit = 250,000`).  
- To complete missing fields (date, block, gas), refer to Polygonscan or execution logs.

---

## 🔗 Verification Links

- [CubeCoin Token on Polygonscan](https://polygonscan.com/token/0x966c3E5c3225af9ABdEbE8Db52D65f51E63037C6)  
- [Recipient 1 Wallet](https://polygonscan.com/address/0x67AaCEdE646fB245047C37017A42A893bb07BF73)  
- [Recipient 2 Wallet](https://polygonscan.com/address/0x6FB802e8Acf78B3243E94aaeaF2315049ad54DdC)

---

## ⚙️ Optional: Auto-Fill Script

To populate missing fields using Polygonscan API, use the following Node.js script:

```javascript
// scripts/update-distribution-log.js
const fs = require('fs');
const axios = require('axios');

const TOKEN = '0x966c3E5c3225af9ABdEbE8Db52D65f51E63037C6';
const ADMIN = process.env.DEPLOYER_ADDRESS;
const API = process.env.POLYGONSCAN_API_KEY;

async function fetchTokenTxs() {
  const url = `https://api.polygonscan.com/api?module=account&action=tokentx&contractaddress=${TOKEN}&address=${ADMIN}&sort=asc&apikey=${API}`;
  const { data } = await axios.get(url);
  if (data.status !== '1') throw new Error(data.message || 'API error');
  return data.result;
}

(async () => {
  const txs = await fetchTokenTxs();
  console.log(`Fetched ${txs.length} token transfers for admin.`);
})();
---

## 🔐 Final Checklist

- Use verified hashes and timestamps from Polygonscan  
- Never commit private keys—use environment variables only  
- Keep this file updated as new distributions occur
