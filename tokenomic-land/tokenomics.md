---
description: $ENGA Token Allocations and Distribution Models
---

# Tokenomics

## Tokenomics

$ENGA is a dynamic supply utility token for the Engaland platform. Token minting is handled by [the bonding curve](bonding-curve.md).

### ICO

There will be **8,000,000** tokens initially minted prior to the public sale.

The fundraising program will take effect on Engaland's official website.

#### Rounds:

* **Seed Sale**
  * Minimum investment: 10 DAI
  * Tokens to sell: 300,000 ENGA
  * ENGA/DAI fixed price: 0.12
  * Hardcap: 36,000 DAI

This round is a whitelisted sale phase intended for raising funds for marketing campaigns, AMAs, etc.

*   **Pre Sale**

    * Minimum investment: 100 DAI
    * Tokens to sell: 2,000,000 ENGA
    * ENGA/DAI fixed price: 0.15
    * Hardcap: 300,000 DAI
      * Bonding Curve share: _**30%,**_ 90,000 DAI
      * SpaceRhino Studio share: _**70%,**_ 210,000 DAI

    This round is intended for raising funds for development and growth of the Engaland. All of the investments will be allocated to the initial reserve of the bonding curve and the SpaceRhino Studio the owner of the Engaland.\
    Participants of both rounds will be elected as councilor, who can propose protocol changes and approve smart contract upgrades.
*   **Public Sale**

    At this phase, ENGA/DAI pair will be available for everyone to buy and sell using Engaland's bonding curve with the initial listing price of **0.25** DAI per ENGA.

### Initial Supply

|    Allocation | Percentage |    ENGA   |
| ------------: | :--------: | :-------: |
|     Seed Sale |    3.8%    |  300,000  |
|      Pre Sale |     25%    | 2,000,000 |
|     Marketing |    2.13%   |  170,000  |
|           DAO |    12.5%   | 1,000,000 |
| Stake Holders |    37.5%   | 3,000,000 |
|          Team |    19.1%   | 1,530,000 |

{% hint style="warning" %}
The share of the stake holders will be held in our gnosis multisig and will be sent to a locked contract.
{% endhint %}

### Vesting

Our vesting program uses cliff mechanism for releasing locked tokens. This means a part of the locked tokens can be initially released one month after cliff start and at each month a portion of the remaining funds can be released.

Number of tokens released can be calculated by the following formula:

`monthly release = total tokens locked / (cliff duration - cliff start)`

|   Allocation | Cliff Start (months) | Cliff Duration (months) |
| -----------: | :------------------: | :---------------------: |
|    Seed Sale |           6          |            12           |
|     Pre Sale |           6          |            18           |
|          DAO |           6          |            12           |
| Stakeholders |          12          |            24           |
|         Team |           6          |            24           |

## Protocol Revenue

At each NFT drop phase, players can purchase NFTs through our auction house. Any purchase from **Engaland** will allocate the spent tokens on different parts of the protocol, listed in the following table:

|    Distribution | Percentage |
| --------------: | :--------: |
|  Rarity Farming |     45%    |
| Staking Rewards |     20%    |
|             DAO |     10%    |
|            Team |     5%     |
|            Burn |     20%    |
