| Blockchain | Node Type                 | Client Examples  | Consensus Mechanism             |
| ---------- | ------------------------- | ---------------- | ------------------------------- |
| Bitcoin    | Full nodes, mining nodes  | Bitcoin Core     | Proof of Work (PoW)             |
| Ethereum   | Full nodes, light clients | Geth, Nethermind | Proof of Stake (PoS)            |
| Solana     | Validator nodes           | Solana Validator | Proof of History (PoH) + PoS    |
| Polkadot   | Validators, nominators    | Parity Polkadot  | Nominated Proof of Stake (NPoS) |
| Avalanche  | Validators                | AvalancheGo      | Avalanche Consensus             |
Part 1 Compare Distributed Ledgers vs Blockchains
| Feature      | Distributed Ledger                      | Blockchain                                                          |
| ------------ | --------------------------------------- | ------------------------------------------------------------------- |
| Definition   | A database spread across multiple nodes | A type of distributed ledger using cryptographic chaining of blocks |
| Structure    | Can be blockless                        | Uses sequential blocks                                              |
| Consensus    | Varies (not always PoW/PoS)             | Always has a consensus mechanism                                    |
| Example      | Corda, Hyperledger Fabric               | Bitcoin, Ethereum                                                   |
| Transparency | Private or public                       | Usually public and transparent                                      |
Part 2 NFTs & Fungible Tokens (Ownership)
NFTs (Non-Fungible Tokens) represent unique assets, while fungible tokens represent interchangeable units of value.
| Type           | Description                | Example                         |
| -------------- | -------------------------- | ------------------------------- |
| NFT            | Unique digital collectible | Bored Ape Yacht Club (Ethereum) |
| NFT            | Game item                  | Axie Infinity (Ronin)           |
| NFT            | Music/Art ownership        | Royal.io NFT Music              |
| Fungible Token | Currency                   | USDT (Tether)                   |
| Fungible Token | Utility token              | Binance Coin (BNB)              |
| Fungible Token | Governance token           | Uniswap (UNI)                   |
Part 3 Blockchain comparison table (5 blockchains)
| Blockchain    |                                                                                  Node types (role) | Example clients / software                                           | Consensus mechanism (short)                                                                                                                              |
| ------------- | -------------------------------------------------------------------------------------------------: | -------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Bitcoin**   |                                      Full nodes (validate blocks & tx), pruned/light nodes, miners | **Bitcoin Core** (most common full-node client).                     | **Proof of Work (PoW)** — mining, longest-chain rule. ([Bitcoin][1])                                                                                     |
| **Ethereum**  | Execution clients (state, EVM) + Consensus clients (validator) after The Merge; full & light nodes | Execution: **Geth**, Nethermind; Consensus: Lighthouse, Prysm, Teku. | **Proof of Stake (PoS)** (validator-based, slashing/rewards; post-Merge architecture uses execution + consensus client split). ([docs.nethermind.io][2]) |
| **Solana**    |                              Validator nodes, RPC nodes, archival nodes (replicators historically) | **solana-validator**, CLI tools; docs & whitepaper for architecture. | **Proof of History (PoH)** as ordering/clock + PoS for validator selection — optimized for high throughput and low latency. ([Solana][3])                |
| **Polkadot**  |                                                 Validators, Nominators, Collators (for parachains) | **polkadot** client (Parity Substrate-based clients).                | **Nominated Proof of Stake (NPoS)** — nominators back validators; staking / governance integrated. ([docs.polkadot.com][4])                              |
| **Avalanche** |                                                     Validators (stake AVAX), full nodes, RPC nodes | **AvalancheGo** (reference implementation).                          | **Avalanche consensus** — randomized sub-sampled voting (fast finality, high throughput). ([Avalanche Builder Hub][5])                                   |

[1]: https://bitcoin.org/en/full-node?utm_source=chatgpt.com "Running A Full Node"
[2]: https://docs.nethermind.io/get-started/running-node/consensus-clients/?utm_source=chatgpt.com "Consensus clients"
[3]: https://solana.com/solana-whitepaper.pdf?utm_source=chatgpt.com "A new architecture for a high performance blockchain"
[4]: https://docs.polkadot.com/polkadot-protocol/architecture/polkadot-chain/pos-consensus/?utm_source=chatgpt.com "Proof of Stake Consensus | Polkadot Developer Docs"
[5]: https://build.avax.network/docs/nodes?utm_source=chatgpt.com "Introduction"
Distributed ledger vs Blockchain
| Feature          |                                                      Distributed Ledger (DLT) | Blockchain                                                                                                      |
| ---------------- | ----------------------------------------------------------------------------: | --------------------------------------------------------------------------------------------------------------- |
| **Definition**   |                 A replicated database across multiple nodes (broad category). | A **type** of distributed ledger that organizes data in chained blocks. ([Medium][1])                           |
| **Structure**    |        Can be blockless; model varies (e.g., directed graph, state channels). | Uses sequential blocks linked by cryptographic hashes. ([Medium][1])                                            |
| **Consensus**    |                      Varies widely; may be permissioned consensus algorithms. | Always relies on a consensus algorithm (PoW, PoS, etc.). ([Medium][1])                                          |
| **Typical use**  | Enterprise workflows, privacy-preserving networks (e.g., Hyperledger, Corda). | Public value transfer / open platforms (Bitcoin, Ethereum) but also private blockchains exist. ([eleks.com][2]) |
| **Transparency** |                                   Often permissioned (restricted read/write). | Often public and transparent (but can be permissioned). ([eleks.com][2])                                        |

[1]: https://medium.com/data-science/the-difference-between-blockchains-distributed-ledger-technology-42715a0fa92?utm_source=chatgpt.com "The Difference Between Blockchains & Distributed Ledger ..."
[2]: https://eleks.com/research/corda-vs-hyperledger-fabric/?utm_source=chatgpt.com "Corda vs Hyperledger Fabric: Comparing DLT Frameworks"
NFTs vs Fungible Tokens

Sources

Bitcoin — Running a full node / Bitcoin Core. 
Bitcoin

How to run a Bitcoin node (requirements explainer). 
GetBlock.io

Ethereum docs — execution & consensus client split (Nethermind). 
docs.nethermind.io

Ethereum RPC / QuickNode / PoS references. 
quicknode.com

Solana — confirmation & whitepaper (Proof of History). 
Solana


Polkadot — Nominated Proof of Stake docs. 
docs.polkadot.com

Avalanche — Avalanche consensus & nodes (AvalancheGo). 
Avalanche Builder Hub


Distributed ledger vs blockchain / Hyperledger & Corda comparisons. 
eleks.com


ERC-721 standard (EIP-721 / ethereum.org). 
Ethereum Improvement Proposals


ERC-20 standard (EIP-20 / ethereum.org). 
Ethereum Improvement Proposals


Bored Ape Yacht Club (OpenSea collection / BAYC). 
OpenSea

Axie Infinity / Ronin docs. 
AxieInfinity


NBA Top Shot / Flow (Dapper Labs docs). 
NBA Top Shot Developers


Royal (music NFT platform) / Alchemy case study. 
Royal


Tether (USDT) & Circle (USDC) official pages (stablecoins).
