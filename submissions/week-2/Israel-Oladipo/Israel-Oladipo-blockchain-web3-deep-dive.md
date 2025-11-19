# Week 2: Blockchain & Web3 Deep Dive Research (Day 1-3)
Student Name: Israel Oladipo
Date: 19th November, 2025
Tweet Link: https://x.com/IamIsrael__1/status/1991132516082721222?t=siqn-BG7Hqwb0P2KeU-0lA&s=19 

## Part 1: Consensus Mechanisms Deep Dive

### Proof of Work (PoW) Analysis

HOW PoW WORKS

1. Transaction broadcast: Users broadcast transactions to the network
2. Transaction pool: Miners verify transactions and add them to a mempool (pending transaction pool)
3. Mining/Solving cryptographic puzzle: Miners compete to solve cryptographic puzzle
4. Block proposal: First miner to solve cryptographic puzzle propose new block
5. Block verification: Other full nodes verify the block
6. Block Added: Once verification is successful, the new block is added to the blockchain and broadcasted to other nodes.

WHAT PROBLEM ARE MINERS SOLVING?

- Miners solve a cryptographic puzzle:  
  Find a nonce that results in a SHA-256 hash of the block that starts with a certain number of leading zeros (based on difficulty).


 DIFFICULTY ADJUSTMENT

- PoW networks like Bitcoin adjust difficulty every 2016 blocks (~2 weeks).
- If blocks are being mined too quickly, the difficulty increases.
- If blocks are too slow, it decreases.
- This keeps the block time around 10 minutes (for Bitcoin).


 WHEN TWO MINERS SOLVE SIMULTANEOUSLY?

- A temporary fork happens, both blocks are added by different nodes.
- The network waits for the next block.
- The longest valid chain wins, the other block becomes an orphan.


 SECURITY MODEL

How PoW Prevents Attacks:
- It requires massive computational work to alter history or double-spend.

51% attack:
If an entity controls over 50% of the network hash rate, they could:
  - Reverse transactions (double spend)
  - Block other miners/transactions

Difficult to pull off due to high cost of hardware + energy + coordination.

Economic incentives:
Miners are rewarded with:
  - Block subsidy (new coins)
  - Transaction fees

Cost of Attacking:
- Requires huge investment in hardware + electricity.
- The attack may devalue the network and the attacker’s own coins.


 REAL-WORLD EXAMPLES

- Bitcoin: The original and most secure PoW chain. Uses SHA-256.
- Ethereum (before Merge): Used Ethash, GPU-friendly.
- Litecoin: Uses Scrypt (ASIC-resistant).
- Monero: Uses RandomX to promote CPU mining and resist centralization.


  EVOLUTION OF PoW

1. New PoW Algorithms
- Older PoW like Bitcoin’s SHA-256 led to ASIC dominance (expensive, centralized).
- Newer algorithms like RandomX (used by Monero) are CPU-friendly to keep mining more decentralized and fair.
- Goal: Make mining accessible and resist specialized hardware.

2. Hybrid PoW + PoS Models 
- Some blockchains (like Decred) combine PoW for security and PoS for governance/efficiency.
- This helps balance security, decentralization, and energy use.

Advantages:
- High level of security
- Highly decentralized (especially in Bitcoin)
- Proven and battle-tested security model

Disadvantages:
- Energy intensive
- Mining centralization (ASICs dominate)
- Slower finality


### Proof of Stake (PoS) Analysis

HOW PoS WORKS 

1. Staking Begins:
   Users (validators) lock up a set amount of tokens (e.g., 32 ETH on Ethereum) as collateral to participate.

2. Validator Selection: 
   The network selects validators pseudo-randomly using a process called RANDAO, often based on stake size and other factors (like time staked or randomness).

3. Block Proposal:
   A selected validator proposes the next block of transactions.

4. Block Attestation/Validation:
   Other validators check the block’s validity and “attest” if correct.

5. Finalization:
   Once enough validators attest, the block is considered final, meaning it can’t be reverted without heavy penalties.


SLASHING IN PoS

