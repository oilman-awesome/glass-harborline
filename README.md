# Glass Harborline (Built for Base)

Glass Harborline is a browser-first Base utility focused on validating network connectivity, inspecting balances, and observing block-level data using Coinbase Wallet SDK and official Base RPC endpoints.

---

## Repository layout

- app/glass-harborline.ts  
  Frontend script responsible for wallet connection, Base chain validation, and read-only RPC queries.

- contracts/  
  Solidity contracts deployed to Base Sepolia for testnet validation:
  - MinimaltokenExercise.sol — minimal contract for deployment and verification checks  

- config/base.networks.json  
  Static configuration file describing supported Base networks, chainIds, RPC endpoints, and explorer URLs used by the application.

- package.json  
  Dependency manifest referencing Coinbase SDKs and multiple Base repositories.

- README.md  
  Technical documentation and testnet deployment records.

---

## Base network context

This project explicitly targets Base networks and enforces Base-compatible chain identifiers.

Base Mainnet  
chainId (decimal): 8453  
Explorer: https://basescan.org  

Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

---

## Capabilities overview

The application provides a minimal, auditable surface for interacting with Base networks in a strictly read-only manner:

- Coinbase Wallet connection  
- ChainId validation for Base networks  
- ETH balance inspection for arbitrary addresses  
- Live block metadata retrieval  
- Direct Basescan references for external verification  

No transactions are signed or broadcast.

---

## Tooling and dependencies

This repository integrates tooling from both the Base and Coinbase open-source ecosystems:

- Coinbase Wallet SDK for EIP-1193 wallet access  
- OnchainKit references for Base-aligned primitives  
- viem for efficient, read-only RPC communication  
- Multiple Base and Coinbase GitHub repositories to reflect ecosystem integration  

---

## License

MIT License

Copyright (c) 2025 YOUR_NAME

---

## Author
Public contact: https://x.com/Augusti77766634

GitHub: https://github.com/oilman-awesome

Email: oilman.awesome_0u@icloud.com 

---

## Testnet Deployment (Base Sepolia)

As part of pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm correct behavior and tooling compatibility.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract MinimaltokenExercise.sol address:  
0x5ece528e83045086fe9944f8fd76cbf3349e2632

Deployment and verification:
- https://sepolia.basescan.org/address/0x5ece528e83045086fe9944f8fd76cbf3349e2632
- https://sepolia.basescan.org/0x5ece528e83045086fe9944f8fd76cbf3349e2632/0#code  

These testnet deployments provide a controlled environment for validating Base tooling, account abstraction flows, and read-only onchain interactions prior to Base Mainnet usage.
