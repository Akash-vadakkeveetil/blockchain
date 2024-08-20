# Remix IDE File Explorer & Code Editor

The Remix IDE is an in-browser IDE, that is open-source. The browser helps to write solidity contracts, compile and deploy to the blockchain network. Written in JavaScript, Remix supports both usage in the browser and locally.

Remix also supports testing, debugging, and much more.

Let’s get started. Visit: [https://remix.ethereum.org/](https://remix.ethereum.org/)

![](https://learn.kba.ai/wp-content/uploads/2021/11/R01-1024x576.png)

Browsing **Help us to improve Remix IDE** pop and IDE tour, you can see the above screen. This is the home page of the Remix IDE. Let’s explore the different sections. First the **FILE EXPLORERS** tab.

![](https://learn.kba.ai/wp-content/uploads/2021/11/R02-1024x576.png)

There are two sections in the **FILE EXPLORERS** tab for managing **workspace** and managing **files** in each workspace.

![](https://learn.kba.ai/wp-content/uploads/2021/11/R03-1024x576.png)

The workspaces are used to group files in Remix IDE. The workspace has the following options:

- - **Create**: To create a new workspace.
    - **Rename**: To rename an existing workspace.
    - **Delete**: To delete an existing workspace.

It is also possible to establish a connection to the file system using the [Remixd NPM package](https://www.npmjs.com/package/@remix-project/remixd).

![](https://learn.kba.ai/wp-content/uploads/2021/11/R04-1024x576.png)

Next, we can manage files in the workspaces with the following options:

- - **Create New File**: To create a new file.
    - **Create New Folder**: To create a new folder.
    - **Publish all current workspace files to a GitHub gist**
    - **Load a local file into the current workspace.**

Remix developers have already provided us with some sample codes. These are divided into different folders:

- - **contracts**: This folder holds three contracts with different complexity levels, denoted with a number prefix in the file name. The programs are
        - **Storage.sol:** Simply storing and retrieval of a number.
        - **Owner.sol:** Access restriction example.
        - **Ballot.sol:** Company proposal voting smart contract.
    - **scripts**: This folder holds two template scripts to deploy a contract.
    - **tests:** This folder contains one test file for **Ballot.sol** contract with unit tests in Solidity.

Keep in mind that all the files listed on the File Explorer are stored within the browser cache. If you want to store the files locally, you can use the **Download all Files as a backup zip** option on the home page. If you ever close the home page you can relaunch it by clicking the Remix IDE icon on the top left corner.

![](https://learn.kba.ai/wp-content/uploads/2021/11/R05-1024x576.png)

Now let’s create a HelloWorld Solidity file, using the **Create New File** option.

![](https://learn.kba.ai/wp-content/uploads/2021/11/R06-1024x576.png)

The file extension of the solidity file is _.sol_. After creating the file, the code editor will automatically open the file and you can start typing your code here.

![](https://learn.kba.ai/wp-content/uploads/2021/11/r7-1024x576.png)

# Remix IDE Compiler Tab

Now that we have our smart contract written let’s compile the code to see if everything is alright. Go to the **Solidity Compiler** Tab. The compiler tab compiles the solidity code and checks for any syntactical errors.

![](https://learn.kba.ai/wp-content/uploads/2021/11/rc8-1024x576.png)

Compiler Tab has the following options:

- - **Compiler:** The solidity language version should be the same as provided in the code.
    - **Language:** This is set to Solidity and cannot be changed. In case if you want to select Vyper, you need to activate that plugin to do so.
    - **EVM Version:** The EVM version of the Ethereum node for which the code is being compiled.

The compiler button will be of the format **Compile <Selected File name>**. The compiler tab has some configuration options too:

- - **Auto Compile:** Automatically compiles the solidity code each time a code change is detected.
    - **Enable Optimization:** This optimizes the code and reduces gas costs for deployment and execution.
    - **Hide Warnings:** Will hide the warnings.

Now, click the **Compile** button.

![](https://learn.kba.ai/wp-content/uploads/2021/11/rc9-1024x576.png)

The compiler will show the syntactical error in the code; in the above case, we have removed a semicolon. Also, it’s always good to turn the auto-compile option so that the compiler will show any errors upon modification. Add the semicolon and press the **Compile** button again.

![](https://learn.kba.ai/wp-content/uploads/2021/11/FC05-1-1024x576.png)

If the contract is successfully compiled, the following options will appear.

- - **Contract:** A dropdown list that shows the list of all compiled contracts.
    - **Publish on Swarm:** You can publish the compiled data onto the swarm network, which can be later called on.
    - **Compilation Details:** The compilation details of the smart contract like Metadata, ABI, Bytecode, etc.
    - **ABI:** Application Binary Interface. The function signature of the smart contract, used for accessing the smart contract along with the contract address.
    - **Bytecode:** The compiled output; the form which can be deployed to an EVM.

Upon successful compilation, the tab symbol will have a green tick.

# Remix IDE Deploy & Run Transactions Tab

After coding and compiling the solidity smart contract code, go to the **Deploy & Run Transaction** Tab .

![](https://learn.kba.ai/wp-content/uploads/2021/11/rc11-1024x576.png)

Deploy & Run Transaction Tab provides with following options:

- **Environment**: The environment to which the contract going to be deployed, can be one of the below.
    - **Remix VM**: The Remix VM (previously called JavaScript VM) is a simulation of the Ethereum node by Remix developers for testing purposes.
    - **Injected Provider- MetaMask**: An option to establish a connection to the wallets like Metamask that provides a connection object.
    - **Hardhat/Foundry/Ganache Provider:** Connecting Remix to a local Hardhat/Foundry/Ganache test chain. 
    - **WalletConnect**:  An option to connect to WalletConnect allowing users to approve transactions on a mobile device.
    - **External HTTP Provider:**  An option to connect to an Ethereum node (Geth, Parity, etc.) running on a computer by providing the URL. This was previously called Web3 Provider.
    - **L2 – <Provider>:**  An option to connect to an Injected Provider (usually Metamask) with the settings for the Optimism Network’s mainnet/Arbitrum One network.

- **Account:** Shows the list of unlocked accounts in the connected environment.
- **Gas Limit:** The limit we set for each transaction from the Remix IDE.
- **Value:** When you are required to transfer ether to contract, the ether value can be given here.

Then we have a dropdown list that will show the list of all the compiled solidity contracts. After selecting the correct one, click the **Deploy** button. The **At Address** button is used to access an already deployed smart contract by providing its address as input (_the same contract should be compiled and selected at the time you use this functionality_).

![](https://learn.kba.ai/wp-content/uploads/2021/11/rc10-1024x576.png)

Let’s put the settings at **default** and deploy the contracts to the **JavaScript VM** by clicking the **Deploy** button. The deployed contract will be displayed under the **Deployed Contracts** section. Under the **logs** section, you can see the status of the transaction. The developer can get the contract address from the Deployed Contracts section and try out all the functions within the deployed contract.

![name](https://learn.kba.ai/wp-content/uploads/2021/11/rc12-1024x576.png)

Note: Check the color difference for the **Deploy, At Address, getMessage,** and **setMessage** buttons. The **blue** indicates the function isn’t changing the blockchain state and will not have any transaction cost. On the other hand, the **o****range** shows the state change and charging of adequate transaction costs.

# Remix IDE Offline Mode [Optional]

To set up Remix IDE for Offline Usage.

Make sure you have installed **NodeJS** and **npm**, then install [Nx CLI](https://nx.dev/react/cli/overview) globally, which enables running nx executable commands.

_**`npm install -g @nrwl/cli`**_

Clone the GitHub repository.

`_**git clone https://github.com/ethereum/remix-project.git**_`

**Note:** The master branch always has the latest stable build of Remix. Including the zip of the build which you can download to run offline.

Now build the Remix IDE from source.

_**`cd remix-project`**_

_**`npm install`**_

_**`nx build remix-ide --with-deps`**_

Finally to run Remix IDE execute the following command.

`_**nx serve**_`

Now go to [http://127.0.0.1:8080](http://127.0.0.1:8080/) in your browser.