- Slashing is the penalty for dishonest or faulty behavior (e.g., proposing invalid blocks or double-signing).
- Part of the staked amount is taken (slashed), and the validator may be removed.


HOW FINALITY WORKS IN PoS

- Finality means a block is confirmed and can’t be changed without major penalties.
- In Ethereum PoS, once 2/3 of validators attest to a block in two consecutive checkpoints, it’s finalized.
- This ensures network stability and prevents chain forks.


PoS SECURITY MODEL

1. How PoS Prevents Attacks:
- Validators must stake real value, which they lose if they act dishonestly.
- Attacks (like proposing invalid blocks) are discouraged due to slashing.

2. Economic Penalties (Slashing):
- Misbehavior (e.g., double-signing, being offline) leads to partial or full loss of staked tokens.
- Penalties scale based on the severity and number of validators involved.

3. Stake Size & Security:
- The more a validator stakes, the higher their influence—and risk.
- An attacker would need to control a large portion (e.g., >33% or 51%) of the stake, which is very expensive.

4. Stake vs Rewards:
- Larger stakes earn more rewards, incentivizing long-term honest participation.
- But reward curves are designed to avoid too much centralization.


 REAL-WORLD EXAMPLES

1. Ethereum:
- Uses Casper FFG (Friendly Finality Gadget) with a 32 ETH minimum stake.
- Validators propose/attest and earn ETH for securing the network.

2. Cardano:
- Uses Ouroboros, a different PoS model where delegation is common.
- Time is split into “epochs” and “slots”, and leaders are chosen per slot.

3. Solana:  
- Uses a hybrid of PoS + Proof of History (PoH) for high throughput.
- Validators are selected via stake but use PoH for time-stamping.


TRADE-OFFS OF PoS

Advantages:
- Energy efficient (no mining).
- Faster finality.
- Lower barrier to entry (via staking pools).

Disadvantages:
- Risk of centralization (large stakers dominate).
- Wealth concentration—“rich get richer” problem.
- Newer, less battle-tested than PoW.


### Comparative Analysis

| Feature                                    | Proof of Work (PoW)                                                                            | Proof of Stake (PoS)                                                                                            |
|--------------------------------------------|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Security Model                             | Computational security: miners solve cryptographic puzzles requiring high computational power. | Economic security: validators stake tokens as collateral, risking slashing for bad behavior.                    |
| Energy Consumption & Environmental Impact  | Very high energy use due to intensive mining hardware; significant environmental concerns.     | Low energy use since no heavy computations; more environmentally friendly.                                      |
| Transaction Speed & Throughput             | Generally slower, limited by block times and mining difficulty (e.g., ~7 TPS for Bitcoin).     | Faster block times and higher throughput; can support hundreds to thousands TPS depending on implementation.    |
| Decentralization Levels                    | Can be centralized due to mining pool dominance and ASIC hardware concentration.               | Can face centralization risks if large stakeholders dominate, but potentially more accessible to average users. |
| Entry Barriers for Participation           | High:  requires expensive mining hardware and access to cheap electricity.                     | Lower:  requires owning and staking tokens; hardware requirements are minimal.                                  |
| Cost Structures                            | High ongoing electricity and hardware maintenance costs.                                       | Lower operational costs; main cost is locking up tokens (opportunity cost).                                     |
| Scalability Potential                      | Limited scalability; hard forks and Layer 2 solutions needed to scale.                         | More scalable with faster consensus; can incorporate sharding and other upgrades easier.                        |
| Real-world Adoption & Track Record         | Used by Bitcoin, Litecoin, and until recently Ethereum; longest proven security history.       | Used by Ethereum 2.0, Cardano, Solana; newer but rapidly growing adoption.                               


### Practical Implications for Creatives

1. How consensus affects NFT minting costs:
- PoW chains (like Ethereum before The Merge) use lots of energy and computing power, making gas fees (minting costs) high.  
- PoS chains are more energy-efficient, so gas fees are usually much lower, reducing minting costs.

