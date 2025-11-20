## Part 6: Transaction Analysis — SimpleGreeting Contract Deployment

**Transaction hash:** 0xa1E395515d9B3DC681523fC19AF4Fb5cf6c13CA7

**Status:** Success

**Timestamp:** (from Remix / Routescan)

**Block number:** 9658254

**Number of confirmations:** (from Routescan)

**Verification links:**
- Sourcify: https://repo.sourcify.dev/11155111/0xa1E395515d9B3DC681523fC19AF4Fb5cf6c13CA7/
- Routescan: https://testnet.routescan.io/address/0xa1E395515d9B3DC681523fC19AF4Fb5cf6c13CA7/contract/11155111/code

### Parties Involved

**Sender:** My MetaMask address (EOA) — this is me deploying the contract

**Receiver:** Contract creation (no standard receiver since this is deployment)

**Contract name:** SimpleGreeting

### Value & Fees

**Amount transferred:** 0 ETH

**Transaction fee:** 0.00097008

### Technical Details

**Method called:** Constructor (constructor(string _greeting))

**Input data:** Hello from Damilola Sogo-Temi

**Tokens transferred:** None

**Events emitted:** None during deployment (events only fire when calling setGreeting)

### Analysis / Thoughts

This was basically me doing the same thing our tutor showed in class — deploying a simple smart contract on a testnet. Since it's Sepolia, gas fees are very low and there isn't any real ETH at stake.

I didn't send any value, just deployed the contract to test how it works. The deployment went smoothly and using Sourcify and Routescan, I can confirm the contract exists and the source code is verified.

The transaction itself doesn't tell me much about the sender besides the fact that this account deployed the contract. The receiver is just the new contract, so there's no activity there yet.

Overall, it's a simple, clean deployment just a basic learning exercise to see how contracts are created and verified on a testnet. The verification links give proof that it exists even though Sepolia Etherscan doesn't show it.