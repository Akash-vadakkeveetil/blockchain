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