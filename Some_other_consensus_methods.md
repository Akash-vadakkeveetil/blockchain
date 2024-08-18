
# Proof of Stake

The [Proof of Stake (PoS)](https://ethereum.org/en/developers/docs/consensus-mechanisms/pos/) consensus algorithm got introduced in 2011. The aim was to solve the problems associated with **Proof of Work**. While they share the same purpose-blockchain consensus, the process is different. PoW requires large computational capabilities to solve puzzles. Therefore, it uses a large amount of electricity and power. Proof of Stake links the mining power to the number of coins a person possess rather the computational power. In PoS, the miner is limited to mining a percentage of transactions reflective of their ownership stake.

PoS is a type of consensus algorithm that emphasis obtaining distributed consensus. The block creator is chosen based on their stake in the specific blockchains that use Proof of Stake. In this network, a person can mine or validate blocks depending on the number of stakes they holds (in cryptocurrencies). The more the stakes, the more is the mining (actually forging/minting) power.

Bitcoin network is vulnerable to a “51% attack”. A “51% attack” is when a miner or mining pool controls 51% of the network’s computational power and creates fraudulent blocks of transactions for himself while invalidating the transactions of others in the network. With Proof of Stake, the attacker would need to obtain 51% of the cryptocurrency to carry out a 51% attack. Although it would be difficult and expensive to accumulate 51% of the total coins, a miner with a 51% stake in the coin would not attack a network he holds the majority share. If the value of the cryptocurrency falls, the value of the holdings would also fail.

**Working of PoS**

In the PoS system, blocks are **forged** or **minted**, not mined. The individuals validating the transactions, creating new blocks are called forgers. In most Proof of Stake networks, the digital currency units are built at the currency’s launch, and their number is fixed. Therefore, the forgers receive transaction fees as rewards instead of cryptocurrencies. A forger must first put their coins at stake to validate transactions and create blocks. If forgers validate a fake transaction, they lose their coins and their rights to participate as a forger in the future.

### **The Selection Criteria**

The forger is chosen randomly, depending on the stake. Selection by stake would result in (undesirable) centralization, as the single richest member would have a permanent advantage on the system. Instead, several different methods of selection have been devised.

- - **Randomized block selection:** It uses a formula that uses the lowest hash value in combination with the size of the stake to predict the next generator. Since the stakes are public, each node can predict which account will next win the right to forge a block with reasonable accuracy.

- - **Coin age-based selection:** It combines randomization with the concept of coinage. Coinage is the product of the number of coins multiplied by the number of days the coin has been held. Coins that have not been spent  30 days begin competing for the next block.

### **Advantages of PoS**

- - Energy Efficiency.
    - Randomization in PoS prevents centralization.
    - No one will try to attack the network as it would vastly decrease the value of the attacker’s coins.
    

### **Disadvantages of PoS**

- - **Nothing at stake problem**: In PoW based blockchains, validators (miners) need computational power for adding new blocks. Miners have to select one branch from the fork as it is practically impossible to mine on both branches. Thus computational power played a major role in fork resolution. In the PoS based blockchains, validators need a stake for adding new blocks and no need for any computational power. So the validators can create blocks on top of multiple branches using their stake. This results in miners collecting rewards even when one branch is selected. There is nothing to lose for a validator, even if he keeps staking on both branches. This problem is referred to as nothing-at-stake problem. In order to avoid this, the stake can be taken by the network as a punishment for staking on two blocks simultaneously.

### **Variants of PoS**

- Delegated Proof of Stake
    - Liquid Proof of Stake
    - Bonded Proof of Stake
    - Hybrid Proof of Stake

# Practical Byzantine Fault Tolerance

https://www.youtube.com/watch?v=Qzd7IFUhj5A

When we talked about consensus, we saw consensus algorithms can be classified into two, lottery-based and voting-based. Proof of Work comes under random leader election lottery-based consensus. Now we will the voting-based consensus algorithm. Here the participants vote on a block created by the leader to reach an agreement.

### What is PBFT?

[Practical Byzantine Fault Tolerance (PBFT)](http://pmg.csail.mit.edu/papers/osdi99.pdf) is a consensus algorithm introduced by Barbara Liskov and Miguel Castro in 1999. PBFT optimizes the concepts of Byzantine Fault Tolerance in solving the Byzantine General’s problem. In a distributed computer network, Byzantine Fault Tolerance is the scenario where we can achieve correct consensus despite the presence of malicious nodes in the network that fails or send incorrect information. PBFT works efficiently in the asynchronous system. It is optimized for low overhead time.

### ****Advantages of PBFT****:

- - ****Energy efficiency****: PBFT does not require complex mathematical computations (like in PoW) in achieving network consensus.
    - ****Transaction finality****: If the nodes in the network agree upon a proposed block, then that block is final. Thus it does not require multiple confirmations like in Proof-of-Work models.
    - ****Low reward variance****: All nodes in the network participate in decision making and all nodes in the system, therefore, will be incentivized to reduce reward variance for miners.

### ****Working of PBFT****

The PBFT model ensures that the network will achieve sufficient consensus despite the malicious nodes present in the system. All the nodes in the PBFT system are sequentially ordered with, one node as the leader or ****primary**** ****node**** and other nodes as secondary or backup nodes. All nodes are eligible to become the primary node. A ****view**** is a period in which a given node is the primary (leader) of the network. All nodes in the system communicate with each other so that all honest nodes will come to an agreement on the state of the system based on a majority rule. A PBFT system can be successful if the maximum number of faulty nodes does not exceed or remain equal to one-third of all the nodes in the system. Therefore, in a PBFT network, the total number of nodes can be represented as __3f + 1,__ where __f__ is the maximum number of faulty nodes the network can tolerate.

### Working Phases

To commit a block and make progress, the nodes in a PBFT network undergoes three phases:

1. 1. ****Pre-prepare:**** The primary node will create a block and publish it to the network in a given view. The secondary nodes will receive this block and do some preliminary verification of this block in order to ensure that it is a valid block. Then the primary node broadcasts a pre-prepare message to all other nodes. This message contains the ID of the block, the block number, the primary view number, and the primary node’s ID. All the nodes will validate this pre-prepare message and then add the message and block to the node’s internal log.
    2. ****Prepare:**** In this phase, each node will send a prepare message to all the nodes in the network including itself. The prepare message contains the block ID, block number, node’s view number, and its ID. Nodes must wait till they receive __2f+1__ matching prepare messages from their peers, where __f__ is the maximum number of faulty nodes allowed. Once the node gets __2f+1__ prepare messages, the messages get added to their internal log.
    3. ****Commit:**** In this phase, each node will send a commit message to the entire network including themselves. The commit messages contain the block ID, block number, node’s view number, and its ID. Just like the prepare phase, nodes wait until they receive __2f+1__ matching commit messages. Once a node gets __2f + 1__ matching commit messages, the messages get added to the log and the block gets committed to the blockchain.

Once the primary node finishes the committing phase, it will create a new block and repeat the process. After each view, a new node will be elected as the primary.

As you can see, each node votes on the block to be published. The primary will add a block to the blockchain only after receiving a sufficient number of votes.

What will happen if _a node does not receive 2f+1 messages_? This means that the network failed to reach an agreement regarding the proposed block, implying more than __f__ nodes in the network are faulty. There can also be scenarios where the primary node becomes faulty. In such cases, the network will fail to reach an agreement that will affect the working of the blockchain network. In order to prevent such scenarios, each view has a time period. If the network couldn’t reach an agreement within the view, any node in the network can request a view change. In the next view, a new node will be elected as primary and the process gets repeated.

****Variants of PBFT****

- - ****RBFT:**** Redundant Byzantine Fault Tolerance (RBFT) is an approach proposed to tackle the robustness problem. In RBFT, multiple instances of Byzantine Fault Tolerance protocol is run in parallel so as to monitor the performance, mainly for detecting malicious primary. Hyperledger Indy uses RBFT.
    - ****IBFT:**** used in Quorum, Hyperledger Besu.
    - ****SBFT:**** Speculative Byzantine Fault Tolerance(SBFT) or Zyzzyva protocol reduces the cost and simplifies the design of BFT state machine replication.
