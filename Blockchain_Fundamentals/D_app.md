# Decentralized Applications

A Decentralized Application (also called DApp) is a piece of software that communicates with the blockchain. A DApp is just like any other software application you use. It could be a website or an app on your phone.

### **Decentralized Application vs Traditional Applications**

DApp is an application built on decentralized technology, rather than built and controlled by a single, centralized entity. For instance, take ****Google Pay****. Google controls this payment app. It is Google that defines the logic and conditions for running and processing the payment requests. However, the control gets distributed and shared among the network participants in a DApp. The code is open and transparent that anyone can build new solutions piecing together the existing logic.

Now let’s take a look at the DApp Architecture.

The DApp is layered. It consists of the following layers.

1. 1. Front End
    2. Web3
    3. Smart Contract
    4. Ethereum Virtual Machine
    5. Operating System

![](https://learn.kba.ai/wp-content/uploads/2021/10/Dapp.png)

**Front End:** Represents what you see. It enables the end-users to seamlessly communicate with the blockchain. It consists of UI; developed in any frameworks/language; text boxes, buttons, etc for interacting with the user.

**Web3:** The second layer consists of a set of libraries enabling users to communicate with Ethereum nodes using HTTP, IPC of WebSocket. Web3 provides a list of APIs that contain specific functionality for the Ethereum ecosystem.

Next comes our important component- [Smart Contracts](https://learn.kba.ai/course/blockchain-foundation-program/lessons/smart-contracts/). The backbone of Ethereum network.

**Smart Contract:** Smart contracts, the third layer governs the exchange of cash, property, shares or anything of value. It enables exchanges to be transparent, clash-free while avoiding the administration of a middle man.

**Ethereum Virtual Machine:** Entry point into the Ethereum network, capable of running a full node.

# Smart Contracts

How do DApps run ?

DApps runs with the help of **Smart Contracts**. They are self-executing computer programs that permit users to exchange money, assets, or anything of significant value. It help exchanges be transparent, tamper-proof, and conflict-free without any middlemen. Developers can program various smart contracts that support the DApps to run without a central authority. The automated contracts help the DApps carry an action faster, cheaper, and secure.

![](https://learn.kba.ai/wp-content/uploads/2021/10/sctc.png)

For  writing the contracts, Ethereum supports the following programming languages :

**Solidity:** Proposed by Gavin Wood in 2014, Solidity is a high-level object-oriented language. It has a large community that supports its development and use.

**Vyper:** Vyper is a contract-oriented, python syntax-based language. Vyper’s goals are Security, Language & Compiler simplicity. Vyper also aims to be more auditable than the rest of the contract programming languages.

Read more on Smart Contracts [here](https://ethereum.org/en/smart-contracts/).

# Smart contracts – A use case

**Let’s explore a real-case scenario with a smart contract.**

Let’s take a house ownership transfer for our study. Imagine Bob wants to sell his house for a certain amount. Under the traditional registry process, he has to depend on a central authority in order to complete his transaction. Take a look:

![](https://learn.kba.ai/wp-content/uploads/2021/10/h13-scaled.gif)

****Now imagine the deal using a smart contract:****

Imagine Bob wants to sell his house. The set price is **150 ETH (** expanded as Ether- native currency of Ethereum blockchain). Bob places his house in a smart contract (this is possible using a token that represents the ownership of your house). The business logic or the condition of the smart contract is that _IF someone sends 150 ETH to the smart contract THEN the token is sent to that person’s address._

1. If someone wants to buy the house, they should send the right amount of ETH to the smart contract.
2. In case, the sent amount is correct, the token (the ownership of your house) is sent to that person. In case, the amount is incorrect, the ETH will be returned back and house stays in the smart contract.

****What differs the smart contract from a conventional computer run program?****

The computer run program represents a set of instructions for a specific task. The smart contract covers the entire business logic including the asset behavior, legal obligations, user roles, access restrictions, and other protocols needed for the smooth running of the business. Isn’t it good enough?? Not only that it offers the following advantages to the businessmen.

****Advantages of a smart contract:****

1. Faster processing
2. Improved security
3. Low cost
4. Better trust among anonymous entities
5. No middlemen/brokers