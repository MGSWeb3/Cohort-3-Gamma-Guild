
  Number 1:

Bitcoin

Bitcoin, launched in 2009 by Satoshi Nakamoto, is the first decentralized cryptocurrency and remains the most valuable blockchain with a market cap exceeding $2.37 trillion as of 2024.

Nodes and Network:

Bitcoin operates on a peer-to-peer network where each node maintains an identical copy of the blockchain
Nodes validate transactions and blocks according to Bitcoin's protocol rules
The network prioritizes security and decentralization over transaction speed

Clients:

Bitcoin Core is the original reference implementation
Each client must adhere to Bitcoin's protocol rules to be considered valid
Nodes running client software can validate transactions, store the blockchain, and participate in consensus

Consensus Mechanism:

Proof of Work (PoW): Bitcoin uses an energy-intensive PoW consensus mechanism where miners solve complex mathematical puzzles to validate transactions and create new blocks

Block rewards: Currently 6.25 BTC per block (as of 2024), with halvings occurring every four years

Transaction fees provide additional incentives for miners

Processes approximately 7 transactions per second (TPS)

2)

Ethereum

Launched in 2015 by Vitalik Buterin, Ethereum is the second-largest cryptocurrency with a market cap of $513 billion. It pioneered smart contracts and decentralized applications (dApps).

Nodes and Network:

Since "The Merge" in September 2022, Ethereum nodes require both an execution client and a consensus client
This dual-client architecture separates responsibilities between transaction execution and consensus validation
Over 1.6 million daily transactions are processed across the network

Clients:

Execution clients: Handle transaction processing and state management

Consensus clients: Manage the Proof of Stake consensus mechanism

Both clients must work together for a node to function properly

Consensus Mechanism:

Proof of Stake (PoS): Ethereum transitioned from PoW to PoS in 2022, reducing energy consumption by 99.95%

Validators stake ETH to participate in block validation

Minimum stake: 32 ETH required to become a validator

Staking rewards: 4-6% annual percentage yield (APY)

Processes 30+ transactions per second on Layer 1

Uses a fork-choice mechanism to select the "heaviest" chain based on validator votes weighted by staked ETH

3)

Solana

Launched in 2020 by Anatoly Yakovenko, Solana is designed for high performance and scalability, processing over 2,600 transactions per second with average fees of $0.02.

Nodes and Network:

Operates on a monolithic, single-layer architecture where all core functions are handled within one blockchain

Over 1,700 validators ensure network distribution

Has experienced network outages on multiple occasions, though stability has improved

Clients:

Uses a unified client architecture rather than separate execution and consensus clients and all nodes run the same software to participate in the network

Consensus Mechanism:

Proof of History (PoH) + Proof of Stake (PoS): Unique hybrid consensus mechanism

- PoH creates a historical record proving events occurred in a specific sequence

- PoS validators then confirm transactions based on this timestamp

- Can theoretically handle up to 50,000+ TPS

- Upcoming Firedancer upgrade promises 1 million TPS

- Energy-efficient: Single transaction uses energy equivalent to a few Google searches

4)

Cardano

Launched in 2017 by Charles Hoskinson (Ethereum co-founder), Cardano emphasizes a research-driven approach with peer-reviewed development and currently trades around $1.01.

Nodes and Network:

Over 3,000 separate validators operate on the network

High Nakamoto coefficient score indicating strong decentralization

Perfect uptime since launch with no network outages

Clients:
Nodes run Cardano client software to participate in validation

Uses Plutus smart contract programming language written in Haskell

Consensus Mechanism:
Ouroboros Proof of Stake: First large blockchain based on peer-reviewed PoS protocol

Processes approximately 1,000 transactions per second

Two-layer architecture:

Cardano Settlement Layer (CSL): Handles token transfers and peer-to-peer transactions

Computation Layer: Manages smart contracts and dApps

Energy-efficient with minimal computational resource requirements

Validators stake ADA tokens to participate in consensus


Number 2

Distributed Ledger Technology vs. Blockchain

Distributed Ledger Technology (DLT)

A distributed ledger is a database that is replicated, shared, and synchronized across multiple sites, locations, or institutions without a central administrator.

Key Characteristics are:

1.Decentralized data storage across multiple nodes
2. No single point of failure
3.Requires consensus mechanism to validate transactions
4. Can use various data structures, not necessarily blocks
5.May be centralized or decentralized in governance

Examples of DLT Beyond Blockchain:

1.Hashgraph: Uses the Gossip protocol for consensus, offering fast and secure transaction validation

2.Holochain: Agent-centric structure where each node operates on its own chain

3.Tempo/Radix: Uses ledger partitioning (sharding) with events ordered by occurrence rather than timestamp

