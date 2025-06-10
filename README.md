<p align="center">
  <img src="https://github.com/base-buzz/basebuzz/raw/main/assets/basebuzz-logo.png" alt="BaseBuzz Logo" width="200"/>
</p>

<h1 align="center">BaseBuzz Smart Contracts</h1>

<p align="center">
  <strong>Decentralized social network smart contracts powering meme culture on Base blockchain</strong>
</p>

<p align="center">
  <a href="https://base.buzz"><img src="https://img.shields.io/badge/Website-base.buzz-blue?style=for-the-badge" alt="Website"/></a>
  <a href="https://github.com/base-buzz/basebuzz"><img src="https://img.shields.io/badge/GitHub-Repository-black?style=for-the-badge&logo=github" alt="GitHub"/></a>
  <a href="https://sepolia.basescan.org/address/0x2D45b79dCe3E217B12cF4cf8eeCE7A02322c7A02"><img src="https://img.shields.io/badge/BaseScan-Verified-green?style=for-the-badge" alt="Verified"/></a>
  <a href="#"><img src="https://img.shields.io/badge/Audit-Pending-yellow?style=for-the-badge" alt="Audit Status"/></a>
</p>

---

## 🚀 Overview

BaseBuzz is a decentralized social network built on Base that revolutionizes meme culture through blockchain technology. Our smart contracts enable users to create, mint, trade, and collect meme-based content through innovative hybrid mechanisms.

### Key Features

- 🎯 **Hybrid Moments**: Trade ERC20 tokens AND/OR mint NFTs for the same content
- 🔥 **Dynamic Bonding Curves**: Exponential price discovery with 1-5% dynamic fees
- 🎨 **Multi-Tier NFT System**: Configurable tiers with custom pricing and metadata
- 🛡️ **Anti-Spam Protection**: Daily limits and progressive fees by user level
- 💎 **Creator Bonds**: 0.01 ETH bonds prevent rug pulls and ensure delivery
- 🎮 **Quest Engine**: On-chain engagement mining with BASEBUZZ token rewards

---

## 📋 Contract Architecture

### Core System (V2 Hybrid)

| Contract                  | Address                                                                                            | Description                                  |
| ------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------- |
| **HybridMomentFactoryV2** | [`0x2D45...7A02`](https://sepolia.basescan.org/address/0x2D45b79dCe3E217B12cF4cf8eeCE7A02322c7A02) | Main factory for creating hybrid moments     |
| **AntiSpamManager**       | [`0xbeB3...dC75`](https://sepolia.basescan.org/address/0xbeB3B0D27B68067FDbAF2D6528D9535e2a15dC75) | Manages daily limits and spam prevention     |
| **CreatorBondManager**    | [`0xB146...FaDa`](https://sepolia.basescan.org/address/0xB14645b0ebb4eBba51a0cbD1b88FA66b5E36FaDa) | Handles creator bonds and delivery deadlines |
| **QuestRegistry**         | [`0x14D6...4a43`](https://sepolia.basescan.org/address/0x14D6B7A565f62D2930319fA32ef08E0b6b6f4a43) | Quest system and BASEBUZZ rewards            |

### Implementation Templates

| Contract                   | Address                                                                                            | Description                           |
| -------------------------- | -------------------------------------------------------------------------------------------------- | ------------------------------------- |
| **DynamicFeeBondingCurve** | [`0xCE00...aFe6`](https://sepolia.basescan.org/address/0xCE00c7C3B0979E1E67Fc5caB3A6b1B8eD8C1aFe6) | ERC20 bonding curve implementation    |
| **TieredNFTMinter**        | [`0x1be3...0C4B`](https://sepolia.basescan.org/address/0x1be3a1A44D9E4e34e8Ef8FEAB41F86b8fE3E0C4B) | Multi-tier NFT minting implementation |

### Token Contracts

| Contract     | Network      | Address                                                                                                                 | Description                      |
| ------------ | ------------ | ----------------------------------------------------------------------------------------------------------------------- | -------------------------------- |
| **BASEBUZZ** | Base Mainnet | [`0x893432c814b6e5970e5f86f8cbc3f97417a9c810`](https://basescan.org/address/0x893432c814b6e5970e5f86f8cbc3f97417a9c810) | Main governance and reward token |

---

## 🏗️ Repository Structure

```
basebuzz-contracts/
├── src/                          # Smart contract source code
│   ├── HybridMomentFactoryV2.sol    # Main factory contract
│   ├── DynamicFeeBondingCurve.sol   # ERC20 bonding curve implementation
│   ├── TieredNFTMinter.sol          # Multi-tier NFT minting
│   ├── AntiSpamManager.sol          # Spam prevention and user levels
│   ├── CreatorBondManager.sol       # Creator bond management
│   ├── QuestRegistry.sol            # Quest system and rewards
│   ├── BASEBUZZ.sol                 # Main token contract
│   ├── interfaces/                  # Contract interfaces
│   └── mocks/                       # Testing utilities
├── script/                       # Deployment and utility scripts
├── test/                         # Comprehensive test suite
├── deployments/                  # Deployment artifacts and records
└── foundry.toml                  # Foundry configuration
```

---

## 🛠️ Development

### Prerequisites

- [Foundry](https://book.getfoundry.sh/getting-started/installation)
- [Git](https://git-scm.com/downloads)

### Installation

```bash
# Clone the repository
git clone https://github.com/base-buzz/basebuzz-contracts.git
cd basebuzz-contracts

# Install dependencies
forge install

# Build contracts
forge build
```

### Testing

```bash
# Run all tests
forge test

# Run tests with verbosity
forge test -vvv

# Run specific test file
forge test --match-path test/HybridMomentFactoryV2.t.sol

# Generate gas report
forge test --gas-report
```

### Deployment

```bash
# Deploy to Base Sepolia (testnet)
forge script script/DeployHybridV2.s.sol:DeployHybridV2 \
    --rpc-url $BASE_SEPOLIA_RPC \
    --private-key $DEPLOYER_PRIVATE_KEY \
    --broadcast \
    --verify

# Deploy to Base Mainnet (production)
forge script script/DeployHybridV2.s.sol:DeployHybridV2 \
    --rpc-url $BASE_MAINNET_RPC \
    --private-key $DEPLOYER_PRIVATE_KEY \
    --broadcast \
    --verify
```

---

## 🔒 Security

### Audit Status

- **Current Status**: ⏳ Audit in progress
- **Audit Firms**: [Pending selection - submit audit proposals](mailto:security@base.buzz)
- **Bug Bounty**: [Contact us](mailto:security@base.buzz) for responsible disclosure

### Security Features

- ✅ **Creator Bonds**: 0.01 ETH deposits prevent malicious behavior
- ✅ **Daily Limits**: Anti-spam protection with progressive fees
- ✅ **Access Controls**: Role-based permissions for critical functions
- ✅ **Reentrancy Guards**: Protection against reentrancy attacks
- ✅ **Integer Overflow**: SafeMath and Solidity 0.8+ built-in protections
- ✅ **Input Validation**: Comprehensive parameter validation

### Known Limitations

- **Bonding Curve Pricing**: Current exponential curves result in high token prices (>0.1 ETH for small amounts)
- **Testnet Only**: V2 system currently deployed on Base Sepolia, mainnet deployment pending

---

## 📊 System Specifications

### Network Support

- **Primary**: Base (Chain ID: 8453)
- **Testnet**: Base Sepolia (Chain ID: 84532)

### Configuration

- **Platform Fee**: 2.5% on all transactions
- **Creator Bond**: 0.01 ETH minimum required
- **Quest Reward Pool**: 10M BASEBUZZ tokens
- **Anti-Spam Limits**: 5-50 mints, 10-100 trades per day (level-based)

### Gas Optimization

- **Proxy Patterns**: Minimal proxy (EIP-1167) for cost-efficient deployment
- **Batch Operations**: Combined transactions for hybrid interactions
- **Optimized Storage**: Packed structs and efficient data layouts

---

## 📚 Documentation

- 📖 **Technical Documentation**: Available on request for developers
- 🔧 **Integration Guide**: Contact team@base.buzz for integration support
- 📋 **API Reference**: See contract interfaces in `src/interfaces/`
- 🔒 **Security Guide**: Contact security@base.buzz for security documentation
- 📈 **Contract Specifications**: Available in source code comments

---

## 🌐 Links

- **Website**: [base.buzz](https://base.buzz)
- **Main Repository**: [github.com/base-buzz/basebuzz](https://github.com/base-buzz/basebuzz)
- **Documentation**: [docs.base.buzz](https://base.buzz) _(coming soon)_
- **Discord**: [discord.gg/basebuzz](https://discord.gg/basebuzz) _(coming soon)_
- **Twitter**: [@realBaseBuzz](https://twitter.com/realBaseBuzz)

---

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](./CONTRIBUTING.md) for details.

### Development Workflow

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Write tests for your changes
4. Ensure all tests pass (`forge test`)
5. Commit your changes (`git commit -m 'Add amazing feature'`)
6. Push to the branch (`git push origin feature/amazing-feature`)
7. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.

---

## ⚠️ Disclaimer

This software is provided "as is", without warranty of any kind. The contracts are currently unaudited and should be used at your own risk. Always conduct your own research and due diligence before interacting with smart contracts.

---

<p align="center">
  <strong>Built with ❤️ by the BaseBuzz team</strong>
</p>
