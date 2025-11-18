Success Adaugo Nnadozie
7th November 2025


Part 1: Blockchain Infrastructure research

Bitcoin

Node Types

Bitcoin has 3 nodes types:
Full node which stores and valideates the entire blockchain. It enforces consensus rules, relays transactions or blocks to other nodes. Basically forms the backbone of a blockchain's security, decentralization, and data integrity.

The requirements to run a full node include: 350GB disk space on a desktop or laptop, 1gb RAM, Operating system of Windows 7/8x/10, Mac OS X, Linux

Simplified Payment Verification (SPV) or Light node which verifies transactions using block headers only. It doesn't download the entire blockchain like the full node. It relies on full nodes through mekle proofs which shows that a transaction is included in a block header without having to download the entire block. They are faster than the full nodes and can be used on mobile 

The requirements to run a light node are, any phone or PC, small storage, Low CPU.

Mining nodes also validate transactions but they do so by solving complex mathematical puzzles to add new blocks to a blockchain. Unlike the other nodes that are responsible for maintaing and validating the entire history of the blockchain, mining nodes focus on adding new blocks to the blockchain.

The requirements to run a mining node are mining software and Application Specific Integrated Circiut hardware. (ASIC)

Client Implementations

There are different client softwares in bitcoin and they are classified based on the nodes the run on.
Full node clients such as Bitcoin core, bitcoind, bitcoin knots, btcd
SPV clients such as Electrum and Bluewallet
Remote clients such as My wallet
Stateless clients

But the major 2 are Bitcoin core and Electrum, with Bitcoin core being the most popular because it defines and enforces the rule of bitcoin protocol by independently verifying every transaction and block.

The key differences between bitcoin core and electrum includes
Bitcoin Core                                            Electrum
Used on full node                                       Used on light node
It downloads and verifies the entire blockchain         Downloads only block headers
Doesn't depend on any 3rd party for verification        Depends on a 3rd party for verification
Slow                                                    Fast
Buile with C++                                          Built with python

Consensus Mechansisms

Bitcoin uses proof of work as its consensus mechanism.
In PoW, miners compete to solve a complex mathematical problem to validate transactions and add new blocks to the blockchain. The first miner to find the correct hash broadcasts it to other nodes. The other nodes verify it and add the new block to their copy of the blockchain. The first miner receives a reward in the form of newly created bitcoins and any transaction fees included in that block.

Its advantages are 
Its the longest standing consensus mechanism so its tested and trusted
Has a high security rate
Decentralization by allowing any of the miners to participate in mining, giving the power to manage transactions to many people.

Its disadvantages are 
It consumes a high level of energy
It is expensive
Has slow transaction speeds

Block validators/Producers

Miners proposes and approves new blocks. Using the PoW, the first miner to find the correct hash proposes and approves the new block.

The requrirememts to be a miner are specialized hardware like the ASIC, stable internet connection, mining software, and low cost electricity

The first miner to solve the complex problem is rewarded with a set amount of newly minted bitcoin that is halved approximately every 4 years. He also collects all the transaction fees of all the transactions made in that block.

There's no direct penalty for malicious behaviour but consensus is designed to make sure that any form of malicious behaviour is unprofitable. But if malicious behaviour is detected, the other nodes will immediately reject the node and in the long run they could lose their reputation and resources.
Who proposes and approves new blocks? (Miners, Validators, Block Producers, Collators, etc.)
What are the requirements to become a validator/miner?
What incentives and rewards do they receive?
What penalties exist for malicious behavior?

Performance metrics

The average block time is the time it takes to produce a new block on the blockchain and in bitcoin it is every 10 minutes.

While a transaction is added to a block after 10 minutes, its not final until 30 to 60 minutes later

The maximum transaction per second that bitcoin does is 

Sources
https://bitcoin.org/en/bitcoin-core/
https://developer.bitcoin.org/devguide/index.html

Ethereum 

Node Types