4. Directed Acyclic Graph (DAG):** Alternative structure without traditional blocks

Blockchain Technology

Blockchain is a specific type of distributed ledger that organizes data into cryptographically linked blocks arranged in a sequential chain.

Key Characteristics include:

1.Data packaged into blocks with unique cryptographic hash links

2.Blocks arranged in chronological, immutable sequence

3.Uses consensus mechanisms like PoW or PoS to add new blocks

4.All transactions encrypted before being added

5.Completely decentralized with no central authority

6.Smart contract capability (in some blockchains)

Key Differences

| Feature | Distributed Ledger Technology | Blockchain |

Data Structure: 

Distributed Ledger: Can use any database structure; not limited to blocks 

Blockchain: Specifically uses chain of cryptographically linked blocks 

Sequence: 

Distributed Ledger: No required sequence for data arrangement

Blockchain: Strict chronological block sequence required 

Consensus:

Distributed Ledger: Various consensus methods possible

Blockchain: Typically PoW, PoS, or Byzantine Fault Tolerance

Architecture:

Distributed Ledger: Generally centralized or semi-decentralized

Blockchain: Fully decentralized network 

Smart Contracts:

Distributed Ledger: Not inherent to DLT 

Blockchain: Available in many blockchain implementations

Scalability:

Distributed Ledger: Generally more scalable 

Blockchain: May have scalability challenges due to full decentralization 

However, all blockchains are distributed ledgers, but not all distributed ledgers are blockchains. Blockchain is a subset of DLT with specific architectural requirements.



Number 3. 

Fungible Tokens vs. Non-Fungible Tokens (NFTs)

Fungible Tokens

Fungible tokens are digital assets that are interchangeable and possess equal value, making each unit identical to every other unit of the same token.

Key Characteristics are:

- Interchangeable on a 1:1 basis
- Divisible into smaller units
- Each unit has identical value and properties
- Used primarily as medium of exchange or store of value
- Follow standardized protocols (ERC-20, BEP-20, TRC-20)

Token Standards:

- ERC-20: Ethereum standard introduced in 2015 for fungible tokens
- BEP-20: Binance Smart Chain standard
- TRC-20: TRON blockchain standard

Real-World Examples of Fungible Tokens

1: Bitcoin (BTC)

- First cryptocurrency launched in 2009
- Capped supply of 21 million coins
- Used as digital currency and store of value ("digital gold")
- Each bitcoin is identical and can be exchanged 1:1
- Divisible to 8 decimal places (smallest unit: 1 satoshi = 0.00000001 BTC)

2: Ethereum (ETH)

- Native token of Ethereum blockchain
- Used to pay for gas fees and computational services
- Each ETH is identical in value and utility
- Used in DeFi protocols, NFT purchases, and smart contract execution
- Unlimited supply but with controlled emission rate

3: USD Coin (USDC)

- Stablecoin pegged 1:1 to US dollar
- Launched on Ethereum, now available on Polygon, Base, Avalanche
- Backed by cash reserves and short-term government securities
- Maintains stable value through audited reserves
- Used extensively in DeFi for liquidity pools and lending protocols

4: Tether (USDT)

- First major stablecoin, launched before USDC
- Pegged to US dollar for price stability
- Available on 12+ blockchain platforms
- High trading volume compared to other stablecoins
- Used for trading pairs and as stable store of value

5: Basic Attention Token (BAT)

- Utility token used in Brave browser ecosystem
- Rewards users for viewing advertisements
- Can be tipped to content creators
- Example of utility token providing access to specific services
- Each BAT token is identical and interchangeable


Non-Fungible Tokens (NFTs)

NFTs are unique digital identifiers recorded on a blockchain that certify ownership and authenticity of digital or physical assets. Each NFT is distinct and cannot be exchanged on a one-to-one basis.

Key Characteristics:

- Unique and non-interchangeable
- Indivisible (cannot send fractions)
- Contains unique identification code and metadata
- Ownership recorded on blockchain
- Can represent digital or physical assets
- Smart contract functionality for royalties

Token Standard:
- ERC-721: Introduced in 2018 by William Entriken, established standard for NFTs on Ethereum
- ERC-1155: Enables semi-fungibility on Ethereum

Real-World Examples of NFTs

1: CryptoPunks

- Launched June 2017 by Larva Labs
- Collection of 10,000 unique pixel art characters
- Includes humans, zombies, and apes with varying rarity
- One of the most commercially successful NFT projects
- Established NFTs as collectible digital art
- Individual punks have sold for millions of dollars

2: Bored Ape Yacht Club

- Collection of 10,000 unique cartoon primate NFTs
- Generated over $2 million in single-day sales
- Created robust "avatar club" community
- Provides membership benefits and exclusive access
- Owners include celebrities and major brands
- Example of NFTs as status symbols and community membership

