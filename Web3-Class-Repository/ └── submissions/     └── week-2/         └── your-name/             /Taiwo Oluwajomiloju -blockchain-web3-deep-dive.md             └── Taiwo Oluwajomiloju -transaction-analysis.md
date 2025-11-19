# Week 2: Blockchain & Web3 Deep Dive Research (Day 1-3)
**Student Name:** [Taiwo Oluwajomiloju]  
**Date:** [19th of November,2025]  
**Tweet Link:** [Your Twitter thread link - add after posting]

---

## Part 1: Consensus Mechanisms Deep Dive

### Proof of Work (PoW) Analysis
[PoW is a consensus mechanism where miners compete to solve a computational puzzle by hashing block data until they find a valid result. The first miner to find it adds the next block and earns rewards.
Security: Altering history requires enormous computing power, making attacks extremely expensive. A 51% attack needs majority hash power, which is hard and costly to acquire.
Used by: Bitcoin, Litecoin, Dogecoin, Monero, Zcash, Kaspa (Ethereum used PoW before The Merge).
Pros: Very secure, battle-tested, decentralized.
Cons: High energy use, hardware centralization, slower throughput.
PoW has evolved from CPU → GPU → ASIC mining and remains one of the most secure consensus models.]

### Proof of Stake (PoS) Analysis
[PoS secures a blockchain by having validators lock (stake) tokens. The more you stake, the higher your chance to propose/validate blocks and earn rewards.
Security: Attacks require buying huge stake, and malicious validators get slashed (lose tokens).
Finality: Blocks finalize when enough validators (usually ≥⅔ stake) vote for them.
Used by: Ethereum, Cardano, Solana, Polkadot, Cosmos, many others.
Pros: Extremely energy-efficient, faster finality, no mining hardware.
Cons: Risk of wealth centralization and reliance on large staking pools.
PoS replaces computing power with economic skin-in-the-game.]

### Comparative Analysis
[Security
PoW: Secured by computational work. Attacks require massive mining power.
PoS: Secured by economic stake. Attacks require buying huge amounts of tokens and risk slashing.
Energy Use
PoW: Very high energy consumption (mining).
PoS: Very low; only requires validator nodes.
Transaction Speed
PoW: Slower; conservative block times.
PoS: Faster; supports quick block times and economic finality.
Decentralization
PoW: Can centralize around ASICs and cheap electricity.
PoS: Can centralize around wealthy stakers and staking pools.
Entry Barriers
PoW: High — needs specialized hardware and power.
PoS: Lower — mainly requires tokens; delegation makes it easy.
Costs
PoW: High operational cost (electricity + hardware).
PoS: Low operational cost but capital locked in staking.
Scalability
PoW: Limited; mostly scaled with Layer-2s.
PoS: High potential; supports sharding, fast finality, and high throughput.
Adoption
PoW: Longest track record (Bitcoin).
PoS: Widely adopted by modern blockchains; Ethereum now runs on PoS.]

### Practical Implications for Creatives
[NFT Minting & Consensus Mechanisms
Minting Costs
PoW: Expensive & volatile (miners compete for block space).
PoS / L2: Lower, more stable fees (validators/stakers replace miners).
DPoS / PoA: Very cheap, high throughput.
Best Mechanism by Use Case
High-value NFTs → PoS L1 (Ethereum)
Gaming / high volume → DPoS or L2 Rollups
Enterprise / predictable control → PoA
Censorship-resistant → PoS L1 / hybrid chains
Gas Fees
PoW: high, unpredictable
PoS: lower, more stable
L2: cheapest
Creator Considerations
Minting/transaction costs
Audience & marketplace compatibility
Security & decentralization
Royalties & sustainability
Developer ecosystem & interoperability]
---

## Part 2: Gas, Blocks & Confirmations