2. Best consensus for different use cases: 
- PoW suits projects valuing strong security and decentralization (e.g., high-value NFTs).  
- PoS is great for projects needing fast, cheap transactions and scalability (e.g., mass minting, games).

3. Gas fees differences:
- PoW chains often have unpredictable and high gas fees during network congestion.  
- PoS chains offer more stable, lower fees due to efficient validation.

4. What you should consider as a creator:
- Cost: Can you afford high minting fees?  
- Speed: Does your project need quick transactions?  
- Security: Is decentralization crucial for your NFT's value?  
- Community & Ecosystem: Where is your target audience active?  
- Blockchain features: Does it support your NFT’s needs (e.g., smart contracts, interoperability)? 


## Part 2: Gas, Blocks & Confirmations

### Gas Economics

WHAT IS GAS?  
- Gas is the cost of computational resources required to execute a transaction or smart contract. 
- It’s called "gas" because it fuels the network, similar to how gas powers a car—without gas, nothing runs.  
- Every transaction or smart contract operation consumes gas proportional to the computational effort.


HOW GAS PRICING WORKS  
- Gas price is how much you pay per unit of gas, usually measured in Gwei (1 Gwei = 0.000000001 ETH).  
- Gas prices fluctuate based on network demand: higher demand = higher prices.  
- Miners/validators prioritize transactions with higher gas prices.  
- Gas limit is the maximum amount of gas you're willing to spend on a transaction.  
- Gas price = how much per gas unit; Gas limit = max gas units to spend.


GAS CALCULATION  
- Total transaction cost = Gas used × Gas price.
- Simple transfers cost less gas; complex smart contract interactions cost more (due to more computation).  
- You can estimate gas using wallet tools or blockchain explorers before sending.  


GAS OPTIMIZATION STRATEGIES  
- Gas prices tend to be lowest during off-peak hours (nights/weekends).  
- Reduce gas costs by:
  - Waiting for low network activity  
  - Using Layer 2 solutions (off-chain scaling that bundles transactions before settling on mainnet)  
  - Batching multiple transactions into one to save on repeated fees.


### Blocks Structure

WHAT IS A BLOCK?
A block is like a page in a digital ledger. It holds a list of verified transactions and links to the block before it.  


WHAT'S INSIDE A BLOCK?
A block contains:  
- Transactions: A list of actions users have made (like transfers, smart contract calls).  
- Block Header: Summary info like time, hash, etc.  
- Block Hash: A unique fingerprint of the block.  
- Previous Block Hash: Links the block to the one before it, forming the chain.  


BLOCK COMPONENTS 
- Block Header: Includes metadata like timestamp, nonce, Merkle root, previous hash, etc.  
- Block Hash: A cryptographic code representing all the block data.  
- Previous Block Hash: This ensures every block points to its parent block, creating the chain.  
- Transactions per Block: Varies by blockchain; Bitcoin fits ~2,000 txns; Ethereum fits more or less depending on gas used.

BLOCK TIME  
- Block time is how long it takes to create a new block.  
  - Bitcoin: ~10 minutes
  - Ethereum (PoS): ~12 seconds  
  - Solana: ~0.4 seconds  
- Why it matters: Shorter block times mean faster transaction confirmations.  

- Blocktime & Finality: Block time is how fast blocks are produced, while finality is when a block becomes irreversible. Shorter block times can lead to quicker finality, but finality depends more on the consensus mechanism than just speed
 

### Confirmations

WHAT ARE CONFIRMATIONS?

- Confirmations are the number of blocks added on top of a block that contains a transaction.  
- Why it matters: The more confirmations a transaction has, the more secure and irreversible it becomes.
- Security: Each confirmation makes it harder for an attacker to reverse the transaction by replacing the block.

 CONFIRMATION REQUIREMENTS

1. How many confirmations are needed?
- 1–2 confirmations: Low value or personal transactions  
- 3–6: Medium value (common for crypto wallets)  
- 12+: High-value or exchange-level safety  
- 30+: For very high security (like BTC withdrawals on big exchanges)

2. Why do exchanges wait for more?
To avoid accepting a transaction from a block that might get replaced during a chain reorg. More confirmations = more finality.

