https://www.youtube.com/watch?v=lBpa0b0ws5I

The Bitcoin network follows the leader election-based consensus mechanism. The network uses **the Proof of Work (PoW)** consensus algorithm to select the leader. We know that consensus is the base factor deciding the following block to the blockchain network. In a public blockchain like Bitcoin, anyone can create a block. Each block will be different, and each block may contain different transactions. Therefore, the network should choose a single block from the different candidate blocks to maintain the blockchain’s consistency. Otherwise, the network nodes will not have a standard blockchain, affecting its purpose.

Selection of Blocks

The network selects a node as a leader. The leader node publishes the block it creates. According to Proof of Work , the nodes competing as leaders need to solve a [**cryptographic puzzle**](https://learn.kba.ai/course/blockchain-foundation-program/lessons/cryptographic-puzzle/). Whoever solves the puzzle will be chosen as the leader. By checking the leader’s solution for the puzzle, the authenticity is determined. The nodes competing to solve the puzzle are mining nodes or [**miners**](https://learn.kba.ai/course/blockchain-foundation-program/lessons/components-of-bitcoin-network/). These miners are responsible for the creation of new blocks in Bitcoin. Miners are rewarded with a fixed amount of Bitcoins for adding new blocks.

Let’s get further and check what this cryptographic puzzle is all about.

# Cryptographic Puzzle

### What is the puzzle all about?

The cryptographic puzzle involves finding a [hash value](https://www.tutorialspoint.com/cryptography/cryptography_hash_functions.htm) below a certain threshold. Such that the generated hash value will have a certain number of zeros preceding it. For example, consider the following hash value in [hexadecimal](https://en.wikipedia.org/wiki/Hexadecimal) representation. Let’s assume this is our threshold.

0000000000000000001101190000000000000000000000000000000000000000

In order to find the solution, you need to find a hash value below this number. For a hash to be below this number, it should have these many leading zeros. For example, consider the following hash as solution. It is below the threshold.

00000000000000000000a2b79f6b75a04fe4ebdfefcc1213ba22dfa59ac9e985

As you can see from the above example, miners in a Bitcoin network compete to solve the puzzle by finding a hash value below a threshold. The network decides the threshold value. And miners know the value.

### How to solve cryptographic puzzle?

Miners calculate the hash of their block’s header. The hash value is compared with the desired threshold value.

If the hash value is higher than the threshold value, the hash is recalculated by increasing the nonce number in the header. This process is repeated until a hash value lesser than the desired threshold is found.

Note that, even a small change in the input for a hash function will result a completely different hash value (avalanche effect). It is, therefore, difficult to predict the output for each nonce value. The mining nodes have to iterate through different nonce values until they find one proposing solution. It’s a computationally-intensive process as miners need to compute enormous number of hashes within short time.

The puzzle is set for 10 minutes. Once a node finds the solution, it can publish the block along with the solution, to the network. The solution to this puzzle can be verified easily, but finding the solution is very difficult. In order to check the solution, the miners calculate the hash of the winning block’s header along with the nonce included in it. If the hash falls below the threshold, the block is valid. Other nodes in the network can easily check if the solution is valid or not and accept the block accordingly. In other words, the winning node provides proof of the work done to its peers, hence the name Proof of Work.

You can experiment with the following tool to generate hash values for different texts. Note that even a small change in the input text affects the entire hash value.

**Note:** The below hashing algorithm is SHA256, which stands for Secure Hash Algorithm. Bitcoin uses SHA256.

# Cryptographic Puzzle

### What is the puzzle all about?

The cryptographic puzzle involves finding a [hash value](https://www.tutorialspoint.com/cryptography/cryptography_hash_functions.htm) below a certain threshold. Such that the generated hash value will have a certain number of zeros preceding it. For example, consider the following hash value in [hexadecimal](https://en.wikipedia.org/wiki/Hexadecimal) representation. Let’s assume this is our threshold.

0000000000000000001101190000000000000000000000000000000000000000

In order to find the solution, you need to find a hash value below this number. For a hash to be below this number, it should have these many leading zeros. For example, consider the following hash as solution. It is below the threshold.

00000000000000000000a2b79f6b75a04fe4ebdfefcc1213ba22dfa59ac9e985

As you can see from the above example, miners in a Bitcoin network compete to solve the puzzle by finding a hash value below a threshold. The network decides the threshold value. And miners know the value.

### How to solve cryptographic puzzle?

Miners calculate the hash of their block’s header. The hash value is compared with the desired threshold value.

If the hash value is higher than the threshold value, the hash is recalculated by increasing the nonce number in the header. This process is repeated until a hash value lesser than the desired threshold is found.

Note that, even a small change in the input for a hash function will result a completely different hash value (avalanche effect). It is, therefore, difficult to predict the output for each nonce value. The mining nodes have to iterate through different nonce values until they find one proposing solution. It’s a computationally-intensive process as miners need to compute enormous number of hashes within short time.

The puzzle is set for 10 minutes. Once a node finds the solution, it can publish the block along with the solution, to the network. The solution to this puzzle can be verified easily, but finding the solution is very difficult. In order to check the solution, the miners calculate the hash of the winning block’s header along with the nonce included in it. If the hash falls below the threshold, the block is valid. Other nodes in the network can easily check if the solution is valid or not and accept the block accordingly. In other words, the winning node provides proof of the work done to its peers, hence the name Proof of Work.

You can experiment with the following tool to generate hash values for different texts. Note that even a small change in the input text affects the entire hash value.

**Note:** The below hashing algorithm is SHA256, which stands for Secure Hash Algorithm. Bitcoin uses SHA256.

# The Difficulty Level and Mining

Bitcoin networks depend on an incentive mechanism. Miners that validate transactions and create blocks, gets bitcoins as rewards. This process is known as ****Bitcoin Mining****. Initially, the reward was 50 bitcoins. The reward halves every four years. At the time of writing this content, the reward is 6.25 Bitcoins per block. Via Bitcoin Mining new bitcoins entered into circulation.

### How many bitcoins? Is there a limit??

Only 21 million Bitcoins can be produced by the network. What happens next. Bitcoin miners will no longer receive bitcoins; Transaction fees will be rewarded in place of bitcoins. In 2140, Bitcoin supply is expected to reach its full.

### **The Difficulty Level**

As more and more nodes joined the Bitcoin network, the solutions emerged more frequently and there was a more frequent generation of blocks and incentives. This was against the Bitcoin economic model. The concept of ****difficulty**** helped with this problem. Difficulty decides how frequently the miners can find the solution for the puzzle and publish the block. The average block creation time of the Bitcoin blockchain is 10 minutes which varies when a large number of nodes enter the network. To maintain the block creation time, the time is readjusted after every 2016th block. For example, if the block creation time is below 10 minutes, the threshold value will be decreased to increase difficulty. Likewise, if the block creation time is above 10 minutes, the threshold value will be increased to decrease difficulty.

The difficulty of the “cryptographic puzzle” may reach a point where the computational power of a single system might not be sufficient. In such scenarios, the mining nodes pool their resources and share their computational powers over the network. These are called ****mining pools****. The pool members work together to solve the puzzle. Based on the individual contributions (in terms of computational power) pool members get rewarded.

# Fork Resolution

In blockchains, forking indicates any divergence in the chain, for instance, a new branch is created within the chain. There are mainly 2 types of forks: ****hard forks**** and ****soft forks****.

### **Hard Fork**

A hard fork is a permanent change that may occur as a result of a change in the underlying software or the consensus algorithm used by the chain. This type of forks results in splitting the blockchain into separate branches. The network gets divided based on the branch they follow. Once hard fork occurs, the branches will continue to exist as separate blockchains with a common parent chain. If fork takes place on software upgrade, the nodes running older versions get rejected.

Hard forks are not backward compatible. A hard fork is a fundamental change to the protocol that makes previously valid blocks or transactions invalid. Any transaction in the new “branch” or chain will be invalid on the old chain.

![](https://learn.kba.ai/wp-content/uploads/2021/10/fork.png)

### **Soft Fork**

Soft forks are backward compatible. They do not result in permanent splitting of the blockchain. Soft fork takes place when two mining nodes find the solution at the same time. There will be two valid blocks in the network and the nodes will add both blocks to their blockchain, resulting forking. To avoid chain splitting, the network should choose one single branch.

How network choose a branch?

Miners use the **longest chain rule** to choose a branch. The longest chain rule suggests choosing the longest branch in the network. The longest chain is the chain with the most cumulative difficulty. In most cases, the longest branch will have more number of blocks. However, if branches of the same length emerge, summation of the work of branches are calculated. The branch with the highest work is considered the longest.

![](https://learn.kba.ai/wp-content/uploads/2021/10/Longest_chain.png)

### Steps Thereafter

Mining nodes starts mining on top of the longest chain. The hash of the last block from the longest chain is added as the previous hash value in the newly created block. Eventually, the longest chain is accepted and the blocks in other chains is discarded.

To avoid situations of blocks getting discarded, the Bitcoin network suggests users to wait until six blocks are added on top of a block. Transaction is said to get confirmed if six blocks go after. In the above diagram, the branch ‘B2’ will be discarded, as it is not the longest chain. Such blocks are called ****Stale**** blocks. There is no reward for mining stale blocks. Occasionally there can be blocks with no valid parent block. These blocks whose parent blocks are not processed by the local nodes are known as ****Orphan**** blocks.

When two blocks are mined within a small time interval and they are received in the opposite order, i.e. child before parent, orphan blocks are formed. The orphan blocks cannot be validated and they are stored in the orphan block pool until their parent block is received. They can be pulled from the orphan block pool and made part of the chain once the parent block is received.

The following video explains how a network maintains the same copy of blockchain even if forks appear.

https://www.youtube.com/watch?v=J1wAgWfX4Pw