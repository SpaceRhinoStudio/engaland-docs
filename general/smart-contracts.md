# Smart Contracts

## Fundraising

There are multiple contracts which form the fundraising part of our app. They are Automated Market Maker (AMM), Tap Mechanism, Pre-Sale, Bancor Formula, Token Manager, Enga Token and finally Controller. There are also some vaults for DAO, Stake Holders (please refer to [tokenomic](../tokenomic-land/tokenomics.md#allocations) for more info), and Reserve. They all have their own permissions and access level, for example no one has access to the Reserve vault expect the AMM contract. All contracts are governed and secured by [Gnosis Safe](https://gnosis-safe.io/) to prevent any malicious activities. None of individual members have extra access to the contracts.

Contract Address:

### Gnosis Safe

The most trusted multisig wallet which also act as team's vault and has the full control on the protocol. You can read more about Gnosis Safe [here](https://gnosis-safe.io/).

### Enga Token

Main Enga Token that acts as a utility token to serve our users and help our team grow the project.

Contract Address: [0xd770bffE492Ffee30E1e9994DB31A5E8992509cf](https://polygonscan.com/address/0xd770bffE492Ffee30E1e9994DB31A5E8992509cf)

### Token Manager

Token Manager is somehow the owner of the Enga Token as well as the container of all the vesting created by the pre-sale , and initial token allocation.

Contract Address: [0x655f961205164Cf23784f42634658D293fB6d6ee](https://polygonscan.com/address/0x655f961205164Cf23784f42634658D293fB6d6ee)

### Treasury Vault

A vault that belongs to all users and the company. We won't use this fund unless DAO let us do that and it's not directly controlled by us.

Contract Address: [0x357E6E7E021b89B81Ee31A2CB0f9BD72ba638F5B](https://polygonscan.com/address/0x357E6E7E021b89B81Ee31A2CB0f9BD72ba638F5B)

### Reserve Vault

The vault that Automated Market Maker has access on. Reserve is the main vault and our token price will be calculated based on it. Before starting the market maker, some portion of our pre-sale will directly be deposited here.

Contract Address: [0xf16862c1a5E68E4b406aCd2CC88c8Fb7990F0fa1](https://polygonscan.com/address/0xf16862c1a5E68E4b406aCd2CC88c8Fb7990F0fa1)

### Team Vault

It's another vault that belongs to [the Team](../tokenomic-land/tokenomics.md#allocations).

Contract Address: [0xa9A7f8F4dC749381AC751DDEb9B0eAab289829Db](https://polygonscan.com/address/0xa9A7f8F4dC749381AC751DDEb9B0eAab289829Db)

### Seed Sale

A contract that controls our seed-sale and makes vesting for participants in itself.

Contract Address: [0xD80CE7890501A111D7220c6f8Cf0697a1b0EAb79](https://polygonscan.com/address/0xD80CE7890501A111D7220c6f8Cf0697a1b0EAb79)

Please read [Tokenomic ](../tokenomic-land/tokenomics.md)section for more details about seed-sale.

### Pre Sale

A contract that controls our pre-sale and makes vesting for participants in Token Manager.

Contract Address: [0xd79643eF39B17380c8092e4a5086861F94ed4331](https://polygonscan.com/address/0xd79643eF39B17380c8092e4a5086861F94ed4331)

Please read [Tokenomic ](../tokenomic-land/tokenomics.md)section for more details about pre-sale.

### Bancor Formula

A contract that calculates the amount of purchased Enga token when receives some collateral and also the amount of collateral when receives some Enga token.

Contract Address: [0x9d4ED959891fDF4410A75456CFA6C16EA3612227](https://polygonscan.com/address/0x9d4ED959891fDF4410A75456CFA6C16EA3612227)

### Market Maker

The most important contract that controls the price of our token based on Bancor Formula, amount of reserve token and finally amount of minted Enga. It uses Bancor Formula contract inside.

Contract Address: [0xd19a2c27A6f834Ca9084758238e23bEa52B02dCd](https://polygonscan.com/address/0xd19a2c27A6f834Ca9084758238e23bEa52B02dCd)

### Tap

As we have talked about before, we have a mechanism named Tap which withdraw exact amount of collateral from the Market Maker and will send it to the Beneficiary vault to help us as an income to our company. The amount of Tap per month will be decided by the DAO members.

Contract Address: [0xB7588a40922083DC21766F3Dc100830d4B1b5B0A](https://polygonscan.com/address/0xB7588a40922083DC21766F3Dc100830d4B1b5B0A)

### KYC Authorization

A contract that controls who can or can't contribute to the Market Maker. We don't have any plans to stop users from contributing to AMM, but in the future and for regulation we may do that.

Contract Address: [0x80A451801533f54BFc5Df99B8E5a3C6d51208249](https://polygonscan.com/address/0x80A451801533f54BFc5Df99B8E5a3C6d51208249)

### Controller

A contract that controls everything, and 99 percent of write operations and transactions including contributions, buy/sell and etc. will go through this contract as the owner of all contracts we have listed above. Having Controller deployed means we are ready to go and the protocol has been functioning.

Contract Address: [0x5F0c1095CF3b579183e8d64892CB83c4f9B17dF2](https://polygonscan.com/address/0x5F0c1095CF3b579183e8d64892CB83c4f9B17dF2)