Ethereum has 3 types of nodes
Full node which stores a complete copy of the most recent blockchain data. It keeps only the last 128 blocks. 
It also validates all transactions and blocks.
It executes smart contracts
It provides data for light nodes
And it maintains the integrity of the blockchainby ensuring adherence to network rules.

The recommended specifications for running a full node includes Fast CPU with 4+ cores, 16 GB+ RAM, Fast SSD with 2+TB, 25+ MBit/s bandwidth

Archive nodes are specialized full nodes that stores all the data on the blockchain from its conception till date and even onwards. It is used for complex queries of past transactions. It's also used for data analysis.

The requirements for running an archive node includes 8+ core CPU, 64GB+ RAM, 10TB+ Enterprise NVMe SSD (size rapidly growing, can reach 16TB+), 100+ Mbps bandwidth.

Light nodes, same as bitcoin, they store only block headers and requests specific data from the full nodes when needed. The requirement for running a light node is small compared to full and archive nodes. It can run on low power devices 

Validator nodes which are a type of full node that is specifically used by stakers to participate in the proof of stake consensus mechansim. The requirement to run a validator node is similar to that of a full node but it also requires high upkeep and stable power and internet connection.

Client Implementations

There are 2 major clients in the ethereum blockchain:
Execution clients which processes transactions and manages the ethereum virtual machine (EVM) E.g Geth, Nethermind, Erigon, Besu

Consensus cients which manages the proof of stake consensus mechansim and block validation E.g Lighthouse, Prysm, Teku

The most popular client on ethereum is Geth(Go Ethereum) because it is the longest standing client and is known for its stability and reliability. It is built on Go

Consensus Mechansisms

Ethereum uses the Proof of Stake consensus mechanism
Validators who are the nodes in the network stake a mininum of 32ETH into a smart contract on the network. The algorothm randomly selects a validator to propose the next block of transacctions. Other validators are also randomly assigned to vote on the validity of that block after it has been proposed. If enough validators agree that the proposed block is valid, it is added to the blockchain.

Advantages
It is still decentralized
High security
Saves energy
Faster block time

Disadvantages
Capital lock up
Requires expertise

Block validators/Producers

Validators proposes and approves new blocks

To become a validator, one must stake a minimum of 32ETH as collateral. He must also run a full ethereum node.

The validator selected to propose a block earns a portion of the transaction fees within that block
Other validators earn from correctly validating a proposed block
some also earn by strategicaly ordering transactions withing the blocks they propose to maximize profit

The penalty for malicious behaviour is slashing where a portion of the staked ETH is immediately removed on suspicious behaviour and inactivity leaks where a validator that goes offline for a long amount of time slowly loses small amounts of their staked ETH

Performance metrics

Average block time on ethereum is 12 sdconds

Time until transaction finality is 5 minutes 

Maximum transactions per second (TPS) is 12 to 20 TPS

Sources
https://www.quicknode.com/guides/ethereum-development/getting-started/ethereum-clients-explained#:~:text=Node%20Types:%20Full%2C%20Archive%2C%20and%20Light%20Nodes%E2%80%8B&text=While%20it%20maintains%20the%20full,recent%20128%20blocks%20by%20default.
https://ethereum.org/developers/docs/consensus-mechanisms/pos/?utm_source= 

Solana

Node Types
What types of nodes exist in this blockchain?
What is the role and function of each node type?
What are the hardware and software requirements to run each node type?

Client Implementations
What are the different client software available for this blockchain?
List at least 2 clients and explain their key differences
What programming languages are they built with?
Which client is most popular and why?

Consensus Mechansisms

What consensus mechanism does this blockchain use?
How does this consensus mechanism work?
What are its advantages and disadvantages?

Block validators/Producers

Who proposes and approves new blocks? (Miners, Validators, Block Producers, Collators, etc.)
What are the requirements to become a validator/miner?
What incentives and rewards do they receive?
What penalties exist for malicious behavior?

Performance metrics

Average block time
Time until transaction finality
Maximum transactions per second (TPS)

Sources

Avalanche

