# Smart Contracts

## Fundraising

There are multiple contracts which form the fundraising part of our app. They are Automated Market Maker (AMM), Tap Mechanism, Pre-Sale, Bancor Formula, Token Manager, Enga Token and finally Controller. There are also some vaults for DAO, Stake Holders (please refer to [tokenomic](../tokenomic-land/tokenomics.md#allocations) for more info), Team (we call it Beneficiary), and Reserve. They all have their own permissions and access level, for example no one has access on the Reserve vault expect the AMM contract. All important contracts are governed and secured by [Gnosis Safe](https://gnosis-safe.io/) consisted of at least 4 members to prevent any malicious activities and secure our contracts. None of individual core members have extra access to the contracts.

Contract Address:

### Gnosis Safe

The most trusted multisig wallet which also act as team's vault and has the full control on the protocol. You can read more about Gnosis Safe [here](https://gnosis-safe.io/).

### Enga Token

Main Enga Token that acts as a utility token to serve our users and help our team grow the project.

Contract Address:

### Token Manager

Token Manager is somehow the owner of the Enga Token as well as the container of all the vesting created by the pre-sale , and initial token allocation.

Contract Address:

### Treasury Vault

A vault that belongs to all users and the company. We won't use this fund unless DAO let us do that and it's not directly controlled by us.

Contract Address:

### Reserve Vault

The vault that Automated Market Maker has access on. Reserve is the main vault and our token price will be calculated based on it. Before starting the market maker, some portion of our pre-sale will directly be deposited here.

Contract Address:

### Stake Holder Vault

It's another vault that belongs to [Stake Holders](../tokenomic-land/tokenomics.md#allocations).

Contract Address:

### Seed Sale

A contract that controls our seed-sale and makes vesting for participants in itself.

Contract Address:

Please read [Tokenomic ](../tokenomic-land/tokenomics.md)section for more details about seed-sale.

### Pre Sale

A contract that controls our pre-sale and makes vesting for participants in Token Manager.

Contract Address:

Please read [Tokenomic ](../tokenomic-land/tokenomics.md)section for more details about pre-sale.

### Bancor Formula

A contract that calculates the amount of purchased Enga token when receives some collateral and also the amount of collateral when receives some Enga token.

Contract Address:

### Market Maker

The most important contract that controls the price of our token based on Bancor Formula, amount of reserve token and finally amount of minted Enga. It uses Bancor Formula contract inside.

Contract Address:

### Tap

As we have talked about before, we have a mechanism named Tap which withdraw exact amount of collateral from the Market Maker and will send it to the Beneficiary vault to help us as an income to our company. The amount of Tap per month will be decided by the DAO members.

Contract Address:

### KYC Authorization

A contract that controls who can or can't contribute to the Market Maker. We don't have any plans to stop users from contributing to AMM, but in the future and for regulation we may do that.

Contract Address:

### Controller

A contract that controls everything, and 99 percent of write operations and transactions including contributions, buy/sell and etc. will go through this contract as the owner of all contracts we have listed above. Having Controller deployed means we are ready to go and the protocol has been functioning.

Contract Address:
