# ArtChain-NFT

A high-performance, decentralized NFT marketplace ecosystem built with Account Abstraction (ERC-4337) and a scalable event-driven architecture.

## Architecture Overview

The ecosystem consists of four specialized services working in unison:

### Core Services

| Service | Repository | Technologies | Description |
| :--- | :--- | :--- | :--- |
| **Smart Contracts** | [contracts-core](https://github.com/NFT-marketplace-blockchain/contracts-core) | Hardhat, Solidity, ERC-4337 | Core marketplace protocol, NFT standards, and Smart Account infrastructure. |
| **API Service** | [api-service](https://github.com/NFT-marketplace-blockchain/api-service) | FastAPI, Python, Web3.py | Off-chain indexer, REST API for data query, and WebSocket gateway. |

### User Interfaces

| Application | Repository | Technologies | Description |
| :--- | :--- | :--- | :--- |
| **Web Client** | [web-client](https://github.com/NFT-marketplace-blockchain/nft-marketplace-admin) | Next.js 15, Wagmi | Primary marketplace interface for trading, collecting, and wallet management. |
| **Admin Portal** | [admin-portal](https://github.com/NFT-marketplace-blockchain/nft-marketplace-app) | Vite, React, Shadcn | Dashboard for platform operations, campaign management, and analytics. |

## System Workflow

1.  **Blockchain Layer**: Assets and Orders are secured on-chain (Sepolia). Account Abstraction allows gasless transactions.
2.  **Indexing Layer**: The **API Service** listens to contract events in real-time, indexing them into a query-optimized database.
3.  **Application Layer**: 
    *   **Web Client** queries the API for fast display and interacts directly with Contracts for execution.
    *   **Admin Portal** manages system configurations and operational data.


#### Core Contracts

| Contract | Address |
|----------|----------|
| Artwork | `0x0b7F8D5DC1ac5B285D26EF4a8778974Cda84bd5A` |
| CampaignManager | `0xa18A951a574A58B7858Ce0aF68D66bD8cA28aA48` |
| Marketplace | `0xcf1cE94896e93d2853583479aB8cf55b48241DC0` |

#### Account Abstraction (ERC-4337)

| Contract | Address |
|----------|----------|
| SimpleAccountFactory | `0xe52624AEefD0E8f1eCdA03E9376518c56D25C4Ef` |
| EntryPoint (v0.6) | `0x5FF137D4b0FDCD49DcA30c7CF57E578a026d2789` |

### Frontend (.env.local)

```env
NEXT_PUBLIC_SEPOLIA_RPC_URL=https://eth-sepolia.g.alchemy.com/v2/YOUR_KEY
NEXT_PUBLIC_CAMPAIGN_MANAGER_ADDRESS=0xa18A951a574A58B7858Ce0aF68D66bD8cA28aA48
NEXT_PUBLIC_MARKETPLACE_ADDRESS=0xcf1cE94896e93d2853583479aB8cf55b48241DC0
NEXT_PUBLIC_FACTORY_ADDRESS=0xe52624AEefD0E8f1eCdA03E9376518c56D25C4Ef
NEXT_PUBLIC_ENTRYPOINT_ADDRESS=0x5FF137D4b0FDCD49DcA30c7CF57E578a026d2789
NEXT_PUBLIC_PIMLICO_API_KEY=your-pimlico-api-key
NEXT_PUBLIC_WEB3AUTH_CLIENT_ID=your-web3auth-client-id
NEXT_PUBLIC_API_BASE_URL=http://localhost:8000
```

### Backend (.env)

```env
DATABASE_URL=sqlite:///./marketplace.db
SECRET_KEY=your-secret-key
SEPOLIA_RPC_URL=https://eth-sepolia.g.alchemy.com/v2/YOUR_KEY
CONTRACT_ADDRESS_CAMPAIGN=0xa18A951a574A58B7858Ce0aF68D66bD8cA28aA48
CONTRACT_ADDRESS_MARKETPLACE=0xcf1cE94896e93d2853583479aB8cf55b48241DC0
```

### Blockchain (.env)

```env
SEPOLIA_RPC_URL=https://eth-sepolia.g.alchemy.com/v2/YOUR_KEY
PRIVATE_KEY=your-private-key
ETHERSCAN_API_KEY=your-etherscan-api-key
```

## 📚 Project Documentation

Each module has detailed documentation:

- **[Smart Contracts](https://github.com/NFT-marketplace-blockchain/contracts-core)** - Smart contracts, deployment, testing
- **[Frontend](https://github.com/NFT-marketplace-blockchain/frontend-nextjs)** - User interface, Web3 integration, AA implementation
- **[Admin Dashboard](https://github.com/NFT-marketplace-blockchain/frontend-admin)** - Admin dashboard features and setup
- **[Backend API](https://github.com/NFT-marketplace-blockchain/api-service)** - API endpoints, authentication, database

## Deployment

The system is currently deployed on the **Sepolia Testnet**.

*   **Network**: Sepolia
*   **Indexer Status**: Active
*   **Contracts**: Deployed & Verified
## 📞 Support

- Email: tphbang.dev@gmail.com
- Email: nguyenminhkhoi02092003@gmail.com

## 🙏 Acknowledgments

- [OpenZeppelin](https://openzeppelin.com/) - Smart contract libraries
- [Pimlico](https://pimlico.io/) - Account Abstraction infrastructure
- [Web3Auth](https://web3auth.io/) - Social login solution
- [Shadcn UI](https://ui.shadcn.com/) - UI components
- [Hardhat](https://hardhat.org/) - Ethereum development environment
---
