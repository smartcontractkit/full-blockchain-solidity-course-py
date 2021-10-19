# About

This file will list issues/updates by timestamp. If you have an issue that you don't see here, please make an issue on this repo. 

## Faucet Issues
- If you have any issues with a faucet, please try another testnet. You'll have to update some contract addresses based on the testnet you're working on. You can find the [most up to date faucets here.](https://docs.chain.link/docs/link-token-contracts/) 
- If the Rinkeby faucet isn't working, you can use a kovan faucet, just be sure to use Kovan Etherscan and Kovan in your Metamask!

## Linting issues

If you see something along the lines of:

```
ParserError: Source "OpenZeppelin/openzeppelin-contracts@3.4.0/contracts/access/Ownable.sol" not found: File not found.
import "@openzeppelin/contracts/access/Ownable.sol";
```

In your vscode, these and be safely ignored. However you can also add to your settings to ignore these. 
1. Create a `.vscode` folder at the root of your project.
2. Create a file called `settings.json`
3. Add the following code:

```json
{
  "solidity.remappings": [
    "@chainlink/=/Users/patrick/.brownie/packages/smartcontractkit/chainlink-brownie-contracts@0.2.2",
    "@openzeppelin/=/Users/patrick/.brownie/packages/OpenZeppelin/openzeppelin-contracts@4.3.2"
  ]
}
```

Or whatever version your `@chainlink` and `@openzeppelin` contracts need. For example:
<img width="1190" alt="Screen Shot 2021-10-05 at 6 01 45 PM" src="https://user-images.githubusercontent.com/54278053/136108868-15739283-0789-4ce1-bf4a-7491ea4b7c2e.png">


## Integration Testing Issues
- In some integration tests, we do something like `time.sleep(60)`. Sometimes, you'll have to do much longer, we've had reports go up to `time.sleep(300)`. So, if you want to try that, go get a coffee break while your integration test runs!

## Lesson 3:
- [2:37:05](https://youtu.be/M576WGiDBdQ?t=9425) Kovan vs Rinkeby
  - Our `FundMe.sol` needs to be deployed to the *rinkeby* chain to work, but if you go to try the price feeds from the Chainlink docs using the remix link, that one has the *kovan* price feeds in it, so needs to be deployed to kovan. 
  - If you want to test the price feeds from the video using the Chainlink docs remix link, you'll need to follow the steps to [get kovan ETH](https://docs.chain.link/docs/link-token-contracts/#kovan).  

## Lesson 4:
- [3:43:52](https://youtu.be/M576WGiDBdQ?t=13432) Installing solcx version 0.6.0
  - In the video, we forgot to do 2 things in order to compile our solidity code:
    - Import `install_solc`, so we need to change this line:
      - `from solcx import compile_standard`
    - To this line:
      - `from solcx import compile_standard, install_solc`
    - And then, we need to add a line right before we run the `compile_standard` code:
      - `install_solc("0.6.0")`

## Lesson 7
- [8:06:54ish](https://youtu.be/M576WGiDBdQ?t=29214)
  - In the video, we use events exclusivly to test our contracts, however, we could have also used `tx.return_value` to get the return value of a function. 
  - However, it's still best practice to learn how to use events, especially when updating mappings!

- [8:10:20ish](https://youtu.be/M576WGiDBdQ?t=29423)
  - In the video, `starting_balance_of_account` and `balance_of_lottery` are retrieved AFTER `lottery.endLottery()`
  - For correctness those 2 statements should be run BEFORE `lottery.endLottery()` 
  - The tests pass because `starting_balance_of_account == account.balance()` (L81) and `lottery.balance()` is already 0
  - This is a subtle bug in the test, which also showcases a problem with tests - we have no one to test the tests ;) Still, having tests is better than not having them, just don't put all your assurances into them
