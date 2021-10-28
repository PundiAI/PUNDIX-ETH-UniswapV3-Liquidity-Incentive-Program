---
description: 'Objectives: Check if your pool/token is eligible for our incentives'
---

# NonfungiblePositionManager (1)

### All subsequent interactions will be on etherscan. Please refer to this [link](https://etherscan.io).

### 0xC36442b4a4522E871399CD717aBDD847Ab11FE88

1. Input `0xC36442b4a4522E871399CD717aBDD847Ab11FE88` in the search bar
2. Navigate to the `Contract` tab
3. Click on the `Read Contract` button
4. Click into the `positions` dropdown
5. Input:
   1. tokenId (uint256)

```markup
<your tokenId>
```

6\. Click `query` (return example):

```
 nonce uint96, operator address, token0 address, token1 address, fee uint24, tickLower int24, tickUpper int24, liquidity uint128, feeGrowthInside0LastX128 uint256, feeGrowthInside1LastX128 uint256, tokensOwed0 uint128, tokensOwed1 uint128

[ positions(uint256) method Response ]
  nonce   uint96 :  0
  operator   address :  0x0000000000000000000000000000000000000000
  token0   address :  0x0FD10b9899882a6f2fcb5c371E17e70FdEe00C38
  token1   address :  0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2
  fee   uint24 :  3000
  tickLower   int24 :  -83040
  tickUpper   int24 :  -69180
  liquidity   uint128 :  759171611158708921
  feeGrowthInside0LastX128   uint256 :  0
  feeGrowthInside1LastX128   uint256 :  0
  tokensOwed0   uint128 :  0
  tokensOwed1   uint128 :  0
```

{% hint style="info" %}
Save these fields in your checklist

1. token0 address
2. token1 address
3. fee uint24
{% endhint %}

> For your information, fees are the % fees for the created pool on Uniswap (in case you don’t know the conversion)
>
> 1. 1% 🡪 10000
> 2. 0.3% 🡪 3000
> 3. 0.05% 🡪 500

![](<../.gitbook/assets/NonfungiblePositionManager 1.PNG>)
