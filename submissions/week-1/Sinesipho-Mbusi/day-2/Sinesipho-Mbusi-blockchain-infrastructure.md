# Week 1 Day 2 Assignment — Blockchain Infrastructure, Distributed Ledgers, NFTs & Tokens

**Author:** Sinesipho Mbusi  
**Cohort:** MGS Web3 Cohort 3 — Gamma Guild  
**Deadline:** Friday 5:00 PM  
**Deliverable Type:** Markdown research summary with comparison tables, examples, Twitter thread & citations.

---

## 1. Overview

Blockchains are a type of distributed ledger that structure transactions into cryptographically linked blocks. Different blockchains balance decentralization, throughput, and finality by using various node roles, client software, and consensus mechanisms.

Permissionless blockchains (e.g., Bitcoin, Ethereum, Solana) rely on open validators or miners, while permissioned ledgers (e.g., Hyperledger Fabric) restrict participation to known entities. NFTs (non-fungible tokens) record unique ownership metadata, whereas fungible tokens represent interchangeable value units. Ownership changes through on-chain transactions that update token registries.

---

## 2. Blockchain Research (4+ chains)

### **Bitcoin (BTC)**

- **Type:** Public, permissionless  
- **Node types:** Full nodes (validate chain), SPV/light clients (partial validation)  
- **Clients:** Bitcoin Core (reference)  
- **Consensus:** Proof-of-Work (PoW) — miners solve hash puzzles; chain with most accumulated work is valid. Probabilistic finality.

### **Ethereum (ETH)**

- **Type:** Public, permissionless  
- **Node types:** Execution nodes (EVM clients), Beacon/consensus nodes, light clients  
- **Clients:** Geth, Nethermind, Besu (execution); Lighthouse, Prysm, Teku (consensus)  
- **Consensus:** Proof-of-Stake (PoS) since the Merge — validators stake ETH and attest to blocks. Finality via epochs on the Beacon Chain.

### **Solana (SOL)**

- **Type:** Public, permissionless  
- **Node types:** Validator nodes, leader nodes (rotating), RPC nodes  
- **Clients:** Solana validator software  
- **Consensus:** Proof-of-History (PoH) combined with PoS — verifiable timestamps + leader rotation for high throughput.

### **Hyperledger Fabric (HLF)**

- **Type:** Permissioned (enterprise)  
- **Node types:** Peers (endorsers/committers), Ordering Service nodes, Clients (SDKs)  
- **Clients:** Fabric peer/orderer binaries, SDKs in Go/Node/Java  
- **Consensus:** Pluggable ordering (Raft, Kafka, BFT variants). Uses endorsement policies; no PoW/PoS. Emphasizes privacy and performance.

---

## 3. Distributed Ledgers vs Blockchains

| Aspect | Distributed Ledger | Blockchain |
|--------|-------------------|-------------|
| **Definition** | Shared database replicated across multiple nodes. | A specific type of DLT using ordered, cryptographically linked blocks. |
| **Data structure** | Can be any data model (not necessarily blocks). | Sequential blocks connected via hashes. |
| **Consensus** | May use centralized or BFT-style consensus. | Usually PoW, PoS, or hybrid mechanisms. |
| **Participants** | Often permissioned (known entities). | Can be permissionless (public). |
| **Use cases** | Enterprise systems, supply chain, banking. | DeFi, NFTs, cryptocurrencies. |

---

## 4. NFTs vs Fungible Tokens — Analysis

**NFTs (Non-Fungible Tokens):** Represent unique assets (art, collectibles, credentials). Built on ERC-721 / ERC-1155 standards. Metadata points to unique identifiers.

**Fungible Tokens:** Interchangeable assets (currencies, governance, stablecoins) under ERC-20 standard. Balances updated within one smart contract.

### Real-World Examples

| Example | Type | Blockchain | Ownership Mechanism | Real-World Impact |
|----------|------|-------------|----------------------|------------------|
| **Beeple — Everydays: The First 5000 Days** | NFT | Ethereum | ERC-721 token transfer | $69.3M sale; legitimized digital art market. |
| **CryptoPunks** | NFT | Ethereum | Smart contract-based ownership | Cultural NFT icon; drives PFP trend. |
| **Bored Ape Yacht Club (BAYC)** | NFT | Ethereum | ERC-721 token with membership rights | Exclusive community, brand collabs (Adidas). |
| **NBA Top Shot** | NFT | Flow | Marketplace transfers on Flow ledger | Sports collectibles for mainstream users. |
| **USDC** | Fungible token | Multi-chain (Ethereum, Solana, etc.) | ERC-20 transfer | Regulated stablecoin used in DeFi payments. |
| **Uniswap (UNI)** | Fungible token | Ethereum | ERC-20 transfer + governance contract | Enables decentralized governance. |
| **Chainlink (LINK)** | Fungible token | Ethereum | ERC-20 token payments to oracle nodes | Supports decentralized data oracles. |

