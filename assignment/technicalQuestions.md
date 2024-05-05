# Technical questions to answer

## What are the benefits of using thirdweb Engine?
The ThirdWeb Engine is like a backend server that makes hard stuff easy for developers. It supports account abstraction, contracts deployments on any EVM compatible blockchain, locally stores backend wallets, stores logs of transactions and much more.

To keep things simple, thirdweb engines can help you with:

- **Handles Lots of Stuff:** It can do many things at once, like sending transactions across the blockchain without any fuss. So, when your app gets busy, it stays reliable.
- **Fixes Mistakes:** Ever had a transaction get stuck or fail? The Engine can automatically sort out these problems, so you don't have to worry about them.
- **Avoids Doing Things Twice:** It's careful not to repeat actions, so you don't accidentally do something twice, like sending money or creating digital items.
- **Keeps Your Wallets Safe:** It works with your wallets, which you control. Whether you keep them on your computer or use fancy cloud storage, it's your call.
- **Makes Smart Contracts Easy:** If you need to use smart contracts (which are like digital agreements), the Engine makes it easy to do so, without needing to understand all the technical stuff.
- **Pays for Transaction Fees:** You can even cover the fees for your users' transactions. This means they don't need to worry about having money for fees themselves.
- **Hides the Hard Parts:** It hides the tricky bits of blockchain stuff, so your app runs smoothly without needing to know all the details.
- **Notifies You of Important Things:** It's good at letting you know when something important happens in your app, like when a transaction finishes or an event occurs.

  
## How can a developer set the sponsorship rules for smart accounts?
Sponsoring rules is a part of account abstraction and it is available in Connect from thirdweb. 
Setting up these rules is straightforward. Navigate to the configuration tab in the Account Abstraction dashboard and define your rules. These rules will automatically apply to transactions processed by the paymaster. Additionally, set up a server verifier by providing a URL for the paymaster to call before sponsoring a transaction. 

There are few different types of rules that can be set, here's a list of them:

- **Global Spend Limits:** Specify the maximum gas cost (in USD) that the paymaster should sponsor during the billing period.
- **Server Verifier:** Set up a custom verification endpoint that the paymaster will call before sponsoring a transaction. This allows implementing custom rules based on specific criteria, such as user activity or transaction context.
- **Contract Address Restrictions:** Define a whitelist of contract addresses to sponsor transactions sent only to specific contracts.
- **Chain Restrictions:** Optionally, restrict sponsorship to transactions on specific blockchain networks.
- **User Lists:** Create allowlists or blocklists to control which users' transactions are sponsored.
- **Admin Accounts:** Specify admin accounts that are exempt from sponsorship rules.

##  What contracts do a developer need to deploy if they want to build an ecosystem with NFTs, ERC20s, staking, and marketplace? Also, the developer wants to split primary sales of the ERC-721 NFT with 2 other addresses. How can this be achieved?

To create an ecosystem with NFTs, ERC20s, staking, and a marketplace, developers need to deploy four types of contracts:

- **ERC20 Token Contract:** This contract handles the ERC20 tokens used in the ecosystem for regular transactions.
- **ERC721 Token Contract:** This contract manages the unique NFTs (non-fungible tokens) representing digital assets like artworks, collectibles, or in-game items.
- **Staking Contract:** This contract enables users to stake their tokens, allowing them to earn rewards or participate in governance.
- **Marketplace Contract:** This contract serves as a platform for buying, selling, and trading NFTs and ERC20 tokens within the ecosystem.

  
Now, to split primary sales of the ERC721 NFT with two other addresses, developers can add a feature within the ERC721 token contract. This feature ensures that when an NFT is sold for the first time (primary sale), the revenue is automatically divided among the seller and the two designated addresses according to predefined percentages. This ensures fair distribution of profits from NFT sales among the involved parties.