### Gas Economics
[Gas = unit of computation on a blockchain; like fuel for transactions.
Why “gas”: analogy to fuel; pays for network resources, not a fixed money value.
Relationship to computation: more complex operations = more gas required.
Gas Pricing
Gas price = cost per unit of gas, measured in Gwei.
Determined by network demand and transaction complexity.
Gas limit = max gas allowed; gas price = cost per unit.
Gas Calculation
Total cost = Gas Used × Gas Price
Examples: ETH transfer ~21,000 gas, ERC-20 transfer ~50k–100k gas, NFT mint ~100k–500k+ gas.
Complex transactions cost more; wallets/tools can estimate gas before sending.
Gas Optimization
Lowest fees: off-peak network hours.
Reduce costs: simpler operations, batching, Layer 2 solutions (rollups, sidechains).
Batching: combines multiple actions → shared gas cost → cheaper per operation.]

### Blocks Structure
[Block = digital container of transactions and metadata; like a ledger page.
Contents: transactions, block header, hashes, timestamps, consensus data.
Linked: each block contains the previous block hash, forming an immutable chain.
Block Components
Block Header: metadata including previous hash, timestamp, nonce, Merkle root.
Block Hash: unique identifier for the block.
Previous Block Hash: links the block to the chain.
Transactions per block: varies by blockchain (e.g., Bitcoin ~2–3k tx, Ethereum ~15–30 tx/sec).
Block Time
Definition: average time to add a new block.
Varies by blockchain: Bitcoin ~10 min, Ethereum ~12 sec, Solana <1 sec.
Importance: affects transaction speed, network throughput, and finality.
Finality relationship: shorter block times → faster confirmations but more forks; longer block times → slower but more stable finality.]

### Confirmations
[Definition: Each block added after a transaction counts as a confirmation, making the transaction more secure and permanent.
Security: More confirmations reduce the risk of reversals or double-spending, especially during chain reorganizations.
Confirmation Requirements
Small/low-risk tx: 1–3 confirmations
Large/high-value tx: 6–12 confirmations (Bitcoin standard)
Exchange deposits: Often 30+ confirmations
Few confirmations risk: Transaction may be reversed if a fork occurs.
Finality
Bitcoin (PoW): probabilistic finality; risk decreases with each confirmation
Ethereum PoS: checkpoint finality; final after ~2 epochs (~12 minutes)
Fast chains (Solana): near-instant finality, but multiple confirmations increase security
Practical Use
1 confirmation enough: small payments, trusted parties
Wait for more: large transactions, exchange deposits, NFT minting
NFT marketplaces: typically wait multiple confirmations before finalizing sales]

---

## Part 3: Wallet Security & Types

### Custodial vs Non-Custodial Wallets
[Custodial Wallets
Definition: Third-party holds your private keys.
Pros: Easy to use, password recovery, exchange integration.
Cons: Provider control, hack risk, limited ownership.
Examples: Coinbase, Binance, Kraken, Gemini, BitGo.
Best for: Beginners, short-term trading, low-risk storage.
Non-Custodial Wallets
Definition: You control your private keys; full ownership.
Pros: Full control, secure from provider hacks, DeFi/NFT compatible.
Cons: Losing keys = permanent loss, no recovery help.
Examples: MetaMask, Trust Wallet, Ledger, Trezor, Rainbow.
Best for: Long-term storage, DeFi, NFTs, privacy/security-focused users.
Key Comparison
Feature
Custodial
Non-Custodial
Security
Provider-dependent
User-controlled
Convenience
High
Medium
Control
Limited
Full
Recovery
Password/email
Seed phrase only
Use Cases
Beginners, exchange trading
DeFi, NFT, high-value assets
Strategy
Beginners: Custodial first.
Active Web3 users: Non-custodial for full control; hardware wallets for high-value assets.]

