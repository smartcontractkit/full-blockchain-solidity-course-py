# About

This file will list issues/updates by timestamp. If you have an issue that you don't see here, please make an issue on this repo. 

## Faucet Issues
- If you have any issues with a faucet, please try another testnet. You'll have to update some contract addresses based on the testnet you're working on. You can find the [most up to date faucets here.](https://docs.chain.link/docs/link-token-contracts/) 
- If the Rinkeby faucet isn't working, you can use a kovan faucet, just be sure to use Kovan Etherscan and Kovan in your Metamask!

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


