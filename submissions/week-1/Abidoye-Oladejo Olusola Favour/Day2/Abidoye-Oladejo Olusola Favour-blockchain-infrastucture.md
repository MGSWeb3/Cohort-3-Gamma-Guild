# Week 1 Day 2 Assignment — Blockchain Infrastructure, Distributed Ledgers, NFTs & Tokens

**Author:** Abidoye-Oladejo Olusola Favour
**Cohort:** MGS Web3 Cohort 3 — Gamma Guild  
**Deadline:** Friday 5:00 PM  
**Deliverable Type:** Markdown research summary with comparison tables, examples, Twitter thread & citations.

# 📘 Blockchain Infrastructure Research

**Comprehensive Analysis — Week 1 Day 2 Assignment**
**Cohort 3 Gamma Guild — By Abidoye-Oladejo Olusola Favour**

---

## Part 1: Blockchain Infrastructure Comparison

### 1.1 Bitcoin

#### **Network Architecture**

* **Node Types:** Full nodes, Light nodes, Mining nodes, Pruned nodes
* **Primary Client:** Bitcoin Core (~95% adoption)
* **Consensus:** Proof of Work (PoW)
* **Block Time:** ~10 minutes

#### **Key Characteristics**

* Strong security via energy-intensive mining
* Highly decentralized
* Limited throughput (~7 TPS)
* High energy consumption

---

### 1.2 Ethereum

#### **Network Architecture**

* **Node Types:** Full, Archive, Light (limited), Validator nodes
* **Execution Clients:** Geth, Besu, Nethermind, Erigon
* **Consensus Clients:** Lighthouse, Prysm, Nimbus, Teku, Lodestar
* **Consensus:** Proof of Stake (PoS) — Gasper
* **Slot Duration:** 12 seconds

#### **Key Characteristics**

* ~15–30 TPS (Layer 1)
* 99.9% lower energy usage post-Merge
* Modular design (execution + consensus layers)
* Supports smart contracts & dApps

---

### 1.3 Solana

#### **Network Architecture**

* **Node Types:** Validator nodes, RPC nodes
* **Consensus:** PoH + PoS + Tower BFT
* **Block Time:** ~0.4 seconds

#### **Key Characteristics**

* Up to 65,000 TPS
* Sub-second finality
* Extremely low fees
* History of occasional outages

---

### 1.4 Sui

#### **Network Architecture**

* **Node Types:** Validators (106), Full nodes (392)
* **Programming Language:** Sui Move
* **Consensus:** Delegated Proof of Stake (DPoS) + Mysticeti BFT

#### **Key Characteristics**

* ~100,000 TPS
* ~390 ms consensus latency
* Object-centric parallel execution
* 82.4% of supply staked
* Validators across 13 countries

---

### 1.5 Aptos

#### **Network Architecture**

* **Node Types:** Validator nodes, full nodes
* **Programming Language:** Aptos Move
* **Consensus:** AptosBFT (BFT + PoS)

#### **Key Characteristics**

* Up to 160,000 TPS
* Sub-second confirmation time
* Parallel execution with Block-STM v2
* Validators stake ≥1M APT
* Launched October 2022

---

## 📊 Comparative Summary Table

| Blockchain   | Consensus             | TPS      | Block Time | Primary Client    | Launch Year |
| ------------ | --------------------- | -------- | ---------- | ----------------- | ----------- |
| **Bitcoin**  | PoW                   | ~7       | ~10 min    | Bitcoin Core      | 2009        |
| **Ethereum** | PoS                   | ~15–30   | 12s        | Geth + Lighthouse | 2015        |
| **Solana**   | PoH + PoS + Tower BFT | ~65,000  | 0.4s       | Solana Client     | 2020        |
| **Sui**      | DPoS + Mysticeti      | ~100,000 | 0.39s      | Sui Client        | 2023        |
| **Aptos**    | AptosBFT              | ~160,000 | <1s        | Aptos Client      | 2022        |

