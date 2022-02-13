# About

This file will list issues/updates by timestamp. If you have an issue that you don't see here, please make an issue on this repo. 

## Faucet Issues
- If you have any issues with a faucet, please try another testnet. You'll have to update some contract addresses based on the testnet you're working on. You can find the [most up to date faucets here.](https://docs.chain.link/docs/link-token-contracts/) 
- If the Rinkeby faucet isn't working, you can use a kovan faucet, just be sure to use Kovan Etherscan and Kovan in your Metamask!
- *Big Update*: [New Rinkeby Faucet Located Here](https://faucets.chain.link/rinkeby)
- You can find [Backup Faucets here](https://docs.chain.link/docs/link-token-contracts/#rinkeby)

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
- [4:00:00](https://www.youtube.com/watch?v=M576WGiDBdQ&t=14423s) Issue with ganache and web3.py
  - As of `5.25.0` of [web3.py](https://github.com/ethereum/web3.py/tags), we now need to add gasPrice to our transactions with a local ganache chain. 
  - Adding `"gasPrice": w3.eth.gas_price,` should fix your issue in the transactions. 

Full Example:
```python
transaction = SimpleStorage.constructor().buildTransaction(
    {
        "chainId": chain_id,
        "gasPrice": w3.eth.gas_price,
        "from": my_address,
        "nonce": nonce,
    }
)
```
- [3:56:20](https://youtu.be/M576WGiDBdQ?t=13372) Colorized Brackets.
  * The referenced extension has been deprecated due to VS code adding native functionality. To enable the new setting search for `bracket` and check the checkbox below:
  `Editor > Bracket Pair Colorization:` **Enabled**

    ![image](https://user-images.githubusercontent.com/2119741/147293025-4dec848b-747b-4da7-9009-3f9174198b54.png)

- [3:55:09](https://youtu.be/M576WGiDBdQ?t=14109) Confusing network ID and chain ID
  - In the video the network ID is copied instead of the chain id. 
Whenever the terms Network ID and Chain ID are used without distinction, it should be noted that both IDs can be different for a server such as Ganache. As you can see here, Ganache can be using different IDs.

```
>>> from web3 import Web3
>>> w3 = Web3(Web3.HTTPProvider("http://127.0.0.1:8545"))
>>> w3.eth.chain_id
1337
>>> w3.net.version
'5777'
>>> 
```
- [4:19:40](https://youtu.be/M576WGiDBdQ?t=15580) Installing ganache-cli with yarn
  - ganache-cli is deprecated
  - visit [GitHub Ganach repo](https://github.com/trufflesuite/ganache/releases/tag/v7.0.0) for details
  - Yarn installation is no longer necessary. Installation is now via
  - `npm install ganache --global`
  - Usage is simply: `ganache` 
  - Visit [https://www.npmjs.com/package/ganache](https://www.npmjs.com/package/ganache) for more information.
  - This has no effect on the later brownie installation, brownie works just fine with the new ganache implementation and the deprecated ganache-cli is not necessary.

## Lesson 6
- [5:49:39](https://youtu.be/M576WGiDBdQ?t=20988) Testing Fund Me
  - The function `test_can_fund_and_withdraw()` in `test_fund_me.py` can easily lead to an incomprehensible error message if the exchange rate calculation has a small deviation.
  `E AttributeError: 'NoneType' object has no attribute '_with_attr'.`
  
  - To prevent this, the test can be adapted as follows. The assert compares the expected value with the calculated value getConversionRate returns.
  - In case of an even higher deviation than the +100 buffer the assert will return an easy to understand error.
  
  
  ```python
  def test_can_fund_and_withdraw():
      account = get_account()
      fund_me = deploy_fund_me()
      entrance_fee = fund_me.getEntranceFee() + 100
      conversion_rate = fund_me.getConversionRate(entrance_fee)
      minimumUSD = 50 * 10 ** 18
      assert conversion_rate >= minimumUSD
      tx = fund_me.fund({"from": account, "value": entrance_fee})
      tx.wait(1)
      assert fund_me.addressToAmountFunded(account.address) == entrance_fee
      tx2 = fund_me.withdraw({"from": account})
      tx2.wait(1)
      assert fund_me.addressToAmountFunded(account.address) == 0
  ``` 


## Lesson 7
- [8:06:54ish](https://youtu.be/M576WGiDBdQ?t=29214)
  - In the video, we use events exclusivly to test our contracts, however, we could have also used `tx.return_value` to get the return value of a function. 
  - However, it's still best practice to learn how to use events, especially when updating mappings!

- [8:10:20ish](https://youtu.be/M576WGiDBdQ?t=29423)
  - In the video, `starting_balance_of_account` and `balance_of_lottery` are retrieved AFTER `lottery.endLottery()`
  - For correctness those 2 statements should be run BEFORE `lottery.endLottery()` 
  - The tests pass because `starting_balance_of_account == account.balance()` (L81) and `lottery.balance()` is already 0
  - This is a subtle bug in the test, which also showcases a problem with tests - we have no one to test the tests ;) Still, having tests is better than not having them, just don't put all your assurances into them


## Lesson 10
- The Aave testnet site has moved from `https://testnet.aave.com` to `https://staging.aave.com` and some of the functionality is lost :( 
- For our `repay_all` function, we originally had:
```python
repay_all(AMOUNT, lending_pool, account)
```

But it should be:

```
repay_all(Web3.toWei(amount_dai_to_borrow, "ether"), lending_pool, account)
```
We want to pay back the DAI not the ETH! Just remember, you'll still have a vveerrrryyyy small amount of DAI borrowed because of interest. If you see something with an `E` in it, you did it right!
