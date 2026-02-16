# CelestiaNFT

**The Premier NFT Marketplace on Stacks**

CelestiaNFT is a cutting-edge NFT marketplace platform built on Stacks, offering creators and collectors a seamless experience for minting, trading, and discovering digital assets with Bitcoin-secured finality.

## Features

- **Creator-Centric Minting**: Full control over SIP-009 NFTs with customizable metadata and royalties
- **Multi-Mode Trading**: Fixed-price listings, offers, and time-extended auctions
- **Bundle Sales**: Sell multiple NFTs in a single transaction
- **Escrow Protection**: Secure settlement for all trades
- **Transparent Auditability**: Full on-chain history via Clarity smart contracts

## Architecture

```
celestia-nft/
├── contracts/           # Clarity smart contracts
│   ├── nft-core.clar    # NFT implementation
│   ├── marketplace.clar # Trading engine
│   └── treasury.clar    # Fee collection
├── frontend/            # Next.js web application
├── tests/               # Clarinet + Vitest coverage
└── deployments/         # Network configurations
```

## Smart Contract Features

### NFT Contract
- SIP-009 compliant
- Metadata management
- Ownership verification
- Delegation support

### Marketplace Contract
- Fixed-price listings
- Offers and counter-offers
- Auction mechanics with bid extensions
- Bundle sales (up to 10 NFTs)
- Automated royalty distribution

## Getting Started

### Prerequisites
- [Clarinet](https://github.com/hirosystems/clarinet)
- Node.js v18+

### Installation

```bash
git clone https://github.com/jamalx-max/celestia-nft.git
cd celestia-nft
npm install
cd frontend && npm install
```

### Development

Run local devnet:
```bash
clarinet integrate
```

Launch frontend:
```bash
cd frontend
npm run dev
```

## Testing

```bash
# Run all tests
npm test

# Run with coverage
npm test -- --coverage

# Watch mode
npm test -- --watch
```

## Configuration

- Contract addresses: `frontend/src/lib/constants.ts`
- Environment variables: `frontend/.env.example`

## Royalty Structure

- Maximum royalty: 25%
- Marketplace fee: Configurable
- Creator-first enforcement on secondary sales

## Contributing

See `CONTRIBUTING.md` for guidelines.

## License

MIT License

---

Empowering creators on Bitcoin L2.