3. What’s the risk of few confirmations? 
The block may still be replaced, causing the transaction to disappear. Risk of double spend or failed delivery.

4. How do chains handle finality?  
- Bitcoin: Probabilistic finality (more confirmations = safer)  
- Ethereum (PoS): Economic finality (finalized after 2 epochs ≈ 12 minutes)

REAL-WORLD APPLICATION

1. When is 1 confirmation enough?  
- Small payments  
- Trusted parties  
- Some NFT listings on L2s

2. When should you wait for more?  
- Large transactions  
- Exchange deposits/withdrawals  
- Untrusted sources

3. NFT marketplaces?  
Many wait for 1–3 confirmations to list a minted or transferred NFT.

4. Chain reorganization?
If a chain reorg happens, a block can be replaced, transactions in it disappear or move to later blocks.


## Part 3: Wallet Security & Types

### Custodial vs Non-Custodial Wallets

CUSTODIAL WALLETS

1. What are they? 
Custodial wallets are wallets  where a third party (e.g., exchange or service provider) holds and manages your private keys for you.

2. How do they work technically?
- Your assets are stored in wallets controlled by the service.  
- You log in with a username/password.  
- The provider signs transactions on your behalf using the private keys they control.

3. Advantages: 
- Easy to use (no need to manage keys)  
- Account recovery available  
- Often integrated with exchanges for fast trading

4. Risks:  
- You don’t truly own your crypto ("not your keys, not your coins")  
- Vulnerable to hacks or platform shutdowns  
- Subject to regulations and freezing

5. Examples:  
- Binance  
- Coinbase  
- Bybit
- Bitget 
- Crypto.com


NON-CUSTODIAL WALLETS

1. What are they?  
Non-custodial wallets are wallets where you control your private keys, full ownership of your assets.

2. How do they work technically?
- The private key is generated and stored on your device.  
- Only you can sign transactions.  
- Most use seed phrases for backup.

3. Advantages:  
- Full control and ownership  
- Not reliant on third-party platforms  
- More privacy and censorship resistance

4. Risks:  
- If you lose your seed phrase or private key, you lose access, no recovery.  
- Requires more technical responsibility  
- Susceptible to phishing or malware on your device

5. Examples:  
- MetaMask  
- Trust Wallet  
- Phantom  
- Ledger (hardware)  
- Trezor (hardware)

CUSTODIAL VS NON-CUSTODIAL WALLETS

|  Feature            |  Custodial Wallet                                                                           |  Non-Custodial Wallet                                                |
|---------------------|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
|  Security           | Depends on provider’s security infrastructure. Vulnerable to hacks if provider is breached. | Security depends on the user. Safer if private keys are kept secure. |
|  Convenience        | Very user-friendly. No need to manage private keys.                                         | Less convenient. Users must manage private keys and backups.         |
|  Control            | Third party controls your funds and private keys.                                           | Full control of funds and private keys.                              |
|  Recovery Options   | Yes,  can reset password or recover account via provider.                                   | No,  if you lose your seed phrase/private key, funds are lost.       |
|  Use Cases          | Best for beginners, traders, and centralized platforms.                                     | Ideal for DeFi users, privacy-focused users, and long-term holders.  


### Hot vs Cold Wallets

HOT WALLETS

Hot wallets are digital wallets connected to the internet, allowing quick access to crypto assets.

How do they work?  
They store private keys on internet-connected devices like phones or computers, enabling instant transactions.

Security Implications:  
- More vulnerable to hacks, malware, or phishing.
- Convenient but less secure for large holdings.

Best Use Cases: 
- Frequent trading.
- Small, daily transactions.
- DApps and DeFi interactions.

Examples:  
- MetaMask  
- Trust Wallet  
- Coinbase Wallet  

COLD WALLETS
 
Cold wallets are offline wallets not connected to the internet, used to store crypto securely.

How do hardware wallets work?  
They store private keys on a physical device. Transactions are signed on the device and then broadcast online, keeping the keys isolated.

