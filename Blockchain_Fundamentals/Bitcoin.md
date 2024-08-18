# What is Bitcoin?

_![](https://learn.kba.ai/wp-content/uploads/2021/11/BTC-300x300.png)_

_Bitcoin is a technology._ _It is also a currency._

_It is a decentralized international network of payments that_ _doesn’t rely on banks or governments._

It is the first-ever application of blockchain. In 2008, Satoshi Nakamoto introduced Bitcoin to the world through a nine-page white paper **[Bitcoin: A Peer-to-Peer Electronic Cash System](https://bitcoin.org/bitcoin.pdf)“**. It called itself the digital representation of value that can be digitally traded. _bitcoin simply acts as medium of exchange; a unit of account; a store of value_.

Today, the cryptocurrency is widely used in exchanging goods and services. Also, it is extensively used for investment purposes.

# Bitcoin/bitcoin/Blockchain- Get It Right

**Bitcoin** is a piece of software used for communication.

**bitcoin** is a digital cryptocurrency used for transactions.

**Blockchain** is an underlying technology running bitcoin.

# How is bitcoin different from fiat currency?

Central jurisdictions like Bank/ Government issue the **Fiat currency**. It is a legal tender.

**bitcoin** isn’t issued or backed by any jurisdiction. Thus, no legal tender status for **bitcoin**. It fulfills the functions via the agreement between the bitcoin community. bitcoin realizes direct online payments without relying on banks or government.

bitcoin is a virtual currency, therefore, it cannot be printed. There is no physical form for bitcoin like coins or currency notes.

_Read about the first country to use bitcoin as legal tender_ [_here_](https://www.livemint.com/news/world/el-salvador-becomes-first-country-to-use-bitcoin-as-legal-tender-11631144769412.html)

# How do people acquire bitcoin?

There are different ways of earning bitcoins (BTC) –

**Earn – Get paid in bitcoin**

- Offer a service – cut hair, wash cars, drive a taxi.
- Sell a product – homemade baklava, gourmet coffee, keychains.
- Wages – ask your employer to pay part of your wages in BTC.

**Buy – Exchange national money (fiat) for bitcoin.**

- Through an exchange – a company offering a service for buying and selling BTC.
- Using ATM – a vending machine selling bitcoin for cash.
- From another person directly, for cash.

**Trade – Trade your belongings for bitcoin**

- Sell your car for BTC.
- Sell your house for BTC.

**Mining – Help in creating blocks in Blockchain**

- Receive miner’s reward by solving a computationally hard [cryptographic puzzle](https://learn.kba.ai/course/blockchain-foundation-program/lessons/cryptographic-puzzle/) to create new blocks.

_The value of BTC is determined by demand and supply. As demand goes up, the price goes high. As supply goes high, the price goes down._


# Components of Bitcoin Network

Four components are concocted to make Bitcoin.

- **Software**
- **Cryptography**
- **Hardware**
- **Miners**

Let us see one by one.

We early read Bitcoin is a piece of **software**. The software uses **cryptography** to regulate the transfer of bitcoin between two parties. Also, the creation of new units of bitcoin.

### **So what is Cryptography?**

_[Cryptography](https://en.wikipedia.org/wiki/Cryptography) is the practice and study of techniques for secure communication in the presence of adversarial behavior._

### **Next comes the Bitcoin Hardware………….**

To run a Bitcoin, it needs **hardware** like any other software application. Bitcoin network is composed of thousands of computers called nodes operating around the globe. Each transaction is a public entry in the Bitcoin blockchain and it demands active participation from these nodes.

Based on node’s utility, they are classified into:

- **Full Node**: A full node maintains the latest complete blockchain of the network. It autonomously and authoritatively verify the transaction without any external reference.
- **Lightweight Node**: Lightweight nodes do not keep a copy of the complete blockchain. Instead, they store only the header information of each block. Thus saving the storage space.
- **Miner Node**: A miner node engages in the mining operation of the blockchain using appropriate consensus algorithm, generally with an advanced set of hardware capabilities . They are responsible for validating transactions and creating new blocks.
- **Router Node**: A router node in blockchain has a similar function as a node in any network. It acts as a bridge in directing requests to the appropriate device for processing transactions.

Among the nodes , miner nodes have an important role to play. Miner nodes are responsible for validating transactions and creating new blocks in the Bitcoin network.

### Why the name Miner?

To create a block, miner computationally hard cryptographic puzzle. The miners get rewarded when they solve this puzzle. Thus the miners are rewarded for their effort and are motivated to run their mining computers in the network. Miners get paid for their service- similar to how a gold miner is rewarded with gold.

Want to learn more about the cryptographic puzzle? visit [here](https://learn.kba.ai/course/blockchain-foundation-program/lessons/cryptographic-puzzle/).

# Working of Bitcoin Network

The bitcoin’s total supply is 21 million. The limit is for giving anti-inflationary properties to bitcoin. New bitcoins enter circulation when miners create new blocks. And once the 21 million limits reach, no further bitcoins are created.

### Miners and Their Rewards

The network issues reward for miners creating new blocks. Rewards are transaction fees associated with each transaction. Initially, the reward for the blockchain miner was 50 bitcoins; this reward gets halved approximately every four years. Currently, it is 6.25 bitcoins for the miner.

### Bitcoin Transaction

A bitcoin transaction involves the transfer of bitcoin from one address to another. The sender must sign the bitcoin transaction to make it valid. The signed transaction gets sent across the network, where each mining node verifies the transaction. The miners then combine all the transactions they receive to form a block. There will be many different transactions in each miner’s block. Bitcoin blockchain limits the size of a block by 1 MB. Therefore, each miner includes transactions till 1 MB and adds the remaining transactions to the next block.

What’s next?

Once the block gets created, the miners compete to solve a [puzzle](https://learn.kba.ai/course/blockchain-foundation-program/lessons/cryptographic-puzzle/). Once the miner finds the solution, it publishes the block to other nodes. Other nodes in the network verify the block and add to their copy of the blockchain. Thus every node in the network gets a similar copy of the blockchain.

_Time taken to solve the puzzle is approximately 10 minutes._

# UTXO

Blockchain is a canonical list of transactions ever recorded by the network. Tracing back, one can easily stroll through the transaction history. The transaction input and output get traced to the instant it got created.

How??

**UTXO** or **Unspent Transaction Output** keeps track of the transactions and account balances in the Bitcoin blockchain.

### **What is UTXO?**

UTXO is similar to physical cash/coins-based transactions in the real world. For example, imagine a scenario. Alice spends cash in a shop, gives the entire notes she has, takes the goods, and takes back the remaining change. If Alice got a cash note of 10 dollars and wants to buy goods priced five dollars, she doesn’t divide the note in half for the payment. Instead, she gives the entire note and takes a new five-dollar note as a change along with the goods.

UTXOs work similarly. Each bitcoin transaction got two parts- inputs and outputs.  
The input specifies the amount of bitcoin used for that transaction, in our example, the 10 dollars. Likewise, the output specifies the amount and address of the recipient. In our example, five dollars to the shop and balance five back to Alice.

![](https://learn.kba.ai/wp-content/uploads/2021/10/Screenshot_from_2021-09-28_17-06-22.png)

Once the transaction is complete, the shop will have 5 BTC in their account, and Alice will have the balance of 5 BTC updated in her account. These are outputs of the transactions. Now, the shop and Alice can use these transaction outputs for other transactions as inputs in that transaction.

![](https://learn.kba.ai/wp-content/uploads/2021/10/Screenshot_from_2021-09-28_17-16-42.png)

# Blockchain Consensus

A single regulatory body makes decisions in a centralized setup. On the other side, no single authority makes decisions in a blockchain.

_So how does blockchain work?_

Blockchain works on a consensus model. It helps blockchain nodes to come up with a favourable solution. Blockchain nodes agree on a single source of truth using blockchain consensus. It ensures every network node has the exact copy of the blockchain, and the network works properly even in the presence of faulty nodes.

Based on the selection and addition of blocks to the blockchain, blockchain consensus is classified into two:

- **Voting-based consensus**: This method depends on voting mechanisms to finalize the block to be published. The consensus model is not computationally intensive and relies on achieving consensus by sending signed messages as votes. For example [PBFT](https://learn.kba.ai/course/blockchain-foundation-program/lessons/practical-byzantine-fault-tolerance/), RAFT, etc.
- **Lottery-based consensus**: The consensus mechanism depends on the chance-based lottery election model to select the block to be published. For example [Proof of Work](https://learn.kba.ai/course/blockchain-foundation-program/lessons/proof-of-work/), [Proof of stake](https://learn.kba.ai/course/blockchain-foundation-program/lessons/proof-of-stake/), etc.

Bitcoin blockchain utilizes Proof of Work as their consensus mechanism. The mining and computational puzzle solving are part of the Proof of Work consensus.