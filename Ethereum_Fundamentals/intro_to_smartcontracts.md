# What is a Smart Contract ?

The DApps control is distributed and shared among the network participants. The source code for DApp is kept open and transparent. Anyone can audit and build innovative solutions using the open source code. But how is this possible? How do DApps run in the absence of a central control system?

Here comes the role of smart contracts. The business logic for DApps is embedded in a self-executing program called a smart contract that gets shared among the network participants. Smart contracts are self-executing agreements that act as a source of truth among the network participants.

**How do smart contracts work:**

![](https://learn.kba.ai/wp-content/uploads/2021/11/sc1-300x185.png)

Smart Contracts are simple and straight, however, it contains certain flaws. They can get out of hand sometimes. Any bug in the smart contract can lead to the failure or collapse of the DApp. The applications can be easily hacked (eg. [DAO attack](https://www.coindesk.com/learn/2016/06/25/understanding-the-dao-attack/)) by the attackers.

**What about the technical specifications?**

Smart contracts are typically written using dedicated languages (Solidity, Vyper, Go, etc.) which are then compiled and deployed as bytecode in the blockchain network. This self-executing code is invoked when the conditions/rules are met and all participants abide by the same rules. To be more simple, they act like the if/then… Else.. conditions as in any programming language. The state, therefore, eliminates the need for intermediaries or third parties to apply the norms and check for discrepancies, thereby saving massive amounts of money for businesses.

Smart contracts are tamper-resistant. It’s deterministic that the outcome of the contract execution is the same for everyone, and it’s distributed that everyone validates the smart contract’s outcome.

**Limitations**

- - Smart contracts can be enforced only on digital assets.
    - The blockchain network is decentralized and not legally regulated.
    - The smart contract can’t bind the interaction with the real world.
    - The enforcements of the smart contracts are some form of if-else, can’t implement sophisticated variations.

What is a Smart Contract ?
The DApps control is distributed and shared among the network participants. The source code for DApp is kept open and transparent. Anyone can audit and build innovative solutions using the open source code. But how is this possible? How do DApps run in the absence of a central control system?

Here comes the role of smart contracts. The business logic for DApps is embedded in a self-executing program called a smart contract that gets shared among the network participants. Smart contracts are self-executing agreements that act as a source of truth among the network participants.

How do smart contracts work:



Smart Contracts are simple and straight, however, it contains certain flaws. They can get out of hand sometimes. Any bug in the smart contract can lead to the failure or collapse of the DApp. The applications can be easily hacked (eg. DAO attack) by the attackers.

What about the technical specifications?

Smart contracts are typically written using dedicated languages (Solidity, Vyper, Go, etc.) which are then compiled and deployed as bytecode in the blockchain network. This self-executing code is invoked when the conditions/rules are met and all participants abide by the same rules. To be more simple, they act like the if/then… Else.. conditions as in any programming language. The state, therefore, eliminates the need for intermediaries or third parties to apply the norms and check for discrepancies, thereby saving massive amounts of money for businesses.

Smart contracts are tamper-resistant. It’s deterministic that the outcome of the contract execution is the same for everyone, and it’s distributed that everyone validates the smart contract’s outcome.

Limitations

Smart contracts can be enforced only on digital assets.
The blockchain network is decentralized and not legally regulated.
The smart contract can’t bind the interaction with the real world.
The enforcements of the smart contracts are some form of if-else, can’t implement sophisticated variations.

# Need and Use of Smart Contract

**Let’s explore a real-case scenario with a smart contract.**

Let’s take a house ownership transfer for our study. Imagine Bob wants to sell his house for a certain amount. Under the traditional registry process, he has to depend on a central authority to complete his transaction. Take a look.

![](https://learn.kba.ai/wp-content/uploads/2021/11/img_98b-scaled.gif)

**Now imagine the deal using a smart contract:**

Imagine Bob wants to sell his house. The set price is 150 ETH (expanded as Ether- native currency of Ethereum blockchain). Bob places his house in a smart contract ( using a token that represents the ownership of the house). The business logic or the condition of the smart contract is that IF someone sends 150 ETH to the smart contract THEN the token is sent to that person’s address.

So, if someone wants to buy the house, all they need to do is send the right amount of ETH to the smart contract.

If it’s the right amount, the token (the ownership of your house) is sent to that person and the 150 ETH is sent to the owner. If it is an incorrect amount, then the ETH will be returned to the sender and the house stays in the smart contract.

**What differs the smart contract from a conventional computer-run program?**

While a computer run program represents a set of instructions for a specific task, the smart contract covers the entire business logic including the asset behaviour, legal obligations, user roles, access restrictions, and any other protocols needed for the smooth running of the business. Isn’t it good enough?? Not only that it offers the following advantages to the businessmen.

**Advantages of a smart contract:**

- - Faster processing
    - Improved security
    - Low cost
    - Better trust among anonymous entities
    - No middlemen/brokers

![](https://learn.kba.ai/wp-content/uploads/2021/11/img_67-298x300.png)

# Writing of First Smart Contract

In Ethereum, smart contracts are written in **Solidity** language.

Let’s write a simple smart contract in Solidity.

The below program is used to store and retrieve an integer value from the blockchain network.

![](https://learn.kba.ai/wp-content/uploads/2021/11/Screenshot-from-2021-11-03-10-43-14-300x142.png)

One needs to specify the SPDX-License-Identifier tag for the source file while writing a Solidity contract. The tag is specified at the beginning of each program, and has the following general syntax:

**_`// SPDX-License-Identifier: name of the license`_**

This will be written as a comment. It is possible to skip specifying the SPDX-License-Identifier. However, the compiler will return a warning though not an error. [Click here](https://spdx.org/licenses/preview/) for the available list of licenses for Solidity Code.

Next, we need to specify the version of the Solidity language. The specification ensures the contract not getting compiled from an incompatible Solidity compiler.

The general syntax is

**_`pragma solidity version;`_**

We use the keywords **pragma** **solidity.** This is followed by the **version** number used for the code.

Compiler version can be mentioned in many ways. For instance,

`**_pragma solidity ^0.8.1;_**`

Here, the version number starts with a 0, followed by a major build number and a minor build number. For example, version number 0.8.1 refers to major build 8 and minor build 1. The caret symbol (^) notifies the Solidity that it can use the latest build during the version range. Solidity can use a compiler from any build in the version 8 build range in the preceding example. Readers are thus notified that the program was written for 0.8.1 but will still compile for subsequent version 8 builds.

Though the caret provides flexibility, it’s always advised to drop the caret. Instead, tell Solidity what compiler version you expect as shown in the above example.

As read, business logic is written inside the smart contract. One can create variables for storing and retrieving data from the blockchain and design functions for handling these variables inside a contract. There should be at least one contract inside the solidity file (there are some exceptions to this, which will be discussed in the CED course). We can have multiple contracts inside the same file.

The general syntax for the contract is:

`_**contract [name] { }**_`

The **contract** keyword followed by the name of the contract uses curly braces to specify the contract body. While naming the contract, it’s best to provide a name that describes the intentions of the contract. In the above example, the contract name is **Storage**.

The next line declares a variable called **number** of the type uint (unsigned integer of the length 256 bits), to storing the numerical value.

`_**uint256 number;**_`

### **How to store data?**

We define a function named **store()** for storing data into the number variable. The function is tagged with the keyword **public**, notifying it’s accessible for anyone who can interact with the contract.

`_**function store(uint256 num) public {**_    _**number = num;**_   _**}**_`

### How to read data?

To read the data from the number variable, we define a function **retrieve()**. The **view** keyword specifies the mutability of the function, function mutability means how the function interacts with the state of the blockchain.

`_**function retreive() public view returns (uint256){**_    _**return number;**_   _**}**_`

Now, let us see how to execute the above smart contract.

# Running First Smart Contract

Now that we have written our first smart contract program, let us see how to execute it. Copy the below code.

|First Smart Contract|
|:--|
|// SPDX-License-Identifier: MIT<br>pragma solidity 0.8.1;<br><br>contract Storage {<br><br>    uint256 number;<br><br>    function store(uint256 num) public {<br>        number = num;<br>    }<br><br>    function retreive() public view returns (uint256){<br>        return number;<br>    }<br>}|

We use an online IDE, know as **Remix IDE** for running our smart contract program. To do that go to [https://remix.ethereum.org/](https://remix.ethereum.org/)

The site displays a quick review of its function. Read through. After that create a new file clicking the _Create New File_ icon on the top left corner.

![](https://learn.kba.ai/wp-content/uploads/2021/11/FC01-1024x576.png)

A prompt opens in the file explore part. Enter the file name.

![](https://learn.kba.ai/wp-content/uploads/2021/11/FC02-300x169.png)

You can omit the extension. Now a new file will be created. Paste our code there.

![](https://learn.kba.ai/wp-content/uploads/2021/11/FC03-1024x576.png)

Go to the **SOLIDITY COMPILER** tab by clicking on the tab switch icon, then click on **Compile FirstContract.sol**.

![](https://learn.kba.ai/wp-content/uploads/2021/11/FC04-1024x576.png)

If there are no errors, the compilation process is successful and we can see the following results under the **Compile** **FirstContract.sol** button. And the **SOLIDITY COMPILER** tab button will have a green tick on it.

![](https://learn.kba.ai/wp-content/uploads/2021/11/FC05-1024x576.png)

Now go to the **DEPLOY & RUN TRANSACTIONS** tab. Click on the **Deploy** button.

![](https://learn.kba.ai/wp-content/uploads/2021/11/Fc06-1024x576.png)

If there are no errors, we can see the following results under the Deployed Contract Section.

![](https://learn.kba.ai/wp-content/uploads/2021/11/Fc07-1024x576.png)

Expand the **STORAGE** contract entry.

![](https://learn.kba.ai/wp-content/uploads/2021/11/Fc08-1024x576.png)

Here we can access the functions written in the smart contract. Write a number into the blockchain using the text box next to the **store** button and click the store button. Click on the retrieve button to read the value-form blockchain.

![](https://learn.kba.ai/wp-content/uploads/2021/11/Fc09-1024x576.png)

Congratulations, we have successfully run our first smart contract program. In the next section, we will learn in detail about the Remix IDE we used to write, compile and store the contract into blockchain.