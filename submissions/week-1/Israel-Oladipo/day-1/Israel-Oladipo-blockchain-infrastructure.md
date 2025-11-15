# Week 1 Day 2: Blockchain Infrastructure Research
Student Name: Israel Oladipo
Date: Friday, November 7th, 2025
Tweet Link:


## Part 1: Blockchain Infrastructure Research

### Blockchain 1: ETHEREUM

#### Node Types

1. Full Nodes:  A full node performs the function of verifying and validating every transaction occurring within the blockchain network.

Hardware requirements to run a full node on the Ethereum blockchain

- A fast CPU with 4+ cores

- 16 GB+ of RAM

- A fast SSD drive with at least 1 TB of space (storage capacity will grow over time)

- 25 MBit/s bandwidth

Software requirements to run a full node on the Ethereum blockchain

Clients software such as:
- Geth (Go-Ethereum)
- Nethermind
- Besu

2. Archive Nodes: Archive nodes preserve the complete blockchain history, commencing from the genesis block.

Hardware requirements to run an archive node on the Ethereum blockchain.

- A fast CPU with 4+ cores

- 16 GB+ of RAM

- Storage will vary depending on the client software (as of March 2023, archive mode on Geth takes ~13.5 TB, and Erigon takes up ~2 TB (3 TB is recommended)).

- 25 MBit/s bandwidth

Software requirements to run an archive node on the Ethereum blockchain

Clients software such as:

- Geth (Go-Ethereum)
- Erigon
- Besu

3. Light Nodes: A light node retains only a small portion or limited data about the blockchain (such as the block header) and not the complete current blockchain state.


Hardware requirements to run light node on the Ethereum blockchain

