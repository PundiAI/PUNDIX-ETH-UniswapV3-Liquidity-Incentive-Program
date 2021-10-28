---
description: 'Objectives: Stake, Unstake, Withdraw and Claim reward'
---

# Step 5: UniswapV3Staker

![](<../.gitbook/assets/UniV3Staker 18-10-21.png>)

{% hint style="info" %}
1. You may unstake then withdraw your tokens or claim rewards before the incentive has ended. The steps are the same.
2. You may unstake then withdraw your tokens or claim rewards in whatever manner you would like. You do not need to withdraw token then claim rewards or vice versa.
3. You may choose to withdraw tokens and not claim rewards or claim rewards and not withdraw tokens.
{% endhint %}

### 0x1f98407aaB862CdDeF78Ed252D6f557aA5b0f00d

### Part 1 (Stake)

{% hint style="info" %}
You may only start staking in the pool when the incentive has started on **Friday, 12 November, 2021 9:00:00 AM (GMT+8).**
{% endhint %}

1. Input `0x1f98407aaB862CdDeF78Ed252D6f557aA5b0f00d` in the search bar
2. Navigate to the `Contract` tab
3. Click on the `Write Contract` button
4. Click into the `stakeToken` dropdown
5. Ensure the correct wallet address is connected
6. Input:
   1. key (tuple)
   2. tokenId

```
['0x0fd10b9899882a6f2fcb5c371e17e70fdee00c38','0xD050430dd432876cF5622fF60c4Dc106b64fA753',1636678800,1639184400,'0x1A63853beA8A8ccFb52898E1783909d7da475E46']
<your tokenID>
```

> Tuple information:
>
> 1. Rewardtoken address
> 2. Pool address
> 3. Start time
> 4. End time
> 5. Refundee

{% hint style="info" %}
Your tokenID needs to match the pool address if not the contract will throw an error
{% endhint %}

7\. Click `write`

8\. A Metamask notification will appear, click `confirm`

![](<../.gitbook/assets/UniswapV3Staker User1 Stake.PNG>)

### Part 2 (Unstake)

{% hint style="info" %}
You will always need to unstake before withdrawing even when the incentive has already ended
{% endhint %}

1. Click into the `unstakeToken` dropdown
2. Input:
   1. key (tuple)
   2. tokenId (uint256)

```
['0x0fd10b9899882a6f2fcb5c371e17e70fdee00c38','0xD050430dd432876cF5622fF60c4Dc106b64fA753',1636678800,1639184400,'0x1A63853beA8A8ccFb52898E1783909d7da475E46']
<your tokenID>
```

{% hint style="info" %}
Once the incentive has ended, your token can be unstaked by anyone, and you may stand to lose your rewards if you do not claim them.
{% endhint %}

3\. Click `write`

4\. A Metamask notification will appear, click `confirm`

![](<../.gitbook/assets/UniswapV3Staker User 2 Unstake.PNG>)

### Part 3 (Withdraw Token)

{% hint style="info" %}
Please ensure your token has been unstaked before withdrawing. Once the incentive has ended, anyone can unstake your token
{% endhint %}

1. Click into the `withdrawToken` dropdown
2. Input:
   1. tokenId (uint256)
   2. to (address)
   3. data (bytes)

```
<your tokenID>
<your wallet address>
0x0000000000000000000000000000000000000000
```

{% hint style="info" %}
Ensure \<your wallet address> is the owner of \<your tokenID>
{% endhint %}

3\. Click `write`

4\. A Metamask notification will appear, click `confirm`

![](<../.gitbook/assets/UniswapV3Staker User 3 (withdrawToken).PNG>)

### Part 4 (Checking rewards getRewardInfo/rewards)

#### 4a) getRewardInfo

{% hint style="info" %}
Use the `getRewardInfo` function if your token is <mark style="color:red;">STILL STAKING</mark>
{% endhint %}

1. Click on the `Read Contract` button
2. Click into the `getRewardInfo`dropdown (this will be the pending reward while your token is still staking)
3. Input:
   1. key(tuple)
   2. tokenId (uint256)

```
['0x0fd10b9899882a6f2fcb5c371e17e70fdee00c38','0xD050430dd432876cF5622fF60c4Dc106b64fA753',1636678800,1639184400,'0x1A63853beA8A8ccFb52898E1783909d7da475E46']
<your tokenID>
```

4\. Click `query` return (eg):

```
reward uint256, secondsInsideX128 uint160
[ getRewardInfo method Response ]
reward uint256 : 6244701548997252
secondsInsideX128 uint160 : 3671934031539594722601452813763156279674
```

![](<../.gitbook/assets/UniswapV3Staker User 4 (getRewardInfo).PNG>)

#### 4b) rewards

{% hint style="info" %}
The `rewards` function can only be used once you have <mark style="color:red;">`UNSTAKED`</mark> your token
{% endhint %}

1. Click into the `rewards` dropdown (your eligible rewards once you unstake your token, it will be 0 until you unstake your NFT if you don’t already have any pending rewards in the contract)
2. Input:
   1. \<input> (address)
   2. \<input> (address)

```
0x0FD10b9899882a6f2fcb5c371E17e70FdEe00C38
<your wallet address>
```

{% hint style="info" %}
Ensure \<your wallet address> is the owner of \<your tokenID>
{% endhint %}

3\. Click `query` return (eg):

```
uint256
[ rewards(address,address) method Response ]
uint256 : 0
```

![](<../.gitbook/assets/UniswapV3Staker User 5 (rewards).PNG>)

### Part 5 (Claim Rewards)

1. Click on the `Write Contract` button
2. Click into the `claimReward` dropdown
3. Ensure the correct wallet address is connected
4. Input:
   1. rewardToken (address)
   2. to (address)
   3. amountRequested (uint256)

```
0x0FD10b9899882a6f2fcb5c371E17e70FdEe00C38
<your wallet address>
<your reward amount you want to claim>
```

{% hint style="info" %}
The amount you requested from part \*\*4b) \*\*will be needed here. You may request any amount between 0 to the amount you requested in **4b).**

Say my eligible rewards was 21961075569626700000. I can claim a reward amount anything ranging from 1 to 21961075569626700000.
{% endhint %}

5\. Click `write`

6\. A Metamask notification will appear, click `confirm`

![](<../.gitbook/assets/UniswapV3Staker User 6 (claimReward).PNG>)
