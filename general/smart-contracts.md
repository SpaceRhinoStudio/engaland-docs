# Smart Contracts

## Fundraising

There are multiple contracts which form the fundraising part of our app. They are Automated Market Maker (AMM), Tap Mechanism, Pre-Sale, Bancor Formula, Token Manager, Enga Token and finally Controller. There are also some vaults for DAO, Stake Holders (please refer to [tokenomic](../tokenomic-land/tokenomics.md#allocations) for more info), Team (we call it Beneficiary), and Reserve. They all have their own permissions and access level, for example no one has access on the Reserve vault expect the AMM contract. All important contracts are governed and secured by a Multisig contract consisted of at least 4 members to prevent any malicious activities and secure our contracts. Not any of individual core members have complete access on contracts.

### Multisig

A contract to which initially passed core members as the owners. All important settings of the app is controlled and secured by it. It's worth mentioning that we will add another Multisig to let our main DAO participants take control over the most of the smart contracts and settings of the app.

Contract Address:

### Enga Token

Main Enga Token that acts as a utility token to serve our users and help our team grow the project.

Contract Address:

### Token Manager

Token Manager is somehow the owner of the Enga Token as well as the container of all the vesting created by the pre-sale , and initial token allocation.

Contract Address:

### Beneficiary Vault

A vault that belongs to the company, some poertion of pre-sale fundraising will be deposited here and the rest will be held in the reserve vault.

### Treasury Vault

A vault that belongs to all users and the company. We won't use this fund unless DAO let us do that and it's not directly controlled by us.

Contract Address:

### Reserve Vault

The vault that Automated Market Maker has access on. Reserve is the main vault and our token price will be calculated based on it. Before starting the market maker, some portion of our pre-sale will directly be deposited here.

Contract Address:

### Stake Holder Vault

It's an another vault that belongs to [Stake Holders](../tokenomic-land/tokenomics.md#allocations).

Contract Address:

### Pre Sale

A contract that controls our private sale and makes vesting for participants in Token Manager.

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

A contract that controls every thing, and 99 percent of write operations and transactions including contributions, buy/sell and etc. will go through this contract as the owner of all contracts we have listed above.

Contract Address:
