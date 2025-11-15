
1) 5 blockchains / DLTs (nodes, clients, consensus mechanism 
Bitcoin (Layer-1, permissionless)
Bitcoin is the first decentralized cryptocurrency. Bitcoin works through the collaboration of computers, each of which acts as a node in the peer-to-peer bitcoin network. Each node maintains an independent copy of a public distributed ledger of transactions, called a blockchain, without central oversight.
•	Node types / clients: Full nodes (Bitcoin Core client), SPV/light clients. Full nodes clients validate blocks and transactions and download the full UTXO/chain. 
•	Consensus mechanism: Proof-of-Work (PoW); Miners compete via hash-puzzle; longest valid chain = canonical. PoW provides Sybil resistance via costly computation.
•	Notes: It is highly decentralized. It has strong censorship resistance and its energy intensive due to PoW. 
Ethereum (Layer-1 smart-contract platform, permissionless)
Ethereum is a peer-to-peer network that maintains a database containing the storage values of all Ethereum accounts and processes state-altering transactions. Approximately every 12 seconds, a batch of new transactions, known as a "block", is processed by the network. Each block contains a cryptographic hash identifying the series of blocks that must precede it if the block is to be considered valid. This series of blocks is known as the blockchain. 
•	Node types / clients: Execution clients (e.g. Geth, Nethermind, Reth) + consensus clients (formerly Beacon nodes) + validator clients (for staking). After The Merge, consensus is PoS with separate execution + consensus client architecture. 
•	Consensus mechanism: Proof-of-Stake (PoS) since the Merge; validators are selected to propose/attest blocks (slot/epoch model). 
•	Notes: Supports EVM smart contracts, ERC-20/721 standards, massive dApp ecosystem. PoS reduces energy use vs PoW. It hosts over 8600 nodes.

Solana (Layer-1 high-throughput design, permissionless)
Solana is a proof-of-stake blockchain which uses a scalable platform for both exchanging value and also running decentralized applications within the network. These dApps are called programs. Solana's main focus is massive transaction throughput on its main, Layer 1, blockchain network, with the transaction speed commonly reaching 1000+ tps. 
•	Node types / clients: Validator and validator clients.  Validator clients are software where validators connect to the Solana chain (e.g Firedancer) , RPC/entry nodes for clients which acts as gateway for dApps. Validators produce/validate blocks.
•	Consensus & engineering: It uses a hybrid of proof-of-history (PoH) as a clocking/timestamp mechanism plus a practical Byzantine Fault Tolerant style leader schedule and vote propagation (optimized stack: Turbine for propagation, Gulf Stream for mempool forwarding, etc.). Solana’s stack emphasizes software tuned to hardware for high throughput and low latency.
•	Notes: Very high TPS in practice. It has experienced outages and centralization concerns around validator distribution.
Polkadot (Layer-0 / relay chain for parachains)
•	Node types / clients: Validator nodes on the Relay Chain, collators on parachains, full nodes for parachains RPC nodes, boot nodes. Clients built on Substrate framework. 
•	Consensus mechanism: Hybrid; BABE (Blind Assignment for Blockchain Extension) for block production (slot leaders), and GRANDPA for finality (BFT finality gadget). This separation allows fast block production and separate finality. 
•	Notes: Designed for interoperability (parachains), on-chain governance and shared security model. Nodes communicate with each other to reach consensus on the state of the network. Within Polkadot there are several types of nodes that have different configurations.
Hyperledger Fabric (permissioned enterprise DLT)
•	Node types / clients: Peers (endorsers/committing peers), ordering service nodes (orderers), clients (submit transactions). Network membership is permissioned (MSP).
•	Consensus mechanism: Pluggable ordering service can use Raft, Kafka (historically), or other deterministic algorithms; Fabric separates endorsement, ordering, and validation so forks are generally not possible (finality is deterministic). 
•	Notes: It’s not designed for public censor-resistance and it’s aimed at enterprise workflows with privacy and permissioning.

2) Distributed ledger vs Blockchain
•	DLT (general): Distributed Ledgers are any system where ledger copies are shared across nodes. They can be permission or permissionless. Not all DLTs use blocks or chain linking, and they are good for private enterprise use (e.g., Hyperledger). 
•	Blockchain (subset of DLT): It appends ordered blocks cryptographically linked; most public cryptocurrencies are blockchains (Bitcoin, Ethereum). Blockchain implies an append-only chain of blocks; some DLTs may use different data structures or ordering services. 
•	Practical difference: Blockchains emphasize immutable block chains and often decentralized consensus (PoW/PoS) while DLT is the broader category that includes blockchains and other replicated ledger designs optimized for permissioned environments. 

3) How NFTs and Fungible Tokens change ownership 
•	Fungible tokens (e.g., ERC-20): interchangeable units (1 USDC = 1 USDC). They change ownership by token transfer to addresses. Distributed ledger records balances. Standards (ERC-20) ensure interoperability.
•	Non-fungible tokens (NFTs, e.g., ERC-721/ERC-1155): are unique token IDs representing a unique asset (digital art, collectible, domain name). Ownership is recorded on chain while transfer changes ownership and can be atomic with marketplace logic (escrow, royalties). The token's metadata may be on-chain or off-chain (IPFS). Ownership means control of the token and any rights encoded/transferred by contract (but note IP rights are a separate legal layer). 
Real-world examples
1.	CryptoPunks (Ethereum / ERC-721 style history)
a.	Early NFT collection (10,000 punks). Cultural & speculative value; sales peaked 2021–2022. Recent shifts saw Yuga Labs transferring collection to non-profit Node Foundation (illustrates preservation & evolving custodianship). Ownership = token in wallet; marketplace controls liquidity. 

2.	Bored Ape Yacht Club (BAYC)
a.	10k unique apes on Ethereum; ownership granted membership perks (events, IP benefits). Shows NFTs as social identity + rights bundles (utility, access). Brands (Adidas, others) have partnered with BAYC for cross-media utility. 

3.	NBA Top Shot (Flow blockchain)
a.	Flow is architected for consumer-grade NFT experiences; Top Shot sells authenticated NBA highlight “moments” as NFTs (Cadence smart contracts). Ownership recorded on Flow; simpler UX and high throughput enabled mainstream adoption. Demonstrates that blockchain choice affects scalability & user experience for NFTs. 

4.	Axie Infinity (Axie NFTs + AXS/SLP fungible tokens)
a.	Game with NFTs representing in-game creatures; paired with fungible governance/reward tokens (AXS, SLP). Showcases token ecosystems: NFTs (game assets) + fungible tokens (economy, staking). Also a cautionary tale (economic collapse & hack created large losses).

5.	USDC (stablecoin, fungible token)
a.	USDC is a fungible ERC-20 (and multi-chain) stablecoin pegged to USD issued by Circle. Fungible tokens enable payments, liquidity and DeFi composability. Real-world events (e.g., network support changes) show cross-chain governance and issuer control have operational consequences. 

6.	ENS (Ethereum Name Service, semi-NFTs / domains)
a.	ENS names are NFTs representing human-readable names (e.g., alice.eth). Ownership of a name token controls resolution & can be used as identity. Shows NFTs as identity primitives beyond art. 
How ownership changes : on-chain transfer function updates token owner in ledger (for fungible tokens, balances change; for NFTs, token ID owner mapping changes). Ownership proofs are cryptographic: private key = control. Marketplaces implement escrow/atomic swaps and often use smart contracts to handle royalties, auctions, transfers.
Legal / practical caveats: token ownership ≠ automatic IP ownership of underlying art (rights depend on license) also custodial wallets, marketplaces, and off-chain metadata hosting create attack/availability points. 

4) Comparison tables
Table A; Blockchains / DLTs (concise)
Network	Type	Node roles / clients	Consensus	Finality / forks	Best fit / tradeoffs
Bitcoin	Permissionless L1	Full nodes (Bitcoin Core), SPV	PoW (SHA-256)	Probabilistic finality (longest chain)	Store of value, censorship resistance; energy heavy.
Ethereum	Permissionless L1 (smart contracts)	Execution clients (Geth), consensus clients, validators	PoS (post-Merge)	Probabilistic → faster finality via attestations; validator finality	dApps, DeFi, large ecosystem; PoS energy reduction. 
Solana	Permissionless L1 (high TPS)	Validators, RPC nodes	PoH + validator consensus (leader schedule)	Fast block production; some centralization/outage history	High throughput; good for NFTs/games but availability concerns. 
Polkadot	Layer-0 Relay + parachains	Validators (relay), collators (parachain)	BABE (block producer) + GRANDPA (finality)	Finality via GRANDPA (BFT); distinct production	Interoperability & shared security for many chains. 
Hyperledger Fabric	Permissioned DLT (enterprise)	Peers (endorsers), orderers, clients	Pluggable (Raft, etc.) ordering service	Deterministic finality (no PoW/PoS fork model)	Enterprise privacy, permissioning; not censorship-resistant public ledger. 
(Sources: Bitcoin whitepaper & docs; Ethereum docs; Solana, Polkadot specs; Hyperledger Fabric docs.)

Tokens: NFT vs Fungible (technical & use)
Property	Fungible token (ERC-20 / stablecoins)	NFT (ERC-721 / ERC-1155)
Divisibility	Usually divisible (decimals)	Non-divisible per token ID
Interchangeability	Fully fungible (1:1)	Unique, not interchangeable
Use cases	Payments, governance, liquidity (USDC, AXS)	Collectibles, identity, game assets (CryptoPunks, BAYC, TopShot)
Standards / example	ERC-20 (USDC, AXS). Fast transfers, composability in DeFi. 	ERC-721 / ERC-1155 (CryptoPunks, BAYC, TopShot). Metadata + ownership per token ID.
Transfer semantics	update balance mapping in contract	update ownerOf(tokenId) mapping; often unique metadata pointer
Legal/rights	Token = ledger balance; issuer may control off-chain peg	Token = ownership of token ID; IP/licensing often separate
Marketplaces	DEX/CEX/OTC	NFT marketplaces (OpenSea, Top Shot marketplace)

5) Risks, limits, and practical implications
•	Scalability vs decentralization: High-TPS chains (Solana, Flow) trade design choices that can introduce centralization or availability tradeoffs vs highly decentralized PoW chains. 
•	Custody & UX: Many users hold NFTs in custodial accounts (marketplaces, exchanges). True ownership requires private key control; custodial systems can freeze or restrict access.
•	Legal ambiguity: On-chain ownership does not automatically transfer copyright/IP unless contract/license states so. Buyers should review licensing terms. 
•	Economic risk: Token economies can be fragile (Axie case), and hacks (smart-contract or bridge exploits) can wipe value. Diversify risk and evaluate tokenomics. 

6) References with their links attached
1.	Satoshi Nakamoto — Bitcoin: A Peer-to-Peer Electronic Cash System (Bitcoin whitepaper). (Bitcoin)
2.	Bitcoin.org — How Bitcoin works / FAQ / devguide. (Bitcoin)
3.	Ethereum.org — Nodes & Clients / PoS docs / Merge overview. (ethereum.org)
4.	Solana docs / Turbine / Solana technical overviews. (docs.solanalabs.com)
5.	Polkadot spec & consensus (BABE / GRANDPA) / Chainsafe blog. (spec.polkadot.network)
6.	Hyperledger Fabric docs & architecture deep-dive. (hyperledger-fabric.readthedocs.io)
7.	Flow (Dapper Labs) blog & NBA Top Shot developer notes. (flow.com)
8.	Research paper / review on DLT (ResearchGate). (ResearchGate)
9.	U.S. GAO — Blockchain & Distributed Ledger Technologies primer. (Government Accountability Office)
10.	ERC-721 primer (Coinbase / EIP link). (Coinbase)
11.	ERC-20 token standard primer (Investopedia). (Investopedia)
12.	CryptoPunks / Yuga Labs news (The Verge). (The Verge)
13.	Bored Ape Yacht Club / partnerships (Vogue Business, GQ). (Vogue)
14.	Axie Infinity reporting (Time). (TIME)
15.	USDC/issuer operational news (Reuters). (Reuters)
16.	Solana Clients (Solana Concepts)



