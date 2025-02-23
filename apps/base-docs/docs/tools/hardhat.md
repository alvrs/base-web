---
title: Hardhat
slug: /tools/hardhat
---

# Hardhat

Hardhat is an Ethereum development environment for flexible, extensible, and fast smart contract development.

You can use Hardhat to edit, compile, debug, and deploy your smart contracts to Base.

---

# Using Hardhat with Base

To configure [Hardhat](https://hardhat.org/) to deploy smart contracts to Base, update your project’s `hardhat.config.ts` file by adding Base as a network:

```typescript
networks: {
   // for mainnet
   "base-mainnet": {
     url: 'https://mainnet.base.org',
     accounts: [process.env.WALLET_KEY as string],
     gasPrice: 1000000000,
   },
   // for testnet
   "base-goerli": {
     url: "https://goerli.base.org",
     accounts: [process.env.PRIVATE_KEY as string]
     gasPrice: 1000000000,
   },
   // for local dev environment
   "base-local": {
     url: "http://localhost:8545",
     accounts: [process.env.PRIVATE_KEY as string]
     gasPrice: 1000000000,
   },
 },
 defaultNetwork: "base-local",
```

:::info

For a complete guide on using Hardhat to deploy contracts on Base, see [Deploying a Smart Contract](/guides/deploy-smart-contracts).

:::

---
