---
description: What Are Endros?
---

# Introduction

## About Endros

Endros are droids constructed by an [Opifex Machine](../gameplay/opifex-machine.md) using the blueprints and controlled by the citizens of [the Engaverse](introduction.md#engaverse). They are represented by NFTs living on Polygon network, backed by ERC-721 standard. Their values are determined by level/experience and rarity score, which is calculated based on multiple factors, such as their stats, amount of staked collateral, and equipped wearables. Endros are representatives of their own realm where they have been manufactured to mobilize a strong army.

Players can participate in [games](../gameplay/games.md), and [governance](../communities/dao.md) to gain experience, upgrade, level up their Endro, and enjoy their time. You could have the rarest Endros and gain rewards in our native token, "[ENGA](../tokenomic-land/enga-token.md)", in [Rarity Farming](../gameplay/rarity-farming.md) - a completely on-chain mini-game that rewards the rarest Endros with ENGA token.

### Staked Collateral

Each ERC-721 Endro holds a staked collateral. These LP tokens generate yield, which increases the number of tokens as an LP reward held in the Endro, thus, the quantity of ENGA token in the Endro increases over time. For now, only ENGA is available as a staked collateral, but other LPs will be added in the future.

{% hint style="info" %}
To clarify, staked collaterals are another term for the [Power Source](../tokenomic-land/collateral.md) used to start the [Opifex Machine](../gameplay/opifex-machine.md).
{% endhint %}

### Traits

Endros possess multiple traits. These traits are used to determine the stats, appearance, and other attributes of the Endro.

* **Random Traits:** Once candidate's blueprints are indexed by the [Opifex Machine](../gameplay/opifex-machine.md), Opifex, using ChainLink VRF, evaluates the traits of the Endro. There are two types of these traits:
  1. **Appearance:** They don't affect [Rarity Score](introduction.md#rarity-score), and they are chosen randomly with an equal chance for each. These traits do not influence or affect gameplay or rarity farming in any way.
  2. **Stats and their BRS:** Stats are crucially important, and they represent the RPG elements of Engaverse. Their values are distributed on a bell curve AKA "Normal Distribution":\
     ![](../.gitbook/assets/bell-curve.png)\
     Depending on its rarity, each stat is assigned a value of Common, Uncommon, Rare or Mythical, which represents a numeric value in the range of 0 to 99. The stats are Strength, Dexterity, Constitution, Mentality, Common-Skills (CS), and Aggressiveness. Every stat has at least a minimum value of 50 for its Base Rarity Score aka BRS. For example if generated random number for stat is 2, then based on the formula below, the in-game stat value and its respective BRS is 97. In other words, a low value like 1 is not considered bad, on the contrary, it is as good as number 98. BRS is calculated like the following:\
     `if randomNumber >= 50 return randomNumber;`\
     `else return 99 - randomNumber;`\
     `//there is no value lower than 50`
* **Zeal:** It defines the level of relationship between the Endro and the owner. It increases or decreases based on how often the owner interacts with the Endro and also how long it has been with the same owner. This trait is not randomly assigned, but rather starts at a fixed value. Moreover, it acts as a constraint to limit stat modifiers given by [Chipset Cards](../gameplay/wearables/chipset-cards.md). Zeal limits the effects of stat modifiers to a range of +/-1 to +/-8.
* **Realm:** As the name suggests, there are realms or in other terms classes, that each Endro belongs to and manufactured in. The realm each Endro belongs to is selected randomly. The probability for each realm is decided by the Enga Federation for each season.
* **Level, Experience (XP) and Merit Point:** Just like any RPG game, Endros level up when they gain XP. It could be gained by voting in the Enga Federation aka "ENGADAO" and also participating in games. Each successive level requires more XP to attain; therefore gaining levels gradually becomes tougher. Every level, Endros receive some Merit Points that can be consumed to increase or decrease a certain trait value. Note that [Wearables](../gameplay/wearables/) require a minimum XP level to be equipped.
* **Rarity Score:** Rarity Score is a dynamically calculated trait based on stat values (their respective BRS in this case, not the raw value chosen on the bell curve) and cosmetic wearables the Endro has equipped. The BRS of cosmetics and all the stats combined form the rarity score. Some wearables, especially [Chipset Cards](../gameplay/wearables/chipset-cards.md), require a minimum rarity score to be equipped or consumed.
* **Generation:** Blueprint production is done generation by generation, under the supervision of the Enga Federation. The number of Endros in each generation is also determined by them. Some [Cosmetics](../gameplay/wearables/cosmetics.md) may only belong to a specific generation.

## Other Characteristics of the Realms

Read more about this topic [here](../gameplay/characteristic-of-realms.md).

## Wearables

They are NFTs backed by ERC-1155. With the aid of ERC-998 we could have NFTs own other NFTs, like an inventory system. It's where those wearables shine. Wearables are divided into two groups:

First group are cosmetics, they are equipped to increase the rarity score and every one of them has their own BRS bonus value associated with. Some may need a minimum XP level and some may need a specific Generation to be equipped.

{% hint style="success" %}
They Increase Rarity Score with their associated BRS bonus value.
{% endhint %}

{% hint style="warning" %}
They might need a minimum XP level to be equipped.

They might belong to a specific Generation.
{% endhint %}

The second group are Chipset Cards. Each CC has its own stat modifiers and, they are equipped to slightly change the value of certain stats, however they don't have a direct impact on BRS - indirectly they are altering the value of the stats which affects the BRS. Each Endro has 4 slots for chipset cards, although there is a constraint on stat modifiers, the range each stat can change is defined by the value of [Zeal](../gameplay/traits.md#zeal). For instance, based on the Zeal value, let's say the limit is +/-5, if you provide four CCs to change the value of one specific stat like Mentality and each CC has a modifier of +3 on that stat, unfortunately Mentality just shifts by +5 instead of +12.

{% hint style="success" %}
They are stat modifiers which change the raw value chosen on the bell curve and cause a shift on BRS value, make it better or worse based on your decision and strategy.
{% endhint %}

{% hint style="danger" %}
The Zeal limits how effective CCs can be.
{% endhint %}

{% hint style="warning" %}
They might need a minimum XP level to be equipped.

They might need a minimum amount of Rarity Score to be equipped.
{% endhint %}

In addition, it's good to mention that the chipset cards are modifying raw value of stats, the value that is randomly chosen on the bell curve. Any sort of change, whether it be an increase or decrease, on stats results in alteration of their respective BRS, thus negative modifiers could be beneficial as well since those stats are moving on a bell curve and smaller ones could be more valuable. You can read more about wearables [here](../gameplay/wearables/).

## Consumables

Yet another group of NFTs that are consumable, meaning they are burnt when they are used. Think of them as potions, boosters and so on.

{% hint style="success" %}
**Simple Consumables**

They could boost your XP gaining.

They could boost your Zeal gaining.

They could stop the decline of Zeal value for a period of time.
{% endhint %}

{% hint style="warning" %}
**Simple Consumables**

They might need a minimum Rarity Score to be consumed.
{% endhint %}

## Endro Value

The value of an Endro comes from its early blueprint and its rarity score.

### Base Value <a href="#base-value" id="base-value"></a>

Base value of an Endro is calculated when you as a player index 10 blueprint candidates and pick the one you want to be constructed by a machine named [Opifex Machine](../gameplay/opifex-machine.md). It is also the minimum staked collateral needed for construction. If the candidate's needed collateral is 15 USD, then the base value is 15 USD, in addition to the extra interests accrued from the staking rewards. Other ERC20 tokens and Liquidity Pools (LP) could be added in the future by the Enga Federation and partnerships with other projects, for now we only use our own native token as an collateral.

### Rarity Score

As we mentioned above in the [Traits](introduction.md#traits) section, Rarity Score is a dynamic value that is assessed by the rareness of each Endro's traits and equipped cosmetics. Over time and with XP level growth your Endro can wear more valuable cosmetic wearables to increase its rarity score, it can also equip chipset cards or gain Merit Point to modify its stats temporary or permanently respectively, which results in the alteration of their relevant Base Rarity Score (BRS). This system of dynamic rarity score that is introduced by Aavegotchi, has enabled a novel concept known as "Rarity Farming", which is explained [here](../gameplay/rarity-farming.md).

## ENGAVERSE

Engaverse is a newly found universe that is under the control of five realms. Every realm having their own personality, backgrounds, and culture, they have formed an association to explore Engaland - a dangerous and unexplored planet that no realm has control over - to tame and colonize the planet. There will be expeditions and missions for Endros to gain experience and grow their XP level to unlock items such as [Chipset Cards](../gameplay/wearables/chipset-cards.md), and [Cosmetic Wearables](../gameplay/wearables/cosmetics.md) which are used to upgrade and strengthen your Endros in rarity farming and games. For more information please read [Where is ENGALAND](../).