---

## 5. Comparison Tables

### Table A — Blockchain Comparison

| Blockchain | Type | Node Roles | Clients | Consensus |
|-------------|------|-------------|----------|------------|
| **Bitcoin** | Public | Full, Light | Bitcoin Core | PoW (mining, longest chain rule) |
| **Ethereum** | Public | Execution, Consensus, Light | Geth, Besu, Prysm | PoS (staking & attestation) |
| **Solana** | Public | Validator, Leader, RPC | Solana Validator | PoH + PoS (leader rotation) |
| **Hyperledger Fabric** | Permissioned | Peers, Orderers, Clients | Fabric SDKs | Pluggable (Raft, BFT) |

### Table B — Tokens and NFTs

| Asset | Type | Chain | Ownership Transfer | Key Takeaway |
|--------|------|--------|--------------------|---------------|
| Beeple Art | NFT | Ethereum | ERC-721 | Proof of digital provenance |
| CryptoPunks | NFT | Ethereum | Smart contract transfer | Early NFT culture anchor |
| BAYC | NFT | Ethereum | Token transfer = membership | IP, branding, exclusivity |
| NBA Top Shot | NFT | Flow | Marketplace trade | Licensed sports moments |
| USDC | Fungible | Multi-chain | ERC-20 balance transfer | Stable digital currency |
| UNI | Fungible | Ethereum | ERC-20 + governance | DAO-style voting power |
| LINK | Fungible | Ethereum | ERC-20 | Powers oracles in DeFi |

---

## 6. Twitter Thread (7+ Tweets)
[Thread](https://x.com/symbusi/status/1986525259193835537)
(https://x.com/symbusi/status/1986792026122203176)

**1️⃣** Week 1 Day 2: exploring blockchain infrastructure, DLTs, NFTs & tokens. Here's the condensed version 👇  
**2️⃣** Bitcoin — PoW, miners, full nodes. Secure but energy-heavy. True decentralization OG.  
**3️⃣** Ethereum — PoS validators, smart contracts, EVM clients (Geth, Besu). Programmable money + assets.  
**4️⃣** Solana — Proof-of-History + PoS = speed & scalability. Ideal for dApps needing high TPS.  
**5️⃣** Hyperledger Fabric — permissioned DLT with Raft/BFT ordering. Enterprise-grade privacy.  
**6️⃣** DLT ≠ Blockchain. DLT = distributed database; Blockchain = DLT with cryptographic chain of blocks.  
**7️⃣** NFTs (unique) vs Fungible tokens (interchangeable). Examples: Beeple, BAYC, Top Shot, USDC, UNI, LINK.  
**8️⃣** Tokenization enables programmable ownership, new revenue models & transparent provenance. Still evolving.

---

## 7. Sources (14)

1. Nakamoto, S. — *Bitcoin: A Peer-to-Peer Electronic Cash System.*  
2. ConsenSys — *Ethereum 2.0 Beacon Chain Explained.*  
3. Solana Foundation — *Proof-of-History and Consensus Overview.*  
4. Hyperledger Fabric Docs — *Architecture and Components.*  
5. World Bank — *Distributed Ledger Technology & Blockchain Primer.*  
6. FINRA — *Blockchain Basics and DLT Distinctions.*  
7. NFTNow — *What is an NFT?*  
8. ERC Standards — *ERC-20, ERC-721, ERC-1155 Specifications.*  
9. The Verge — *Beeple’s $69M NFT Sale at Christie’s.*  
10. Investopedia — *CryptoPunks & Early NFT Collections.*  
11. Flow Docs — *NBA Top Shot Architecture.*  
12. Circle — *USDC Stablecoin Transparency Report.*  
13. Uniswap Blog — *UNI Governance Launch Announcement.*  
14. Chainlink Docs — *LINK Token Economics and Oracle Network.*

---

### **Submission Summary**
>
> **Week 1 Day 2 Deliverables:** Research notes, comparison tables, NFT vs Token analysis, Twitter thread, and 14 cited sources.

---

**Prepared by:** Sinesipho Mbusi  
*MGS Web3 — Gamma Guild (Cohort 3)*