Security Benefits:  
- Immune to online attacks.
- Best for long-term storage and large amounts.

Limitations:  
- Less convenient for fast or frequent use.
- Risk of physical loss or damage.

Examples of Hardware Wallets:  
- Ledger Nano S / X  
- Trezor Model T  
- Keystone Wallet


HOT WALLET VS COLD WALLET

| Feature           |  Hot Wallets                                |  Cold Wallets                                  |
|-------------------|---------------------------------------------|------------------------------------------------|
|  Security Level   | Medium,  always online, more hack risk      | High,  offline, safe from online threats       |
|  Convenience      | Very convenient,  instant access, fast txns | Less convenient,  requires physical access     |
|  Cost             | Usually free (apps/extensions)              | Costs money (hardware devices)                 |
|  Best Use Cases   | Daily trading, DApps, small holdings        | Long-term storage, large amounts, HODLing      |


### Security Best Practices

SEED PHRASE SECURITY
  
  A seed phrase is a series of 12 or 24 random words generated when you create a crypto wallet. It acts as the master key to access your wallet and funds.

- Why is it critical? 
  Anyone with your seed phrase can take full control of your wallet. Lose it, and you lose access forever. Share it, and your funds are at risk.

- How should you store it? 
  - Write it down on paper and keep it offline.
  - Store in a fireproof, waterproof place.
  - Never take a screenshot or save it in cloud storage.

- Common mistakes to avoid:  
  - Saving the phrase digitally (photos, notes app, email).  
  - Sharing it with anyone.  
  - Losing the only copy.  
  - Entering it on suspicious websites.


COMMON ATTACK VECTORS

- Phishing: 
  Fake websites or emails trick you into entering your seed phrase or private keys. Always double-check URLs and never trust links from strangers.

- Malware Attacks:  
  Malicious software on your device can log keystrokes, take screenshots, or monitor clipboard activity. Use antivirus and avoid downloading from shady sources.

- Social Engineering:
Scammers may pretend to be support agents, friends, or influencers to trick you into giving up sensitive info. No legit platform will ever ask for your seed phrase.

How to protect yourself:  
  - Always verify links and sources.  
  - Keep your device clean and updated.  
  - Don’t share wallet info online.  
  - Use hardware wallets for large amounts.  
  - Educate yourself about common scams. 

CRYPTO WALLET SECURITY CHECKLIST

 Wallet Setup

1. Use a Trusted Wallet Provider  
   - Choose reputable wallets (e.g., MetaMask, Trust Wallet, Ledger).

2. Secure Your Seed Phrase 
   - Write down the 12/24-word phrase offline.  
   - Store in a safe, private place (fireproof safe or metal backup).  
   - Never store digitally or online.

3. Enable Security Features  
   - Set a strong password or PIN.  
   - Enable biometric login (if available).  
   - Use 2FA on platforms that support it.

4. Use a Hardware Wallet for Large Funds  
   - Cold wallets (e.g., Ledger, Trezor) are safest for long-term holding.


Daily Security Practices

1. Double-check URLs  
   - Only access wallets via official websites or apps.  
   - Bookmark trusted links.

2. Beware of Phishing  
   - Don’t click on unknown links or DMs.  
   - No legit support will ask for your seed phrase.

3. Keep Devices Secure  
   - Use antivirus software.  
   - Regularly update your OS and apps.

4. Avoid Public Wi-Fi  
   - Use a VPN if needed for extra protection.

5. Keep Wallets Private  
   - Don’t share screenshots of wallet interfaces.  
   - Don’t brag about wallet balances online.

 Emergency Procedures

1. Lost Seed Phrase?
- If not backed up = funds are likely lost.  
- If backed up = recover using seed on a new device.

2. Seed Phrase Exposed?  
   - Immediately transfer funds to a new wallet with a new seed phrase.

3. Compromised Wallet? 
   - Disconnect from dApps.  
   - Revoke token permissions using tools like revoke.cash.  
   - Move funds to a secure wallet.

4. Regular Backups 
   - Periodically confirm your seed is still accessible and readable.  
   - Keep multiple physical backups in separate safe locations.