Node Types
What types of nodes exist in this blockchain?
What is the role and function of each node type?
What are the hardware and software requirements to run each node type?

Client Implementations
What are the different client software available for this blockchain?
List at least 2 clients and explain their key differences
What programming languages are they built with?
Which client is most popular and why?

Consensus Mechansisms

What consensus mechanism does this blockchain use?
How does this consensus mechanism work?
What are its advantages and disadvantages?

Block validators/Producers

Who proposes and approves new blocks? (Miners, Validators, Block Producers, Collators, etc.)
What are the requirements to become a validator/miner?
What incentives and rewards do they receive?
What penalties exist for malicious behavior?

Performance metrics

Average block time
Time until transaction finality
Maximum transactions per second (TPS)

Sources


Part 2: Distributed ledger vs blockchain

All blockchains are distributed ledgers but not all distributed ledgers are blockchains

1. What is a distributed ledger technology (DLT)?
DLT is a system that recors transactions and infomation across multiple independent computers forming a network, so that data is stored simultaneously and is verified by the network.

The core characteristics of DLT are:
Transparency: All independent computers that form the network has access to the same data, so no one can hide anything, and no one can add anything.
Decentralization: It takes authority from one person's hand and shares it to different people. Everyone has a say making the system more walled off from attacks
Reliability: Once data has been added to the ledger, it is almost impossible to alter or delete it making anything in the DLT unchangeable and therefore reliable
Consensus mechanisms: The system uses to specific protocols to agree on the validity of new data.

The problems DLT solves are:
Eliminates 3rd parties in data handling
Reduces fraud and tampering of data
Centralization
Increases accessibility
Increases efficiency and speed

Sources
https://www.investopedia.com/terms/d/distributed-ledger-technology-dlt.asp#:~:text=Key%20Takeaways,as%20complexity%20and%20scalability%20remain.

2. What Makes a Blockchain Unique?**
   - What specific features make blockchain a type of DLT?
   - How does the chain structure work?
   - Why is it called a "blockchain"?

2. Blockchain is a type of DLT, its special features include:
Its use of blocks: data is stored as blocks
Crytographic chaining: and each block is linked to its previous and next one crytographically
Immutabilit: Because of this cryptographic linking of, altering one block would require altering all subsequent blocks in the chain, which is infeasible.

This is how the chain structure works:
Transactions are made and added together to form a block. The block is then validated by independent nodes, that is they make sure that all the transactions in the block are valid through a consensus mechanism. Once the block is validated, it is sealed a unique digital fingerprint called a block header hash that is generated from the blocks data and the hash of the previous block. The hash is then entered and added to the next block as it comes, and so on. This chaining, that is addding of blocks to blocks, is how blockchain is formed.

It is called a blockchain because data is stored in blocks and those blocks are chained together.

Source
https://www.investopedia.com/terms/b/blockchain.asp#:~:text=You%20might%20be%20familiar%20with,process%2C%20depending%20on%20the%20blockchain.

3. Key Differences**
   - What are the technical differences between general DLT and blockchain?
   - Compare data structure, consensus requirements, and architecture
   - Create a comparison table

3. The technical differences between general DLT and blockchain includes:
The main difference between blockchain and DLT is that blockchain is a specific structure of DLT that organizes data in blocks instead of any other way. DLT is a much broader system that also includes hashgraphs, DAGs etc

| Feature | Blockchain | Non-Blockchain DLT Example |
|---------|------------|---------------------------|
| Data Structure | Joins data together to form blocks | |
| Consensus Mechanism | Uses mechansims like PoW or Pos to validate  | |
| Scalability | | |
| Energy Efficiency | | |
| Use Cases | | |


4. Non-Blockchain DLT Examples**
   - Research and identify at least 3 distributed ledger technologies that are NOT blockchains
   - Explain how each one works differently from blockchain
   - What are their use cases?
   - What are their advantages over traditional blockchains?

DLT examples include:
Hedera Hashgraph: 

IOTA Tangle


git add .
git commit -m "chore: submit week 1 day 1 blockchain research assignment"
