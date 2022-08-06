---
description: On-Chain Game Mechanism
---

# Rarity Farming

## Introduction

Rarity Farming is an innovative game mechanism introduced by [Aavegotchi](https://aavegotchi.com). It's an appreciation reward to those enthusiastic gamers who interact with the platform on-chain daily and consecutively.

The following will explain how you can interact with the game and get rewarded.

## How Can You Engage In Rarity Farming?

* When you index the candidates using an [Opifex Machine](opifex-machine.md), make sure to choose the Endro that has the best stats and the highest initial [Rarity Score](traits.md#rarity-score)
* Strengthen and dress your Endro up with [Wearables](wearables/), including [Cosmetics](wearables/cosmetics.md) and [Chipset Cards](wearables/chipset-cards.md) to affect the overall Rarity Score
* Participate in games to gain [Experience](traits.md#experience)
* Interact with your Endros on a daily basis to increase their [Zeal](traits.md#zeal)

## Calculate Rarity

There are 2 types of rarity scores, namely BRS (Base Rarity Score) and ARS (Absolute Rarity Score).

### BRS

BRS is calculated from accumulating the rarity score of Endro's stats and equipped wearables.

#### Stats

The formula below determines the final value of BRS for a stat:

```
if stat >= 50 return stat;
else return 99 - stat;
//there is no value lower than 50
```

#### Wearables

On the platform wearables are divided into two categories: Cosmetics and Chipset Cards.

Cosmetics have a BRS value bonus which is listed here.

Chipset Cards on the other hand change the value of stat as a modifier, which will affect the BRS of that stat, they are listed here.

### ARS - Absolute Rarity Score

Aavegotchi has come up with a great idea that focuses on how you as a player must be aware of other players' strategies to have the best rarity score. It is called Absolute Rarity Score (ARS). ARS is a mechanism that incentivizes players to have a strategy in upgrading their stats. Meaning, upgrading the stat towards their maximum/minimum value (99 or 1) will not necessarily result in a better rarity score, as the ARS of that value might be low. The way ARS works is rather complex, but using an example might help you better grasp the concept.

For example if a considerable number of players have trained their Endro to have the highest Aggressiveness level, then the ARS for that high Aggressiveness level will be lower than that of the lowest Aggressiveness Level, since it would not be rare anymore.

{% hint style="danger" %}
ARS has not been included yet in our project yet, but you should be aware of it. How much it influences and the formula to calculate ARS is being discussed.
{% endhint %}

### Final Rarity Score

```
finalRarityScore = traitsBRS + cosmeticsBRS + traitsARS
```

Example:

For simplicity, only three of the stats, one chipset card and two cosmetics are included in the table below.

|                    Trait, Wearables                    |                     Trait Value                    | BRS |                   ARS                   |
| :----------------------------------------------------: | :------------------------------------------------: | :-: | :-------------------------------------: |
|                     Aggressiveness                     | 0 <mark style="color:green;">+ 1</mark> (modifier) |  98 |              2(98% possess)             |
|                        Mentality                       |                         61                         |  61 |              50(50%possess)             |
|                      Common-Skill                      |                         23                         |  76 |              40(60%possess)             |
| Chipset Card, <mark style="color:green;">AGG +1</mark> |                          -                         |  -  |                    -                    |
|                       Flossy Hair                      |                          -                         |  20 |                    -                    |
|                       Army Shirt                       |                          -                         |  50 |                    -                    |
|                        TOTAL BRS                       |                          -                         | 305 |                    -                    |
|                        TOTAL ARS                       |                          -                         |  -  |                    92                   |
|      <mark style="color:red;">TOTAL RARITY</mark>      |                          -                         |  -  | <mark style="color:red;">**397**</mark> |

While Aggressiveness has a high stat value (1) and BRS (98), the ARS is low (2) since 98 percent of Endros have an Aggressiveness value of 1. Removing the chipset card would decrease the Aggressiveness value to 0, which would result in a higher BRS and ARS value.

{% hint style="danger" %}
As mentioned previously, the formula for deriving ARS is not specified yet. ARS is not used in rarity farming for the time being.
{% endhint %}

## Rewards

Based on the [tokenomics](../tokenomic-land/tokenomics.md#protocol-revenue), In each season of Rarity Farming, the rarest Endros will be rewarded with a number of ENGA tokens.

At the moment, there are three categories of rarity farming rewards, however that could be expanded in the future by the Enga Federation. The categories are as follows:

* Endro [Rarity Score](traits.md#rarity-score) (BRS, ARS is not included yet)
* Endro [Zeal](traits.md#zeal) value
* Endro [Experience and Level](traits.md#experience)

For each category, rewards are distributed based on a descending curve, top Endros will receive more rewards than other Endros who are positioned lower on the curve. Also, there is a limit on the number of Endros that can receive a reward.

{% hint style="info" %}
This limitation is specified by the Enga Federation every season of the rarity farming, and the proportion of rewards allocated to each of the categories will be decided by them as well.
{% endhint %}

{% hint style="info" %}
More categories might be added when new game mechanisms are introduced.
{% endhint %}

## Rarity Farming Seasons <a href="#rarity-farming-seasons" id="rarity-farming-seasons"></a>

Rarity Farming is divided into different seasons. Each season has its own competition categories, size of reward pool, and reward distribution curve.

## Collecting Rarity Farming Rewards <a href="#collecting-rarity-farming-rewards" id="collecting-rarity-farming-rewards"></a>

Rarity Farming Rewards are disbursed to your Endro inventories. You will see your Endro's wearables and the amount of ENGA your Endro has won from Rarity Farming on the inventory page.
