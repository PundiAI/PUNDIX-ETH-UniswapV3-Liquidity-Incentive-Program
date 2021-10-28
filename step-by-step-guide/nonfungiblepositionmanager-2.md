---
description: >-
  Objectives: Approve NFT for safe transfer and transfer NFT to UniswapV3Staker
  Contract
---

# NonfungiblePositionManager (2)

### 0xC36442b4a4522E871399CD717aBDD847Ab11FE88

> Before conducting liquidity mining, you will have to approve the **UniswapV3Staker** contract to use your token and then do a safe transfer to this contract address. This approval process is needed so that the smart contract is given the authority to “use” your tokens.

### Part 1 (Approve)

1. Input `0xC36442b4a4522E871399CD717aBDD847Ab11FE88`in the search bar
2. Navigate to the `Contract` tab
3. Click on the `Write Contract` button
4. Click into the `approve` dropdown
5. Ensure the correct wallet address is connected

![](<../.gitbook/assets/Metamask to Etherscan.PNG>)

&#x20;  6\.  Input:

&#x20;        1\.  to (address)

&#x20;        2\.  tokenId (uint256)

```
0x1f98407aaB862CdDeF78Ed252D6f557aA5b0f00d
<your tokenID>
```

> for Field 1, be sure to put in this address: 0x1f98407aaB862CdDeF78Ed252D6f557aA5b0f00d
>
> &#x20;this is the contract address of UniswapV3Staker

7\. Click `write`

8\. A Metamask notification will appear, click `confirm`

![](<../.gitbook/assets/NonfungiblePositionManager 3 (approve).PNG>)

### Part 2 (safeTransferFrom)

1. Click into the `safeTransferFrom` dropdown (there are 2 safeTransferFrom, please choose number 11 not 12)
2. Input:
   1. from (address)
   2. to (address)
   3. tokenId (uint256)

```
<token owner address ie yours>
0x1f98407aaB862CdDeF78Ed252D6f557aA5b0f00d
<your tokenID>
```

> for Field 2, be sure to put in this address: 0x1f98407aaB862CdDeF78Ed252D6f557aA5b0f00d
>
> this is the contract address of UniswapV3Staker

&#x20; 3\.  Click `write`

12\. A Metamask notification will appear, click `confirm`

![](<../.gitbook/assets/NonfungiblePositionManager 4 (safeTransferFrom).PNG>)
