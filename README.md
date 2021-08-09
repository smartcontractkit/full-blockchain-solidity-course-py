Welcome to the repository for the Ultimate Solidity, Blockchain, and Smart Contract - Beginner to Expert Full Course | Python Edition FreeCodeCamp course!

# Table of Contents
- [Table of Contents](#table-of-contents)
- [Resources For This Course](#resources-for-this-course)
    - [Questions](#questions)
- [Lesson 0: Welcome To Blockchain](#lesson-0-welcome-to-blockchain)
  - [What is a Blockchain?](#what-is-a-blockchain)
  - [Making Your First Transaction](#making-your-first-transaction)
  - [How Do Blockchains Work?](#how-do-blockchains-work)
    - [Consensus](#consensus)
  - [The Future](#the-future)
  - [Miscellaneous](#miscellaneous)
- [Lesson 1: Simple Storage](#lesson-1-simple-storage)
    - [Everything in this section can be read about in the Solidity Documentation](#everything-in-this-section-can-be-read-about-in-the-solidity-documentation)
    - [Remix](#remix)
    - [Basic Solidity](#basic-solidity)
    - [Deploying to a "Live" network](#deploying-to-a-live-network)
- [Lesson 2: Storage Factory](#lesson-2-storage-factory)
    - [Inheritance, Factory Pattern, and Interacting with External Contracts](#inheritance-factory-pattern-and-interacting-with-external-contracts)
- [Lesson 3: Fund Me](#lesson-3-fund-me)
    - [Payable, msg.sender, msg.value, Units of Measure](#payable-msgsender-msgvalue-units-of-measure)
    - [Chainlink Oracles](#chainlink-oracles)
    - [Importing from NPM and Advanced Solidity](#importing-from-npm-and-advanced-solidity)
- [Lesson 4: Web3.py Simple Storage](#lesson-4-web3py-simple-storage)
    - [Installing VSCode, Python, and Web3](#installing-vscode-python-and-web3)
    - [Our First Python Script with Web3.py - Deploying a Contract](#our-first-python-script-with-web3py---deploying-a-contract)
    - [Interacting with Our Contract in Python & Web3.py](#interacting-with-our-contract-in-python--web3py)
- [Lesson 5: Brownie Simple Storage](#lesson-5-brownie-simple-storage)
    - [Brownie Introduction](#brownie-introduction)
    - [Installing Brownie](#installing-brownie)
    - [Brownie Simple Storage Project](#brownie-simple-storage-project)
    - [Testing Basics](#testing-basics)
    - [[Brownie console]](#brownie-console)
- [Lesson 6: Brownie Fund Me](#lesson-6-brownie-fund-me)
    - [Introduction](#introduction)
    - [Dependencies, Deploying, and Networks](#dependencies-deploying-and-networks)
    - [Funding and Withdrawing Python Scripts](#funding-and-withdrawing-python-scripts)
    - [Testing across networks](#testing-across-networks)
    - [Git](#git)
- [Lesson 7: SmartContract Lottery](#lesson-7-smartcontract-lottery)
    - [Introduction](#introduction-1)
    - [`Lottery.sol`](#lotterysol)
    - [Testing Lottery.sol](#testing-lotterysol)
    - [Lottery.sol Testnet Deployment](#lotterysol-testnet-deployment)
- [Lesson 8: Chainlink Mix](#lesson-8-chainlink-mix)
  - [Brownie Mixes](#brownie-mixes)
- [Lesson 9: ERC20s, EIPs, and Token Standards](#lesson-9-erc20s-eips-and-token-standards)
- [Lesson 10: Defi & Aave](#lesson-10-defi--aave)
    - [Defi Intro](#defi-intro)
    - [Aave UI](#aave-ui)
    - [Programmatic Interactions with Aave](#programmatic-interactions-with-aave)
    - [Testing](#testing)
- [Lesson 11: NFTs](#lesson-11-nfts)
    - [Non-Technical Explainer](#non-technical-explainer)
    - [Simple NFT](#simple-nft)
    - [SimpleCollectible Testing](#simplecollectible-testing)
    - [Advanced NFT](#advanced-nft)
    - [Advanced deploy_and_create](#advanced-deploy_and_create)
    - [Creating Metadata & IPFS](#creating-metadata--ipfs)
- [Lesson 12: Upgrades](#lesson-12-upgrades)
    - [Introduction to upgrading smart contracts](#introduction-to-upgrading-smart-contracts)
    - [Upgrades-mix and code](#upgrades-mix-and-code)
    - [Testing Upgrades](#testing-upgrades)
    - [Upgrades on a testnet](#upgrades-on-a-testnet)
- [Bonus Lesson 13: Full Stack Defi](#bonus-lesson-13-full-stack-defi)
    - [Defi Stake Yield Brownie Scripts & Tests](#defi-stake-yield-brownie-scripts--tests)
    - [Testing our Defi Stake Yield Brownie Dapp](#testing-our-defi-stake-yield-brownie-dapp)
    - [Front End / Full Stack](#front-end--full-stack)
- [Bonus Lesson 14: Security](#bonus-lesson-14-security)

# Resources For This Course
### Questions
- [Github Discussions](https://github.com/smartcontractkit/full-blockchain-solidity-course-py/discussions)
  - Ask questions and chat about the course here!
- [Stack Exchange Ethereum](https://ethereum.stackexchange.com/)
  - Great place for asking technical questions about Ethereum
- [StackOverflow](https://stackoverflow.com/)
  - Great place for asking technical questions overall

# Lesson 0: Welcome To Blockchain
## What is a Blockchain?
- [Bitcoin Whitepaper](https://bitcoin.org/bitcoin.pdf)
- [Ethereum Whitepaper](https://ethereum.org/en/whitepaper/)
- [Hybrid Smart Contracts](https://blog.chain.link/hybrid-smart-contracts-explained/)
- [Blockchain Oracles](https://betterprogramming.pub/what-is-a-blockchain-oracle-f5ccab8dbd72?source=friends_link&sk=d921a38466df8a9176ed8dd767d8c77d)
- [What is a blockchain](https://www.investopedia.com/terms/b/blockchain.asp)
## Making Your First Transaction
- [Metamask](https://metamask.io/)
- [Etherscan](https://etherscan.io/)
- [Rinkeby Etherscan](https://rinkeby.etherscan.io/)
- [Rinkeby Faucet](https://faucet.rinkeby.io/)
  - NOTE: The Chainlink documentation always has the most up to date faucets on their [link token contracts page](https://docs.chain.link/docs/link-token-contracts/#rinkeby). If the faucet above is broken, check the chainlink documentation for the most up to date faucet.  
- [Gas and Gas Fees](https://ethereum.org/en/developers/docs/gas/)
- [Wei, Gwei, and Ether Converter](https://eth-converter.com/)
- [ETH Gas Station](https://ethgasstation.info/)
## How Do Blockchains Work? 
- [Blockchain Demo](https://andersbrownworth.com/blockchain/)
- [Public / Private Keys](https://andersbrownworth.com/blockchain/public-private-keys/keys)
- [Layer 2 and Rollups](https://ethereum.org/en/developers/docs/scaling/layer-2-rollups/)
- [Decentralized Blockchain Oracles](https://blog.chain.link/what-is-the-blockchain-oracle-problem/)
- [Block Rewards](https://www.investopedia.com/terms/b/block-reward.asp)
- [Run Your Own Ethereum Node](https://geth.ethereum.org/docs/getting-started)
### Consensus
- [Consensus](https://wiki.polkadot.network/docs/learn-consensus)
- [Proof of Stake](https://ethereum.org/en/developers/docs/consensus-mechanisms/pos/)
- [Proof of Work](https://ethereum.org/en/developers/docs/consensus-mechanisms/pow/)
- [Nakamoto Consensus](https://blockonomi.com/nakamoto-consensus/)
## The Future
- [Ethereum 2](https://ethereum.org/en/eth2/)
## Miscellaneous 
- [DAOs](https://www.investopedia.com/tech/what-dao/)
# Lesson 1: [Simple Storage](https://github.com/PatrickAlphaC/simple_storage)
### Everything in this section can be read about in the [Solidity Documentation](https://docs.soliditylang.org/en/v0.8.6/index.html)
### [Remix](https://remix.ethereum.org/)
### Basic Solidity
- Versioning
- Compiling
- Contract Declaration
- [Types & Declaring Variables](https://docs.soliditylang.org/en/v0.8.6/types.html)
  - `uint256`, `int256`, `bool`, `string`, `address`, `bytes32`
- Default Initializations
- Comments
- Functions
- Deploying a Contract
- Calling a public state-changing Function
- [Visibility](https://docs.soliditylang.org/en/v0.7.3/contracts.html#visibility-and-getters)
- Scope
- View & Pure Functions
- Structs
- Intro to Storage
- Arrays - Dynamic & Fixed sized
- Compiler Errors and Warnings
- Memory
- Mappings
- SPDX License
### Deploying to a "Live" network
- A testnet or mainnet
- [Find a faucet here](https://docs.chain.link/docs/link-token-contracts/#rinkeby)
- Connecting Metamask
- Interacting with Deployed Contracts
- The EVM
# Lesson 2: [Storage Factory](https://github.com/PatrickAlphaC/storage_factory)
### Inheritance, Factory Pattern, and Interacting with External Contracts
- Factory Pattern
- Imports
- Deploy a Contract From a Contract
- Interact With a Deployed Contract
# Lesson 3: [Fund Me](https://github.com/PatrickAlphaC/fund_me)
### Payable, msg.sender, msg.value, Units of Measure
- Payable
- [Wei/Gwei/Eth Converter](https://eth-converter.com/)
- msg.sender & msg.value
### Chainlink Oracles
- Decentralized Oracle Network Chainlink
  - Blockchains can't make API calls
  - Centralized Nodes are Points of Failure
- [data.chain.link](https://data.chain.link/)
- Getting External Data with Chainlink Oracles
  - [Chainlink](https://docs.chain.link/)
  - [Faucets and Contract Addresses](https://docs.chain.link/docs/link-token-contracts/)
    - [Kovan](https://docs.chain.link/docs/link-token-contracts/#kovan)
  - [Getting Price Information](https://docs.chain.link/docs/get-the-latest-price/)
### Importing from NPM and Advanced Solidity
- Decimals/Floating Point Numbers in Solidity
- latestRoundData
- Importing from NPM  in Remix
- Interfaces
  - Introduction to ABIs
- [Getting Price Feed Addresses](https://docs.chain.link/docs/reference-contracts/)
- getPrice
- Tuples
  - Unused Tuple Variables
- Matching Units (WEI/GWEI/ETH)
- getConversionRate
- Matching Units (Continued)
- SafeMath & Integer Overflow
  - using keyword
  - [Libraries](https://docs.soliditylang.org/en/v0.8.6/contracts.html#libraries)
  - SafeMath PSA
- Setting a Threshold
- Require
- Revert
- Withdraw Function 
- Transfer
- Balance
- this
- Contract Owners
- Constructor
- ==
- Modifiers
- Resetting
- for loop
- Array Length
- Forcing a Transaction
- Recap
# Lesson 4: [Web3.py Simple Storage](https://github.com/PatrickAlphaC/web3_py_simple_storage)
### Installing VSCode, Python, and Web3
- [Developer Bootcamp Setup Instructions (metamask, vscode, python, nodejs..)](https://chain.link/bootcamp/brownie-setup-instructions)
- [VSCode](https://code.visualstudio.com/download)
- [VSCode Crash Course](https://www.youtube.com/watch?v=WPqXP_kLzpo)
- Extensions
- Short Cuts:
  - [VSCode Shortcuts](https://code.visualstudio.com/docs/getstarted/keybindings)
  - [VSCode MacOS Shortcuts](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf)
- [Python](https://www.python.org/downloads/)
  - Install Troubleshooting
- Terminal
- Making a directory/Folder
- Opening the folder up with VSCode
- Creating a new file
- Syntax Highlights
- Remember to save!
- Setting linting compile version
- VSCode Solidity Settings
  - Formatting & Format on Save
  - Solidity Prettier
  - [Python Black](https://pypi.org/project/black/)
  - [pip](https://pypi.org/project/pip/)
### Our First Python Script with Web3.py - Deploying a Contract
- Reading our solidity file
- Running a Python Script in the Terminal
- [MaxOS Shortcuts](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf)
- [Windows Shortcuts](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)
- [Linux Shortcuts](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-linux.pdf)
- Compiling in Python
- [py-solc-x](https://pypi.org/project/py-solc-x/)
  - compile_standard
- Colorized Brackets
- JSON ABI 
- Saving Compiled Code
- Formatting JSON
- Deploying in Python
  1. Get Bytecode
  2. Get ABI
  3. Choose Blockchain to Deploy To
    - Local Ganache Chain
      - [Ganache UI](https://www.trufflesuite.com/ganache)
      - [Ganache Command Line](https://github.com/trufflesuite/ganache-cli)
- [Web3.py](https://web3py.readthedocs.io/en/stable/)
- HTTP / RPC Provider
- Private Keys MUST start with "0x"
- Contract Object
- Building a Transaction
- Account Nonce 
- Calling "Contructor"
- Transaction Parameters
- Signing the Transaction
- NEVER put your private key directly in your code
- [Setting Environment Variables (Windows, Linux, MacOS)](https://www.twilio.com/blog/2017/01/how-to-set-environment-variables.html)
  - [More on Windows Environment Variables](https://www.youtube.com/watch?v=tqWDiu8a4gc&t=40s)
- Exported Environment Variables Only Last the Duration of the Shell/Terminal
- Private Key PSA
- .env file
- .gitignore
- Loading .env File in Python
  - [python-dotenv](https://pypi.org/project/python-dotenv/)
- Viewing our Transaction / Deployment in Ganache
- Waiting for Block Confirmations
### Interacting with Our Contract in Python & Web3.py
- 2 Things you always need
  1. Contract Address
  2. Contract ABI
- Getting address from transaction receipt
- Calling a view function with web3.py
  - Call vs Transact
- Updating State with Web3.py
- [ganache-cli](https://github.com/trufflesuite/ganache-cli)
  - Installing Ganache
    - [Install Nodejs](https://nodejs.org/en/)
    - [Install Yarn](https://classic.yarnpkg.com/en/docs/install)
- Working with ganache-cli
- Open a new terminal in the same window
- Deploying to a testnet
- [Infura](https://infura.io/)
- [Alchemy](https://www.alchemy.com/)
- Using Infura RPC URL / HTTP Provider
- [Chain Ids](https://chainlist.org/)
- Wow this seems like a lot of work... Is there a better way?
# Lesson 5: [Brownie Simple Storage](https://github.com/PatrickAlphaC/brownie_simple_storage)
### Brownie Introduction
- Some Users:
  - https://yearn.finance/
  - https://curve.fi/
  - https://badger.finance/
### Installing Brownie
- [Installing Brownie](https://eth-brownie.readthedocs.io/en/stable/install.html)
  - Install pipx
  - pipx install eth-brownie
  - Testing Successful Install
### Brownie Simple Storage Project
- A new Brownie project with `brownie init`
  - Project Basic Explanation
- Adding `SimpleStorage.sol` to the `contracts` folder
- Compiling with `brownie compile`
- Brownie deploy script
  - `def main` is brownie's entry point
- brownie defaults to a `development` `ganache` chain that it creates
- Placing functions outside of the `main` function
- brownie `accounts`
  - 3 Ways to Add Accounts
    1. `accounts[0]`: Brownie's "default" ganache accounts
       - Only works for local ganache 
    2. `accounts.load("...")`: Brownie's encrypted command line (MOST SECURE)
       - Run `brownie accounts new <name>` and enter your private key and a password
    3. `accounts.add(config["wallets"]["from_key"])`: Storing Private Keys as an environment variable, and pulling from our `brownie-config.yaml`
        - You'll need to add `dotenv: .env` to your `brownie-config.yaml` and have a `.env` file
- Importing a Contract
- Contract.Deploy
- View Function Call in Brownie
- State-Changing Function Call in Brownie / Contract Interaction
- `transaction.wait(1)`
### Testing Basics
- `test_simple_storage.py`
- Arrange, Act, Assert
- [`assert`](https://docs.pytest.org/en/6.2.x/assert.html)
- `brownie test`
- `test_updating_storage`
- [Pytest / Brownie Test Tips](https://docs.pytest.org/en/6.2.x/)
- Deploy to a Testnet
- `brownie networks list`
- Development vs Ethereum
  - Development is temporary
  - Ethereum networks persist
- RPC URL / HTTP Provider in Brownie
- The network flag
  - `list index out of range`
- `get_account()`
- `networks.show_active()`
- build/deployments
- Accessing previous deployments
- Interacting with contracts deployed in our brownie project
### [Brownie console]
- `brownie console`
# Lesson 6: [Brownie Fund Me](https://github.com/PatrickAlphaC/brownie_fund_me)
### Introduction
- Setup
### Dependencies, Deploying, and Networks
- Dependencies
- [chainlink-brownie-contracts](https://github.com/smartcontractkit/chainlink-brownie-contracts)
- remappings
- Deploy Script (V1)
- `helpful_scripts.py`
- `__init__.py`
- Deploy to Rinkeby
- Contract Verification (`publish_source`)
  - The Manual Way
    - "Flattening"
  - The Programatic Way
    - Getting an [Etherscan API Key](https://etherscan.io/apis)
    - `ETHERSCAN_TOKEN`
  - Interacting with Etherscan
- Deploying to Local Chains
- Introduction to Mocking 
- Constructor Parameters
- `networks` in our `brownie-config.yaml`
- Copying [Mock Contracts from chainlink-mix](https://github.com/smartcontractkit/chainlink-mix)
- Deploying and using our mock
- Refactoring
- Deploying to a persistent ganache
- brownie attach
- Adding a persistent brownie network
- resetting a network build
### Funding and Withdrawing Python Scripts
- Whoops! Let's fix an issue...
- Fund Script
- Withdraw Script
### Testing across networks
- `test_can_fund_and_withdraw`
- default networks
- pytest `pip install pytest`
- pytest.skip
- brownie exceptions
- `mainnet-fork`
- Custom mainnet fork
- Adding a development brownie network
  - `brownie networks add development mainnet-fork-dev cmd=ganache-cli host=http://127.0.0.1 fork='https://infura.io/v3/$WEB3_INFURA_PROJECT_ID' accounts=10 mnemonic=brownie port=8545`
- [Alchemy](https://www.alchemy.com/)
- `brownie test --network mainnet-fork`
- brownie ganache vs local ganache vs mainnet-fork vs testnet...
### Git
- Installing Git
- Creating a repository (repo)
# Lesson 7: [SmartContract Lottery](https://github.com/PatrickAlphaC/smartcontract-lottery)
### Introduction
- Add a `README.md`
- Defining the project
- Is it decentralized?
### `Lottery.sol`
- basic setup
- Main Functions
- address payable[]
- getEntranceFee & Setup
  - [Chainlink Price Feed](https://docs.chain.link/docs/get-the-latest-price/)
  - brownie-config
  - SPDX
- Matching Units of Measure
  - Can't just divide
- Test early and often
- Quick Math Sanity Check
- deleting networks
- [Alchemy](https://www.alchemy.com/) again
- Enum
- `startLottery`
- [Openzeppelin](https://openzeppelin.com/contracts/)... Is this the first openzeppelin reference? 
- [Openzeppelin Contracts Github](https://github.com/OpenZeppelin/openzeppelin-contracts)
- Randomness
- Pseudorandomness
- `block` keyword
  - `block.difficulty`
  - `block.timestamp`
- `keccack256`
- [True Randomness with Chainlink VRF](https://docs.chain.link/docs/get-a-random-number/)
- Chainlink VRF Remix Version
- Inheriting Constructors
- Oracle Gas & Transaction Gas
- [Why didn't we pay gas on the price feeds?](https://ethereum.stackexchange.com/questions/87473/is-chainlinks-price-reference-data-free-to-consume)
- Chainlink Node Fees
- [Request And Receive Introduction](https://docs.chain.link/docs/architecture-request-model/)
- [Kovan Faucets](https://docs.chain.link/docs/link-token-contracts/#kovan)
- Funding Chainlink Contracts
- [Request And Receive Explanation](https://docs.chain.link/docs/architecture-request-model/)
- A Clarification
- `endLottery`
- `returns (type variableName)`
- `fulfillRandomness`
- `override`
- Modulo Operation (Mod Operation %)
- Paying the lottery winner
- Resetting the lottery
### Testing Lottery.sol
- `deploy_lottery.py`
- `get_account()` refactored
- `get_contract`
  - `contract_to_mock`
  - `Contract.from_abi`
- Adding the parameters to deploying to lottery
- `vrfCoordinatorMock` and adding mocks
- `LinkToken` and Mocks
- Successful Ganache Deployment!
- Python Lottery Scripts/Functions
  - `start_lottery`
  - Brownie tip: Remember to `tx.wait(1)` your last transaction
  - `enter_lottery`
  - `end_lottery`
- Funding with LINK
- brownie interfaces
- Waiting for callback
- Integration Tests & Unit Tests
- Test all lines of code
- `test_get_entrance_fee`
- `pytest.skip` (again)
- `test_cant_enter_unless_started`
- `test_can_start_and_enter_lottery`
- `test_can_pick_winner_correctly`
- Events and Logs
- `callBackWithRandomness`
### Lottery.sol Testnet Deployment
- `topics`
- [conftest.py](https://stackoverflow.com/questions/34466027/in-pytest-what-is-the-use-of-conftest-py-files)
# Lesson 8: [Chainlink Mix](https://github.com/smartcontractkit/chainlink-mix) 
## [Brownie Mixes](https://github.com/brownie-mix)
# Lesson 9: [ERC20s, EIPs, and Token Standards](https://github.com/PatrickAlphaC/erc20-brownie)
- [ERC20/EIP20 Standard](https://eips.ethereum.org/EIPS/eip-20)
- What is an ERC20?
- Creating an ERC20
- [OpenZeppelin ERC20](https://docs.openzeppelin.com/contracts/2.x/api/token/erc20)
- [Solidity 0.8](https://docs.soliditylang.org/en/breaking/080-breaking-changes.html)
- I Challenge you to code this yourself!
- `deploy_token.py`
- Copy paste `helpful_scripts.py`
- Viewing our token in metamask
- Adding to an exchange
# Lesson 10: [Defi & Aave](https://github.com/PatrickAlphaC/aave_brownie_py)
### Defi Intro
- [Defipulse](https://defipulse.com/)
- [Defillama](https://defillama.com/)
- [Aave Testnet Site](https://testnet.aave.com/)
- [Paraswap](https://paraswap.io/)
- Decentralized Exchange
### Aave UI
- [Kovan ETH](https://docs.chain.link/docs/link-token-contracts/#kovan)
- What is Aave?
- Borrowing and Lending
- Connecting to Aave
- Depositing Tokens / Lending
- Checking your transaction is correct
- WETH Gateway
- Interest Bearing Token (aToken)
- Collateral
- [DAI](https://makerdao.com/en/)
- [Stablecoin](https://www.investopedia.com/terms/s/stablecoin.asp)
- [Wrapped Bitcoin (wBTC)](https://www.gemini.com/cryptopedia/wrapped-bitcoin-what-can-you-do)
- [Why borrow tokens?](https://docs.aave.com/faq/borrowing)
- [Blockchain Fintech Tutorial](https://blog.chain.link/blockchain-fintech-defi-tutorial-lending-borrowing-python/)
- DISCLAIMER ABOUT BORROWING
- Borrowing Tokens
- [Liquidations](https://docs.aave.com/faq/liquidations)
- Your health factor must be above 1
- [Solvent](https://www.investopedia.com/terms/s/solvency.asp)
- [Stable vs Variable Interest Rate](https://docs.aave.com/faq/borrowing#what-is-the-difference-between-stable-and-variable-rate)
- Repaying our borrows/loans
- Reward token / governance token
- Governance
### [Programmatic Interactions with Aave](https://github.com/PatrickAlphaC/aave_brownie_py)
- Quant Defi Engineer
- [Aave Documentation](https://docs.aave.com/developers/)
- Setup
- Converting ETH -> WETH
- `get_weth.py`
- [IWETH](https://github.com/PatrickAlphaC/aave_brownie_py/blob/main/interfaces/WethInterface.sol)
- [Kovan WETH Token Address: 0xd0a1e359811322d97991e03f863a0c30c2cf029c](https://kovan.etherscan.io/token/0xd0a1e359811322d97991e03f863a0c30c2cf029c)
- [Mainnet WETH Token Address: 0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2](https://etherscan.io/token/0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2)
- Converting WETH -> ETH with `withdraw`
- `aave_borrow.py`
- [LendingPool](https://docs.aave.com/developers/the-core-protocol/lendingpool)
- [LendingPoolAddressProvider](https://docs.aave.com/developers/the-core-protocol/addresses-provider)
- [LendingPool and LendingPoolAddressProvider Addresses](https://docs.aave.com/developers/deployed-contracts/deployed-contracts)
- Fixing import dependencies
- [Aave Github](https://github.com/aave/protocol-v2)
- [ERC20 Approve Function](https://medium.com/ethex-market/erc20-approve-allow-explained-88d6de921ce9)
- [IERC20 from Patrick's repo](https://github.com/PatrickAlphaC/aave_brownie_py/blob/main/interfaces/IERC20.sol)
- `deposit`
- [getUserAccountData](https://docs.aave.com/developers/the-core-protocol/lendingpool#getuseraccountdata)
- Liquidation Threshold
- [Risk Parameters](https://docs.aave.com/risk/asset-risk/risk-parameters)
- Borrowing DAI 
- Getting DAI Conversion Rate
  - [Chainlink Price Feeds](https://docs.chain.link/docs/reference-contracts/)
  - [AggregatorV3Interface](https://github.com/PatrickAlphaC/aave_brownie_py/blob/main/interfaces/AggregatorV3Interface.sol)
- [borrow](https://docs.aave.com/developers/the-core-protocol/lendingpool#borrow)
- [Mainnet DAI Address: 0x6b175474e89094c44da98b954eedeac495271d0f](https://etherscan.io/token/0x6b175474e89094c44da98b954eedeac495271d0f)
- [Aave Testnet Token Addresses](https://aave.github.io/aave-addresses/kovan.json)
- Repaying
- Kovan Run
- Viewing the transactions
### Testing
# Lesson 11: [NFTs](https://github.com/PatrickAlphaC/nft-mix)
### Non-Technical Explainer
- [End-to-end article](https://www.freecodecamp.org/news/how-to-make-an-nft-and-render-on-opensea-marketplace/)
- What is an NFT?
- [ERC721](https://eips.ethereum.org/EIPS/eip-721)
- Token URI
- [Token Metadata Example](https://docs.opensea.io/docs/2-adding-metadata)
- [IPFS](https://ipfs.io/)
### Simple NFT 
- [brownie mix](https://github.com/PatrickAlphaC/nft-mix)
- Initial Setup
- `SimpleCollectible.sol`
- [OpenZeppelin ERC721](https://docs.openzeppelin.com/contracts/3.x/)
- [Pug Image](https://github.com/PatrickAlphaC/nft-mix/blob/main/img/pug.png)
- NFT Constructor
- NFT is a type of factory pattern
- `createCollectible`
  - `_safeMint`
- TokenURI & Metadata
- Opensea listing example
- Is this decentralized?
- Ethereum Size and dStorage
  - [Ethereum Size](https://ycharts.com/indicators/ethereum_chain_full_sync_data_size)
  - [dStorage Solutions](https://ethereum.org/en/developers/docs/storage/)
  - [IPFS](https://www.ipfs.com/)
- You need to have your NFT attributes both on-chain and inside your tokenURI metadata
- `deploy_and_create.py`
- [TokenURI used for the demo: https://ipfs.io/ipfs/Qmd9MCGtdVz2miNumBHDbvj8bigSgTwnr4SbyH6DNnpWdt?filename=0-PUG.json](https://ipfs.io/ipfs/Qmd9MCGtdVz2miNumBHDbvj8bigSgTwnr4SbyH6DNnpWdt?filename=0-PUG.json)
- [IPFS Companion](https://chrome.google.com/webstore/detail/ipfs-companion/nibjojkomfdiaoajekhjakgkdhaomnch?hl=en)
- Rinkeby Deployment
- [Opensea Example](https://testnets.opensea.io/assets/0x8acb7ca932892eb83e4411b59309d44dddbc4cdf/0)
### SimpleCollectible Testing
- What else with NFTs?
### Advanced NFT
- `AdvancedCollectible.sol`
- [Dungeons and Dragons Example](https://github.com/PatrickAlphaC/dungeons-and-dragons-nft)
- Double Inherited Constructors
- `createCollectible` (Advanced)
  - `tokenIdToBreed`
- Working with in-flight Chainlink VRF requests
- Download the NFT images from the [nft-mix](https://github.com/PatrickAlphaC/nft-mix)
- `setTokenURI`
  - `_isApprovedOrOwner`
- Emit events when you update mappings
- [`indexed` event keyword](https://ethereum.stackexchange.com/questions/8658/what-does-the-indexed-keyword-do/8659)
### Advanced deploy_and_create
- Move `OPENSEA_URL` to `helpful_scripts`
- Deploying AdvancedCollectible
  - Opensea testnet is only compatible with Rinkeby
- [Rinkeby Chainlink VRF Contract Addresses](https://docs.chain.link/docs/vrf-contracts/#rinkeby)
- Speeding through adding functions from previous projects
- Deploy to Rinkeby
- `create_collectible.py`
- A quick unit test
- A quick integration test
### Creating Metadata & IPFS
- `create_metadata.py`
- `get_breed`
- Metadata Folder
- `metadata_template`
- NFT Metadata Attributes
- Checking if Metadata file already exists
- Uploading to IPFS
  - `upload_to_ipfs`
  - [Download IPFS Command Line](https://docs.ipfs.io/install/command-line/)
  - [Download IPFS Desktop](https://docs.ipfs.io/install/ipfs-desktop/)
  - [HTTP IPFS Docs](https://docs.ipfs.io/reference/http/api/)
  - `ipfs daemon`
  - [Pinata](https://app.pinata.cloud/)
  - [Pinata Docs](https://docs.pinata.cloud/)
  - Refactoring to not re-upload to IPFS
- Setting the TokenURI
- End-To-End Manual Testnet Test
- Viewing on Opensea
# Lesson 12: [Upgrades](https://github.com/PatrickAlphaC/upgrades-mix)
### Introduction to upgrading smart contracts
- [Original Video](https://www.youtube.com/watch?v=bdXJmWajZRY)
- Smart Contracts can be upgraded!
- Does this mean they are not immutable? 
- [Trail of Bits on Upgradeable Smart Contracts](https://blog.trailofbits.com/2018/09/05/contract-upgrade-anti-patterns/)
- The "Not Really Upgrading" / Parameterization Method
- The Social Yeet / Migration Method
- [Contract Migration](https://blog.trailofbits.com/2018/10/29/how-contract-migration-works/)
- Proxies
  - DelegateCall
  - Terminology:
    - Implementation Contract
    - Proxy Contract
    - User
    - Admin
  - Gotchas:
    - Storage Clashes
    - Function Selector
    - Function Selector Clashes
  - Proxy Patterns:
    - [Transparent Proxy Pattern](https://blog.openzeppelin.com/the-transparent-proxy-pattern/)
    - [Universal Upgrade Proxy Standard](https://eips.ethereum.org/EIPS/eip-1822)
    - [Diamond/Multi-Facet Proxy](https://eips.ethereum.org/EIPS/eip-2535)
### Upgrades-mix and code
- Setup
- `Box.sol`
- `BoxV2.sol`
- Getting the proxy contracts
- [Openzeppelin Proxy Github](https://github.com/OpenZeppelin/openzeppelin-contracts/tree/master/contracts/proxy/transparent)
- `01_deploy_box.py`
- Hooking up a proxy to our implementation contract
- (Optional) [Creating a Gnosis Safe](https://help.gnosis-safe.io/en/articles/3876461-create-a-safe)
- Initializers
- Encoding Initializer Function
- Assigning ABI to a proxy
- Running the script
- Upgrade Python Function
### Testing Upgrades
- Testing our proxy
- Testing our upgrades
### Upgrades on a testnet
# Bonus Lesson 13: [Full Stack Defi](https://github.com/PatrickAlphaC/defi-stake-yield-brownie)
- [FreeCodeCamp React](https://www.freecodecamp.org/news/tag/react/)
- What are we building?
- Setup
- `DappToken.sol`
- `TokenFarm.sol`
  - `tokenIsAllowed`
  - `addAllowedTokens`
  - mapping of a mapping
  - `stakeTokens`
  - `issueTokens`
  - `getUserTotalValue`
  - `getUserSingleTokenValue`
  - `getTokenValue`
  - `setPriceFeedContract`
  - `unStakeTokens`
  - Can this be reentrancy attacked?
### Defi Stake Yield Brownie Scripts & Tests
- `deploy.py`
  - Deploying DappToken
  - Deploying TokenFarm
  - Adding allowed tokens
- [ERC20 Kovan Faucet](https://erc20faucet.com/)
- Mocking our ERC20s
### Testing our Defi Stake Yield Brownie Dapp
- `test_set_price_feed_contract`
- `test_stake_tokens`
- Fixtures
- `test_issue_tokens`
- Now you try on tests!
### Front End / Full Stack
- Front End Introduction
- Typescript
- [React](https://reactjs.org/)
- [useDapp](https://usedapp.readthedocs.io/en/latest/)
- [npx](https://www.npmjs.com/package/npx)
- [yarn](https://classic.yarnpkg.com/en/docs/install/)
- `create-react-app`
  - Layout
- [Testing Front End](https://www.freecodecamp.org/news/testing-react-hooks/)
- yarn && yarn start
- Connecting our wallets
  - Install useDapp
  - Header Component
  - Connect Button
- [Material-UI](https://material-ui.com/)
- Making our button nicer
- `Main.tsx`
  - Sending `brownie-config` & `build` folder to our UI
  - Helper Config
  - TypeScript error suppression
  - Getting addresses
  - [Ethers](https://docs.ethers.io/v5/)
  - Only support kovan
- `YourWallet`
  - `supportedTokens`
  - State Hooks
  - Showing tokens
  - `WalletBalance`
  - [`ethersproject/units`](https://www.npmjs.com/package/@ethersproject/units)
  - `BalanceMsg`
  - Stake Form
  - Calling `approve`
# Bonus Lesson 14: Security
- [Best Practices](https://consensys.github.io/smart-contract-best-practices/)
- [Attacks](https://consensys.github.io/smart-contract-best-practices/known_attacks/)
  - Oracle Attacks
  - Re-entrancy Attacks
TODO:
github (fund_me)
(also show git clone on the projects in here)
Add lesson transition slides
Add summaries
Add photos & green screen stuff
Clarify the part about adding erc20s to uniswap. Say it's for mainnet only. 
Clarify that we aren't going to go too deep into the fintech terms, but we will go through the UI and then teach how to code it
On the NFT stuff, make sure you mention IPFS compainion earlier
NFT pip install requests
