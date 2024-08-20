# Ethereum World Computer

Ethereum’s vision is to create a single blockchain for the entire world calling Ethereum World Computer.

![](https://learn.kba.ai/wp-content/uploads/2021/11/ewc-300x157.png)

Ethereum World Computer is a group of individual computers forming one massive computer. Each computer in the network will run a program called _Ethereum Client._ The Ethereum Client helps other systems to collaborate and form the Ethereum World Computer.

Now, this was an amazing idea. It needed certain key properties for such a system to exist and maintain its integrity.

- Deterministic
- Isolation
- Terminability

**Deterministic**

Any operation or program is deterministic if it gives the same output every single time to a given set of inputs, regardless of the systems or the processing speed. Any operations or programs running in Ethereum World Computer should be of deterministic nature. This is to uphold the system’s integrity. A program becomes non-deterministic if a non-deterministic system function is invoked. Or taking in the non-deterministic data source as input during runtime.

**Isolation**

Ethereum World Computers are formed by interconnecting computers from all over the world. An Ethereum Client program is executed to achieve this result. Via clients, anyone can upload smart contracts into the Ethereum World Computer. However, in case any contract contains viruses and bugs, and is not isolated, it can hamper the whole network. Any program running on the computer should not affect the working of Ethereum World Computer. Thus these Ethereum clients should run as isolated entities.

**Terminability**

The smart contracts are self-executing programs; once triggered, there is no way to intervene and stop. The program may enter into an endless loop that would drain the ecosystem’s resources. It will be unknown whether or not a contract can execute within a given amount of time, also known as the **Halting Problem,** leading to a non-deterministic scenario. A mechanism should be in place to counter this. There are many ways in which we can implement such a measurement.

- **Step:** The contract can simply keep track and limit the number of **steps** it has taken.
- **Timer**: A predetermined timer can be kept. If the contract execution exceeds the time limit then its execution is aborted.
- **Turing Incompleteness**: A Turing Incomplete smart contract language will have limited functionality and not be capable of making jumps and/or loops. Hence they can’t enter an endless loop.
- **Fee-meter:** A contract is a program, and a program is a set of instructions, we can put a fee or cost for each instruction to be executed, and specify a limit for the fee to be used for each contract execution. Ethereum uses this method, here the contracts are executed with a prepaid fee and every instruction requires a particular amount of fee. If the fee spent exceeds the pre-paid fee then the contract is terminated. For the Ethereum blockchain, the **fee is paid using its native cryptocurrency called Ether**.

To ensure the above properties, it is critical for a contract to be kept isolated in a sandbox to save the entire ecosystem from any negative effects. This sandbox environment is called an **Ethereum Virtual Machine.**


# Ethereum Virtual Machine (EVM)

**EVM** is “the runtime environment for smart contracts in Ethereum”. A smart contract is a self-executing program that resides in EVM.

**EVM: The Need Behind**

The Ethereum World Computer, for its continued existence, needs to accomplish three features. The running programs on the Ethereum world computer should run exactly as programmed – **Deterministic.** Anything and everything on the Ethereum World Computer should be terminatable at will – **Terminable.** The system should not be affected by any external factors – **Isolated.**

EVM enables smart contracts (EVM Code) to get executed on any operating system. It acts as a middle layer between the smart contract and the operating system. Also, it performs an essential role in Ethereum reading the code, computing transaction costs, executing transactions, etc.

![](https://learn.kba.ai/wp-content/uploads/2021/11/EvmArch__1_-300x197.png)

EVM got three storage areas:

1. **Storage:** Storage area pointed inside each account storing the contract state variables. The location is allocated during contract creation time.

2. **Memory:** The memory area holds temporary variables. Memory is only accessible during contract execution, and contents get discarded between calls.

3. **Stack:** Stack location used for storing intermediate values in computations. The stack doesn’t persist after contract execution.

Gas is the fee or pricing value used to execute a transaction on the Ethereum blockchain successfully.

Basically, EVM enables you to join the Ethereum network, create Ethereum transactions and execute smart contracts.

# Ethereum World State

There is a single prime computer known as Ethereum World Computer in the Ethereum universe. The computer’s state is agreed by everyone in the Ethereum network. Every Ethereum network participant keeps a copy of the computer state. Any participant in the network can execute and broadcast a request into the network for the computer to perform arbitrary computation. Now whenever such a request is initiated, other participants of the Ethereum network verify, validate and execute the computation. This changes the state of EVM, and this state change is committed and propagated throughout the entire network.

The requests are called transactions, participants in the network are called nodes.

Basically, the Ethereum blockchain is a transaction-based state machine. The state can be defined as a particular condition of something at a specific time. For example, we can take the state of a door, which will be either open or close.

The Ethereum world state is a mapping between address (160-bit identifiers for an account) and account states. It moreover, functions like a bank account that keeps track of the balance and customer spending.

![](https://learn.kba.ai/wp-content/uploads/2021/11/WorldState-300x138.png)

# Gas & Ether

**Gas** refers to the unit that measures the amount of computational effort required to execute specific operations on the Ethereum network; usually represented in wei, the smallest denomination of Ether.

Simply saying, gas fees help to keep the Ethereum network secure. By setting a fee for executing computations of the network, prevents malicious actors from spamming the network. It also helps to prevent accidental infinite loops. Also encourages developers to create optimized code for running in the EVM. In any case, the gas that hasn’t been used will be returned to the user.

For enforcing **terminablility** for any instruction running on the EVM, Ethereum uses the **fee meter** method. This fee is **paid** in **Ether**. This was the real use of Ether in Ethereum. It was never meant to be a cryptocurrency, rather it is used for anti-spamming and to enforce the terminability property for EVM.

### What is Ether?

[**Ether**](https://ethereum.org/en/eth/) (ETH) is the native currency of Ethereum. Ether is a metric unit and it has different denominations. The smallest denomination or base unit is known as Wei. The denominations are named after the names of people who played important roles in the evolution of computer science and crypto-economics.

| Unit                    | Wei Value | Wei                       |     |
| ----------------------- | --------- | ------------------------- | --- |
| **wei**                 | 1 wei     | 1                         |     |
| **Kwei (babbage)**      | 1e^3 wei  | 1,000                     |     |
| **Mwei (lovelace)**     | 1e^6 wei  | 1,000,000                 |     |
| **Gwei (shannon)**      | 1e^9 wei  | 1,000,000,000             |     |
| **microether (szabo)**  | 1e^12 wei | 1,000,000,000,000         |     |
| **milliether (finney)** | 1e^15 wei | 1,000,000,000,000,000     |     |
| **ether**               | 1e^18 wei | 1,000,000,000,000,000,000 |     |

# Accounts

An Ethereum account is an entry that can hold an ether balance, or send it to another account on the Ethereum blockchain network. These accounts can either be user-controlled know as **Externally Owned Accounts** or controlled by codes (contracts); termed as **Contract** **Accounts.**

An account is recorded in the blockchain state when its receives ether (ETH) or code gets associated with it.

**Externally Owned Accounts (EOA)**

1. - The creation has no cost.
    - It is controlled by the private key.
    - Has no associated code.
    - Is able to initiate a transaction, ether transaction, or contract execution.
    - Transaction between EOA to EOA is only an Ether transaction.

**Contract Accounts**

1. - The creation of contract accounts has cost due to the fact you are using the network storage.
    - It is controlled by contract code.
    - Can only send transactions in response to another transaction.
    - Has associated code.
    - Contract code execution is triggered by transactions received from other contracts or externally owned accounts.

**Both account types can**

- - Receive, hold and send ETH and tokens.
    - Interact with deployed smart contracts.

Ethereum contracts are live inside the Ethereum Virtual Machine, always executing a particular part of code when triggered by a transaction from an Externally Owned Account.

So, how are the Address value for Externally Owned Accounts and Contract Accounts created?

![](https://learn.kba.ai/wp-content/uploads/2021/11/Screenshot-from-2021-11-03-10-08-33-300x194.png)

For externally owned accounts, the address is derived from the [public key](https://en.wikipedia.org/wiki/Digital_Signature_Algorithm) which is in turn derived from the [private key](https://en.wikipedia.org/wiki/Digital_Signature_Algorithm). For contract accounts, the address is derived from the sender address (who has deployed the contract) and the nonce value associated with the sender address is the total number of transactions triggered from that account.

**Ethereum accounts have four fields:**

- - **nonce** – is a counter used to keep track of the number of transactions sent from a particular account address. This makes sure that the transactions are only processed once. In the case of a contract account, this value keeps track of the number of contracts created by the account.
    - **balance** – the number of Ether owned by the address, which is always specified in Wei. Wei is the smallest denomination of Ether (ETH). And 1e+18 wei is one Ether.
    - **codeHash** – refers to the hash of the code associated with an account in the Ethereum Virtual Machine. Contract accounts are the ones that have value in codeHash field. This value can’t be changed, unlike other values. The codeHash value for externally owned accounts is the hash of an empty string.
    - **storageRoot** – The 256-bit hash of the root node of a [Merkle Patricia Trie](https://kba.ai/6771-2/).

# Consensus

The consensus mechanism defines the rules by which the participants agree on the same copy of the ledger. Before the Merge, Ethereum was running on proof of work consensus. The first phase of the Serenity upgrade established the [Beacon chain](https://medium.com/blockchain-stories/ethereum-2-0-the-beacon-chain-d669fa65e50d) as a separate blockchain which runs on Proof of Stake consensus. Ethereum switched its consensus mechanism from proof of work to proof of stake once the merge was complete on September 15, 2022. Under the proof of stake consensus, a group of validators are responsible for creating blocks.

**Beacon Chain**

The Beacon Chain is the consensus engine of Ethereum 2.0. It randomly selects validators for a block based on a pseudorandom process called RANDAO and manages the consensus mechanism. It stores a registry of validator addresses, the state of each validator, attestations (validator votes), and links to shards (in future).

**Validator**

One can become a validator by depositing 32 ETH using a specific transaction in the [deposit contract](https://github.com/ethereum/consensus-specs/blob/dev/specs/phase0/deposit-contract.md) in the Ethereum mainnet. The validators are responsible for creating new blocks (block proposer) and voting on a proposed block (committee). Validators are rewarded for honest behaviour and also penalized for dishonest behaviour.

**Proof of Stake (PoS)**

Time is divided into epochs, which are further sub-divided into 32 slots of 12 seconds each. Before the start of an _epoch_, each _slot_ is assigned a validator as a block proposer, and a specific group of validators(minimum 128) called a committee. A validator can only be in one committee per epoch. There can also be more than one committee per slot. All the committees must be of same size.

![](https://learn.kba.ai/wp-content/uploads/2022/10/committee.png)

During each slot, its block proposer will select a block to append to the existing chain, and the committee will vote to add this to the main chain. These votes are termed attestations and are weighted by the validator’s deposit. The validators broadcast their votes, and a block which gets a two-thirds majority of validator votes is accepted. The majority is decided based on the weight of deposits rather than the number of validators.

# Block

The number of transactions in the Ethereum network at a time is very high, so these transactions are committed as batches instead of as single ones; these batches are known as blocks. Generally, a block will contain hundreds of transactions.

To maintain the transaction history, all of these blocks are strictly stored in an ordered manner, basically saying every new block will have a reference to the parent block (previous block). These references are hashes that are cryptographically derived from the data of the block. This prevents fraud because any change in the block data will change the hash, which will not go unnoticed.

![](https://learn.kba.ai/wp-content/uploads/2022/10/eth2block.png)

**Fields in a block:**

- **slot**: the timeslot number the block belongs to
- **proposer_index**: the ID of the validator proposing the block
- **parent_root**: the unique identifier (hash) of the preceding block
- **state_root:** identifier of the entire state of the system: account balances, contract storage, contract code, and account nonces.

Consensus Information part consists of fields related to the Proof of Stake algorithm.

- **randao_reveal**: Block proposer’s sign on current epoch. A value used to randomly select the next block proposer.
- **eth1_data**: status of the deposit contract
- **graffiti**: arbitrary data used by validator to tag blocks
- **proposer_slashings** & **attester_slashings**: list of validators to be slashed
- **attestations**: list of votes in favour of the current block
- **deposits**: list of new deposits to the deposit contract
- **voluntary_exits**: list of validators exiting the network
- **sync_aggregate**: subset of validators used to serve light clients ( devices which have low resources)

The **execution_payload** section will consist of transactions passed from the execution client (EVM).

- **parent_hash**: hash of the parent (previous) block
- **fee_recipient**: validator’s account address which receives transaction fees
- **state_root**: identifier of the entire state of the system after applying changes in this block
- **receipts_root**: hash of the transaction receipts trie
- **logs_bloom**: data structure containing event logs
- **prev_randao**: value used in random validator selection
- **block_number**: the number of the current block
- **gas_limit**: maximum gas allowed in this block
- **gas_used**: the actual amount of gas used in this block
- **timestamp**: the block time
- **extra_data**: arbitrary additional data as raw bytes
- **base_fee_per_gas**: the minimum fee per gas required for a transaction to be included in a block.
- **block_hash**: Hash of execution payload block
- **transactions**: list of transactions batched together in the block.

**Block Size:**

The blocks are bound by a size limit. You can’t create a block with a huge number of transactions. To execute a transaction, a certain cost must be paid, known as gas. Each block has a gas limit; that is, the total amount of gas collectively for all the transactions in the block should not exceed this limit. The gas limit is set by the network and miners collectively. This is because if a block is arbitrarily large, it will affect the network due to limitations in space and speed. The genesis block gas limit was 5000 Wei. Any miner who creates a new block has the right to alter it by a percentage of 0.1 in Ether from the gas limit of the parent block.


# Ethereum Transaction

Transaction in Ethereum is an important core function because the transaction is the only thing that can change or update the Ethereum state. In this unit, we are going to see the structure of Ethereum transactions and the details of the transaction fee in Ethereum.

Ethereum transaction is initiated by an externally-owned account. An account managed by a human.

Any transactions, that change the EVM state, needs to be broadcasted to the network.

**Transaction Structure:**

Ethereum transaction has the following elements.

![](https://learn.kba.ai/wp-content/uploads/2022/10/eth_txn.png)

- **nonce:**  Nonce in a transaction is a sequence number of transactions from an Ethereum account.
- **gasLimit:** It is the maximum amount of gas units you are happy to spend on a specific transaction. 
- **maxPriorityFeePerGas:** the maximum amount of gas to be included as a tip to the validator
- **maxFeePerGas**:  the maximum amount of gas willing to be paid for the transaction (inclusive of baseFeePerGas and maxPriorityFeePerGas)
- **to**: Destination account address; this is either an externally owned account (EOA) or a contract account.
- **value:** It represents the amount of ether/wei from the sender to the receiver.
- **v** along with **r**, **s** from the digital signature.
- **data:** Data field is for contract activities (deployment or execution of the contract).

**Transaction Fee:**

Every operation (write or read) performed in the blockchain network is known as a transaction and each transaction has a fee, which is paid in ether and is known as Gas Cost.

Gas refers to a unit that estimates the amount of computational work required for executing specific operations under the EVM. The system is similar to measuring electricity in our house, where the unit of work is expressed in kilowatts (KW). Gas cost is expressed in ether.

Gas cost for every single operation is fixed. However, the smart contract code can be complex. For instance, a small piece of code can generate a lot of computational work, similarly, a long piece of code can generate less computational work. This is the reason the expenses in the Ethereum Virtual Machine are subjected to the measure of work being finished.

_Transaction Fee (paid in ether)  = Gas Limit *(Base fee + Tip)_

The base fee is the minimum price per unit of gas the user has to pay. The base fee will be burnt (destroyed), so users are expected to include a tip (priority fee) in their transactions. The tip incentivizes miners to process transactions in blocks and is usually set automatically by wallets. The burning of the base fees is intended to make ETH deflationary. 

The gas is also a way in which EVM ensures the terminable nature of **Ethereum World Computer** i.e.; when the allotted gas for an operation is consumed, the operation gets stopped regardless of being completed or not.

# Account Balance Model

We saw blockchain uses a distributed record-keeping system called ledgers that keep track of transactions happening within the chain. Currently, there are two popular record keeping models used in the Blockchain world.

1. 1. **[UTXO Model](https://learn.kba.ai/course/%20blockchain-foundation-program/lessons/utxo/) (Unspent Transaction Output)**
    2. **Account Balance Model**

In the Bitcoin system, each transaction takes UTXO generated by the previous transaction. However, balance management in Ethereum uses the Account Balance Model, which is much similar to our traditional banking system. Under the Account Balance Model, network nodes store the world state locally rather than transferring with the blocks.

**Account Balance Model**

In Ethereum, a global state stores a list of accounts with balances, code, and internal storage. Here a transaction is valid if the sending account has enough balance to pay for it. Under this case, the sending account is debited and the receiving account is credited with the value.

**Benefits:**

- - **Simplicity:** Ethereum opted for a simple record-keeping model which is helpful for developers who develop a complex smart contract, mainly those that require state information.
    - **Efficiency:** The Account Balance Model is more efficient because each transaction just needs to validate that the sender’s account has enough balance to pay for that transaction.

**Drawbacks:**

- - Account Balance model is exposed to double-spending attacks.

An incrementing **nonce** is a solution for this type of attack. In Ethereum, each account has a globally accessible nonce, which is a sequence number. Every time a transaction is made, the nonce is increased by one. If a block is having a transaction with an incorrect nonce, then it is an invalid block.


# Ethereum Transaction Life Cycle

![](https://learn.kba.ai/wp-content/uploads/2022/12/TransactionFlowEthereumFinal.png)