---

## Part 2: Distributed Ledgers vs Blockchains

### 2.1 Distributed Ledger Technology (DLT)

A decentralized, replicated database that uses consensus for updates.

**Characteristics:**

* Decentralized data replication
* Cryptographically secured
* Consensus-based updates
* Can be permissioned or permissionless
* Not strictly block-based

---

### 2.2 Blockchain

A specific type of distributed ledger that stores data in cryptographically linked blocks.

**Characteristics:**

* Sequential block structure
* Immutable once confirmed
* Public or private networks
* Hash-linked chain
* All blockchains are DLTs

---

### 2.3 Key Differences

| Aspect           | Distributed Ledger           | Blockchain                |
| ---------------- | ---------------------------- | ------------------------- |
| **Structure**    | Flexible (DAG, tree, etc.)   | Linear chain of blocks    |
| **Architecture** | Can vary                     | Strict block-based design |
| **Examples**     | Hyperledger, IOTA, Hashgraph | Bitcoin, Ethereum, Solana |
| **Ordering**     | May not be strict            | Always chronological      |
| **Permissions**  | Often permissioned           | Often permissionless      |

**Example:** IOTA’s Tangle is a DAG-based ledger → a DLT, not a blockchain.

---

## Part 3: NFTs and Fungible Tokens

### 3.1 Fungible Tokens

Tokens that are identical, divisible, and interchangeable.

**Standards:** ERC-20 (Ethereum), SPL (Solana)
**Uses:** Currency, utility, governance, rewards

**Examples:**

* **USDT, USDC** — Stablecoins
* **UNI** — Governance
* **LINK** — Oracle token
* **MATIC**, **SOL** — Network tokens

---

### 3.2 Non-Fungible Tokens (NFTs)

Unique digital assets with distinct metadata.

**Standards:** ERC-721, ERC-1155, Metaplex (Solana)

**Examples:**

* Bored Ape Yacht Club (BAYC)
* CryptoKitties
* ENS Domains
* Decentraland Land
* Sorare Fantasy Cards
* Gods Unchained Cards

---

### 3.3 Token Comparison Table

| Feature                | Fungible Tokens (ERC-20) | NFTs (ERC-721)        |
| ---------------------- | ------------------------ | --------------------- |
| **Interchangeability** | Yes                      | No                    |
| **Divisibility**       | Yes                      | Generally No          |
| **Value**              | Uniform                  | Varies                |
| **Metadata**           | Minimal                  | Rich                  |
| **Use Cases**          | Currency, governance     | Art, gaming, identity |
| **Ownership Proof**    | Balance                  | Token ID              |
| **Standards**          | ERC-20                   | ERC-721 / ERC-1155    |

---

## 📚 References

* Visa. (2024). What are Consensus Mechanisms? Visa USA.
* Ethereum.org. Consensus Mechanisms.
* Ethereum.org. Proof-of-Stake (PoS).
* Yakovenko, A. (2018). Solana Whitepaper.
* Helius Blog (2025). Consensus on Solana.
* Sui Documentation (2024). Mysticeti Consensus.
* Aptos Documentation (2024). AptosBFT Overview.
* Messari (2024). State of Aptos Q2.
* Ethereum.org. ERC-20 Token Standard.
* Ethereum.org. NFT Overview.
* World Economic Forum (2023). Guide to NFTs.
* GAO (2022). Science & Tech Spotlight: NFTs.
* Chainlink Education Hub (2024). NFTs Explained.
* AWS (2024). What is an NFT?
* Wikipedia (2024). Non-Fungible Token.

---
**Submission Summary**
>
> **Week 1 Day 2 Deliverables:** Research notes, comparison tables, NFT vs Token analysis, Twitter thread, and 14 cited sources.

---


### ✍️ Research by: **Favour Abidoye**

📘 **MGS Web3 Cohort 3 – Gamma Guild**