### Hot vs Cold Wallets
[Hot Wallets
Definition: Online wallets connected to the internet.
Pros: Instant access, convenient for trading or daily use.
Cons: Vulnerable to hacks, phishing, malware.
Best Use Cases: Small holdings, daily transactions, DeFi.
Examples: MetaMask, Trust Wallet, Coinbase Wallet.
Cold Wallets
Definition: Offline wallets, often hardware devices.
Pros: Highly secure, immune to online attacks.
Cons: Less convenient, device loss can be catastrophic, upfront cost.
Best Use Cases: Long-term storage, large holdings.
Examples: Ledger Nano X, Trezor Model T, BitBox02.
Comparison
Feature
Hot Wallet
Cold Wallet
Security
Low (online risk)
High (offline storage)
Convenience
High
Low
Cost
Free
$50–$200
Use Case
Frequent transactions
Long-term storage
Recommended Strategy
Small funds: Hot wallet for easy access.
Medium funds: Mix of hot (spending) + cold (savings).
Large funds: Mostly cold wallet; minimal hot wallet for active use.
Balance: Hot wallets for convenience, cold wallets for security.]

### Security Best Practices
[Seed Phrase
Definition: 12–24 word recovery key for your wallet.
Criticality: Full access to funds; losing it = permanent loss.
Storage: Offline (paper/metal), multiple secure locations, never online.
Mistakes to Avoid: Screenshots, sharing with anyone, storing in one risky place.
Common Attack Vectors
Phishing: Fake websites/emails tricking you to reveal keys.
Malware: Keyloggers, clipboard theft.
Social Engineering: Scammers posing as support.
Protection Tips: Use hardware wallets, 2FA, antivirus, verify URLs, avoid unknown apps.
Security Checklist
Wallet Setup: Use reputable wallet, generate offline seed phrase, secure backups, PIN/password, 2FA.
Daily Practices: Trusted sites, verify links, software updates, cautious app connections.
Emergency Procedures: Transfer funds if compromised, monitor accounts, keep backups, stay informed.]

---

## Part 4: Testnets & Blockchain Explorers

### Testnets
[Definition: Testnets are sandbox blockchains with valueless tokens for safe development and testing.
Purpose: Test smart contracts, dApps, network upgrades, and learn blockchain without risking real funds.
Difference from Mainnet: Tokens have no real value, lower security, may reset, cheaper transactions.
Popular Testnets:
Ethereum: Sepolia (dApp dev), Holesky/Hoodi (staking/validator tests)
Polygon: Mumbai (L2 dev)
Usage: Connect via MetaMask, get test tokens from faucets, deploy/test contracts, simulate transactions.
Limitations: No real value, faucet limits, resets, network differences.
Hands-On: Connect MetaMask → get test ETH/MATIC → send transactions → optionally deploy contracts → verify on explorer.]

### Blockchain Explorers
[Definition: Tools that let you view and search blockchain data—blocks, transactions, wallets, tokens, and smart contracts.
Importance: Provide transparency, security, debugging, and network monitoring.
Main Uses: Track transactions, check wallet balances, explore smart contracts, monitor gas fees, verify NFTs.
Etherscan Key Features:
Search transactions and read details (sender, receiver, value, gas, status).
Explore wallets, smart contracts, and token approvals.
Use gas tracker for real-time fees.
Other Explorers:
Polygonscan: Polygon network, MATIC, smart contracts.
Solscan: Solana network, tokens, NFTs.
BscScan: Binance Smart Chain, BEP-20 tokens.
SnowTrace: Avalanche, AVAX tokens.
Practical Use Cases:
Verify NFT ownership.
Check transaction status.
Investigate wallet activity.
Verify smart contract code.
Track gas prices.]

---

## Part 5: MEV (Maximal Extractable Value)

### Understanding MEV
[Definition: Extra profit validators or miners can capture by reordering, including, or excluding transactions in a block.
Meaning of “Maximal Extractable Value”: Maximum theoretical profit achievable from transaction ordering in a block.
MEV Extractors: Validators/miners and independent searchers who scan mempools for profitable opportunities.
How MEV Works:
Searchers identify opportunities (arbitrage, liquidations) in the mempool.
They submit transactions or bundles with higher fees to be prioritized.
Validators include/reorder transactions to capture MEV.
Types of MEV:
Front-running: Execute before a target transaction.
Back-running: Execute immediately after a target transaction.
Sandwich attacks: Execute before and after a target transaction.
Arbitrage & liquidation MEV: Exploit price differences or liquidation events.
Real-World Examples:
Total extracted MEV on Ethereum: hundreds of millions USD.
Famous cases: sandwich bots, validator bundles earning hundreds of ETH, bots front-running hackers.
Impacts:
Pros: Price alignment, faster liquidations, extra validator revenue.
Cons: User harm (slippage), network congestion, centralization risks, potential security threats.]