## Part 4: Testnets & Blockchain Explorers

### Testnets

WHAT ARE TESTNETS?

Testnets are sandbox versions of a blockchain where developers can test apps, smart contracts, and upgrades without using real money or affecting the main network.


Why Do Testnets Exist?

- To test new features or apps safely.
- To identify bugs before launching on mainnet.
- To simulate real-world activity using free test tokens.
- To train developers without risk.

 TESTNET vs MAINNET

| Feature            | Testnet                          | Mainnet                          |
|--------------------|----------------------------------|----------------------------------|
| Purpose            | Testing & experimentation        | Real-world transactions          |
| Currency           | Free, worthless test tokens      | Real, valuable crypto            |
| Risk Level         | Zero financial risk              | Financial consequences           |
| Stability          | Less stable, may reset often     | Highly stable                    |


POPULAR TESTNETS

1. Sepolia (Ethereum)  
- Replaced Rinkeby & Goerli  
- Fast, stable Ethereum testnet  
- Uses ETH test tokens  
- Closely mirrors Ethereum mainnet behavior  

2. Mumbai (Polygon)  
- Testnet for Polygon PoS chain
- Uses MATIC test tokens  
- Developers test dApps before deploying to Polygon mainnet  

3. Other Major Testnets 
- Holesky (new Ethereum testnet, replacing Goerli)  
- Base Sepolia (for Coinbase’s Base chain)  
- Fuji (for Avalanche)  
- Amoy(for Polygon CDK chains) 

HOW TO USE TESTNETS 

1. Connect to a Testnet in MetaMask

a. Enable Testnets:
- Open MetaMask.
- Click your account icon → Settings → Advanced.
- Toggle on "Show test networks".

b. Select a Testnet:
- Click the network dropdown at the top.
- Choose a testnet like Sepolia, Mumbai, etc.


 2. Get Test Tokens (Faucets)

Use a faucet site to request free test tokens:
- Sepolia ETH: Search “Sepolia faucet”
- Mumbai MATIC: Search “Mumbai faucet”
- Paste your MetaMask address and receive token.

 3. What You Can Practice

- Deploy smart contracts (e.g., using Remix or Hardhat)
- Interact with dApps safely
- Test DeFi, NFT, or token protocols
- Simulate transactions without using real crypto


4. Limitations of Testnets

- Test tokens have no value
- Network may reset, losing history
- Lower reliability compared to mainnet
- Limited real-world integration

### Blockchain Explorers

 WHAT ARE BLOCKCHAIN EXPLORERS?

A blockchain explorer is a tool that lets you search, view, and verify everything happening on a blockchain, like a public search engine for blockchain data.


 Why Are They Important?

- They promote transparency (everyone can see the data).
- Help users track transactions and wallet activity.
- Allow developers to debug smart contracts or test dApps.
- Let users verify ownership of NFTs or tokens.


What Can You Do With a Blockchain Explorer?

- Check if a transaction was successful
- View wallet balances and histories
- Track gas fees
- Explore token info (e.g., NFTs, ERC-20s)
- Audit smart contract code
- Monitor network activity


ETHERSCAN DEEP DIVE 

1. Search for Transactions:
   - Paste your wallet address or transaction hash (TXN) in the search bar.

2. Read Transaction Details:
   - Status: Success or Failed
   - Gas used & gas price
   - From and To addresses
   - Timestamp
   - Block number

3. Explore Wallet Addresses:
   - See balance
   - View all incoming/outgoing transactions
   - Track NFTs or tokens held

4. View Smart Contracts:
   - Go to “Contracts” tab on a token page
   - Read or write functions via the UI
- See contract source code (if verified)

5. Check Token Approvals:
   - Use tools like Etherscan Token Approval Checker
   - See which dApps can spend your tokens

6. Use Gas Tracker:
   - Shows real-time gas price estimates (low/avg/high)
   - Helps you choose the right gas fee for sending transactions


OTHER EXPLORERS

 Polygonscan (Polygon)

