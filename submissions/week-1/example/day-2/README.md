# Day 2 Assignment

Place your Day 2 assignment file here.

File name format: your-name-blockchain-intro.md

Example: john-doe-blockchain-intro.md

Deadline: Submit by the deadline specified by your tutor

# Week 1 Day 2: Blockchain Infrastructure Research
**Student Name:** [Idris Babatunde]  
**Date:** [8 November 2025]  
**Tweet Link:** [https://x.com/brothermanidris/status/1988160668051320908]

---

## Part 1: Blockchain Infrastructure Research

### Blockchain 1: [Bitcoin]

#### Node Types
[Full node; pruned node; lightweight (SPV) node]

#### Client Implementations
[Bitcoin core; Libbitcoin; Bitcoin Knots; Bcoin]

#### Consensus Mechanism
[Proof of Work]

#### Block Validators
[Your findings]

#### Performance Metrics
[Active users; total transaction; Market Value to Realized Value (MVRV); Network Value to Transaction (NVT) Ratio]

#### Sources
- [https://www.osl.com/hk-en/academy/article/what-is-a-bitcoin-node-a-beginners-guide-on-blockchain-nodes]
- [https://river.com/learn/terms/b/bitcoin-implementation/]
[https://www.investopedia.com/terms/p/proof-work.asp#:~:text=Proof%20of%20work%20(PoW)%20is%20a%20consensus%20mechanism%20used%20by,leading%20to%20high%20energy%20consumption.]
[https://omenics.com/blog/bitcoin-blockchain-metrics-indicators/]

---

### Blockchain 2: [Ethereum]

#### Node Types
[Full node; archive node; light node]

#### Client Implementations
[Geth; Nethermind; Erigon; Hyperledger Besu]


#### Consensus Mechanism
[Proof-of-Stake]

#### Performance Metrics 
[Attestation Success Rate; Attestation Inclusion Delay; Participation Rate; Uptime]

#### Sources
[https://www.alchemy.com/overviews/full-vs-light-vs-archive-nodes]
[https://www.hord.fi/blog/a-guide-to-validator-performance-metrics-in-ethereum]

---

### Blockchain 3: [Solana]

#### Node Types
[Validator; Leaders, RPC nodes

]

#### Client Implementation 
[Agave; Firedancer; Frankendancer; Jito; Mithril; Sig; Tinydancer]

#### Consensus Mechanism 
[Proof of History; Proof of Stake]

#### Performance Metrics 
[Circulating Markup; Average Daily transaction; Average Daily Active Address]

#### Sources

[https://www.alchemy.com/overviews/solana-nodes]
[https://www.withtap.com/fr/blog/run-a-solana-node#:~:text=Validator%20vs%20RPC%20Nodes,data%20access%20for%20their%20apps]
[https://www.kiln.fi/post/introduction-to-solana-clients]
[https://solana.messari.io/performance]
---

### Blockchain 4: [Avalanche]

---

#### Node Types 
[Full Node; Validator Node, RPC Node]

#### Client Implementation 
[P-Chain, X-Chain, C-Chain]

#### Consensus Mechanism 
[Proof of Stake (Snowman Consensus Protocol)]

#### Sources
[https://getblock.medium.com/avalanche-node-peculiarities-and-benefits-6a4de4cbc814]
[https://build.avax.network/docs/tooling/avalanche-sdk/client/clients]
[https://www.debutinfotech.com/blog/avalanche-blockchain-guide]

### Comparison Table

| Blockchain | Consensus | Node Types | Main Client | Block Time | Validator Type |
|------------|-----------|------------|-------------|------------|----------------|
| [Bitcoin] | Proof of Work | Full node; pruned node; lightweight (SPV) node | Bitcoin core; Electrum and Wasabi wallet |            |                |
| [Euthereum] | Proof-of-Stake | Full node; archive node; light node | Geth; Nethermind; Erigon; Hyperledger Besu |            |                |
| [Solana] | Proof of History; Proof of Stake | Validator nodes; RPC nodes | Agave; Firedancer; Frankendancer; Jito; Mithril; Sig; Tinydancer |            |                |
| [Avalanche] | Nominated Proof-of-Stake | Relay-chain validators; Collators for parachains | P-Chain, X-Chain, C-Chain |            |                |

---

### Key Takeaways
[1. Consensus evolution reveals a trade-off between security, speed and energy efficiency. For example, Bitcoin’s PoW is most secure, but consumes large energy. Eutherum’s PoS saves energy. The PoS of both Solana and Avalanche boasts of high speed and scalability. In all, efficiency is becoming top priority for blockchain]

[2. Node diversity reflects each network’s purpose: Bitcoin for security-first transactions, Ethereum for programmability, and Solana/Avalanche for speed and scalability.]

[3. Client diversity determines developer flexibility. More client implementations equals stronger resilience and decentralization, and Ethereum currently leads in this aspect.]

[4. Each blockchain’s performance metrics mirror its priority and core function. Bitcoin focuses on store value; with this, it retains its position and Digital Gold. Ethereum leads with decentralized computing, and its metrics (attestation success, participation rate) reflect network reliability for validators and smart contract operations. Solana’s capacity for large network activities makes it appealing to consumer-facing apps and games.  Avalanche favors enterprise and DeFi apps, given its emphasis on time to finality]  

---

## Part 2: Distributed Ledger Technology vs Blockchain

### Introduction
[Distributed ledger technology (DLT) refers to any system that records and shares data across multiple computers without a central authority. Each participant in the network holds a copy of the ledger, and all updates are synchronized across them.
Blockchain is a type of distributed ledger; it organizes data into blocks that are cryptographically linked together in a chain.
]

### What is Distributed Ledger Technology (DLT)?
[DLT is a digital system for recording transactions or data across multiple sites simultaneously. The key idea in Distributed Ledger technology is distributed trust.  No single organization owns or controls the ledger.
Each participant has an identical copy of the ledger, and changes are verified through a consensus mechanism agreed upon by the network.
DLT can use different data structures. It can be permissioned (private) or permissionless (public).]

### What Makes Blockchain Special?
[Blockchain is special because it uses chronologically linked blocks to form an immutable chain. It relies on cryptography to secure transactions. Each block references the one before it, this makes it transparent. 
]

### Key Differences Between DLT and Blockchain
[In Distributed Ledger Technology (DLT), data is recorded and synchronized across multiple nodes (computers) without the need for a central authority. Blockchain is a specific implementation within this category; structures data into cryptographically‐linked blocks which form a chain. 
The key architecture of DLT lies in its decentralised database model: nodes replicate and maintain ledger copies; consensus algorithms ensure uniformity; and peer-to-peer network topologies distribute data and responsibilities. Many DLT systems, however, do not use the linear, time-ordered “block→block” chaining mechanism that blockchain systems use. For instance, some DLT implementations adopt Directed Acyclic Graphs (DAGs) or other graph-based or agent-centric structures. This paves way for parallel confirmation of transactions and alternative consensus models. But blockchain’s key feature is the block-structure: each block contains a set of transactions, a timestamp and a cryptographic reference (hash) to the previous block. This arrangement is what makes immutability and chronological ordering possible. 
In terms of consensus mechanism, DLT systems allow a wider array of protocols: these may include virtual-voting (as seen in Hashgraph), gossip-protocols, or permissioned-network voting. The design may favour faster confirmation, lower energy consumption and flexible permissioning. On the other hand, blockchain systems typically employ Proof of Work (PoW) or Proof of Stake (PoS) (and variants) to guard against double-spending, Sybil attacks and to enforce a consistent ledger state across all nodes. The necessity of mining (in PoW) or staking (in PoS) imposes specific architectural constraints and energy/latency trade-offs. 
Another important technical difference concerns data structure and state synchronization. In many non-blockchain DLT systems, nodes may maintain only a subset of the ledger relevant to them, or validation may occur locally and asynchronously. This helps improve scalability by avoiding the need for each node to process every transaction. By contrast, in most blockchain networks, every full node typically retains the full chain, processes all transactions in the sequence of blocks, and thus endures greater redundancy and lower scaling potential. Because blockchain enforces strict immutability (once a block is accepted it cannot be changed without breaking the chain), there is a performance cost (latency, storage, verification) inherent in that model. DLT systems that relax the block‐structure may allow faster throughput or customisation of consistency models (e.g., eventual vs. strong consistency). 
Another area of difference lies in energy efficiency and scalability. Blockchain networks using PoW (e.g., early Bitcoin) consume vast amounts of computational power; even PoS systems carry inherent staking / validation overhead. DLT systems outside of this model (especially those not using mining or staking) can be far more energy-efficient and scale more easily in terms of transactions per second or network size. 
]

### Non-Blockchain Distributed Ledgers

#### DLT Example 1: [Directed Acylic Graph]

- **What it is:**
[IOTA is a DLT designed for the Internet of Things (IoT). It uses a structure called a Directed Acyclic Graph (DAG) instead of a blockchain.]

- **How it works:**
[Each transaction confirms two previous transactions before being validated without blocks and miners. As more transactions are made, the network becomes faster.]

- **Key differences from blockchain:**
No block, no miners or fee, and it is highly scalable  as transaction volume increase

- **Use cases:**
[IoT data exchange, microtransactions, smart cities, supply chain tracking]

- **Advantages over blockchain:**
[Greater scalability; Zero transaction fees; Better suited for small, frequent transactions.]

#### DLT Example 2: [Hashgraph]

- **What it is:**
[Hashgraph is a patented DLT developed by Hedera. It uses a “gossip about gossip” protocol to share data efficiently]

- **How it works:**
[Nodes gossip with each other about transactions and events. Consensus is reached through virtual voting without needing to record every vote on-chain.]

- **Key differences from blockchain:**
[Transactions are confirmed through virtual voting, not PoW or PoS.]

- **Use cases:**
Enterprise applications, payments, identity management, gaming, and NFTs

- **Advantages over blockchain:**
[Much faster and more energy-efficient]

#### DLT Example 3: [Holochain]

- **What it is:**
[An agent-centric distributed ledger. Each participant keeps their own chain of data instead of sharing one global ledger.]

- **How it works:**
[Each user validates and stores their own data. Shared data is only published to a distributed hash table (DHT) when necessary.]

- **Key differences from blockchain:**
[No single global ledger. Focuses on personal data ownership and peer-to-peer apps.]

- **Use cases:**
[Decentralized applications, social media, reputation systems, collaborative platforms]

- **Advantages over blockchain:**
Lightweight and energy-efficient. Gives users full data control

### Comparison Table: Blockchain vs Non-Blockchain DLT

| Feature | Blockchain | Non-Blockchain DLT Example |
|---------|------------|---------------------------|
| Data Structure | Chain of blocks linked cryptographically | DAG, gossip graph, or agent-centric structures |
| Consensus Mechanism | PoW, PoS, PoH, etc. | Virtual voting, local validation, or parallel confirmation |
| Scalability | Limited by block size and time | Very high due to parallel processing |
| Energy Efficiency | Varies (PoW means high consumption) | Very efficient |
| Use Cases | Cryptocurrencies, DeFi, NFTs | IoT, enterprise apps, decentralized identity, P2P networks

 |

---

### Deep Analysis and Conclusions
[To determine whether to use blockchain or another DLT, the problem environment must first be understood. Public blockchains excel in open, trustless ecosystems where participants do not know or trust one another, and the ledger’s transparency provides verifiable truth. For instance, Bitcoin and Ethereum rely on consensus mechanisms (Proof of Work and Proof of Stake, respectively) that allow anyone to join the network and validate transactions. Integrity is maintained through cryptographic proofs. This design ensures security and censorship resistance, but its downside lies in limited transaction throughput, energy intensity (especially in PoW systems), and higher transaction fees. Thus, public blockchains are best suited for use cases demanding global accessibility, verifiable ownership, token economies, and transparent governance, such as decentralized finance (DeFi), NFTs, and decentralized identity.
On the other hand, permissioned DLTs are better suited for controlled, enterprise, or consortium environments where participants are known and privacy or regulatory compliance is essential. Solutions like Hyperledger Fabric or Corda enable selected organizations to maintain nodes and share data securely, without exposing sensitive information publicly. These DLTs eliminate the need for cryptocurrency mining or staking, making them energy-efficient and scalable, while also providing flexible access controls and audit trails. Enterprises in supply chain management, healthcare, or interbank settlements often prefer permissioned DLTs because they combine distributed consensus with privacy and accountability. 
Another critical factor is performance and scalability. Traditional blockchains process transactions sequentially—one block after another—while many non-blockchain DLTs use parallel transaction validation. Directed Acyclic Graphs (DAGs), used in networks like IOTA’s Tangle and Hedera Hashgraph, remove the concept of blocks entirely, which allows multiple transactions to be confirmed simultaneously through “gossip” or virtual voting mechanisms. This architecture significantly increases throughput and reduces latency. As a result, DAG-based systems become suitable  for high-frequency or microtransaction environments such as IoT data exchange, machine-to-machine payments, and large-scale event logging . However, DAGs often trade off some degree of decentralization or ecosystem maturity, and their consensus models may be more complex or less battle-tested than blockchain’s.
Another area of distinction is governance and data control. Blockchain’s immutability and global consensus guarantee a single version of truth, but they can also limit flexibility. DLTs Holochain make agent-centric validation paramount. In this case, users maintain control over their own data and share only what’s necessary. Instead of storing a universal ledger, each node holds its own signed records and validates interactions locally. This structure enables data sovereignty  privacy, and is ideal for social, identity, or peer-to-peer platforms that do not need a global ledger. However, it may not suit financial or legal systems that require a universally consistent record of ownership.
The open and immutable nature of blockchain can be concerning when we consider regulations and governance. This is because it can conflict with laws that require data erasure or identifiable actors (e.g., GDPR, AML/KYC). Permissioned or hybrid DLTs mitigate this issue by giving organizations granular control over access, and data retention. Conversely, blockchain’s openness can give a leverage in regions or industries where censorship resistance and transparency are paramount. Such instances include public registries, cross-border payments, or decentralized content platforms. 
Ecosystem maturity is also worth considering. Major blockchains like Bitcoin and Euthereum have extensive developer communities, tooling, and interoperability layers. Because other newer DLTs may lack this, enterprises adopting them need to weigh performance benefits against the cost of integration and long-term sustainability. 
Realistically, and in conclusion, the technology should ideally be finding a balance between decentralization, performance, privacy, and compliance while being aware of project constraints.]

---

### All Sources and References
1. [https://coinmarketcap.com/currencies/holo/]
2. [https://www.hashgraph.com/]
3. [https://www.hashgraph.com/]
4. [https://blog.iota.org/dags-over-blockchains-iota20/]
5. [https://www.holochain.org/what-holochain/]
6. [https://arxiv.org/abs/2109.03667]
7. [https://techresearchonline.com/blog/distributed-ledger-technology-overview/]
8. [https://www.consensus.com/blog/blockchain-vs-dlt/]
9. [https://www.investopedia.com/terms/d/distributed-ledger-technology-dlt.asp?]
10. [https://www.theserverside.com/tip/Know-how-and-when-to-use-blockchain-vs-distributed-ledgers]

---

## Part 3: NFTs and Fungible Tokens - Digital Transformation

### Understanding Fungible Tokens
[Your detailed explanation]

### Understanding NFTs
[Your detailed explanation]

### How NFTs and Tokens Conquer the Physical World
[Your deep analysis on digital ownership revolution, transforming physical assets, new economic models, breaking physical limitations, and interoperability]

### Real-World Examples and Case Studies

#### Example 1: [CryptoPunks]

- **What it is:**
[One of the earliest and most iconic NFT collections (10,000 algorithmically generated pixel portraits) that helped spark the modern NFT market]

- **How it works:**
[Each Punk is a unique ERC-721 token on Ethereum with provenance recorded on-chain; token metadata defines traits and rarity. Ownership transfers and sale history are publicly visible.]

- **Physical world connection:**
[CryptoPunks are primarily digital collectibles, but institutional preservation efforts and museum exhibitions (and high-value sales at Christie’s) demonstrate crossover into the physical art world and cultural institutions.]

- **Impact:**
[Established cultural legitimacy for NFTs, created celebrity collectors, and showed how digital provenance can carry real monetary and cultural value.]

- **Token type:**
[NFT (ERC-721)]

- **Blockchain:**
[Euthereum]

#### Example 2: [Bored Ape Yacht Club (BAYC)]

- **What it is:**
[A 10,000-piece NFT collection that bundles social membership and IP rights to owners; includes real-world events and branded merchandise.]

- **How it works:**
[Ownership of a BAYC NFT (ERC-721) proves membership; owners authenticate with wallets to access gated drops, merch, and community events. Yuga Labs expanded IP ecosystems (merch, media)]

- **Physical world connection:**
[BAYC owners gain access to exclusive IRL events, merch drops, and potential media/exploitation of IP — combining digital ownership with physical experiences and revenue.]

- **Impact:**
[Demonstrated how NFTs can build community, real-world perks, and brand ecosystems—transforming tokens into membership passes and cultural capital.]

- **Token type:**
[NFT (ERC-721)]

- **Blockchain:**
[Ethereum]

#### Example 3: [NBA Top Shot (Dapper Labs / Flow)]

- **What it is:**
[Licensed digital collectibles (“Moments”) of NBA highlights sold as limited-edition NFTs]

- **How it works:**
[The NBA and Dapper Labs mint a controlled number of Moment NFTs on the Flow blockchain. Collectors buy packs, trade on marketplace; rarity and edition size drive value]

- **Physical world connection:**
[Top Shot brings mainstream sports collectors into digital ownership: while the assets are digital, they replicate the sports-memorabilia economy (rarity, licensed authenticity) and have spawned fan meetups and promotions]

- **Impact:**
[Showed how licensed IP + user-friendly onboarding can scale NFT adoption beyond crypto natives, validating tokenized collectibles for mainstream audiences.]

- **Token type:**
[NFT (Flow native standard)]

- **Blockchain:**
[Flow (Dapper Labs)]

#### Example 4: [RealT (Tokenized Real Estate)]

- **What it is:**
[ Platform that issues ERC-20 “RealTokens” representing fractional economic ownership in U.S. property, with legal structures to map tokens to equity.]

- **How it works:**
[Properties are held in series LLCs; corresponding ERC-20 tokens represent shares and distribute rental income via smart contracts to token holders, subject to on-chain/off-chain compliance]

- **Physical world connection:**
[RealTokens correspond to literal rental properties — token holders receive real cash flows and have exposure to real estate markets, while transfers are recorded on the blockchain for liquid secondary trading]

- **Impact:**
[Lowered barriers to property investment, created liquid markets for traditionally illiquid assets, and highlighted legal and compliance importance in tokenizing regulated assets]

- **Token type:**
[Fungible token (ERC-20 representing fractional ownership) / security token design with legal wrapper]

- **Blockchain:**
[Ethereum (or EVM compatible)]

#### Example 5: [TFKT / Nike Cryptokicks (digital + physical sneakers)]

- **What it is:**
[RTFKT (acquired by Nike) minted NFT sneaker tokens tied to limited-edition physical sneakers (Cryptokicks iRL), enabling digital collectors to redeem physical pairs or claim hybrid experiences]

- **How it works:**
[NFTs act as proofs of right to claim a physical item (redemption events/“forging”), and also as digital wearables usable in virtual spaces; minting, ownership transfers, and redemption processes are governed by NFTs on the relevant chain/platform]

- **Physical world connection:**
[NFT ownership granted rights to obtain a real pair of shoes, attend IRL events, or access post-drop physical delivery—directly tying a unique token to manufactured goods]

- **Impact:**
[Showed how brands can merge scarcity, community, and physical fulfilment, but also highlighted project risk and consumer protection issues (recent legal disputes and wind-down news underscore redemption/custody risks)]

- **Token type:**
[NFT (ERC-721/collection standard) with redemption right (hybrid)]

- **Blockchain:**
[Various (drops used Ethereum and other platforms), often bundled with off-chain logistics.]
---

### Comparison Table: Physical vs Digital Ownership

| Feature | Physical Ownership | Digital Ownership (NFTs/Tokens) |
|---------|-------------------|--------------------------------|
| Ownership Verification | Paper/title or centralized registry; requires manual checks| Cryptographic proof on public/private ledgers; instant verifiable history|
| Transfer Speed |Hours to weeks (legal processes, escrow) | Seconds to minutes (on-chain settlement; subject to finality).|
| Transfer Cost |Legal fees, intermediaries, registration costs | Network fees + possible platform/escrow fees (often lower, but variable).|
| Storage |Physical safekeeping, warehousing, title records | Digital wallet custody; metadata hosted off-chain sometimes requires IPFS or centralized storage.|
| Divisibility |Often indivisible (e.g., a house), requires legal fractional schemes |Highly divisible via fungible tokens (fractional ownership). |
| Global Accessibility |Cross-border transfer friction, legal constraints | Global transfers possible (subject to KYC/regulation) — near-instant cross-border. |
| Fraud Prevention | Dependent on centralized registries; forgery possible| Strong tamper resistance if on-chain + robust KYC/oracle processes. Off-chain data risk remains.|
| Intermediaries | Often necessary (banks, registries, agents)| Can be reduced or automated (smart contracts), though legal & custody intermediaries still commonly used. |
| Programmable Features |Hard to automate legally; often manual  | Smart contracts enable royalties, conditional transfers, compliance gates.|

---

### Deep Analysis: The Future of Ownership
[Tokenization and NFTs are a structural change in how claim and provenance are recorded and enforced. Looking forward, the future of ownership will be hybrid and layered: immutable on-chain registries (or permissioned ledgers) combined with legal instruments and custodial services that map tokens to enforceable real-world rights. This hybrid model solves two core issues: (1) the oracle problem — ensuring off-chain facts (did the shipping container actually arrive?) are reliably represented on-chain; and (2) legal enforceability — ensuring courts recognize on-chain transfers as transfers of legal title.
We should expect several broad trends. First, institutionalization: large financial institutions and asset managers are already experimenting with tokenized funds and securities (BlackRock’s tokenized fund via Securitize partnerships), indicating tokenization’s path from fringes to regulated markets. Second, regulatory maturation: as securities regulators clarify how tokenized assets map to existing rules, we will see compliant token offerings that combine smart contracts with KYC/AML tooling and revocation controls (Securitize’s DS Protocol). Third, vertical adoption in provenance-sensitive industries (diamonds, luxury goods, pharmaceuticals, food) will expand as stakeholders seek traceability to defend brand value and consumer trust (Everledger examples). 
However, the path is not without friction. Legal ambiguity (are NFTs securities?), custodial risks (platform shutdowns or project wind-downs), off-chain data integrity, and UX barriers remain meaningful obstacles. The RTFKT/Nike situation illustrates how brand projects that promise physical redemption or long-term product ecosystems can still create consumer exposure if off-chain fulfilment or corporate strategy changes. 
In the medium term, the most successful models will be those that marry blockchain’s verification power with robust legal wrappers and trusted custodial processes.  Token-enabled franchising of assets (fractional real estate portfolios), tokenized funds for institutional investors, digital identity combined with NFTs for membership economies, and increased interoperability standards (digital identity, token metadata standards) that make tokens portable across metaverses, marketplaces, and DeFi products… all of these should be expected. 
And lastly (most importantly too),  ownership will be more liquid and programmable, but its real-world reliability will depend on legal clarity, standards, and the fidelity of off-chain integration.]

---

**Twitter Thread:** [https://x.com/brothermanidris/status/1988160668051320908]
```

---