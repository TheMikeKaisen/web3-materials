
## Table of Contents
- [What is Blockchain?](#bitcoin-and-blockchain)
- [Why Smart Contracts?](#why-smart-contracts)
- [Features of Blockchain](#features-of-blockchain)
- [Gas](#gas)
- [How does a Blockchain work?](#how-does-a-blockchain-work)
- [Public and Private Keys](#public-and-private-keys)
- [More about Gas](#more-about-gas)
- [PoW and PoS](#pow-and-pos)
- [Blockchain Overview](#blockchain-overview)
- [L1, L2, and Rollups](#l1-l2-and-rollups)
- [More on L1, L2, and Rollups](#more-on-l1-l2-and-rollups)
- [How does Optimistic Rollups work](#how-does-optimistic-rollups-work)
- [How does ZK Rollups work](#how-does-zk-rollups-work)
- [If ZK Rollups, then why Optimistic Rollups?](#if-zk-rollups-then-why-optimistic-rollups)
- [Operators](#operators)
- [Sequencers](#sequencers)
- [Operators vs Sequencers](#operators-vs-sequencers)
- [Composability](#composability)
- [Revert](#revert)
- [ChainLink](#chainlink)

### Bitcoin and Blockchain

You might be familiar with `Bitcoin`, which is one of the first protocols to utilize the revolutionary blockchain technology. The Bitcoin Whitepaper, authored by the pseudonymous `Satoshi Nakamoto`, described how Bitcoin could facilitate peer-to-peer transactions within a decentralized network using cryptography. This gave rise to censorship-resistant finance and presented `Bitcoin` as a superior digital store of value, often referred to as *digital gold*. There is a fixed amount of Bitcoin, similar to the scarcity of gold. You can learn more about this in the [Bitcoin Whitepaper](https://bitcoin.org/bitcoin.pdf).

### Ethereum and Smart Contracts

A few years after Bitcoin's creation, Vitalik Buterin and others founded `Ethereum`, which builds upon the blockchain infrastructure, but with additional capabilities. With Ethereum, you can create decentralized transactions, organizations, and agreements without a centralized intermediary. This was achieved through the addition of `smart contracts`.

Though the concept of smart contracts was originally conceived in 1994 by [**Nick Szabo**](https://en.wikipedia.org/wiki/Nick_Szabo), Ethereum made it a reality.

> Smart contracts are a set of instructions executed in a decentralized way without the need for a centralized or third party intermediary.
> 

Smart Contract functionality is the primary difference between blockchains like `Ethereum` and `Bitcoin`. Technically `Bitcoin` does have smart contracts but they're intentionally `turing incomplete`.

### The Oracle Problem

However, smart contracts face a significant limitation – they cannot interact with or access data from the real world. This is known as the `Oracle Problem`.

Blockchains are deterministic systems, so everything happens within their ecosystem. To make smart contracts more useful and capable of handling real-world data, they need external data and computation.

Oracles serve this purpose. They are devices or services that provide data to blockchains or run external computation. To maintain decentralization, it's necessary to use a decentralized Oracle network rather than relying on a single source. This combination of on-chain logic with off-chain data leads to `hybrid smart contracts`.

> Note: Most of this course will assume we're working with an Ethereum or EVM environment. The skills you learn here will be compatible with the vast majority of blockchain architectures!
> 

### Chainlink

[**Chainlink**](https://chain.link/) is a popular decentralized Oracle network that enables smart contracts to access external data and computation. Chainlink is also blockchain agnostic - so it's going to work with any chain out there.

### Layer 2 Scaling Solutions

As blockchains grow, they face scaling issues. Layer 2, or L2, solutions have been developed to address this. L2 solutions involve other blockchains hooking into the main blockchain, essentially allowing it to scale. There are two primary types of L2 solutions:

- **Optimistic Rollups:** eg. Optimism, Arbitrum
- **Zero-Knowledge Rollups:** eg. ZKsync, Polygon ZK EVM

Don't worry too much about this now. Once we understand how blockchains work 'under the hood', we'll go further into Layer 2's then.

### Terminology

You're going to hear some terms used in this course (and the community as a whole) a little interchangeably. Maybe you haven't heard these terms before. I hope this offers a bit of clarification.

Common Terms:

1. **Blockchain**: In web3, a blockchain is a digital ledger that records transactions across many computers in a secure and decentralized manner. Each block contains a number of transactions, and every new block is linked to the previous one, forming a chain. This makes the data tamper-resistant. *Example*: Bitcoin's blockchain records all BTC transactions.
2. **Oracle**: Oracles in web3 are intermediaries that provide smart contracts with external data. They act as bridges between blockchains and the outside world, allowing smart contracts to execute based on real-world events and data. *Example*: A weather oracle provides data for a smart contract that triggers crop insurance payments based on rainfall data.
3. **Layer 2**: Layer 2 solutions in web3 are technologies built on top of a blockchain (Layer 1) to improve its scalability and efficiency. These solutions handle transactions off the main chain, reducing congestion and fees, and then settle the final state on the main chain. *Example*: The Lightning Network for Bitcoin.
4. **Dapp (Decentralized Application)**: A Dapp is an application that runs on a decentralized network, typically a blockchain. It is powered by smart contracts and operates without a central authority. Dapps can serve various purposes, from finance to gaming. *Example*: Uniswap, a decentralized finance application.
5. **Smart Contract**: In web3, a smart contract is a self-executing contract with the terms of the agreement directly written into code. They run on blockchains and automatically execute when predetermined conditions are met, without the need for intermediaries. *Example*: A smart contract for an escrow service.
6. **Hybrid Smart Contract**: Hybrid smart contracts combine on-chain code (running on a blockchain) with off-chain data and computations provided by oracles. This allows the contracts to interact with data and systems outside their native blockchain. *Example*: A smart contract for insurance that uses real-world data (like weather or flight delays) provided by oracles.
7. **Ethereum/EVM (Ethereum Virtual Machine)**: Ethereum is a blockchain platform known for its smart contract functionality. The Ethereum Virtual Machine (EVM) is its computation engine that executes smart contracts. Ethereum allows developers to build decentralized applications and is the basis for many web3 projects. *Example*: ERC-20 tokens, a standard for creating fungible tokens on Ethereum.

### Web3

Web3 is a term used to describe the new paradigm of the internet powered by blockchain and smart contracts. Unlike the previous versions of the web, web3 is permissionless and relies on decentralized networks rather than centralized servers. This ushers in an era of censorship-resistant and transparent agreements and transactions, often called an ownership economy.

**Web1:** The permissionless open sources web with static content

**Web2:** The permissioned web, with dynamic content where companies run your agreements on their servers.

**Web3:** The permissionless web with dynamic content.

- Decentralized censorship resistant networks run your agreements and code.
- User owned ecosystems where one owns a portion of the protocol they interact with - instead of solely being the product

### Wrap Up

We've taken a high-level view of the blockchain landscape, including its history and the problems that smart contracts solve.

At this point you might be asking yourself *what do these smart contracts really mean?* or *what is meant by trust minimized agreements/unbreakable promises?*

In my mind a technology is really only as good as the problem it solves. So next, we're going to look at what the **purpose** of `smart contracts` is - what's the value proposition exactly?

Let's take a closer look at the undeniable value of `smart contracts` in the next lesson

- Why Smart Contracts?

## The Essence of Blockchain and Smart Contracts

Almost every interaction or transaction in our lives involves some form of agreement or contract. For instance, purchasing a chair involves a contract to buy lumber, assemble it, and sell the finished product. Your electricity supply is also based on an agreement between you and the electric company. When you get an oil change for your car, you're promised a service in exchange for money.

Almost everything we do in modern life relates to an agreement or contract in some way.

To make it more relatable, think of contracts and agreements as promises. Traditional contracts, however, require trust between parties, and this doesn’t always work in favor of honesty and fairness.

### The Problem with Traditional Agreements

Lets consider some real world examples of where trust leveraged agreements can go wrong and why blockchain technology and smart contracts mitigate these risks.

### Consumer Trust

In the 80s and 90s, McDonald’s Monopoly game promised customers a chance to win money through game cards obtained with purchases. However, it turned out that the game was rigged by insiders who manipulated the system for their gain. Essentially, McDonald’s failed to keep its promise.

This example demonstrates that relying on trust within agreements can lead to fraudulent activities and broken promises.

With smart contracts, we can eliminate the need for trust. A smart contract is an agreement or a set of instructions that are deployed on a decentralized blockchain. Once deployed, it cannot be altered, it automatically executes, and everyone can see its terms.

Imagine if McDonald’s Monopoly game was operated on a blockchain through a smart contract. The fraudulent activities would have been impossible due to the immutable, decentralized, and transparent nature of smart contracts.

### Banking and Trust

Traditional banks have sometimes failed to keep the promise of safeguarding people's money, as seen during the Great Depression. Blockchain and smart contracts can ensure transparency and execute automated solvency checks, preventing the bank from becoming insolvent.

The core of blockchain and smart contracts lies in creating a trustless system where agreements are transparent, unchangeable, and executed without human intervention. This technology holds the potential to revolutionize industries and everyday agreements by ensuring honesty and fairness.

### Financial Markets Access

Centralized bodies, like traditional exchanges, have the power to restrict access to financial markets. This was evident when Robinhood restricted trading on certain assets in 2021. With decentralized exchanges like Uniswap, there is no central authority that can alter or limit market access. This introduces fairness and openness to the financial markets.

### To Summarize

- Traditional Agreements: Require trust in a centralized entity.
- Smart Contracts: Transparent, decentralized, and tamper-proof.

In a scenario where you have to choose, smart contracts are an obvious choice as they cannot be manipulated or altered in anyone's favor.

Smart contracts are *the* solution to minimizing the reliance on trust based systems that have historically failed us time and time again.

### Under the Hood

Smart contracts are relatively new, but have already started transforming various markets. They do this by representing 'promises' as code on the blockchain. This code is executed by a decentralized collective, such that no single entity can alter the agreemeent in any way! The agreement and its terms are public knowledge and will automatically execute without human intervention.

More industries are adopting smart contracts and blockchain due to the numerous advantages they offer. This results in trust-minimized agreements or what can be simply termed as unbreakable promises.

### Beyond Trust Minimization

It is important to note that blockchain, smart contracts, and cryptocurrencies are not just about trust-minimized agreements. They offer security benefits, uptime advantages, execution speed, and **much more**.

### Caution: Not All Are Equal

However, beware of platforms that claim to be decentralized but are not in practice. An example from 2022 is the `SBF's FTX platform`. It presented itself as a Web3 platform, but was essentially a traditional Web2 company using cryptocurrency without the benefits of smart contracts.

As an emerging developer or user in this space, it's important to discern between legitimate projects and those that aren't contributing to the ethos of Web3. I want you to be successful, but I want you to be successful because you're creating value. Platforms like `FTX` were pretending to bring value to the space and leeching value from it.

### Wrap Up

What we've learnt is that traditional contracts or agreements between parties are almost always trust based. Trust based agreements come with inherent flaws and the potential of broken agreements, the consequences of which we've seen throughout history - The Great Depression, Monopoly Lottery, Robin Hood etc.

Blockchain technology and smart contracts solve these problems by introducing fairness, transparency and immutability to promises. These attributes of smart contracts assure that trust isn't required and we can be certain that an agreement will be executed as described 100% of the time.

Lastly, it's important to note that there are several actors, such as `FTX` which *pretend* to embody the ideologies of Web3, but are really centralized entities looking to extract value from the system, be aware of these.

- Features of blockchain

### Introduction

Blockchain technology has transformed digital transactions and agreements. Bitcoin was the first protocol to popularize blockchain, facilitating transactions without intermediaries. Building on this foundation, Ethereum and other smart contract platforms have advanced the technology by enabling the creation of smart contracts and decentralized applications. These platforms interact with the real world through decentralized networks like Chainlink, extending blockchain's capabilities. This aspect challenges traditional finance, offering a new way to manage and transfer wealth.

### Bitcoin and Ethereum

Bitcoin introduced the concept of a decentralized digital currency. It functions as a store of value and allows for peer-to-peer transactions without the need for a central authority. This decentralization ensures that no single entity controls the network, making Bitcoin resistant to **censorship** and **central points of failure**.

Ethereum expanded on Bitcoin's technology by introducing smart contracts. Smart contracts are self-executing contracts with all the terms and conditions transparently written into code. These contracts are **trust-minimized agreements**, and they remove the need for intermediaries. Ethereum's platform allows for the creation of decentralized applications (dApps) that can interact with the blockchain and real-world data through decentralized networks.

### Chainlink

Chainlink is a decentralized network that facilitates the creation of **hybrid smart contracts**. By combining on-chain logic with off-chain data and computation, they ensure that both the logic and the data remain decentralized.

### Key Features and Benefits

✅ **Decentralization**. Smart contracts operate on decentralized networks maintained by nodes, which remove the need for central intermediaries

✅ **Transparency and Flexibility**. All transactions and contract executions on the blockchain are visible to everyone, ensuring transparency and fairness. Additionally, pseudoanonimity ensures that **privacy** is maintained, since accounts are not tied to real-life identities.

✅ **Speed and Efficiency**: Blockchain transactions are instant, unlike traditional bank transfers that can take days or weeks to execute. This efficiency extends to financial settlements, eliminating the need for clearing houses and reducing settlement times.

✅ **Security and Immutability**: Once deployed, smart contracts cannot be altered, ensuring that the terms remain unchanged. Hacking a blockchain is extremely challenging due to its decentralized nature, offering a more secure method for protecting information compared to centralized systems.

✅ **Reduced Counterparty Risk**: Smart contracts remove the need for trust in intermediaries, ensuring that agreements are executed as coded without the risk of human interference or fraud.

### Conclusion

Blockchain technology has revolutionized digital transactions and agreements. Bitcoin introduced decentralized digital currency, Ethereum expanded it with smart contracts, and Chainlink enhanced it with hybrid networks. These advancements challenge traditional finance, offering secure, transparent, and efficient ways to manage and transfer wealth, leading to a new era of trust-minimized agreements.

### 🧑‍💻 Test Yourself

1. 📕 Describe briefly what are Bitcoin, Ethereum and Chainlink
2. 📕 What are the key advantages of smart contracts over traditional financial systems?
- Gas

In this lesson, we will discuss important concepts ranging from transaction fees and gas prices, mining incentives, computational measures in transactions, to hands-on experience of sending a transaction in Ethereum’s test network.

Let's jump right in!

### **Transaction Fee and Gas Price: What are they?**

!https://updraft.cyfrin.io/blockchain-basics/06-intro-to-gas/intro-to-gas1.png

While inspecting an Ethereum transaction, two terms invariably catch the glance: "transaction fee" and "gas price". Let's clarify what they are and why they matter.

The transaction fee is the amount rewarded to the block producer for processing the transaction. It is paid in Ether or GWei. The gas price, also defined in either Ether or GWei, is **the cost per unit of gas specified for the transaction**. The higher the gas price, the greater the chance of the transaction being included in a block.

> Gas price is not to be confused with gas. While **gas refers to the computational effort required to execute the transaction, gas price is the cost per unit of that effort**.
> 

When we click on "more details" in a transaction overview, we can see further information including the `Gas Limit and Usage by transaction`.

Now, let's address an important question: who gets these transaction fees and why?

### **The Role of Nodes in Blockchain**

Blockchains are run by a group of different nodes, sometimes referred to as miners or validators, depending on the network. These miners get incentivized for running the blockchain by earning a fraction of the native blockchain currency for processing transactions. For instance, Ethereum miners get paid in Ether, while those in Polygon get rewarded in MATIC, the native token of Polygon. This remuneration encourages people to continue running these nodes.

### **Understanding Gas in Transactions**

In the context of transactions, gas signifies a unit of computational complexity.

The higher a transaction's complexity, the more gas it requires. For instance, common transactions like sending Ether are less complex and require relatively small amounts of gas. However, more sophisticated transactions like minting an NFT, deploying a smart contract, or depositing funds into a DeFi protocol, demand more gas due to their complexity.

The total transaction fee can be calculated by multiplying the gas used with the gas price in Ether (not GWei). Therefore, `Transaction fee = gasPrice * gasUsed`.

### **Hands-on: Sending an Ethereum Transaction**

In any blockchain, making a transaction requires the payment of a transaction fee (in terms of the native token) to the blockchain nodes processing that transaction. Let's take an example of a transaction using the MetaMask extension, a popular Ethereum wallet.

Here are the steps:

1. Open MetaMask and click "Expand View".
2. Choose the account to use for the transaction.
3. Click on "Send".
4. Select "Transfer between my accounts".
5. Enter the account to send the Ether to, and the amount you wish to send.
6. Click "Next". MetaMask will automatically calculate the gas fee for you. The total amount to be paid is the sum of the Ether value you're sending and the gas fee.

Something of note, if you click the `market` link in MetaMask, you'll be shown some optional settings for gas in the transaction. You may wonder *Why would I choose to spend more gas?*

A simplified explanation of this is: if lots of people are trying to process transactions at the same time, the space on a given block is competitive, gas prices are increased to throttle and prioritize transactions during congestion.

1. Click "Confirm".

The transaction will now appear in the Activity tab of MetaMask. After a short while, the transaction gets processed, and you can view its details in a block explorer like Etherscan.

You have now executed your first blockchain transaction!

Despite its simplicity, knowing how to process transactions with MetaMask is vital and empowers you to interact with protocols on the Ethereum network and other blockchains. However, to fully understand Ethereum and the blockchain landscape, it's crucial to delve into the details behind these transactions and the fundamental mechanics of blockchains.

Remember, mastering the nuances of blockchain transactions and understanding the mechanics behind Ethereum will enable you to become a powerful developer in the decentralized world

- How does a blockchain work?

### **Understanding Hash Functions**

At its simplest, a hash is a unique, fixed-length string that serves to identify any piece of data. When you input any kind of data into a hash function, it produces a hash. In this demo, the hash algorithm we'll focus on is SHA-256.

!https://updraft.cyfrin.io/blockchain-basics/07-how-do-blockchains-work/how-do-blockchains-work1.png

If I add `Patrick Collins` to our `SHA-256` algorithm, it will:

1. Convert the letters to numbers
2. Convert the numbers to a fixed-length “string” or “hash”

`Patrick Collins` gets converted to `7e5b5a1a6b80e2908b534dd5728a998173d502469c37121dd63fca283068077c`

Ethereum, uses its own version of a hashing algorithm (Keccak256) that isn't exactly SHA-256 but belongs to the SHA family. This doesn't change things significantly here as we're primarily concentrating on the concept of hashing.

In the application, whatever data you enter into the data section, undergoes processing by the SHA-256 hash algorithm resulting in a unique hash.

> For example, when I input my name as "Patrick Collins," the resulting hash uniquely represents "Patrick Collins." The fascinating aspect is, no matter how much data is input, the length of the generated hash string remains constant.
> 

### **Understanding Blocks**

Now that we've grasped the concept of hashing and fixed-length string, let's inspect the structure of a blockchain. A collection of "blocks."

!(https://updraft.cyfrin.io/blockchain-basics/07-how-do-blockchains-work/how-do-blockchains-work2.png)

A block takes the same data input, but instead of a singular data field, a block is divided into 'block', 'nonce', and 'data.' All three are then run through the hash algorithm, producing the hash for that block. As a result, even a minor change in the data leads to an entirely different hash, hence, invalidating the block.

In essence, mining involves the computational trial and error process of finding an acceptable value to produce a hash which typically follows a certain pattern, such as starting with four zeros. The value found, which satisfies this criterion, is known as the 'nonce'.

The problem or criteria a miner has to solve will vary from blockchain to blockchain, but the concept is the same.

### **The Inherent Beauty of Blockchain: Immutability**

In a blockchain, which is essentially a sequence of blocks, each block is comprised of the previous elements - a block number, a nonce and data - as well as `the hash of the previous block`

!https://updraft.cyfrin.io/blockchain-basics/07-how-do-blockchains-work/how-do-blockchains-work3.png

What this means in practice is that any changes to data, in any block of the chain, will invalidate every proceeding block, until they are recalculated, or re-mined.

> Genesis Block: This is the first block in a blockchain.
> 

### **Decentralized Distribution**

Now, if a single entity were to control the blockchain, they could conceivably change any data they want, and then re-mine, or re-validate subsequent blocks. This is bad.

*Enter Decentralized Distribution.*

!https://updraft.cyfrin.io/blockchain-basics/07-how-do-blockchains-work/how-do-blockchains-work4.png

The crux of blockchain's power lies in its decentralization or distributed nature. Under this system, multiple entities or "peers" run the blockchain technology, each holding equal weight and power. In the event of disparity between the blockchains run by different peers (due to tampering or otherwise), the majority hash wins, as the majority of the network agrees on it.

Nodes that don't agree with the majority effectively fork the network, continuing on their own with their own history.

### **Interplay of Blockchain & Transactions**

Until now we've been considering the data passed in a block to be a random string of text, but the reality is - this data can be anything. In the token and coinbase sections of this demo you can see how each block is comprised of a number of transactions that all get hashed together. Any edits to any of these transactions is going to invalidate the chain!

!https://updraft.cyfrin.io/blockchain-basics/07-how-do-blockchains-work/how-do-blockchains-work5.png

### **Wrap Up**

To summarize, every transaction, block, and indeed the whole blockchain itself comes down to understanding the concept of a hash. This unique fixed-length string that is intrinsically linked with the original data. We've also underscored the importance of decentralization and highlighted how the concept of immutability plays into the system's security

- Public and Private Keys

### **Public and Private Keys**

In this lesson, all the pieces we learnt about with MetaMask should start coming together.

Understanding the relationship between private and public keys is essential to grasping the concept of blockchain transactions. In essence, a private key is a randomly generated secret key used to sign all transactions.

The private key is then passed through an algorithm (the [**Elliptic Curve Digital Signature Algorithm**](https://en.wikipedia.org/wiki/Elliptic_Curve_Digital_Signature_Algorithm) for Ethereum and Bitcoin) to create the corresponding public key. Both the private and public keys are central to the transaction process. However, while the private key must remain secret, the public key needs to be accessible to everyone.

When we send a transaction to the blockchain, we're passing a private key. This allows others to verify the transaction through the generated public key.

!https://updraft.cyfrin.io/blockchain-basics/08-signing-transactions/signing-transactions1.png

### **How does Transaction Signing Happen?**

When we sign a transaction on the blockchain, we're digitally signing some data with our private key. The hashing algorithm used makes it impossible for something to derive your private key from a message signature.

!https://updraft.cyfrin.io/blockchain-basics/08-signing-transactions/signing-transactions2.png

This signing method allows anyone to verify the validity of a transaction by comparing the message signature to a user's public key!

!https://updraft.cyfrin.io/blockchain-basics/08-signing-transactions/signing-transactions3.png

### **Importance of Hiding Private Keys**

Your MetaMask account's private key is accessible through `Account Details` > `Show Private Key`. You'll be asked to provide a password, again underscoring the importance of keeping this key safe.

Anyone with access to your private key can perform and sign transactions, on your behalf consequently making it absolutely vital to safeguard private keys.

> Note: As an interesting side note, wallet addresses, like the one MetaMask provided to you, are actually derived from your public key. A public key is passed through the Ethereum Hashing Algorithm, the last 20 bytes of the resulting hash is the address!
> 

### **Wrap Up**

Lets recap some of the things covered in this lesson.

We discovered that transactions on the blockchain are signed using a user's `private key`. The generated `message signature` can then be verified by anyone through a comparison to a user's `public key`.

**KEEP YOUR PRIVATE KEY SECURE!**

- Private Keys allow someone to sign a transaction, they should be kept secret and secure.

We learnt that `public keys` are generated by using the [**Elliptic Curve Digital Signature Algorithm**](https://en.wikipedia.org/wiki/Elliptic_Curve_Digital_Signature_Algorithm) on a user's private keys.

In addition to this, Ethereum addresses are derived from public keys by hashing a user's public keys with the Keccak256 algorithm.

The deeper we go, the more complicated things get, but you're doing great and we still have a ways to go. In the next lesson we'll look again at gas and investigate some of the more low level interactions of gas in a blockchain ecosystem

- More about Gas

### **Transactions and Gas**

In this lesson we're going to take an even closer look at `gas`, how it functions and the purpose it serves on the blockchain.

Don't stress if this topic sounds complex; gas can absolutely be a confusing topic, but the more experience you gain and more examples we go through, it'll start to become clear.

**Note:** What we're covering here is applicable to Ethereum post implementation of [**EIP-1559**](https://eips.ethereum.org/EIPS/eip-1559) wherein gas limits, priority fees and the discussed burn mechanism were all introduced.

### **Transaction Breakdown**

Before we continue, there are a couple important terms to understand.

**Copy to clipboard**

**12Wei:  1,000,000,000 Wei  = 1 Gwei (Gigawei)Gwei: 1,000,000,000 Gwei = 1 Eth**

!https://updraft.cyfrin.io/blockchain-basics/09-gas-II/gas-II1.png

*Reference the above image, the labelled sections will be detailed below*

**1. Transaction Fee:** This is calculated as Total `Gas Used * Gas Price` where `Gas Used` represents the computational units required to perform the work and `Gas Price` is comprised of a `Base` and `Priority Fee`

**2. Gas Limit:** This is the maximum amount of gas allowed for the transaction. This can be set by the user prior to sending a transaction.

In Metamask, you can navigate to `Market > Advanced > Edit Gas Limit` in order to set this value.

!https://updraft.cyfrin.io/blockchain-basics/09-gas-II/gas-II2.png

**3. Base Gas Fee:** The base fee of a transaction, represented in Gwei. Remember, this is cost per gas.

There are a couple important points to note regarding the Base Fee

- The fee is burnt as of EIP-1559. Burning serves to remove the value from circulation, combating inflation on the protocol. The amount burnt can be seen beneath the `Base Fee` in the image above.
- The fee is dynamic, under EIP-1559, if a block is more than 50% full, the `Base Gas Fee` is increased for the next block. Likewise, if a block is less then 50% full, the fee decreases. This serves to balance network demand and capacity.

**4. Max Gas Fee:** This is the maximum cost per cast the transaction has been configured to allow. This can again be configured prior to sending a transaction.

**5. Max Priority Fee:** Again, configurable prior to sending a transaction, this represents the maximum `tip` we're willing to give miners. This incentivizes the inclusion of our transaction within a block.

**6. Block Confirmations:** These are he number of blocks which have been mined or validated which have been confirmed to contain your transaction. The more confirmations the more sure we can be of the transaction's validity.

### **Wrap Up**

Lets recap some of what we've learnt about transactions on the blockchain!

We learnt that every transaction has a unique `transaction hash` that uniquely identifies the transaction on chain.

Pulling up a transaction in a block explorer like Etherscan can provide us a tonne of additional information, including:

- The block which contains the transaction
- The time stamp of when the transaction was requested
- Where the transaction is originating
- Where the transaction is being sent
- The value included in a transaction

From here we can also see details about the `transactions fees` and `gas` costs.

`Gas` is a measure of computation required to perform a task, the cost of a transaction is derived from a `Gas Price` (made of `Base` and `Priority Fees`) and the amount of `gas` used.

We learnt that a `Gas Limit` can be set before a transaction is set and that the `Base Fee` on all Ethereum transactions is actually `burnt`, in order to reduce inflation and stabilize the network economy.

We also discovered that the Base Fee goes up and down depending on the congestion of a block. If a block is >50% full, the fee goes up, <50% and the fee goes down.

- PoW and PoS

---

### 1. **Proof of Work (PoW)**

- **Purpose**: PoW was created to secure the blockchain and prevent fraud by making participants (miners) put in a lot of effort (work) to verify transactions.
- **How It Works**:
    - Every time a block of transactions is ready to be added to the blockchain, miners compete to solve a complex math puzzle.
    - The puzzle isn’t easy to solve, so miners use powerful computers to make millions of guesses every second to find the right answer.
    - The first miner to solve the puzzle broadcasts the solution to the network. Other participants quickly check if the solution is correct.
    - If it’s correct, the miner gets rewarded with cryptocurrency, and the block is added to the blockchain.
- **Why It’s Secure**: Solving the puzzle is hard and requires significant computing power, which means it’s tough for someone to cheat the system.
- **Example**:
Imagine there’s a contest to guess a password, and it’s set up so that it’s really hard to guess. Dozens of people are trying, but only the first person who guesses it right gets a prize and records their entry. They then announce their answer to the group, and if it’s correct, they get rewarded, and the answer is locked in as official.
- **Pros and Cons of PoW**:
    - **Pros**: Very secure and decentralized. The effort required makes it hard for bad actors to change anything on the blockchain.
    - **Cons**: It requires a ton of energy and computing power, making it slow and costly.

---

### 2. **Proof of Stake (PoS)**

- **Purpose**: PoS was created as a more energy-efficient alternative to PoW. It reduces the need for heavy computing work by making the validation process more accessible.
- **How It Works**:
    - Instead of miners, PoS uses *validators*, who are selected based on the amount of cryptocurrency they hold (or “stake”) and are willing to lock up as collateral.
    - Validators don’t have to solve complex puzzles. Instead, the network chooses one at random based on their stake size and other factors.
    - The selected validator verifies the transactions and creates a new block. If they do this correctly, they receive a reward. If they try to add false information, they can lose some or all of their staked cryptocurrency.
- **Why It’s Secure**: Validators have something to lose (their staked cryptocurrency) if they act dishonestly, which motivates them to be truthful.
- **Example**:
Imagine a neighborhood where people pool money to buy groceries each week, and every week, they randomly choose someone to do the shopping. The more money someone has put in, the higher their chances of being picked to shop. If they come back with incorrect or overpriced items, they risk losing the money they put in.
- **Pros and Cons of PoS**:
    - **Pros**: It’s much faster and less energy-intensive than PoW, which makes it more eco-friendly.
    - **Cons**: Wealthier people (who have more cryptocurrency to stake) have a better chance of being chosen, which can make the network less decentralized.

---

### **Comparison Recap**

| Feature | Proof of Work (PoW) | Proof of Stake (PoS) |
| --- | --- | --- |
| **Who can validate** | Miners who solve puzzles | Validators with staked cryptocurrency |
| **Energy requirement** | Very high (energy-intensive) | Low (energy-efficient) |
| **Speed** | Slower due to computational work | Faster due to simpler selection |
| **Risk of Centralization** | Low, as computing power is widely distributed | Higher, as richer validators have more influence |
| **Example** | Puzzle-solving contest | Lottery based on how much money is put in |

---


- Blockchain overview

### Traditional Networks vs Blockchain

Traditionally, when you run an application be it a website or something that connects to a server you are interacting with a centralized entity. This is the opposite of what you may recall from our distributed blockchain example, in that the server is controlled and run by a single centralized group.

Blockchains, as we saw, run on a network of independent nodes. In our previous example, each of the `Peers` was representative of an independent `node` operator. The term `node` typically refers to a single instance of a decentralized system, Peer A would be a `node`. This network, this combination of these nodes interacting with each other is what creates a blockchain. What makes these networks so potent, is that anybody can join. All anyone needs is a little bit of hardware and you can participate in securing a blockchain network. You could go to GitHub and start operating a node in a few seconds!

In the traditional world applications are run by centralized entities and if that entity goes down or is malicious or decides that they want to shut off - they just can. They're the ones that control everything.

Blockchains, by contrast, don't have this problem. If one node or one entity that runs several nodes goes down, since there are so many other independent nodes running, it doesn't matter, the blockchain and the system will persist so long as there is at least one node always running. Luckily for us, the most popular chains like Bitcoin and Ethereum have thousands and thousands of nodes. Malicious nodes are kicked from the network, or even punished in some cases. Majority rules when it comes to the blockchain.

This gives blockchains this incredibly potent immutability trait where nothing can be changed or corrupted so in essence we can think of a blockchain as a decentralized database. In the case of Ethereum it has an extra additional feature where it also can do computation in a decentralized manner now.

### Consensus

Let's talk consensus. This includes `Proof of Work` and `Proof of Stake`. You've probably heard these terms before and they're really important to how these blockchains work.

The `mining` feature of our previous blockchain example was an example of `Proof of Work`

`Proof of Work` and `Proof of Stake` fall under this umbrella of `consensus`. And `consensus` is a really important topic when it comes to blockchains.

> Consensus is defined as the mechanism used to reach an agreement on the state or a single value on the blockchain especially in a decentralized system.
> 

Very roughly, a consensus protocol in a blockchain or decentralized system can be broken down into two pieces: a chain selection algorithm and a sybil resistance mechanism. Mining, or Proof of Work, is a sybil resistance mechanism. This is what Bitcoin currently uses.

`Proof of Work` is known as a sybil resistance mechanism because it defines a way to figure out who is the block author or which node did the work to mine a block. Sybil resistance is a blockchain's ability to defend against users creating a large number of pseudo-anonymous identities to gain a disproportionately advantageous influence over said system.

As mentioned, there are two primary types of sybil resistance:

- Proof of Work
- Proof of Stake

We'll look a little closer at `Proof of Work` first.

### Proof of Work

Proof of work is a system of sybil resistance used in many blockchains, in its essence a miner needs to go through a very computationally heavy process (mining) to find the block's answer. As a result, it doesn't matter how many additional nodes you're running, each node is obligated to do this work in order to receive a reward. The playing field is kept fair.

> Note: Some blockchains may make their riddle or their block answer intentionally hard, or intentionally easy to adjust the block time - which is the average time it takes to mine a block. Blocktime is proportional to how difficult these algorithms are.
> 

Proof of Work needs to be combined with a `chain selection rule` to create `consensus`.

A `chain selection rule` is implemented as a means to determine which blockchain is the *real* blockchain. Bitcoin (and prior to the merge, Ethereum), both use something called `Nakomoto Consensus`. This is a combination of Proof of Work (Etherum has since switched to Proof of Stake) and the `longest chain rule`.

In the `longest chain rule`, the decentralized network decides that whichever chain has the most number of blocks will be the valid, or *real* blockchain. When we saw `block confirmations` in Etherscan earlier, this was representing the number of blocks ahead of our transaction in the longest chain.

> You'll sometimes hear people use Proof of Work to describe a consensus mechanism, but it's a little bit inaccurate, it's really the combination of sybil resistance and chain selection that create consensus.
> 

`Proof of Work` also serves as a means to determine who receives transaction fees as we discussed earlier. These transaction fees are paid by whomever initiates the transaction. In a Proof of Work system, every node is competing against eachother to solve the block problem first. The first node to solve the problem gets paid the transaction fees accumulated in the block they mine. In addition to this, miners are also paid a `block reward`, the `block reward` is given by the blockchain itself.

> If you've previously heard of the Bitcoin Halving - this is the concept of the block reward being cut in half roughly every 4 years.
> 

Block rewards are in the blockchains native currency - Bitcoin = BTC, Ethereum = ETH. This effectively increases the amount of that cryptocurrency in circulation.

### Blockchain Attacks

There are two major types of attacks that exist in the blockchain space.

- Sybil Attack - When a user creates a number of pseudo-anonymous accounts to try to influence a network.
- 51% attack - Occurs when a single entity possesses both the longest chain and majority network control. This would allow the entity to `fork` the chain and bring the network onto the entities record of events, effectively allowing them to validate anything.

Blockchains are very democratic. The bigger a blockchain is, the more decentralized, the more secure it becomes.

I encourage you to look into running a node yourself to increase the security of the network!

Proof of Work does come with drawbacks. For example, Proof of Work consumes a LOT of electricity. When you have thousands of nodes all working as hard as they can to solve a block problem the energy consumption is HUGE and as such, so is the potential environmental impact.

With the above in mind, many protocols are choosing the shift to a different consensus mechanism that is more environmentally friendly. The most popular of which is...

### Proof of Stake

In contrast to trying to solve a block problem, Proof of Stake nodes put up some collateral that they are going to behave honestly aka they `stake`. If a node is found to be misbehaving, it's stake is slashed. This serves as a very effective sybil resistance mechanism because for each account, the validator needs to put up more stake and misbehaving risks losing all that collateral.

> In a Proof of Stake system, miners are known as validators. They aren't actually mining blocks, they're validating other nodes.
> 

Unlike in Proof of Work, where each node is racing to solve the block problem first, in Proof of Stake, validators are pseudo-randomly chosen to propose the next block and other nodes will validate it.

Proof of Stake of course comes with its own Pros and Cons.

Pros:

- great sybil resistance mechanism
- great for the environment, much less energy

Cons:

- seen as less decentralized due to upfront staking costs

This raises the question of *how decentralized is decentralized enough?* and I think I need to leave that to the community to decide.

### Layer 1 and Layer 2

I want to briefly touch on the concepts of Layer 1 and Layer 2 networks here as well.

1. `Layer 1` solutions: This refers to base layer blockchain implementations like Bitcoin or Ethereum.
2. `Layer 2` solutions: These are applications added on top of a layer one, like [Chainlink](https://chain.link/) or [Arbitrum](https://arbitrum.io/).

Layer 2s like Arbitrum and Optimism are special in that they're trying to solve the problem of scalability. These protocols leverage something called `rollups`. We won't go too deep, but the idea is that the protocols bundle their transactions to be processed by a Layer 1.

- L1, L2 and Rollups

Understanding **Layer 1 (L1)** and **Layer 2 (L2)** along with **rollups** is key to grasping the scalability and efficiency improvements being made in blockchain technology. Let’s walk through these terms and why they are important.

---

### 1. **Layer 1 (L1)**: The Main Blockchain

- **Definition**: A Layer 1 blockchain is the main network, the foundational layer where transactions are directly processed and recorded. Examples include **Bitcoin**, **Ethereum**, and **Solana**.
- **Purpose**: These blockchains are designed to be secure, decentralized, and transparent. They maintain the primary ledger and are responsible for consensus and transaction validation.
- **Challenges**:
    - **Scalability**: Layer 1 networks process each transaction individually. This means as demand grows, the network can become slow and costly (like during high-traffic times on Ethereum when transaction fees can spike).
    - **Throughput**: Due to their design, most L1s can only handle a limited number of transactions per second (e.g., Bitcoin ~7 TPS, Ethereum ~15 TPS).

### 2. **Layer 2 (L2)**: Scalability Solution for Layer 1

- **Definition**: Layer 2 solutions are built on top of Layer 1 blockchains to handle transactions off the main chain, reducing congestion and lowering fees on the L1.
- **Purpose**: L2 solutions aim to **increase transaction speed** and **reduce costs** by processing transactions on a separate layer and then finalizing them on the main blockchain (L1).
- **How It Works**: Instead of every transaction being processed on L1, groups of transactions are processed on L2, then bundled and submitted to L1 in batches. This minimizes the work done on L1 and increases the network’s overall capacity.

### 3. **Rollups on Layer 2**

- **What are Rollups?** Rollups are a type of L2 solution that “rolls up” multiple transactions into a single batch and submits them as one transaction on the L1 blockchain.
- **Types of Rollups**:
    - **Optimistic Rollups**: Assume that transactions in a rollup are valid and only check for fraud if someone challenges the validity. They’re called “optimistic” because they optimistically assume no one is cheating.
    - **Zero-Knowledge Rollups (ZK Rollups)**: Use cryptographic proofs to validate each transaction. Every batch has a "validity proof" that proves the transactions in the rollup are legitimate without revealing details.
- **Why Rollups?** Rollups drastically reduce congestion and costs on the main blockchain by moving transaction processing to Layer 2. The L1 only verifies the final proof or batch, making it more efficient without sacrificing security.

### **Why Were Rollups and L2 Solutions Developed?**

- **Scalability and Cost**: As blockchain networks like Ethereum grew in popularity, they faced major congestion issues, leading to higher transaction fees. Rollups and other L2 solutions were developed to allow more transactions per second while keeping fees low.
- **User Experience**: By reducing congestion and fees, L2 solutions improve the user experience, making blockchain more accessible and usable.
- **Security**: Rollups allow L2 transactions to benefit from the security of the main blockchain (L1) without adding significant load to it. L2 processes transactions and only relies on L1 for security and finality.

### **Example to Understand L1, L2, and Rollups**

Imagine you have a highway (L1) with only one lane, so during rush hour, it gets crowded and slow. Now, consider an additional lane (L2) where cars can drive and then merge onto the main road after a while. Rollups work similarly—by allowing many cars (transactions) to drive in parallel on the additional lane, only merging in large groups at a few points, which eases congestion on the main highway.

---

### **Quick Summary**

- **L1**: The main blockchain (e.g., Ethereum) where transactions are directly recorded but can get congested.
- **L2**: An additional layer built on L1 to process transactions separately, reducing load and costs on L1.
- **Rollups**: An L2 solution that batches (or “rolls up”) multiple transactions and posts them as a single transaction on L1.

- More on L1, L2 and Rollups

### **Blockchain layers**

A **Layer 1 (L1)** blockchain is the base layer of the blockchain ecosystem, where nodes help the chain to reach consensus. It operates without any additional plugins and is often referred to as the *settlement layer*. Examples of L1 chains include Bitcoin, BNB Chain, Solana, and Avalanche. In this course, we primarily focus on Ethereum, which serves as the **hub** of the Ethereum ecosystem. Applications directly deployed on Ethereum, like Uniswap, are not considered L2s but rather dApps on L1.

A **Layer 2** is any application built on outside an L1 blockchain that *hooks back into it*. There are different types of Layer 2, for example **Chainlink**, a decentralized Oracle networks and event indexing networks like **The Graph**, which enable applications to access on-chain data. But the most popular type of L2 is the **rollup**, or **L2 chain**.

### **Rollups**

**Rollups** are L2 scaling solutions that enable to increase the number of transactions on Ethereum by bundling multiple transactions into one, reducing gas costs.

!https://updraft.cyfrin.io/blockchain-basics/15-l1s-l2s-and-rollups/tx-bundle.png

Rollups help solve the blockchain trilemma, which states that a blockchain can only achieve two out of three properties: *decentralization*, *security*, and *scalability*. In the case of Ethereum, **scalability** is sacrificed as it can only process approximately 15 transactions per second. Rollups, on the other hand, aim to enhance scalability without compromising security or decentralization.

!https://updraft.cyfrin.io/blockchain-basics/15-l1s-l2s-and-rollups/bc-trilemma.png

### **How Rollups Work**

When a user [**submits a transaction**](https://docs.zksync.io/zk-stack/concepts/transaction-lifecycle) to a rollup, an **operator** (a node or entity responsible for processing transactions) picks it up, bundles it with other transactions, compresses them, and submits the batch back to the L1 blockchain. This process allows for efficient handling of transactions as gas costs associated with the transaction, are split among all the users that submitted the transactions in the batch.

There are two types of rollups, Optimistic and Zero-Knowledge rollups. The main difference between the two lies in how each rollup verifies the validity of the transactions.

### **Optimistic Rollups**

They assume that off-chain transactions are *valid by default*. Operators propose the **valid state** of the rollup chain, and during a **challenge period**, other operators can challenge potentially fraudulent transactions by computing a **fraud proof**.

This **fraud proof process** involves the operator engaging in a *call and response interaction* with another operator to identify and isolate a specific computational step. This specific step is then executed on the Layer 1 blockchain: if the result differs from the original state, it indicates that the transaction was fraudulent. When the fraud proof succeeds, the rollup will re-execute the entire batch of transactions correctly, and the operator responsible for including the incorrect transaction will be penalized, usually by losing staked tokens (*slashing*).

### **Zero-Knowledge (ZK) Rollups**

ZK rollups use validity proofs, known as *zk proofs*, to verify transaction batches. In this process, the **prover** (operator) generates a zk proof to show that their inputs (the transactions) satisfy this equation. A **verifier** (an L1 contract) then checks this proof to ensure that the output matches the expected result. The solution that the prover uses to demostrate that their input satisfies the mathematical equation in the zk proof is commonly referred as the **witness**.

### **Conclusion**

Rollups enhance Ethereum's scalability by processing transactions off-chain, bundling them, and submitting them back to Ethereum with validity proofs. This method maintains the security and decentralization of L1 while significantly increasing transaction throughput

- How does optimistic rollups work

Let’s walk through **Optimistic Rollups** with a detailed example so you can see exactly how they work.

### What Are Optimistic Rollups?

Optimistic Rollups process transactions off the main blockchain (Layer 1, like Ethereum) and only send summarized data to L1, assuming all transactions are valid by default. They only check for fraud if someone challenges the validity of the transactions.

### How Optimistic Rollups Work: A Step-by-Step Example

Imagine there’s a sidechain (L2) built on top of Ethereum where people can make fast, cheap transactions, but the main Ethereum blockchain (L1) will still be used to finalize and secure everything.

---

### Example Scenario: Buying Concert Tickets with Optimistic Rollups

1. **User Transactions on Layer 2**:
    - Alice, Bob, and Charlie want to buy concert tickets, and the transaction process is managed on the L2 (Optimistic Rollup chain).
    - Alice sends 0.1 ETH to buy her ticket, Bob sends 0.2 ETH, and Charlie sends 0.15 ETH. All these transactions are processed by the rollup on L2 instead of directly on Ethereum’s main chain (L1).
2. **Batching the Transactions**:
    - Instead of sending each individual transaction to Ethereum’s main blockchain, the rollup operator (a special entity that handles rollups) batches all transactions.
    - These transactions are bundled together into a single **rollup batch** along with a summary that says, “Total 0.45 ETH was spent on tickets by three people.”
3. **Submitting the Batch to Layer 1**:
    - The rollup operator sends this batch summary (not the actual details of each individual transaction) to the Ethereum main blockchain (L1) and claims, “All these transactions are valid.”
    - This is called an **Optimistic Assumption** because the rollup assumes the transactions are correct without immediate proof.
4. **Challenge Period (for Fraud Detection)**:
    - After the batch is submitted to Ethereum, there is a period (e.g., one week) called the **challenge period**.
    - During this time, anyone on the network can check the batch details. If someone believes there is an invalid or fraudulent transaction, they can challenge the batch.
5. **How Fraud Detection Works**:
    - Let’s say Dave suspects that one transaction in the batch is incorrect, so he submits a challenge and provides proof to back up his claim.
    - If Dave’s proof is correct, he’s rewarded (usually with a small bounty), and the rollup operator who submitted the fraudulent batch is penalized.
    - The incorrect transactions are removed, and the rest of the valid transactions in the batch are re-submitted or corrected.
6. **Finality on Layer 1**:
    - If no one challenges the batch during the challenge period, it is accepted as valid on L1, and all transactions within it are finalized.
    - Now, Alice, Bob, and Charlie’s ticket purchases are secured by the Ethereum main blockchain without each individual transaction needing to be posted on L1.

### **Why Optimistic Rollups Are Efficient**

- **Efficiency**: By assuming that most transactions are valid, Optimistic Rollups avoid the need to submit every detail to L1, saving space and reducing costs.
- **Fraud Prevention**: The challenge period allows the network to catch invalid transactions without slowing down the whole process, keeping it fast and secure.
- **Lower Fees**: Since multiple transactions are rolled up into a single L1 submission, users pay only a fraction of the usual L1 transaction fees.

---

### Summary of Optimistic Rollups

In this example:

- **Optimism**: Transactions are assumed valid by default, making them quicker and cheaper.
- **Challenge Period**: Creates a window for anyone to catch fraud and keeps the system honest.
- **Finality**: Once the challenge period passes, transactions are finalized on the main blockchain, securing them without congestion.

Optimistic Rollups are designed to improve scalability while maintaining security through this clever use of "optimism" and optional fraud detection.

- How does ZK rollups work

Let’s explore **ZK Rollups** (Zero-Knowledge Rollups) in detail and see how they work to achieve scalability and security in blockchain.

### What Are ZK Rollups?

**ZK Rollups** (Zero-Knowledge Rollups) are a type of Layer 2 scaling solution that, like Optimistic Rollups, bundle multiple transactions together and post them as a single batch on the main blockchain (Layer 1). However, unlike Optimistic Rollups, ZK Rollups use **cryptographic proofs** called **Zero-Knowledge Proofs** (specifically, "validity proofs") to guarantee that all transactions are valid.

This approach allows for almost instant finality without the need for a challenge period, as ZK Rollups provide proof of validity upfront.

### How ZK Rollups Work: A Step-by-Step Example

Let’s walk through a simplified example where users make multiple transactions, and ZK Rollups are used to batch and validate them.

---

### Example Scenario: Sending Payments Using a ZK Rollup

1. **User Transactions on Layer 2**:
    - Suppose there’s an L2 chain where Alice, Bob, and Charlie are each sending payments to each other, similar to how they would on L1 (e.g., Ethereum).
    - Alice sends 0.1 ETH to Bob, Bob sends 0.2 ETH to Charlie, and Charlie sends 0.15 ETH to Alice.
2. **Bundling Transactions**:
    - Instead of each transaction being processed on Ethereum’s main blockchain, they are bundled on the ZK Rollup Layer 2 chain.
    - This bundle groups all individual transactions and compresses them into one “batch” that will eventually be posted to Layer 1.
3. **Creating a Zero-Knowledge Proof (Validity Proof)**:
    - To ensure that this batch of transactions is valid without revealing the actual transaction details, the ZK Rollup generates a **Zero-Knowledge Proof**.
    - This proof mathematically confirms that every transaction in the batch is valid (e.g., the balances were correct, transactions were authorized) without needing to show each transaction on L1.
4. **Posting the Batch and Proof to Layer 1**:
    - The rollup posts the batch of transactions to the Ethereum main blockchain, along with the Zero-Knowledge Proof.
    - This proof is tiny in size, so it requires minimal space on L1. Ethereum only needs to verify the validity proof, not each individual transaction, saving time and costs.
5. **Instant Finality**:
    - Once the Zero-Knowledge Proof is verified on Layer 1, all transactions in the batch are immediately considered final and valid.
    - Since the proof already guarantees validity, there is no need for a challenge period like in Optimistic Rollups, resulting in faster finality.

---

### Why ZK Rollups Are Efficient

- **Efficiency**: The main blockchain (Layer 1) only needs to verify a small cryptographic proof rather than every single transaction in the batch. This allows ZK Rollups to process many transactions at once, reducing fees and increasing throughput.
- **Immediate Security and Finality**: Since transactions are verified with Zero-Knowledge Proofs before posting to L1, there’s no need for a challenge period. This offers instant finality, making ZK Rollups ideal for applications that need high-speed, confirmed transactions.
- **Privacy**: The Zero-Knowledge Proof verifies transactions without revealing specifics, which can add an extra layer of privacy to the transactions on the blockchain.

---

### **Comparison Between ZK Rollups and Optimistic Rollups**

| Feature | ZK Rollups | Optimistic Rollups |
| --- | --- | --- |
| **Validation Method** | Zero-Knowledge Proof (validity proof) upfront | Assumes validity, uses challenge period |
| **Finality Speed** | Immediate (no waiting period) | Delayed (needs challenge period) |
| **Scalability** | High, as proofs are lightweight and fast to verify | High, but requires challenge period to confirm |
| **Privacy** | Higher, as ZK Proofs can hide transaction details | Lower, as all data is available to verify |

---

### Summary of ZK Rollups

In this example:

- **Zero-Knowledge Proof** ensures each batch of transactions is valid without showing individual transaction details, reducing storage and enhancing privacy.
- **Instant Finality** because the proof is validated upfront.
- **No Challenge Period** needed, making ZK Rollups faster and more efficient than Optimistic Rollups for certain use cases.

ZK Rollups are well-suited for applications needing high throughput, immediate finality, and privacy, such as payments, decentralized finance (DeFi), and high-frequency trading.

- If ZK rollups then why optimistic rollups?

While it might seem like **ZK Rollups** are superior since they don’t need a challenge period, **Optimistic Rollups** still exist and are widely used because they have some advantages over ZK Rollups in certain areas.

Let’s break down why **Optimistic Rollups** are still valuable:

### 1. **Complexity and Compatibility with Smart Contracts**

- **Smart Contract Support**: Optimistic Rollups are generally easier to implement for general-purpose smart contracts. Ethereum’s smart contracts were originally designed without ZK Rollups in mind, so adapting complex smart contract code to work with ZK proofs can be difficult and computationally intensive.
- **Programming Flexibility**: Optimistic Rollups use Ethereum-compatible virtual machines (such as Optimism and Arbitrum), allowing developers to use existing Ethereum smart contracts without much modification. They support a broad range of decentralized applications (dApps) with fewer technical constraints.
- **ZK Rollups Limitation**: ZK Rollups currently struggle with complex computations, like the logic-heavy, stateful smart contracts that are common on Ethereum. Creating ZK Proofs for these kinds of contracts is still an ongoing technical challenge and can be very costly in terms of computational resources.

### 2. **Computation Cost and Proof Generation**

- **Proof Generation in ZK Rollups**: Generating Zero-Knowledge Proofs is computationally intensive, especially for complex transactions or smart contracts. This requires significant computing resources and can sometimes be slow or expensive.
- **Optimistic Rollups are Less Computationally Intensive**: Since they assume transactions are valid by default and only require computation for challenges, Optimistic Rollups can handle complex transactions more easily without the high cost of proof generation.

### 3. **Current Maturity and Ecosystem Support**

- **Developer Adoption**: Optimistic Rollups have broader support and are relatively mature in terms of ecosystem adoption. Projects like **Arbitrum** and **Optimism** have developed extensive compatibility with existing Ethereum dApps.
- **ZK Rollup Ecosystem**: While ZK Rollups are advancing rapidly, the technology is newer and less mature for general-purpose applications compared to Optimistic Rollups. Many projects are still in development or early deployment stages, especially when it comes to complex dApp support.

### 4. **Use Cases Favoring Each Rollup Type**

- **Optimistic Rollups** are better suited for applications that rely heavily on smart contracts and need compatibility with Ethereum’s existing tools, such as decentralized exchanges (DEXs), lending platforms, and complex financial protocols.
- **ZK Rollups** are excellent for applications with high transaction volumes but less complex logic, like payments, token transfers, and specific DeFi applications. They excel in privacy-focused applications, where hiding transaction details is advantageous.

---

### Summary Table: Why Both Rollups Exist

| Aspect | ZK Rollups | Optimistic Rollups |
| --- | --- | --- |
| **Smart Contract Support** | Limited for complex contracts | Full Ethereum compatibility |
| **Proof Generation Cost** | Higher (computationally intensive) | Lower (only needed if challenged) |
| **Finality Speed** | Immediate (no challenge period) | Delayed due to challenge period |
| **Privacy** | Higher privacy with zero-knowledge proofs | Lower privacy; relies on public verification |
| **Ideal Use Cases** | Payments, token transfers, simple dApps | Complex dApps, DeFi, dApps needing Ethereum compatibility |

---

In short, **Optimistic Rollups** fill the gap for Ethereum-compatible dApps requiring complex smart contracts, while **ZK Rollups** are optimal for applications needing privacy, high throughput, and simple transactions. Both technologies are evolving, and it’s likely that over time, ZK Rollups will become more general-purpose—but for now, **Optimistic Rollups provide practical scalability for complex Ethereum applications** that ZK Rollups can’t yet handle efficiently.

- Operators

In rollups (both **Optimistic** and **ZK Rollups**), an **operator** is an entity or group responsible for processing transactions on the Layer 2 (L2) rollup chain, bundling them, and posting the necessary data and proofs back to the Layer 1 (L1) blockchain (like Ethereum). The operator plays a key role in making sure the rollup functions efficiently, securely, and reliably. Here’s a closer look at what operators do in each type of rollup.

---

### Role of an Operator in Rollups

1. **Transaction Aggregation**:
    - Operators collect individual user transactions that occur on L2.
    - These transactions are grouped or “rolled up” into batches, which are then submitted as a single transaction on L1.
    - This process is what allows rollups to reduce congestion and transaction costs on L1.
2. **Data Submission to L1**:
    - Operators submit summaries or proofs of the L2 transactions to L1 to finalize and secure them.
    - The way this data is posted depends on the type of rollup:
        - **Optimistic Rollups**: Operators submit batches of transactions and assume they’re valid. They’re responsible for managing the challenge period.
        - **ZK Rollups**: Operators generate Zero-Knowledge Proofs (validity proofs) to prove the batch’s validity before submitting it to L1, so no challenge period is needed.
3. **Fraud Prevention (for Optimistic Rollups)**:
    - In Optimistic Rollups, the operator is responsible for handling the challenge period, during which anyone can dispute the validity of a batch if they believe it contains fraudulent transactions.
    - Operators also deal with any challenges by potentially re-submitting corrected transactions or losing a penalty if fraud is proven.
4. **Proof Generation (for ZK Rollups)**:
    - In ZK Rollups, operators generate Zero-Knowledge Proofs for each batch, proving transaction validity cryptographically.
    - These proofs require significant computational power to produce, so the operator needs the capability to handle these computations.
5. **State Updates and Data Availability**:
    - Operators are responsible for updating the state of the rollup chain (e.g., balances, contract states) after each batch.
    - Ensuring data availability is also key, as users need to be able to access the data required to reconstruct the rollup’s state on L1 if necessary.

---

### Who Can Be an Operator?

- **Centralized vs. Decentralized Operators**: In some rollup implementations, operators are centralized entities (e.g., a single organization), while in others, they might be decentralized networks of nodes.
- **Staking Requirements**: In certain rollup systems, operators might need to stake tokens as collateral, which they forfeit if they’re found to process fraudulent transactions. This helps maintain trust in the system.
- **Decentralization Plans**: Many rollups are moving toward decentralizing operators to avoid central points of failure and censorship risks, aiming for models where multiple operators can take turns in transaction processing or compete for the role based on reputation and collateral.

---

### Why Operators Matter

Operators are crucial for the security and efficiency of rollup systems. They ensure that transactions are bundled, validated, and posted to the main blockchain correctly and fairly. In decentralized rollup systems, operators might evolve to resemble miners or validators, where multiple parties share the responsibility of securing the network, adding to the rollup’s decentralization and security.

- Sequencers

In rollups, a **sequencer** is a specialized operator responsible for ordering and processing transactions on Layer 2 (L2). They play a critical role in managing the flow of transactions efficiently. Let’s dive into what sequencers are, their function, and the concept of centralized sequencers.

---

### What is a Sequencer?

A **sequencer** is a key component in a rollup that:

1. **Receives Transactions**: The sequencer receives and orders all incoming transactions on the rollup’s L2 network.
2. **Creates Batches**: It bundles transactions into batches to be posted on the main blockchain (Layer 1).
3. **Provides Fast Confirmation**: The sequencer can instantly confirm transactions on L2, meaning users don’t have to wait for L1 confirmation to see their transactions processed.
4. **Maintains Order**: By ordering transactions, the sequencer prevents issues like double-spending and maintains consistency in the rollup’s state.

### Why Sequencers Are Important in Rollups

Sequencers help rollups achieve high throughput, low fees, and fast transaction finality on L2, while still ensuring that all transactions are eventually verified on L1. For example:

- **In Optimistic Rollups**: The sequencer posts transaction batches along with minimal data to L1. During the challenge period, any disputes can be raised if a batch is suspected of containing invalid transactions.
- **In ZK Rollups**: The sequencer is also responsible for generating Zero-Knowledge Proofs and submitting them to L1 to prove the validity of each batch.

---

### Centralized Sequencers

In many rollup implementations, especially early versions, the sequencer is **centralized**, meaning a single entity or organization operates it. This is called a **centralized sequencer**, and it has certain implications:

1. **Faster Operations**: A centralized sequencer can be optimized to process transactions very quickly, providing fast confirmations on L2 without requiring consensus among multiple nodes.
2. **Single Point of Control**: Since a single entity is in control, they can prioritize transactions, manage the rollup’s state, and control the order in which transactions are processed.
3. **Centralization Risks**:
    - **Censorship**: A centralized sequencer can potentially censor or reorder transactions, which goes against the decentralization ethos of blockchain.
    - **Downtime**: If the centralized sequencer goes offline or is compromised, transaction processing could halt, impacting the rollup’s availability.
    - **Trust Assumptions**: Users must trust the centralized sequencer to act honestly, especially when processing transactions and ensuring data availability on L1.

---

### Decentralized Sequencer Models (Future Vision)

Many rollup projects plan to decentralize their sequencers over time to improve security, censorship resistance, and decentralization. Here’s how a decentralized sequencer model would work:

1. **Multiple Sequencers**: In a decentralized model, multiple entities would operate sequencers, either in a permissionless or permissioned environment.
2. **Consensus Among Sequencers**: Similar to validators or miners, sequencers would reach consensus on transaction ordering, making it harder for any single party to censor or manipulate transactions.
3. **Incentives and Slashing**: Sequencers might need to stake tokens as collateral, ensuring they act honestly; otherwise, they risk losing their stake if they engage in fraud or censorship.

---

### Summary

| Feature | Centralized Sequencers | Decentralized Sequencers |
| --- | --- | --- |
| **Speed** | Very fast, with low latency | May be slightly slower due to consensus needs |
| **Control** | Single entity orders and batches transactions | Shared control among multiple participants |
| **Security & Trust** | Requires trust in one entity | More censorship-resistant, less need for trust |
| **Censorship Resistance** | Vulnerable to censorship | Resistant to censorship, as control is distributed |
| **Reliability** | Downtime risk if the sequencer fails | Higher reliability with multiple sequencers |

In summary, centralized sequencers provide efficiency and simplicity, but come with trust and censorship risks. Moving to decentralized sequencers is an evolving approach that aims to combine the benefits of high transaction throughput with enhanced security and decentralization.

- Operators vs Sequencers

Sequencers and operators are related but not exactly the same. Here’s a breakdown:

### Key Differences Between Sequencers and Operators

1. **Function and Role**:
    - **Operators**: This term is broader and refers to any entity responsible for managing the rollup’s transactions, including aggregating them, validating them, and posting them to the main blockchain (Layer 1). Operators ensure the integrity and security of the rollup by overseeing the overall process.
    - **Sequencers**: A sequencer is a specific type of operator primarily focused on ordering transactions, creating batches, and providing fast, near-instant transaction confirmation on Layer 2. Sequencers handle the transaction flow in real time on L2, but may not perform all tasks that an operator does.
2. **Scope of Responsibility**:
    - **Operators**: Their scope can include responsibilities beyond just transaction ordering, like fraud detection (for Optimistic Rollups) or generating Zero-Knowledge Proofs (for ZK Rollups).
    - **Sequencers**: Their primary responsibility is efficient transaction ordering, batch creation, and managing the transaction pool on Layer 2. They help optimize the user experience by confirming transactions instantly on L2, but they typically rely on operators to finalize and validate these transactions on L1.
3. **Centralization and Decentralization**:
    - **Sequencers**: In many cases, sequencers are initially centralized for efficiency, but projects plan to decentralize them over time.
    - **Operators**: An operator can be a single entity or a set of decentralized participants who manage various aspects of the rollup system.

---

### Summary: Are Sequencers Operators?

You could think of sequencers as a **type of operator** with a specific focus on transaction ordering and batching, but not necessarily responsible for every aspect of rollup management. The term “operator” can be used more broadly, while “sequencer” is more specific to the task of transaction sequencing and fast L2 confirmation.

- Composability

It is the ability of smart contracts to interact with each other

- Revert

A revert action undoes all prior operations and returns the remaining gas to the transaction’s sender. If a transaction reverts, it is defined as failed. The gas that has already been used in the transaction will not be refunded if the transaction fails due to a revert statement. 
The has already been consumed because the code was executed by the computers. The gas which was needed to be required by the computation if the transaction had not failed would be returned back to the user.

- ChainLink

### **How Chainlink Works**

Chainlink is a *modular and decentralized Oracle Network* that enables the integration of data and external computation into a smart contract. When a smart contract combines on-chain and off-chain data, can be defined as **hybrid** and it can create highly feature-rich applications.

Chainlink offers ready-made features that can be added to a smart contract. And we'll address some of them:

- **Data Feeds**
- **Verifiable Random Number**
- **Automation (previously known as "Keepers")**
- **Functions**

### **Chainlink Data Feeds**

*Chainlink Data Feeds* are responsible for powering over $50 billion in the DeFi world. This network of Chainlink nodes aggregates data from various **exchanges** and **data providers**, with each node independently verifying the asset price.

!https://updraft.cyfrin.io/solidity/remix/lesson-4/datafeeds/datafeed2.png

They aggregate this data and deliver it to a reference contract, the **price feed contract**, in a single transaction. Each contract will store the pricing details of a specific cryptocurrency

!https://updraft.cyfrin.io/solidity/remix/lesson-4/datafeeds/datafeed1.png

### **Chainlink VRF**

The Chainlink VRF (Verifiable Random Function) provides a solution for generating **provably random numbers**, ensuring true fairness in applications such as NFT randomization, lotteries, and gaming. These numbers are determined off-chain, and they are immune to manipulation.

!https://updraft.cyfrin.io/solidity/remix/lesson-4/datafeeds/datafeed3.png

### **Chainlink Automation (previously known as "Keepers")**

Another great feature is Chainlink's system of *Keepers*. These **nodes** listen for specific events and, upon being triggered, automatically execute the intended actions within the calling contract.

### **Chainlink Function**

Finally, *Chainlink Functions* allow **API calls** to be made within a decentralized environment. This feature is ideal for creating innovative applications and is recommended for advanced users with a thorough understanding of Chainlink ecosystem.

### **Conclusion**

*Chainlink Data Feeds* will help integrate currency conversion inside of our `FundMe` contract. Chainlink's decentralized Oracle network not only addresses the 'Oracle problem', but provides a suite of additional features for enhancing every dApp capabilities