- URL: polygonscan.com  
- Key Features:
  - View Polygon (MATIC) transactions, blocks, tokens (ERC-20, ERC-721)
  - Smart contract interaction
  - NFT tracking
  - Gas tracker for Polygon network
- Use when:
  - You’re working with dApps on Polygon (e.g., Aave, QuickSwap)
  - Verifying MATIC or token transfers on Polygon

Solscan (Solana)

- URL: solscan.io  
- Key Features:
  - Solana account and transaction tracking
  - Token and NFT explorer
  - Validator information
  - Rich transaction details (slot, program interactions)
- Use when:
  - You’re tracking SOL, SPL tokens, or NFTs on Solana
  - Debugging Solana-based apps

BscScan (BNB Smart Chain)

- URL: bscscan.com    
- Key Features:
  - View BNB and BEP-20 token transactions
  - Smart contract explorer
  - Token approval checker
  - DApp integration
- Use when:
  - You’re using DeFi/NFT dApps on BNB Chain (e.g., PancakeSwap)
  - Tracking BNB or tokens like CAKE

## Part 5: MEV (Maximal Extractable Value)

### Understanding MEV

What is MEV (Maximal Extractable Value)?

- MEV refers to the maximum value that miners or validators can extract from block production by reordering, including, or excluding transactions beyond just collecting gas fees.


 Who Are MEV Extractors?
- Validators/miners: They control transaction order.
- Searchers: Bots or people who scan the mempool for profitable opportunities and submit optimized bundles via services like Flashbots.

How MEV Works

1. Transaction monitoring: Searchers monitor mempool for profitable opportunities (e.g., large DEX swaps).
2. Transaction bundling: They create custom transaction bundles that exploit these opportunities.
3. Block manipulation: Validators include these bundles for a cut or execute it themselves.

Types of MEV

- Front-running: Inserting a transaction before another to profit (e.g., buy before a large trade).
- Back-running: Executing a transaction immediately after another (e.g., sell right after price pumps).
- Sandwich attacks: A combo, placing a buy before and sell after someone else's large trade to profit from the price movement they cause. 

### Impact on Users

Impact on Transaction Costs

- MEV can increase gas fees during high activity (e.g., NFT mints, DeFi trades).
- Bots competing to extract MEV bid higher gas to be prioritized, pushing up fees for everyone else.

 Impact on Transaction Ordering

- MEV allows validators/searchers to reorder your transaction, potentially placing theirs before or after to profit.
- Your txn might not execute at the price you expect, especially in DEX trades.


 Can MEV Cause Your Transaction to Fail?

Yes, if a MEV bot front-runs your trade and drains the liquidity or causes slippage, your transaction could:
- Fail due to price impact
- Revert, wasting gas


Impact on DeFi users

- Slippage increases
- Bots might extract arbitrage before you do
- Can result in worse trade execution, especially with large or time-sensitive swaps

 MEV in NFT Context

- MEV bots can front-run NFT mints, minting rare NFTs before regular users.
- They can bulk mint ahead of others by paying high gas and using multiple wallets.
- This leads to:
  - Regular users missing out
  - Gas wars
  - Price spikes immediately after mint

 How Creators Protect Against MEV

- Allowlist & pre-mint access to trusted wallets
- Minting caps per wallet
- Use of commit-reveal schemes (hide mint details until block confirmation)
- Launch on MEV-resistant L2s or chains 

### MEV Solutions

Current Solutions to MEV

1. Flashbots 
- A system that routes transactions privately to miners/validators, bypassing the public mempool.  
- Helps reduce harmful MEV (like front-running) and allows bundling txns for custom ordering.

2. Private Mempools 
- Transactions are submitted directly to a validator without entering the public mempool.  
- Prevents bots from seeing your txn and exploiting it before inclusion.

3. Commit-Reveal Schemes  
- Used in NFT mints and auctions.  
- Step 1: Commit phase, user submits hashed intent  
- Step 2: Reveal phase, user reveals actual input  
- Prevents bots from reacting to live txns.

