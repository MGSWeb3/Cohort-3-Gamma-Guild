# Week 1 Day 2: Blockchain Infrastructure Research
**Student Name:** Benita 
**Date:** 07-Nov-2025  
**Tweet Link:** [https://x.com/basil_benita/status/1986696416991830440]

---

## Part 1: Blockchain Infrastructure Research

### Blockchain 1: Bitcoin (BTC)

**Node Types:**  
- Full nodes: Independently validate all transactions and blocks.  
- SPV/Light nodes: Only download block headers; rely on full nodes for verification.  

**Client Implementations:**  
- Bitcoin Core (official)  
- BTCD, bcoin, Libbitcoin  

**Consensus Mechanism:**  
- Proof of Work (PoW): miners solve cryptographic puzzles to propose blocks.  

**Block Validators:**  
- Miners: verify transactions and add blocks by solving PoW puzzles.  

**Performance Metrics:**  
- Block time: ~10 minutes  
- TPS: ~7  
- Energy usage: Very high  

**Sources:**  
- [Bitcoin.org](https://bitcoin.org)  
- [Investopedia: Bitcoin](https://www.investopedia.com/terms/b/bitcoin.asp)  

---

### Blockchain 2: Ethereum (ETH)

**Node Types:**  
- Full nodes, archive nodes, light nodes  

**Client Implementations:**  
- Geth (Go), Nethermind (.NET), Besu (Java)  

**Consensus Mechanism:**  
- Proof of Stake (PoS) after Ethereum 2.0 upgrade  

**Block Validators:**  
- Validators stake ETH to propose and confirm blocks  

**Performance Metrics:**  
- Block time: ~12–14 seconds  
- TPS: 30–100  
- Energy usage: Low  

**Sources:**  
- [Ethereum.org](https://ethereum.org)  
- [CoinDesk: Ethereum](https://www.coindesk.com/learn/what-is-ethereum)  

---

### Blockchain 3: Solana (SOL)

**Node Types:**  
- Validator nodes: produce blocks and validate transactions  
- Archiver nodes: store historical data  

**Client Implementations:**  
- Solana Validator Software (Rust-based)  

**Consensus Mechanism:**  
- Proof of History (PoH) + PoS hybrid  

**Block Validators:**  
- Staked validators confirm blocks based on PoH sequencing  

**Performance Metrics:**  
- Block time: ~400 milliseconds  
- TPS: 50,000+  
- Energy usage: Low  

**Sources:**  
- [Solana.com](https://solana.com)  
- [Binance Academy: Solana](https://academy.binance.com/en)  

---

### Blockchain 4: Cardano (ADA)

**Node Types:**  
- Core nodes: produce blocks  
- Relay nodes: relay data between nodes  

**Client Implementations:**  
- Cardano-node (Haskell)  
- Daedalus wallet (full node)  

**Consensus Mechanism:**  
- Ouroboros PoS  

**Block Validators:**  
- Slot leaders: selected staked validators produce blocks  

**Performance Metrics:**  
- Block time: ~20 seconds  
- TPS: 250–1,000  
- Energy usage: Low  

**Sources:**  
- [Cardano.org](https://cardano.org)  
- [IOHK Research](https://iohk.io/en/research/)  

---

### Comparison Table

| Blockchain | Consensus | Node Types | Main Client | Block Time | Validator Type |
|------------|-----------|------------|-------------|------------|----------------|
| Bitcoin    | PoW       | Full, SPV  | Bitcoin Core| 10 min     | Miner          |
| Ethereum   | PoS       | Full, Light, Archive | Geth | 12–14 sec | Validator |
| Solana     | PoH + PoS | Validator, Archiver | Solana Validator | 400 ms | Staked Validator |
| Cardano    | PoS (Ouroboros) | Core, Relay | Cardano-node | 20 sec | Slot Leader |

---

### Key Takeaways
1. PoW blockchains are secure but slow and energy-intensive.  
2. PoS blockchains are faster and more energy-efficient.  
3. Solana is optimized for extremely high throughput.  
4. Cardano emphasizes formal verification and sustainable operations.  
5. Node types influence speed, validation independence, and storage.  

---

## Part 2: Distributed Ledger Technology vs Blockchain

### Introduction
Distributed Ledger Technology (DLT) is a decentralized system that records transactions across multiple nodes. Blockchain is one type of DLT, using a chain of blocks to store immutable data.  

### What is DLT?
- Decentralized database shared among participants  
- Synchronizes records without a central authority  
- Ensures transparency, immutability, and trust  

### What Makes Blockchain Special?
- Data stored in **chronologically linked blocks**  
- Uses cryptography and consensus (PoW/PoS)  
- Supports smart contracts and programmable assets  

### Key Differences Between DLT and Blockchain

| Feature | DLT | Blockchain |
|---------|-----|-----------|
| Data Structure | Graph, table, ledger | Chain of blocks |
| Consensus | Flexible, not always PoW/PoS | PoW, PoS, PoH |
| Transparency | Public or private | Mostly public |
| Immutability | Varies | High |
| Use Cases | Banking, supply chain | Crypto, NFTs, DeFi |

---

### Non-Blockchain DLT Examples

**Hyperledger Fabric**  
- Permissioned enterprise DLT  
- Uses channels, modular consensus  
- No global block chain, private data control  
- Use cases: Supply chain, finance  
- Advantages: Faster, private  

**Corda**  
- Enterprise DLT for regulated environments  
- Transactions between participants, no global chain  
- Use cases: Banking, insurance, trade finance  
- Advantages: Confidentiality, compliance  

**IOTA Tangle**  
- DLT for IoT devices  
- DAG structure; each transaction validates others  
- Use cases: IoT micropayments  
- Advantages: High scalability, feeless, low energy  

---

### Comparison Table: Blockchain vs Non-Blockchain DLT

| Feature | Blockchain | Non-Blockchain DLT |
|---------|-----------|------------------|
| Data Structure | Linked blocks | DAG, transaction graph |
| Consensus | PoW/PoS | Pluggable, transaction-based |
| Scalability | Moderate | High (Tangle) |
| Energy Efficiency | Low | High |
| Use Cases | Crypto, NFTs, DeFi | Enterprise, IoT, finance |

---

### Deep Analysis
- Use **blockchain** for decentralized, trustless systems (crypto, NFTs).  
- Use **other DLTs** when privacy, speed, and regulatory compliance matter (finance, IoT).  
- Blockchain is a subset of DLT; application needs determine which to use.  

---

## Part 3: NFTs and Fungible Tokens – Digital Transformation

### Fungible Tokens
- Interchangeable, divisible (BTC, ETH)  
- Used as currency, staking, or platform utility  

### NFTs
- Unique digital assets representing ownership  
- Non-interchangeable; programmable and verifiable on blockchain  

### NFTs and Tokens Conquering the Physical World
- Digitize real-world assets  
- Enable fractional ownership, global access, smart contracts  
- Reduce reliance on intermediaries  

---

### Real-World Examples

1. **Decentraland** – Virtual land NFTs on Ethereum; digital real estate.  
2. **NBA Top Shot** – Collectible highlight moments; fans own unique sports moments.  
3. **VeVe Collectibles** – Licensed digital collectibles (Marvel/DC); global pop culture access.  
4. **RealT** – Fractional real estate ownership via Ethereum tokens.  
5. **CryptoKitties** – Digital collectible cats; first mainstream NFT adoption.  

---

### Comparison Table: Physical vs Digital Ownership

| Feature | Physical Ownership | Digital Ownership (NFTs/Tokens) |
|---------|------------------|--------------------------------|
| Ownership Verification | Legal docs | Blockchain ledger |
| Transfer Speed | Days/weeks | Seconds/minutes |
| Transfer Cost | High | Low |
| Storage | Physical | Digital wallet |
| Divisibility | Limited | Fractional possible |
| Global Accessibility | Restricted | Worldwide |
| Fraud Prevention | Moderate | High |
| Intermediaries | Required | Optional |
| Programmable Features | None | Smart contracts |

---

### Deep Analysis: The Future of Ownership
- Digital ownership transforms access, investment, and trading  
- NFTs and tokens remove intermediaries, enable fractional ownership, and programmable assets  
- Hybrid economy with physical + digital assets is emerging  

---

### Sources (12–15)
1. [Bitcoin.org](https://bitcoin.org)  
2. [Ethereum.org](https://ethereum.org)  
3. [Solana.com](https://solana.com)  
4. [Cardano.org](https://cardano.org)  
5. [IOHK Research](https://iohk.io/en/research/)  
6. [Binance Academy: Solana](https://academy.binance.com/en)  
7. [Investopedia: Bitcoin](https://www.investopedia.com/terms/b/bitcoin.asp)  
8. [CoinDesk: Ethereum](https://www.coindesk.com/learn/what-is-ethereum)  
9. [Hyperledger Fabric Docs](https://hyperledger-fabric.readthedocs.io)  
10. [Corda Documentation](https://docs.corda.net)  
11. [IOTA Tangle Overview](https://www.iota.org)  
12. [Decentraland](https://decentraland.org)  
13. [NBA Top Shot](https://nbatopshot.com)  
14. [RealT](https://realt.co)  
15. [CryptoKitties](https://www.cryptokitties.co)
