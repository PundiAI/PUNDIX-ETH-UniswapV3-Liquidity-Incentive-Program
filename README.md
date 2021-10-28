---
description: Teaching users how to stake in an incentive pool created by Pundi X
coverY: 0
---

# Uniswapv3Staker User Manual

**Overview**

You will essentially be interacting with 3 contracts (high level overview)

1. **UniswapV3Factory (0x1F98431c8aD98523631AE4a59f267346ea31F984)**
   1. **This contract will mainly be used for finding the pool address for the liquidity you provided**
   2. _You may refer to the _[_Uniswapv3 Factory technical docs_](https://docs.uniswap.org/protocol/reference/core/UniswapV3Factory)_ or_
   3. _The Github _[_Uniswapv3 Factory_](https://github.com/Uniswap/v3-core/blob/v1.0.0/contracts/UniswapV3Factory.sol)_ code_
2. **NonfungiblePositionManager (0xC36442b4a4522E871399CD717aBDD847Ab11FE88)**
   1. **This will be your NFT token manager for approvals, querying of NFT info, safeTransferFrom to other accounts or smart contracts**
   2. To put it simply, this is a bridge/router/manager on your NFT.
   3. _You may refer to the to the _[_NonfungiblePositionManager technical docs_](https://docs.uniswap.org/sdk/reference/classes/NonfungiblePositionManager)_ or_
   4. _The Github _[_NonfungiblePositionManager_](https://github.com/Uniswap/v3-periphery/blob/main/contracts/NonfungiblePositionManager.sol)_ code_
3. **UniswapV3Staker (0x1f98407aaB862CdDeF78Ed252D6f557aA5b0f00d):**
   1. **This is the main contract to interact with for liquidity mining/stake in the incentive pool created**
   2. _You may refer to the _[_UniswapV3Staker technical docs_](https://docs.uniswap.org/protocol/reference/periphery/staker/UniswapV3Staker)_ or_
   3. _The Github _[_Uniswapv3Staker_](https://github.com/Uniswap/v3-staker)_ code_

![High level overview of the flow of interaction with the contracts](<.gitbook/assets/Overview Chart.PNG>)

{% hint style="info" %}
**If you are sure about your pool info i.e. that you have provided liquidity for PUNDIX-ETH at the 0.3% fee level, you may skip directly to **[**NonfungiblePositionManager (1)**](step-by-step-guide/nonfungiblepositionmanager-1.md)** and just follow the steps accordingly. Make sure you have your tokenID handy too!**
{% endhint %}
