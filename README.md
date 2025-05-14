Here is the complete README.md for your basebuzz-contracts repo in Markdown format:

<p align="center">
  <img src="https://raw.githubusercontent.com/base-buzz/brand-kit-main/main/assets/logo.svg" alt="BaseBuzz Logo" width="120" />
</p>

<h1 align="center">BaseBuzz Smart Contracts</h1>

<p align="center">
  Trustless token mechanics for the decentralized meme market on Base.
</p>

---

## 🧾 Overview

This repository contains the **core smart contracts** powering the BaseBuzz protocol. All contracts are written in **Solidity** and deployed on the **Base** L2 chain.

These contracts manage:

- 🔁 **Token bonding curves + liquidity**
- ⏳ **FOMO & gamified buy/sell mechanics**
- 🛡️ **Immutable architecture with no admin keys**
- 🧠 **Onchain minting, reputation, and incentives**

---

## 🧠 Key Contracts

| Contract           | Description                                        |
|--------------------|----------------------------------------------------|
| `Token.sol`        | ERC-20 logic with bonding curve pricing            |
| `Fomo.sol`         | Last-buy-wins and FOMO liquidity event logic       |
| `MintManager.sol`  | Meme/NFT minting and validation manager            |
| `BuzzTreasury.sol` | Handles fee routing and reward distribution logic  |

> Smart contracts are immutable and fully verified on BaseScan.

---

## 🔐 Security & Admin Policy

- ✅ **No owner**
- 🔒 **No upgradable proxies**
- 🧱 **All contracts are immutable after deployment**
- 🔍 Verified at [BaseScan](https://basescan.org/token/0x893432C814b6e5970e5F86F8cBc3F97417A9C810)

---

## 🧪 Build & Test

```bash
pnpm install
pnpm compile
pnpm test

Supports [Foundry] or [Hardhat] workflows. See package.json for exact setup.

⸻

📄 License

MIT — see LICENSE.

⸻

🔗 Links
	•	🌐 Website
	•	📈 View BUZZ on DexScreener
	•	🧠 Whitepaper
	•	🎨 Brand Kit
	•	🐦 Twitter

⸻