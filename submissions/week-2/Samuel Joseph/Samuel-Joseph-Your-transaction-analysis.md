## Part 6: Transaction Analysis

# 🔗 Blockchain Transaction Analysis Assignment

## Objective
To analyze a real-world blockchain transaction in detail, utilizing a block explorer to document and interpret its key characteristics.

## Chosen Transaction (Option B: Famous Transaction)

This analysis focuses on the final on-chain transfer of the record-breaking NFT, **Beeple's "Everydays: The First 5000 Days"**, confirming the sale's successful execution on the Ethereum network.

| Detail | Value |
| :--- | :--- |
| **Transaction Hash (TXID)** | `0x32c18080c325c8421bc2775f0a35978a3c8699b662283e583c9146522c7a0210` |
| **Explorer Link (Etherscan)** | [View on Etherscan](https://etherscan.io/tx/0x32c18080c325c8421bc2775f0a35978a3c8699b662283e583c9146522c7a0210) |

---

## 📋 Analysis Checklist Documentation

### I. Basic Information

| Detail | Value |
| :--- | :--- |
| **Status** | **✅ Success** |
| **Timestamp** | Mar-12-2021 00:39:41 AM +UTC |
| **Block Number** | 11977937 |
| **Number of Confirmations** | Millions (Fully confirmed) |

### II. Parties Involved

| Detail | Address | Type | Contract Name (If Applicable) |
| :--- | :--- | :--- | :--- |
| **Sender Address** | `0x19945037E90B2E15848834d85206F75231908709` | **Contract** (Auction/Escrow) | N/A |
| **Receiver Address** | `0xc6b0562605D35eE710138402B878ffe6F2E23807` | **EOA** (Buyer's Wallet - MetaKovan's Metapurse) | N/A |
| **NFT Contract** | `0x2a46...3072756` (Targeted Contract) | **Contract** | Everydays (ERC-721) |

### III. Value & Fees

| Detail | Value | Notes |
| :--- | :--- | :--- |
| **Amount of ETH/Tokens** | **0 ETH** | This transaction is the **NFT transfer**, not the payment. |
| **Transaction Fee (ETH)** | **0.00392095817887752 ETH** | Paid to the miner/validator. |
| **Transaction Fee (USD)** | **~ $7.78 USD** | Based on the ETH price at the time of the block (~$1,984). |
| **Gas Price (Gwei)** | **10 Gwei** | The payment per unit of gas. |
| **Gas Used** | **392,095** | The actual gas consumed by the transaction. |
| **Gas Limit** | **1,000,000** | The maximum gas the sender was willing to use. |
| **Total Cost Breakdown** | **Gas Used $\times$ Gas Price = Fee** | $392,095 \times 10 \text{ Gwei} = 0.00392 \text{ ETH}$ |

### IV. Technical Details

* **Method Called:** `Transfer` (This is an internal function call within the NFT's smart contract logic, triggered by the auction contract).
* **Input Data Analysis:** The input data is the encoded call instructing the `Everydays` contract to change the ownership record of the specific **Token ID 40913** from the auction contract to the buyer's EOA.
* **Tokens Transferred:**
    * **1 NFT:** *Everydays: The First 5000 Days (EVERYDAYS)*
    * **Token Standard:** ERC-721
    * **Token ID:** 40913
* **Events Emitted:** A standard ERC-721 **`Transfer`** event was emitted, which is the official log entry recording the change in ownership of Token ID 40913 to the new receiver's address.

---

## 🔍 Detailed Analysis

### What was this transaction for?
This transaction served as the **final, immutable confirmation** of the sale of Beeple's "Everydays: The First 5000 Days" NFT. It executed the transfer of the ERC-721 token from the controlling auction contract to the buyer's wallet (Metapurse), finalizing the record-breaking $69.3 million acquisition on the blockchain.

### Was the gas price reasonable?
**Yes, highly reasonable.** At **10 Gwei**, the gas price was modest for the time (March 2021). It was not an urgent transaction, as the payment had already been secured. The resulting fee of only **~ $7.78 USD** for a transaction worth tens of millions of dollars is incredibly efficient.

### Could the sender have saved on gas?
**No, not significantly.** The *Gas Used* was **392,095**, which is reasonable for a complex contract interaction involving an NFT transfer. The fee optimization would be negligible relative to the total value of the sale, and attempting to go much lower than 10 Gwei could have delayed the block confirmation unnecessarily.

### What can you learn about the sender from their history?
The sender is a **Smart Contract** address designed specifically to manage the auction and distribution of this NFT. Its history would show interactions primarily limited to the `Everydays` NFT contract, confirming its role as the custodian/escrow service for the sale.

### What can you learn about the receiver?
The receiver is an **Externally Owned Account (EOA)** linked to **Metapurse (MetaKovan)**. This address is a known "whale" in the crypto and NFT space. Its history reveals extensive involvement in high-value digital asset purchases and DeFi activity, confirming the buyer as a major and influential entity within the Ethereum ecosystem.