4. Layer 2s and MEV
- L2s (like Optimism, Arbitrum) batch transactions and submit to L1, limiting MEV exposure.  
- Some L2s are experimenting with fair sequencing or MEV-aware rollups.

 Future Developments & MEV Evolution

1. Proposer-Builder Separation (PBS)
- Separates block proposers from block builders to limit centralized MEV extraction.  
- Helps democratize access to MEV profits.

2. Encrypted Mempools  
- Proposed solutions (like SUAVE) to encrypt txns until they’re finalized, preventing bots from exploiting ordering.

3. Fair Ordering Protocols
- Aim to ensure txns are ordered fairly and deterministically, not based on gas bribes.

4. Debate Around MEV  
- Some argue MEV is unavoidable and can be harnessed safely (e.g., for arbitrage).  
- Others believe it threatens fairness and decentralization, especially if few entities dominate MEV extraction.  

## Key Takeaways

1. Consensus Mechanisms (PoW vs PoS): 
   PoW secures the network using computational work (mining), while PoS relies on validators who stake tokens. PoS is more energy-efficient and enables faster finality compared to PoW.

2. Gas & Transactions:
   Gas is the fee users pay to perform operations on blockchains like Ethereum. Gas cost = gas used × gas price. Complex or high-demand transactions cost more gas. Users can optimize by transacting during low network congestion.

3. Blocks & Confirmations:  
   A block contains a batch of verified transactions. Each new block added increases the confirmation count for previous blocks, making it harder to reverse them. More confirmations mean higher security.

4. Wallet Types (Custodial vs Non-Custodial):  
   Custodial wallets manage private keys for users (e.g., exchanges), offering convenience but less control. Non-custodial wallets (like MetaMask) give users full control and responsibility over their keys and funds.

5. Testnets: Testnets like Sepolia and Mumbai let developers test smart contracts and dApps without using real funds. They simulate real network conditions and are critical for safe development and experimentation.

6. Blockchain Explorers:
   Explorers like Etherscan or Polygonscan allow users to search, verify, and analyze blockchain data, such as wallet balances, transactions, contracts, and gas usage. They're essential for transparency and debugging.

7. MEV (Maximal Extractable Value):
   MEV refers to the extra profit validators or bots can gain by reordering, inserting, or censoring transactions in a block. It impacts fairness and user costs, especially in DeFi and NFT minting. 

## All Sources and References

PoW & PoS

1.https://contabo.com/blog/proof-of-stake-vs-proof-of-work/ 

2.https://www.ledger.com/academy/glossary/proof-of-stake 

3.https://ethereum.org/developers/docs/consensus-mechanisms/pos/ 

4.https://www.openware.com/news/articles/the-evolution-of-consensus-algorithms-from-pow-to-pos-and-beyond 

GAS

 5.https://www.web3.university/tracks/create-a-smart-contract/what-is-gas-and-how-is-it-used 

6.https://www.tokenmetrics.com/blog/what-is-a-gas-fee-and-how-is-it-calculated-complete-guide-for-2025 

BLOCK & CONFIRMATIONS

7. https://www.cube.exchange/what-is/block 

8. https://finchtrade.com/glossary/confirmations 

WALLETS & SECURITY PRACTICES

9.https://www.gemini.com/cryptopedia/crypto-wallets-custodial-vs-noncustodial 

10.https://calebandbrown.com/blog/cold-storage-vs-hot-wallets-understanding-the-best-options-for-secure-crypto/  

11.https://zimperium.com/glossary/crypto-wallet-security

TESTNETS & BLOCKCHAIN EXPLORERS

12.https://www.alchemy.com/overviews/what-are-testnets 

13. https://coinledger.io/learn/blockchain-explorers 

14. https://info.etherscan.com/tag/tutorials/ 

MEV

15.https://www.quicknode.com/guides/ethereum-development/MEV/what-is-mev 

16.https://zerocap.com/insights/research-lab/maximal-extractable-value/ 


Twitter Thread: https://x.com/IamIsrael__1/status/1991132516082721222?t=siqn-BG7Hqwb0P2KeU-0lA&s=19 