-  Standard SSD with storage of 400 MB – 2 GB (since it doesn't store the full blockchain)

- 1-2 GB of RAM

- CPU with 1-2 core

- 10 Mbps bandwidth

Software requirements to run light node on the Ethereum blockchain
 
Clients software such as:

- Geth (Go-Ethereum)
- Nethermind


#### Client Implementations

Clients softwares on the Ethereum blockchain.

1. Geth (Go-Ethereum): It is built with Golang programming language

2. Nethermind: It is built with C# .NET programming language

3. Besu: It is built with Java programming language

GETH VS NETHERMIND

- Geth is known for its robustness and extensive documentation.
- It is written in Golang programming language

- Nethermind is known for its modularity and flexibility, making it easier for developers to customize and extend its functionalities.
- It is written in C# .NET programming language

Geth is the most popular Ethereum client because:  
- It's officially supported.  
- Easy to set up.  
- Well-documented.  
- Large support base from the community.


#### Consensus Mechanism

Ethereum uses a POS (Proof-of-stake) consensus mechanism.

The POS consensus mechanism is a way to prove that validators have put something of value into the network that can be destroyed if they act dishonestly.

 In Ethereum's proof-of-stake, validators explicitly stake capital in the form of ETH into a smart contract on Ethereum.

ADVANTAGES
- Proof-of-stake offers greater crypto-economic security than proof-of-work

- Less issuance of new ETH is required to incentivize network participants

DISADVANTAGES
- Proof-of-stake is younger and less battle-tested compared to proof-of-work

- Users need to run three pieces of software to participate in Ethereum's proof-of-stake.


#### Block Validators

Validators are responsible for proposing and approving new blocks on the Ethereum blockchain

To become a validator in the Ethereum blockchain, one must make a deposit of 32 ETH into the deposit contract and run three separate pieces of software: an execution client, a consensus client, and a validator client.

Rewards come in form of newly insured ETH and a share of transaction fees (tips)

The penalty for malicious behavior is slashing (losing a portion or all of your 32 ETH staked)

#### Performance Metrics

Average block time = 12.09s

Time until transaction finality = 12m 48s

Maximum transaction per second = 62.34 tx/s

#### Sources

-https://www.lcx.com/ethereum-nodes-and-clients-explained/ 

-https://www.quicknode.com/guides/infrastructure/node-setup/ethereum-full-node-vs-archive-node 

-https://getblock.io/blog/ethereum-clients-comparison-best-ethereum-client-2023/ 

-https://ethereum.org/developers/docs/consensus-mechanisms/pos/ 

-https://chainspect.app/chain/ethereum?range-cm=month 


### Blockchain 2: SOLANA

#### Node Types

1. Validator Nodes: Validator nodes (also known as Consensus Nodes) within Solana’s Proof-of-Stake (PoS) consensus model are the entities responsible for confirming if blocks are valid, and ultimately finalizing the transactions by voting on blocks produced by a leader node, or by being the leader. 

2. RPC (Remote Procedure Call) Nodes: A Solana RPC (Remote Procedure Call) Node is a non-voting validator node, which performs all validator node functions except voting on the validity of blocks. 

Hardware requirements to run validator nodes on Solana blockchain.

- Memory of 128GB or more
- CPU of 12 cores/24 threads
- Storage: Ledger 1TB or larger. High TBW (Total Bytes Written) suggested 

Software requirements to run validator nodes on Solana blockchain

Clients softwares such as:
- Agave
- Firedancer

Hardware requirements to run solana RPC nodes

- Memory of 258GB or more
- CPU of 16 cores/32 threads

Software requirements to RPC nodes on Solana blockchain

Clients softwares such as:
- Agave
- Firedancer

#### Client Implementations

1. Agave: Agave is the continuation of the original Solana Labs validator client, now being developed by Anza. It's written in Rust and forms the foundation of Solana's validator ecosystem.

2. Firedancer: Firedancer is a high-performance validator client developed by Jump Crypto. Written in C/C++, it aims to dramatically increase Solana's transaction processing capabilities. 

3. Mithril: Mithril is a Solana full node client written in Golang, designed to serve as a "verifying full node" for the Solana blockchain. It aims to provide lower hardware requirements compared to traditional Solana validators and RPC nodes, making it more accessible for users to run a full node.

4. Sig: Sig is a Solana validator client written in the Zig programming language. It focuses on optimising RPC processes to boost validator performance.

5. Solana labs validator client: Built with Rust and highly optimized for solana high throughput


Solana labs Validator Client is the most popular client software on the blockchain because:

- of its first mover advantage
- its reliability and wide adoption in the solana ecosystem 

#### Consensus Mechanism

Solana uses a Proof of Stake (PoS) + Proof of History (PoH) consensus mechanism

The Solana consensus algorithm is a Proof-of-Stake (PoS) blockchain where a designated leader is chosen for each slot to create a new block. This leader sequence is randomly determined in advance before the start of an epoch (a fixed period of slots). Blocks consist of the proof of history (PoH) chain, a sequence of cryptographic hashes, where every hash is computed based on the previous hash and transaction data. This serves as proof of passed time until enough hashes are computed so the block is finished and the next leader builds on top of it. 

ADVANTAGES

1. High throughput (TPS)
2. Low latency and fast finality
3. Energy efficient

DISADVANTAGES

1. High hardware requirements
2. Centralization risk
3. Complex Consesus

#### Block Validators

Validators are responsible for proposing and approving new blocks


Validators receive incentives in form of inflationary SOL issuance, transaction fees and priority fees (tips)

Validators can lose delegations from users and become excluded from leader schedule due to malicious behaviors

#### Performance Metrics

Average block time = 0.4s

Time until transaction finality = 12.8s

Maximum transactions per second (TPS) = 5289 tx/s


#### Sources

-https://www.alchemy.com/overviews/solana-nodes
 
-https://www.kiln.fi/post/introduction-to-solana-clients
 
-https://neodyme.io/en/blog/solana_consensus/#introduction 

-https://chainspect.app/chain/solana 

### Blockchain 3: BITCOIN

#### Node Types


1. Full nodes: nodes that run a compatible version of the Bitcoin client software and store a full copy of the Bitcoin blockchain history. A full node handles all protocol aspects and can independently verify the entire blockchain and any transaction. 

Hardware requirements to run a full node of Bitcoin blockchain

Software requirements to run a full node on Bitcoin blockchain

Client software such as Bitcoin Core
2. Pruned nodes: nodes that hold only a truncated version of the blockchain in order to save storage space.

Hardware requirements to run pruned nodes on Bitcoin blockchain


Software requirements to run pruned nodes on Bitcoin blockchain
Client software such as Bitcoin Core 
3. Lightweight or SPV (Simple Payment Verification) nodes: nodes that do not have a copy of the blockchain but instead rely on some other node to serve them data about their transactions via a protocol called “Simple Payment Verification.” This may be problematic because the SPV node has to trust the node that delivers the data. 

Hardware requirements to run a SPV nodes on Bitcoin blockchain

Software requirements to run SPV nodes on Bitcoin blockchain
Client software such as Bitcoin core and btcd

4. Mining nodes: nodes that participate in transaction ordering and block creation in conjunction with running specialized mining hardware called ASICs (Application Specific Integrated Circuits). 

Hardware requirements to run a mining nodes on Bitcoin blockchain


Software requirements to run mining nodes on Bitcoin blockchain
Client software such as Bitcoin core
#### Client Implementations

Bitcoin Core: Bitcoin Core is free and open-source software that serves as a bitcoin node (the set of which form the Bitcoin network) and provides a bitcoin wallet which fully verifies payments. It was built usimg C++ programming language

BTCD: btcd is an alternative full node bitcoin implementation written in Go (golang).

One key difference between btcd and Bitcoin Core is that btcd does NOT include wallet functionality and this was a very intentional design decision.

Bitcoin Core is the most popular because

1. of its security and reliability
2. It's widely supported by nearly all Bitcoin blockchain infrastructure  

#### Consensus Mechanism

Bitcoin uses a Proof of Work (PoW) consensus mechanism

How It Works:

1. Miners compete to solve a complex mathematical puzzle (hashing a block header).
2. The first miner to solve it proposes a new block of transactions.
3. The network validates the block, and if valid, adds it to the blockchain.
4. That miner receives a block reward + transaction fees.

ADVANTAGES
1. It is extremely secure due to high cost of attacking the network
2. It promotes decentralization because anyone with hardware can mine, thereby promoting openness.

DISADVANTAGES
1. It is energy intensive and requires significant electricity leading to environmental concerns
2. High cost of hardwares to run nodes

#### Block Validators

Miners propose and approve (other nodes can also approve) new blocks

Requirements to become a miner

- Mining hardware (typically ASICs)
- Bitcoin client software (Bitcoin Core)
- Mining software (CG Miner or BFGMiner)

Rewards/Incentives

- Block subsidy (newly minted bitcoins)
- Transaction fees

Penalties for malicious behaviour

- Deprivation of mining rewards


#### Performance Metrics

Average block time = 5m 7s

Time until transaction finality = 1hr

Maximum transactions per second = 13.2 tx/s


-https://blog.blockstream.com/education/nodes/what-are-the-types-of-bitcoin-nodes/ 

-https://github.com/btcsuite/btcd/blob/master/README.md   

-https://chainspect.app/chain/bitcoin 

### Blockchain 4: BASE

#### Node Types


1. Full Node (Full Execution Node)

Function/Role:  
- Maintains/persists the current blockchain state and recent history needed to validate new blocks and execute transactions.  

Hardware requirements to run full nodes on Base blockchain:  
- CPU: 8–16 cores  
- RAM: 16–32 GB  
- Storage: 2 TB+ NVMe SSD  
- Network: High-speed, stable connection (ideally 1 Gbps or more)

Software requirements to run full nodes on Base blockchain:  
- Base node client software (Geth, Reth, Nethermind)  
- Docker + Docker Compose (for running containerized nodes)    
- Git (to clone Base node repo)

2. RPC/API Nodes  
Function/Role:  
- Focuses on high availability, low-latency access to chain data.  
- Serves dApps, wallets, explorers, bots, and other services.  

Hardware requirements to run RPC nodes on Base blockchain:  
- CPU: 8–16 cores  
- RAM: 32 GB (or more if serving many requests)  
- Storage: 2–4 TB SSD- High-bandwidth network (for fast API response)  

Software requirements to run RPC nodes on Base blockchain:  
- Base full or archive node client (Geth, Reth, Nethermind)  
- RPC interface enabled (configured in client’s settings)  
- Docker/Docker Compose  

3. Archive Node
Function/Role:  
- Stores all historical states of the blockchain, useful for explorers, indexers, analytics, and historical state queries.  

Hardware requirements to run an archive node on Base blockchain:  
- CPU: 16+ cores  
- RAM: 64 GB+ (for high performance)  
- Storage: 6–8 TB NVMe SSD (and growing)  

Software requirements to run an archive node on Base blockchain:  
- Archive capable client (preferably Reth, it is more efficient than Geth for archive mode)  
- Docker + Docker Compose   
- Sufficient storage configuration to retain full historical state

#### Client Implementations

1. Geth (Go Ethereum): Built using the Golang programming language. It is the most widely used Ethereum client and offers strong stability and community support. Ideal for running full nodes, though not optimized for archive node performance.

2. Reth: Built using Rust. It is extremely fast and designed primarily for high-performance and archive node use cases. It’s a newer client focused on modularity and speed.

3. Nethermind: Built using C#. Known for its enterprise-grade features, high performance, and support for multiple interfaces like JSON-RPC, GraphQL, and WebSockets. Ideal for institutional and analytics-heavy environments.

Geth (Go Ethereum) is the most popular and most used because of

- its early adoption
- Strong community support
- its stability and reliability

#### Consensus Mechanism

Base blockchain leverages Proof of Stake (PoS) consensus mechanism of Ethereum blockchain via optimistic rollups

How it Works  

1. Transaction execution off‑chain: On Base, user transactions are collected and executed on the L2 environment.  
2. Batching & commitment: These results are batched and published periodically to Ethereum mainnet (L1) as a commitment, including cryptographic proofs. [1]   
3. Challenge/fraud window (optimistic roll‑up): Because it’s optimistic, there is a period during which submitted batches can be challenged for fraud or invalid state transitions.   
4. Finality via L1: Once the L1 transaction confirming the roll‑up batch is finalized, the L2 state becomes final.

ADVANTAGES 
- Scalability because transactions are processed off-chain and then committed in batches
- Lower cost and faster UX

DISADVANTAGES
- Data dependency on L1
- Optimistic roll-up lag because of fraud window

#### Block Validators

Sequencers on base network propose new blocks while Ethereum validators approve new blocks

Requirements to become a validator
- High performance hardwares to L1 (Ethereum) for committing batches
- Approval from authority inorder to run sequencer

Rewards/Incentives
- Transaction fees

Penalties for malicious behavior
- Withdrawal from being a sequencer
- Slashing of bonded assets

#### Performance Metrics

Average block time = 2s

Time until transaction finality = 13m 13s

Maximum transactions per second = 1267 tx/s


-https://getblock.io/blog/how-to-run-a-base-node-requirements/ 
-https://chainspect.app/chain/base 

### Comparison Table

| Blockchain | Consensus | Node Types | Main Client | Block Time | Validator Type |
|------------|-----------|------------|-------------|------------|----------------|
| Ethereum  | Proof of Stake    |  Full Nodes, Archive Nodes, Light Nodes   |     Geth (Go Ethereum)   |   12.09 seconds     | Proof of Stake Validator |

| Solana      | Proof of Stake (PoS) + Proof of History (PoH) | Validator Node, RPC Node   |   Solana  Labs Validator Clients  | 0.4 seconds        |  PoS Validator   |  
             
| Bitcoin     | Proof of Work (PoW)     |  Full Node, Pruned Node, SPV Node    |   Bitcoin Core      |   5 min 7 sec         |  PoW Miners    |

| Base        |  PoS + Optimistic roll-ups    |   RPC Node, Full Node, Archive Node   |   Geth (Go Ethereum)     |   2 seconds     |    Sequencers and Proof of Stake Validators    |


### Key Takeaways


1. Each Serves a Unique Purpose

They’re built in ways that enable them to perform their core functions effectively.  
- Solana is optimized for high-speed transactions.  
- Ethereum excels at smart contract deployment and dApp development.  
- Bitcoin serves as a store of value, focusing on decentralization over scalability.  

2. Different Consensus Mechanisms with Trade-offs

No blockchain has a perfect consensus model.  
- Each mechanism (PoW, PoS, PoH, Rollups) has its own pros and cons in terms of speed, energy usage, and security.  
- Choosing a mechanism is about balancing trade-offs, not finding a one-size-fits-all solution.

3. Scalability Often Comes at the Cost of Decentralization

- Solana offers high throughput but at the cost of requiring high-performance hardware, limiting validator diversity.  
- Bitcoin is extremely decentralized but trades off speed and throughput.  
- Ethereum and Base use rollups to try to maintain a balance between scalability and decentralization.

## Part 2: Distributed Ledger Technology vs Blockchain

### Introduction

Distributed Ledger Technology (DLT) represents a broad category of decentralized database systems, while blockchain is one specific type of DLT. This section explores the distinctions between them, how blockchain evolved from DLT, and when each might be more suitable.

### What is Distributed Ledger Technology (DLT)?

DLT is a decentralized database managed by multiple participants across different nodes. It ensures consensus without a central authority. Key features include:
- Decentralization  
- Cryptographic security  
- Immutable records  
- Consensus protocols  

DLT doesn't require data to be stored in blocks or chains, making it more flexible in structure and application.

### What Makes Blockchain Special?

Blockchain is a structured form of DLT where data is:
- Grouped in blocks  
- Each block is cryptographically linked to the previous one  
- Secured through consensus mechanisms (like PoW or PoS)  
- Immutable and transparent  

This chain-like structure ensures high integrity and traceability.

### Key Differences Between DLT and Blockchain

| Feature                    | DLT (General)         | Blockchain |
|----------------------------------|---------------------------------|---------------------|

| Data structure         | Flexible                  | Linear chain of blocks |
| Block requirement  | Not required          | Required |
| Immutability            | Varies                    | Strong immutability |
| Use of tokens          | Optional                | Often used |
| Popularity                | Less common      | Widely adopted |
| Speed & scalability | Potentially faster | Often slower (depending on consensus) |

### Non-Blockchain Distributed Ledgers

#### DLT Example 1: Hedera Hashgraph

- What it is: A distributed ledger using a gossip protocol and virtual voting.  

- How it works: Nodes share information randomly (gossip) and reach consensus through a unique DAG (Directed Acyclic Graph) model.  
- Key differences from blockchain: No blocks or mining. Much faster than blockchain.  
- Use cases: Supply chain, micropayments, identity
- Advantages over blockchain: High throughput, energy-efficient, fair ordering.

#### DLT Example 2: IOTA (Tangle)

- What it is: A DLT designed for the Internet of Things (IoT).  
- How it works: Uses a DAG structure called the Tangle. Each transaction validates two previous ones.  
- Key differences: No blocks, no miners, feeless transactions.  
- Use cases: IoT data sharing, device-to-device payments.
- Advantages: Scalability, zero fees, lightweight.

#### DLT Example 3: Corda

- What it is: A DLT platform by R3 for financial institutions.  
- How it works: Transactions are private between parties and use a notary system for consensus.  
- Key differences: No global ledger. Not all data is shared with all participants.  
- Use cases: Banking, legal contracts, insurance.  
- Advantages: Privacy, regulatory compliance, modular.

### Comparison Table: Blockchain vs Non-Blockchain DLT

| Feature               | Blockchain        | IOTA (Tangle)         |
|-------------------------------|---------------------------|------------------------|

| Data Structure   | Block + chain     | DAG (Tangle)  |        

| Consensus Mechanism | PoW / PoS  | Transaction approval   |

| Scalability          | Moderate          | High       |

| Energy Efficiency    | Lower (PoW)      | Very high  |    
       
| Use Cases   | Finance, DeFi, NFTs | IoT, microtransactions  |


### Deep Analysis and Conclusions

Blockchain offers high security and traceability, making it ideal for applications needing transparency, like DeFi and NFTs. However, non-blockchain DLTs like IOTA or Hashgraph are better suited for high-throughput, low-energy use cases like IoT or enterprise applications.

Use blockchain when you need:
- Public transparency  
- Strong immutability  
- Token-based systems  

Use non-blockchain DLT when you need:
- Scalability  
- Speed  
- Private, permissioned environments  

### All Sources and References

1. https://hedera.com
2. https://www.iota.org
3. https://www.r3.com

## Part 3: NFTs and Fungible Tokens - Digital Transformation

### Understanding Fungible Tokens

Fungible tokens are interchangeable digital assets with equal value, just like money.  
- Examples: ETH, USDC, AAVE 

Key Features:  
- Identical in value  
- Divisible  
- Used for payments, governance, DeFi  

### Understanding NFTs
[Your detailed explanation]
Non-Fungible Tokens (NFTs) are unique, indivisible digital assets that prove ownership of specific items.  
- Examples: Art, domain names, virtual land, tickets  

Key Features:  
- Unique 
- Not interchangeable  
- Typically indivisible  
- Blockchain-verified ownership  

### How NFTs and Tokens Conquer the Physical World

Digital Ownership Revolution: True ownership without intermediaries  
- Tokenization of Physical Assets: Real estate, fashion, wine, etc.- 
- Breaking Physical Limits: Global access to previously local assets  
- New Economic Models: Royalties, fractional ownership, DAO-driven assets  
- Breaking Physical Limits: Global access to previously local assets  
- Interoperability: Assets used across platforms (e.g., games, metaverse)

### Real-World Examples and Case Studies

#### Example 1: RealT

- What it is: Real estate tokenization platform  
- How it works: Users buy fractional ownership via tokens  
- Physical world connection: Real properties in the US  
- Impact: Democratizes real estate investment  
- Token type: ERC-20  
- Blockchain: Ethereum  


#### Example 2: Nike x RTFKT

- What it is: Digital sneakers backed by physical shoes  
- How it works: NFTs represent exclusive shoes  
- Physical world connection: Redeemable sneakers  
- Impact: Merges fashion and identity  
- Token type: ERC-721 NFT  
- Blockchain: Ethereum  

#### Example 3: Wine Vault (WiV)

- What it is: Fine wine tokenization  
- How it works: NFTs represent insured bottles in storage  
- Physical world connection: Actual wine stored securely  
- Impact: Liquidity for rare assets  
- Token type: NFT  
- Blockchain: Ethereum  


#### Example 4: Mattereum 

- What it is: Legal-backed NFT asset registry  
- How it works: Links NFTs to legal ownership contracts  
- Physical link: Real estate, art, instruments  
- Impact: Trustable tokenization
- Token type: NFT + legal contract  
- Blockchain: Ethereum  

#### Example 5: Boson Protocol 

- What it is: Web3 e-commerce platform  
- How it works: NFTs act as redeemable vouchers  
- Physical world connection: Items from real-world stores  
- Impact: Decentralized shopping  
- Token type: NFT voucher  
- Blockchain: Polygon  

### Comparison Table: Physical vs Digital Ownership

| Feature                | Physical Ownership       | Digital Ownership (NFTs/Tokens)     |
|------------------------|--------------------------|--------------------------------------|
| Ownership Verification | Paper/manual records     | Blockchain, immutable proof          |

| Transfer Speed         | Days/weeks               | Minutes or seconds                   |

| Transfer Cost          | High (middlemen/legal)   | Low (gas fees or zero)               |

| Storage                | Physical locations       | Digital wallets                      |

| Divisibility           | Hard/Impossible          | Easy (fungible tokens, fractional NFTs) |

| Global Accessibility   | Limited by geography     | 24/7 borderless access               |

| Fraud Prevention       | Risk of counterfeiting   | Tamper-proof and verifiable          |

| Intermediaries         | Required (agents, brokers)| Not required                         |

| Programmable Features  | None                     | Royalties, access control, etc.      |


### Deep Analysis: The Future of Ownership

NFTs and tokens are redefining what it means to own something. They eliminate the need for trust in third parties and enable global, verifiable, programmable ownership. As real-world assets become tokenized, we’re entering an era where ownership becomes fluid, digital-first, and inclusive.

chore: submit week 1 day 1 blockchain assignment
