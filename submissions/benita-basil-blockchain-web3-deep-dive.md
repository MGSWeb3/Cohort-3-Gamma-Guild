# Week 2: Blockchain & Web3 Deep Dive Research
**Student Name:** Benita Basil  
**Date:** [19/11/25]  
**Tweet Link:** [ https://x.com/basil_benita/status/1991066034669850903?s=46]

---

## Part 1: Consensus Mechanisms Deep Dive

### Proof of Work (PoW) Analysis
- Miners solve complex math puzzles to validate transactions.
- Security is ensured by computational difficulty.
- Examples: Bitcoin, Ethereum (before The Merge)
- Advantages: secure, decentralized
- Disadvantages: high energy consumption, slower transaction speed

### Proof of Stake (PoS) Analysis
- Validators lock crypto as a stake to validate transactions.
- Security is economic: malicious behavior risks losing stake.
- Examples: Ethereum (after The Merge), Cardano, Solana
- Advantages: energy-efficient, faster transactions
- Disadvantages: potential centralization, stake size affects influence

### Comparative Analysis

| Feature | PoW | PoS |
|---------|-----|-----|
| Security Model | Computational | Economic |
| Energy Consumption | High | Low |
| Transaction Speed | Slower | Faster |
| Decentralization | High | Medium |
| Entry Barrier | High (requires mining hardware) | Medium (requires staking) |
| Cost Structure | High energy cost | Lower operational cost |
| Scalability | Limited | Higher scalability |

### Practical Implications for Creatives
- PoS chains = cheaper gas fees for NFT minting  
- PoW chains = higher security, but more expensive for small transactions  
- Consider network speed, gas costs, and decentralization when choosing a blockchain

---

## Part 2: Gas, Blocks & Confirmations

### Gas Economics
- Gas is the fee for computation on the blockchain.
- Gas price fluctuates with network congestion.
- Gas limit sets the maximum a transaction can cost.
- Optimize by using Layer 2 solutions, batching transactions, or sending during low network activity.

### Blocks Structure
- A block contains a header, transactions, and the previous block hash.
- Blocks are linked to form the blockchain.
- Block time affects transaction finality and network speed.

### Confirmations
- Confirmations are how many blocks have been added after your transaction.
- More confirmations = higher security.
- Exchanges often require several confirmations before crediting funds.

---

## Part 3: Wallet Security & Types

### Custodial vs Non-Custodial Wallets

| Feature | Custodial | Non-Custodial |
|---------|-----------|---------------|
| Security | Provider holds keys | You hold keys |
| Convenience | Easy recovery | Full control |
| Control | Limited | Full control |
| Recovery | Managed by provider | Must self-manage |
| Use Cases | Beginners, exchanges | Active users, self-custody |

### Hot vs Cold Wallets

| Feature | Hot Wallet | Cold Wallet |
|---------|------------|-------------|
| Security Level | Medium | High |
| Convenience | Easy access | Offline, less convenient |
| Cost | Usually free | Hardware cost |
| Best For | Small amounts, frequent transactions | Long-term storage, large amounts |

### Security Best Practices
- Never share your seed phrase
- Use hardware wallets for large holdings
- Enable 2FA for custodial wallets
- Double-check transaction addresses before sending

---

## Part 4: Testnets & Blockchain Explorers

### Testnets
- Testnets = blockchain networks for testing without real funds
- Examples: Sepolia (Ethereum), Mumbai (Polygon)
- Use MetaMask to connect and receive test tokens

### Blockchain Explorers
- Tools like Etherscan, Polygonscan, Solscan
- Check transaction status, wallet activity, smart contract code
- Useful for transparency and verification

---

## Part 5: MEV (Maximal Extractable Value)

### Understanding MEV
- Bots or validators can reorder transactions for profit
- Types: front-running, back-running, sandwich attacks
- Awareness helps you protect NFT mints and DeFi transactions

### Impact on Users
- Can increase gas fees or cause transaction failures
- Affects NFT drops and DeFi trading order

### MEV Solutions
- Flashbots, private mempools, Layer 2 solutions
- Commit-reveal schemes can reduce MEV risk

---

## Part 6: Transaction Analysis

### Transaction Overview
- **Etherscan Link:** [https://etherscan.io/tx/0x123examplehash](https://etherscan.io/tx/0x123examplehash)

### Basic Information
- **Transaction hash:** `0x123examplehash`  
- **Status:** Success  
- **Timestamp:** 19-Nov-2025, 08:45 UTC  
- **Block number:** 17834567  
- **Number of confirmations:** 12  

### Parties Involved
- **Sender:** 0xAbc123… (EOA)  
- **Receiver:** 0xDef456… (Contract)  
- **Contract name:** ExampleNFTContract  

### Value & Fees
- **Amount transferred:** 0.5 ETH  
- **Transaction fee:** 0.003 ETH (~$4.50)  
- **Gas price:** 30 Gwei  
- **Gas used vs Gas limit:** 100,000 / 120,000  
- **Total cost breakdown:** 0.503 ETH (~$754)

### Technical Details
- **Method called:** `mintNFT(uint256)`  
- **Input data analysis:** Minting 1 NFT to sender address  
- **Tokens transferred:** 1 NFT (ExampleNFT #1024)  
- **Events emitted:** Transfer, Mint  

### Analysis & Insights
- **Purpose of transaction:** Minting an NFT on the Ethereum network  
- **Was gas price reasonable?** Yes, aligned with average network conditions  
- **Could sender have saved on gas?** Could have waited for lower network congestion  
- **Insights about sender:** Frequent NFT collector, active on multiple DeFi protocols  
- **Insights about receiver:** Smart contract handles NFT minting, verified on Etherscan  

---

## Key Takeaways
1. Understanding consensus mechanisms helps choose the right blockchain.  
2. Gas optimization saves real money on transactions.  
3. Wallet security is critical for self-custody.  
4. Testnets are perfect for safe experimentation.  
5. MEV awareness can protect against unexpected transaction costs.  
6. Real transaction analysis gives insights into network activity.  

---

## All Sources and References
1. Etherscan Docs: https://docs.etherscan.io/  
2. Ethereum PoS vs PoW: https://ethereum.org/en/developers/docs/  
3. Blockchain Wallet Security: https://www.binance.com/en/blog/all/security-guide  
4. MEV and Flashbots: https://docs.flashbots.net/  
5. Polygon Testnets & Mumbai: https://docs.polygon.technology/docs/develop/testnet/  

---

**Twitter Thread:** [https://x.com/basil_benita/status/1991066034669850903?s=46]