3: Nike CryptoKicks

- Patent filed in 2019 for NFT-based authentication
- Verifies authenticity of physical Nike products
- Provides virtual version of shoe to customer
- Links physical and digital ownership
- Prevents counterfeiting through blockchain verification
- Example of NFTs for product authentication

4: Beeple's "Everydays: The First 5000 Days"

- Digital art collage sold for $69.3 million via Christie's auction (March 2021)
- One of the highest-value NFT art sales
- Demonstrated mainstream acceptance of digital art ownership
- Artist retains copyright, buyer owns NFT proving authenticity
- Revolutionized digital art market

5: NBA Top Shot

- Digital basketball collectible moments
- Licensed partnership with NBA
- Users collect and trade video highlights as NFTs
- Combines sports fandom with digital collecting
- Generated over $700 million in sales
- Example of NFTs in sports memorabilia

6: Decentraland Virtual Real Estate

- NFTs representing virtual land parcels in metaverse
- Owners can build, monetize, and sell virtual property
- Land parcels have sold for hundreds of thousands of dollars
- Example of NFTs representing virtual assets
- Enables digital property ownership and development

5 Comparing Fungible vs. Non-Fungible Tokens

| Feature | Fungible Tokens | Non-Fungible Tokens (NFTs) 

Uniqueness:

Fungible Tokens: Identical and duplicable 

NFTs: Each token is unique with distinct properties 

Interchangeability: 

Fungible Tokens: Can be exchanged 1:1 without value loss

NFTs: Cannot be exchanged 1:1; each has unique value 

Divisibility:

Fungible Tokens: Easily divisible into smaller units 

NFTs: Indivisible; only whole tokens can be transferred 

Value: 

Fungible Tokens: Consistent market value per unit

NFTs: Individual value based on unique characteristics 


Use Cases: 

Fungible Tokens: Currency, payments, DeFi, utility access

NFTs: Digital art, collectibles, gaming items, authentication |


References

1. Morais, J.P. (2024). "Learn Ethereum in 2024. #4. Nodes and clients." Medium. https://jpmorais.medium.com/learn-ethereum-in-2024-4-nodes-and-clients-88b17a8dd736

2. MDPI (2024). "Blockchain Consensus Mechanisms: A Bibliometric Analysis (2014–2024)." Information Journal. https://www.mdpi.com/2078-2489/15/10/644

3. Ethereum.org (2024). "Consensus mechanisms." https://ethereum.org/developers/docs/consensus-mechanisms/

4. Taylor & Francis Online (2024). "Consensus-based methods for distributed systems, blockchain, and voting: a survey." https://www.tandfonline.com/doi/full/10.1080/24751839.2024.2416728

5. Visa (2024). "What are Consensus Mechanisms?" https://usa.visa.com/solutions/crypto/consensus-mechanisms.html

6. Nature Scientific Reports (2024). "An enhanced consensus algorithm for blockchain." https://www.nature.com/articles/s41598-024-68120-4

7. TheServerSide (2024). "Know how and when to use blockchain vs. distributed ledgers." https://www.theserverside.com/tip/Know-how-and-when-to-use-blockchain-vs-distributed-ledgers

8. 101 Blockchains (2023). "Blockchain vs. Distributed Ledger Technology: A Detailed Guide." https://101blockchains.com/blockchain-vs-distributed-ledger-technology/

9. Wikipedia (2025). "Non-fungible token." https://en.wikipedia.org/wiki/Non-fungible_token

10. U.S. Government Accountability Office (2022). "Science & Tech Spotlight: Non-Fungible Tokens (NFTs)." https://www.gao.gov/products/gao-22-105990


11. World Economic Forum (2023). "What are non-fungible tokens (NFTs) and are they useful?" https://www.weforum.org/stories/2023/10/nfts-non-fungible-tokens-blockchain/


12. Trust Wallet (2024). "Fungible vs Non-Fungible Tokens: Explained." https://trustwallet.com/blog/nft/fungible-vs-non-fungible-tokens-explained


13. Ledger Academy (2025). "Solana vs. Ethereum: Performance, Architecture, and Potential." https://www.ledger.com/academy/topics/crypto/solana-vs-ethereum-performance-guide


14. MEXC Blog (2025). "Ethereum Vs Bitcoin, Solana, Cardano, Polkadot, XRP, Litecoin, WETH." https://blog.mexc.com/ethereum-vs-bitcoin-solana-cardano-polkadot-xrp-litecoin-weth/


15. Precedence Research (2025). "Non-Fungible Token Market Size to Hit USD 703.47 Bn by 2034." https://www.precedenceresearch.com/non-fungible-token-market
