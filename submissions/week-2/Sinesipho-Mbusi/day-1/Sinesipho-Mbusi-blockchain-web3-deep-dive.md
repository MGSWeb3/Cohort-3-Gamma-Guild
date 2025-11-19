# Week 2: Blockchain & Web3 Deep Dive Research (Day 1-3)

**Student Name:** Sinesipho Mbusi  
**Date:** 2025-11-19  
**Tweet Link:** [(https://x.com/symbusi/status/1991123987611492817?s=20)]

---

## Part 1: Consensus Mechanisms Deep Dive

### Proof of Work (PoW) Analysis

#### How PoW Works

- **Mining process:**
  1. Transactions are broadcast to the network and collected into a candidate block by miners.
  2. Miners build a block header containing the previous block hash, Merkle root of transactions, timestamp, difficulty target, and nonce.
  3. Miners repeatedly hash the block header with different nonces aiming to produce a hash below the network difficulty target.
  4. When a miner finds a valid nonce, they broadcast the block to peers.
  5. Nodes validate the block and, if valid, add it to their local chain and propagate it further.
- **Computational problem:** Miners solve a cryptographic puzzle (finding a nonce so the hash has enough leading zeros). This is intentionally hard to compute but easy to verify.
- **Difficulty adjustment:** Networks adjust the difficulty periodically (e.g., Bitcoin every 2016 blocks) to keep block time near a target.
- **Race condition:** If two miners solve simultaneously, the network temporarily forks. Eventually, one chain becomes longer (more cumulative work), and the shorter branch is orphaned.

#### Security Model

- **How PoW prevents attacks:** It requires an attacker to control a majority of the hashing power (>51%) to reverse transactions. This requires immense capital and energy.
- **Economic incentives:** Miners are rewarded with block subsidies and fees. Attacking risks devaluing the currency they are mining and renders their hardware investment useless.

#### Real-World Examples

- **Bitcoin:** Uses SHA-256 mining. Prioritizes security and decentralization over speed.
- **Ethereum (Pre-Merge):** Used Ethash to resist ASIC concentration before switching to PoS.

#### Trade-offs

- **Advantages:** Proven security track record, simple model, strong economic guarantees tied to physical resource expenditure.
- **Disadvantages:** Massive energy consumption, slower finality, risk of hardware centralization in mining farms.

### Proof of Stake (PoS) Analysis

#### How PoS Works

- **Staking process:**
  1. Validators lock up (stake) native tokens to be eligible to propose/validate blocks.
  2. The protocol pseudo-randomly selects validators based on stake size and randomness sources.
  3. Validators attest to blocks; these attestations are aggregated to finalize the chain.
- **Slashing:** A punitive mechanism that destroys a portion of a validator's stake if they act maliciously (e.g., double-signing blocks).

#### Security Model

- **How PoS prevents attacks:** It relies on "Economic Security." An attacker must own 51% of the staked supply to attack the network. If caught, they are "slashed," losing their investment.
- **Finality:** PoS chains often use explicit finality mechanisms (like Casper FFG on Ethereum), making blocks irreversible much faster than PoW.

#### Real-World Examples

- **Ethereum (Post-Merge):** Validators stake 32 ETH.
- **Solana:** Uses a hybrid of PoS and Proof of History (PoH) for high throughput.
- **Cardano:** Uses Ouroboros, a research-driven PoS protocol.

#### Trade-offs

- **Advantages:** ~99.95% lower energy consumption, faster finality, lower hardware entry barriers (no ASICs needed).
- **Disadvantages:** Risk of wealth centralization (rich get richer), "Nothing-at-Stake" theoretical issues (solved by slashing).

### Comparative Analysis

*(See Comparison Tables section at the end of this document)*

### Practical Implications for Creatives

- **NFT Minting Costs:** PoS chains (Ethereum, Solana) generally offer more predictable or lower fees than PoW chains during congestion, though Ethereum Mainnet can still be expensive due to demand.
- **Chain Selection:** - **Store of Value:** PoW (Bitcoin) is historically favored for high-value, long-term assets (Ordinals).
  - **High Volume:** PoS (Solana, Polygon) is better for gaming or low-cost NFT collections due to speed and low fees.

---

## Part 2: Gas, Blocks & Confirmations

### Gas Economics

#### What is Gas?

Gas is the unit that measures the computational work required to execute operations. It decouples resource consumption from the native token's market value.

#### How Gas Pricing Works

- **Gas Limit:** The maximum amount of gas units a user is willing to spend (e.g., 21,000 for a transfer).
- **Gas Price (Gwei):** The cost per unit of gas.
- **The Formula:** `Total Fee = Gas Limit * (Base Fee + Priority Fee)`

#### Gas Optimization Strategies

- **Timing:** Mint or transfer during off-peak hours (often weekends or UTC nights) when network demand is low.
- **Layer 2s:** Use Optimism, Arbitrum, or Base. These rollups process transactions off-chain and batch them, reducing fees by ~90-99%.
- **Batching:** Grouping multiple operations (like listing 10 NFTs) into a single transaction to pay the base fee only once.

### Blocks Structure

#### What is a Block?

A block is a container for a batch of transactions and metadata, cryptographically linked to the previous block.

#### Block Components

- **Header:** Contains the previous block hash, timestamp, Merkle root, and difficulty/nonce.
- **Body:** Contains the list of transactions included in that block.

#### Block Time

The average interval between blocks.

- **Bitcoin:** ~10 minutes.
- **Ethereum:** ~12 seconds.
- **Solana:** ~400 milliseconds.
*Shorter block times improve UX but require more robust hardware for nodes.*

### Confirmations

#### What are Confirmations?

A confirmation count represents the number of blocks added to the chain *after* the block containing your transaction.

- **Significance:** Each confirmation makes it exponentially harder to reverse the transaction.
- **Standard:** 1 confirmation is usually enough for small payments; exchanges often require 6-12 confirmations for large deposits to ensure finality.

---

## Part 3: Wallet Security & Types

### Custodial vs Non-Custodial Wallets

#### Custodial Wallets (Exchanges)

- **Definition:** A third party (Coinbase, Binance) holds the private keys.
- **Pros:** Easy account recovery (Forgot Password), fiat on-ramps.
- **Cons:** Counterparty risk (if the exchange fails, you lose funds). "Not your keys, not your crypto."

#### Non-Custodial Wallets (Self-Custody)

- **Definition:** The user holds the private keys/seed phrase.
- **Pros:** Full control, censorship resistance, direct interaction with DeFi.
- **Cons:** No customer support. If you lose your seed phrase, the funds are gone forever.

### Hot vs Cold Wallets

#### Hot Wallets (Software)

- **Definition:** Connected to the internet (MetaMask, Phantom).
- **Best For:** Daily transactions, connecting to DApps, minting.
- **Risk:** Vulnerable to malware, screen scrapers, and phishing sites.

#### Cold Wallets (Hardware)

- **Definition:** Offline devices (Ledger, Trezor) that keep keys air-gapped.
- **Best For:** Long-term storage, high-value assets.
- **Security:** Keys never leave the device; physical button presses are required to sign transactions.

### Security Best Practices

1. **Seed Phrase Hygiene:** Write it on paper or metal. NEVER store it digitally (cloud, screenshots, email).
2. **Phishing Awareness:** Always verify URLs. Never click links in DMs or emails claiming "airdrops."
3. **Burner Wallets:** Use a hot wallet with small funds for minting and a cold wallet for storage.
4. **Revoke Allowances:** Regularly use tools like Revoke.cash to remove permission from old smart contracts.
5. **Verification:** Don't trust the UI blindy; check the transaction details on a hardware wallet screen before confirming.

---

## Part 4: Testnets & Blockchain Explorers

### Testnets

#### What are Testnets?

Sandbox environments (like Sepolia for Ethereum or Amoy for Polygon) that mimic mainnet behavior but use valueless currency. They allow developers to test code without financial risk.

#### Hands-on Experience

I successfully connected my MetaMask wallet to the Sepolia testnet. I visited the Google Cloud Web3 Faucet, entered my wallet address, and received 0.05 Sepolia ETH. I then sent 0.01 Sepolia ETH to a random test address to observe the gas fees. The transaction was confirmed within 12 seconds, and I viewed the details on Sepolia Etherscan, noting the significantly lower gas pressure compared to Mainnet.

### Blockchain Explorers

#### What are Explorers?

Tools like Etherscan or Solscan that index the blockchain, allowing users to search for transactions, addresses, and smart contract code.

#### Key Features Analyzed

- **Transaction Hash:** The unique receipt ID for every action.
- **Input Data:** The field showing *what* function was called (e.g., `Mint`, `Transfer`, `Swap`). Reading this is crucial for spotting scams.
- **Status:** Visual confirmation (Green/Red) of whether a transaction succeeded or failed.

---

## Part 5: MEV (Maximal Extractable Value)

### Understanding MEV

MEV is the profit miners/validators/bots extract by reordering, including, or excluding transactions within a block. The "Mempool" (waiting area) is a "Dark Forest" where bots monitor for profitable trades.

### Impact on Users

- **Sandwich Attacks:** A bot sees you buying a token, buys it before you (raising the price), and sells it immediately after you. You get a worse price; they profit.
- **Front-Running:** Bots pay higher gas fees to jump ahead of you in the line to snag NFT mints or arbitrage opportunities.
- **Gas Wars:** MEV bots bidding up gas prices congest the network for regular users.

### MEV Solutions

- **Flashbots:** A service that allows users/searchers to send transactions directly to validators via a private channel, bypassing the public mempool and preventing front-running.
- **Private RPCs:** Wallet settings that route transactions privately to avoid detection by bots.

---

## Part 6: Transaction Analysis

 See my separate transaction analysis document: `Sinesipho-Mbusi-transaction-analysis.md`

---

## Comparison Tables

### PoW vs PoS Comparison

| Feature | Proof of Work (PoW) | Proof of Stake (PoS) |
| :--- | :--- | :--- |
| **Security Model** | Computational work (Energy/Hashpower) | Economic stake (Financial Commitment) |
| **Energy Consumption** | High (Bitcoin consumes ~150 TWh/yr) | Low (~99.95% more efficient than PoW) |
| **Transaction Speed** | Moderate (Example: BTC ~7 TPS) | High (Example: Solana ~65k TPS) |
| **Decentralization** | Risk of hardware centralization (Mining farms) | Risk of wealth centralization (Stake pools) |
| **Entry Barrier** | High (Expensive hardware & electricity) | Lower (Token capital + standard hardware) |
| **Cost Structure** | OPEX heavy (Electricity bills) | CAPEX heavy (Locking up capital) |
| **Scalability** | Low (requires Layer 2s to scale) | High (supports sharding/parallel processing) |

### Custodial vs Non-Custodial Wallets

| Feature | Custodial (Exchange) | Non-Custodial (Self-Custody) |
| :--- | :--- | :--- |
| **Security** | Vulnerable to exchange hacks (e.g., FTX) | Vulnerable to user error (Phishing) |
| **Convenience** | High (Forgot password recovery available) | Medium (Must manage own keys) |
| **Control** | Low ("Not your keys, not your crypto") | High (Total sovereignty) |
| **Recovery** | Managed by customer support | Impossible if Seed Phrase is lost |
| **Use Cases** | Onboarding, Fiat on-ramps | DeFi, NFTs, Long-term storage |

### Hot vs Cold Wallets

| Feature | Hot Wallet (Software) | Cold Wallet (Hardware) |
| :--- | :--- | :--- |
| **Security Level** | Lower (Connected to Internet) | Highest (Air-gapped / Offline) |
| **Convenience** | High (Browser extensions, Mobile apps) | Low (Requires physical device to sign) |
| **Cost** | Free (e.g., MetaMask, Phantom) | $50 - $200+ (e.g., Ledger, Trezor) |
| **Best For** | Active trading, Minting, DApps | Long-term "Vault" storage |

---

## Key Takeaways

1. **Consensus Evolution:** The industry is shifting from energy-intensive Proof of Work (security via physical cost) to Proof of Stake (security via economic cost) to address environmental concerns and scalability.
2. **Gas is a Market:** Gas prices are not fixed; they are determined by supply and demand for block space. Understanding `Gas Limit` vs. `Gas Price` is essential for avoiding failed transactions and overpayment.
3. **The Trilemma:** Every blockchain makes trade-offs between Security, Scalability, and Decentralization. No single chain has perfectly solved all three at the base layer yet.
4. **Wallet Hygiene:** The distinction between Hot and Cold wallets is critical. A best practice is to use a "Burner" hot wallet for minting and a Cold wallet that never interacts with smart contracts for storage.
5. **The Dark Forest:** The Mempool is adversarial. MEV bots actively monitor unconfirmed transactions to sandwich or front-run users, acting as an "invisible tax" on DeFi trading.
6. **Don't Trust, Verify:** Blockchain explorers like Etherscan are the ultimate source of truth. Reading input data helps identify malicious transactions that UI front-ends might hide.

---

## All Sources and References

1. **Ethereum Foundation:** *Consensus Mechanisms* (ethereum.org/en/developers/docs/consensus-mechanisms/)
2. **Investopedia:** *Proof of Work vs. Proof of Stake* (investopedia.com)
3. **Consensys:** *What is MetaMask and How to Use It* (consensys.net/blog)
4. **Flashbots:** *The Ethereum MEV Ecosystem* (docs.flashbots.net)
5. **Ledger Academy:** *Hot Wallet vs. Cold Wallet* (ledger.com/academy)
6. **Etherscan:** *Sepolia Testnet Explorer* (sepolia.etherscan.io)


[https://x.com/symbusi/status/1991123987611492817?s=20]