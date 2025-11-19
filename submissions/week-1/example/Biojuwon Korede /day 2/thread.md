Ethereum (public smart-contract platform)
• Nodes / roles: execution clients and consensus clients (post-Merge separation). Operators run full nodes or light clients.
• Common client software: Execution — Geth, Erigon, Nethermind, Besu; Consensus — Prysm, Lighthouse, Teku, Nimbus, Lodestar.
• Consensus: Proof-of-Stake (post-Merge) with finality by consensus clients; pre-Merge was PoW. Client diversity matters for network safety. 
Bitcoin
• Nodes / roles: full nodes (validate blocks & transactions), lightweight/SPV nodes, miners (specialized mining nodes).
• Common client: Bitcoin Core is the reference/full-node implementation.
• Consensus: Nakamoto Proof-of-Work (PoW); miners produce blocks and nodes validate via longest-valid-chain rules. 
Solana
• Nodes / roles: validators (vote & produce blocks), leaders for slots, RPC nodes for apps.
• Client tooling: solana-validator, RPC endpoints, Solana tooling; token handling via SPL Token program.
• Consensus: hybrid — Proof of History (PoH) acts as a global clock + PoS leader selection + Tower BFT (PBFT variant) for finality. Designed for high throughput/low latency. 
Polkadot
• Nodes / roles: validators (finalize & validate), collators for parachains, nominators (stake delegators).
• Clients/stack: Substrate-based nodes (Parity implementation and others).
• Consensus: hybrid model — BABE for block production + GRANDPA for finality (Nominated PoS for validator selection). Built for interoperability (relay + parachains). 
Hyperledger Fabric (permissioned DLT / enterprise)
• Nodes / roles: peers (endorse and maintain ledger), orderers (ordering service), CAs (identity), clients.
• Implementations: Fabric reference code; pluggable components (consensus is modular).
• Consensus: not Nakamoto style — ordering service implementations (Raft is common); permissioned models with identity & policy controls. Used when privacy, permissioning, and modular governance matter. 
Avalanche (short note)
• Uses probabilistic repeated sampling (Avalanche family) and Snowman for linear chains; validator set and staking; aims for fast finality with high safety. 

2ND ANSWER
• Definitions: Distributed Ledger Technology (DLT) = a replicated, shared database across nodes. Blockchain = a type of DLT that sequences data into cryptographically-linked blocks. Not all DLTs use a chained block structure (some use DAGs, etc.). 
• When blockchain wins: public censorship-resistant money/token use, open ecosystems, composability (smart contracts).
• When DLT (non-blockchain) or permissioned ledger wins: enterprise workflows requiring privacy, identity, and controlled governance (lower latency, no native token required). Hyperledger Fabric is a classic permissioned DLT example. 

3RD ANSWER 
How ownership changes (short): Ownership is a change of the ledger state a transfer transaction moves the token id (NFT) or token balance (fungible) from one address to another; marketplaces often implement smart-contract transfers + on-chain settlement or use approved transfer mechanisms (e.g., ERC-721 safeTransferFrom or ERC-20 transfer/approve). For Solana, SPL token program handles token accounts and transfers. 
For Example 
• CryptoPunks: NFT on Ethereum (ERC-721 / historical custom contracts) — original 10,000 collection; transfers recorded on Ethereum; historically high cultural/market value. 
• Bored Ape Yacht Club (BAYC) — NFT collection on Ethereum (ERC-721) — membership utility + IP/licensing claims; trades via marketplaces, ownership moves via ERC-721 transfers. 
• NBA Top Shot — Collectible moments on Flow (Dapper Labs) — Flow is architected for collectible video moments (different architecture than Ethereum), ownership changes on Flow’s ledger and via their marketplace. 
• Art Blocks / generative art  On-chain/contract-driven NFTs on Ethereum  minting generates unique token metadata, ownership transfers via standard ERC-721 flows. 
• OpenSea marketplace (infrastructure for transfers)  Cross-chain marketplace (mainly Ethereum, other chains supported) — facilitates listing, bidding, and safeTransferFrom to move NFTs between owners. OpenSea uses smart contracts to effect on-chain transfers. 
• Fungible tokens — USDC / DAI / ERC-20 examples — ERC-20 defines transfer/approve functions; ownership of fungible units is a ledger balance change (on Ethereum). Stablecoins (USDC/DAI) are ERC-20 tokens used for payments, collateral, and DeFi. 
Solana SPL tokens (fungible & NFTs) — Solana uses SPL Token program for fungible tokens and token accounts; NFTs on Solana are usually SPL tokens with supply=1 + metadata account (Metaplex). Ownership changes via SPL token transfers.