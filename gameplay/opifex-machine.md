---
description: It's All About A Machine And The Endro It Constructs
---

# Opifex Machine

## Introduction

What is the Opifex Machine?

Opifex Machines are highly advanced machines that are used to construct Endros. Upon the indexing of Endros, you can pick and construct one of them. Indexing can only be done once per machine, and once indexed, the candidates will stay unmodified forever until one is picked for construction. Enga Federation is in full control of these machines, and they are also responsible for the production of these machines. For each generation, Enga Federation decides how many machines will be produced and how much each realm's contribution will be.

Opifex Machines need power source (staked collateral) that acts as a fuel to the machine, and once it is provided, the machine will begin constructing the Endro.

Opifex Machines have four states:

* **Idle**: The machine is idle and ready to call for indexing.
* **Indexing**: The machine is currently indexing the Endro candidates.
* **Indexed**: The machine has indexed the candidates, and it is ready for construction.
* **Endro**: The Endro is constructed and ready.

Each state of the machine has a value on the market. For example, a machine that is idle might have a higher value to a machine that has been indexed but with weak and bad candidates. Or, an indexed machine with rare Endros might have a higher value to an idle machine, or even to many already constructed Endros.

The starting price of an Opifex Machine in auctions is determined by the Enga Federation.

## Buying an Opifex Machine

Before you can foster and spend time with your Endros on Engaland, you will need an Opifex Machine to build them for you.

You have three ways of acquiring an Opifex Machine:

* Participating in Auctions
* Participating in Drop-Ticket Raffles
* Using a Marketplace

Auctions and raffles are time-limited events. If you miss out on them, the only other way that you can purchase an Opifex Machine is through the Marketplace.

As mentioned above, Opifex Machines are distributed in "generations" and the number of machines produced in a generation is determined by the Enga Federation.

## Starting Your Opifex Machine

Once you have an Opifex Machine, you can start it by calling for indexing. The process of indexing takes place on Polygon network. Upon calling for indexing, the machine will send a request to ChainLink VRF to generate a random number. That random number is going to serve as the seed for the indexing process to ensure that all 10 candidates are truly unique and random.

Once the indexing is done, 10 different candidates will be presented to you. You will have to pick one of them to construct the Endro. The rest of the candidates will be discarded.

These machines all carry different provably random numbers which are called "seeds" to ensure [Traits](traits.md) integrity and randomness for each candidate. As you look at the candidates, you can view their traits and [Rarity Scores](../general/introduction.md#endro-value).

The trait range and rarity probabilities are shown below:

|  Rarity  | Range(L) | Range(H) | Percentage |  BRS  |
| :------: | :------: | :------: | :--------: | :---: |
|  Common  |   25-74  |   25-74  |     50%    | 50-74 |
| Uncommon |   10-24  |   75-89  |     30%    | 75-89 |
|   Rare   |    2-9   |   90-97  |     16%    | 90-97 |
| Mythical |    0-1   |   98-99  |     4%     | 98-99 |

## Constructing an Endro

When you select the desired candidate you want to construct, you will need to provide [Power Source](../tokenomic-land/collateral.md#introduction) to the machine. This power source or collateral is used as the fuel for the machine to start the process of constructing.

As mentioned on [Introduction](../general/introduction.md#base-value), the power source is the base value of the Endro. For more information regarding collaterals, read [this](../tokenomic-land/collateral.md).

Initial Rarity Score of a candidate determines the minimum collateral needed to construct them. The higher the score, the more collateral it requires.

The minimum amount of collateral required is 5 [DAI](https://en.wikipedia.org/wiki/Dai\_\(cryptocurrency\)), while the maximum is 450 DAI worth of collateral. The formula to calculate the collateral is as follows:

```
if rarityScore < 300 return 5;
    else if rarityScore >= 300 and rarityScore < 400 return 5;
    else if rarityScore >= 400 and rarityScore <= 475 return 15;
    else if rarityScore >= 476 and rarityScore <= 525 return 60;
    else if rarityScore >= 526 and rarityScore <= 570 return 150;
    else if rarityScore >= 571 return 450;
```

For example, if the Rarity Score is less than 300, you need to stake at least 5 DAI worth of the collateral to build the Endro.

## What to do next?

Once you have an Endro, you can play with them in games, upgrade and train them, participate in ENGADAO, or just interact with them on a daily basis to increase their Zeal.

## Transferring Your Endro

When you transfer your Endro to a new owner, the collateral and all the items the Endro owns or wears, including skins, cosmetics and chipset cards will also transfer along with it.

You can also withdraw your collateral if you deem it necessary, however, doing so will result in **dismissing your Endro**, which is a non-reversible action and your Endro will be burnt as a result.

{% hint style="danger" %}
Dismissing your Endro means destroying it, you will lose your NFT if you withdraw all the staked collateral, although, if you just reserve enough collateral within your NFT that equals the minimum required to run the opifex machine, then you will still have your NFT and can withdraw the interests you gained from staking.
{% endhint %}