### Impact on Users
[On Transactions and DeFi Users:
Higher costs: MEV triggers competition (Priority Gas Auctions), increasing gas fees.
Transaction ordering: Bots/validators can reorder, include, or exclude transactions, affecting execution and slippage.
Failed transactions: Front-running or sandwich attacks can make your transaction revert.
DeFi impact: Small users face higher costs, worse execution, and potential unfairness; network congestion can increase.
In NFT Context:
NFT mints: MEV bots can front-run public mints, grabbing rare NFTs before regular users.
Front-running: Bots monitor mempool and submit higher-fee transactions to beat you.
Protections: Creators can use commit-reveal schemes, private/protected mempools, anti-MEV logic, and slippage/fee controls to reduce bot advantage.]

### MEV Solutions
[Current Solutions:
Flashbots: Infrastructure to reduce harmful MEV; provides MEV‑Boost (block building separation) and private transaction submission.
Private Mempools: Transactions hidden from public mempool to prevent front-running.
Commit–Reveal Schemes: Users commit a hashed transaction first, reveal later to hide intent and reduce MEV.
Layer 2 MEV Defenses: Decentralized sequencers and private RPCs to protect user transactions.
Future / Proposed Solutions:
Protocol-level PBS (ePBS): Block proposer and builder separation built into the protocol.
SUAVE: Decentralized auction layer for fair transaction ordering across chains.
Cryptographic solutions: Threshold encryption, verifiable decryption, and protected order flow to prevent front-running.
Debates / Trade-offs:
Centralization vs decentralization: Private pools reduce MEV harm but introduce trust.
Performance vs privacy: Encryption adds latency; commit-reveal delays execution.
Economic incentives: Completely removing MEV may reduce validator revenue; fair redistribution is preferred.
Adoption risk: Broad support needed across validators, builders, sequencers, and wallets.
Bottom Line: Mix of protocol-level fixes, private channels, and competitive builder markets is the likely path forward.]

---

## Part 6: Transaction Analysis

📖 See your separate transaction analysis document: `your-name-transaction-analysis.md`

---

## Comparison Tables

### PoW vs PoS Comparison

| Feature | Proof of Work | Proof of Stake |
|---------|---------------|----------------|
| Security Model |High, relies on computational power| High, relies on economic stake.|
| Energy Consumption | very high | low |
| Transaction Speed | moderate | fast|
| Decentralization | High | Moderate|
| Entry Barrier | high | low |
| Cost Structure | High electricity + handware| mostly staking deposits|
| Scalability | limited| better scalability, Layer 2 helps|

### Custodial vs Non-Custodial Wallets

| Feature | Custodial | Non-Custodial |
|---------|-----------|---------------|
| Security | Depends on provider| User controlled|
| Convenience | very convenient, no private key management| requires key management|
| Control | limited| full control|
| Recovery | provider can recover account| User must manage seed phrase |
| Use Cases | Beginners, exchanges| Experienced users, DeFi, self-custody|

### Hot vs Cold Wallets

| Feature | Hot Wallet | Cold Wallet |
|---------|------------|-------------|
| Security Level | Medium to high | very high|
| Convenience |Very convenient| less convenient |
| Cost | free or very cheap| expensive |
| Best For |daily spendin, Defi, trading,  small stake| large term holding, large stake|

---

## Key Takeaways
[Write 5-7 key insights you learned]

---

## All Sources and References
1. [ChatGPT]
2. [Grok]
3. [Source 3]
[List all sources used in your research]

---

**Twitter Thread:** [Add your tweet link here]
