
### Kitty Inu Token Supply API

Currently implemented with my JSON Server as a temporary solution to create api endpoints for circulating, total, and max supply of the token.

#### Endpoints:

[Total Minted Supply](https://my-json-server.typicode.com/KittyInu/token-supply/total)

- Return: 1 Trillion tokens (constant)

[Circulating Supply](https://my-json-server.typicode.com/KittyInu/token-supply/circulating)

- Return: `TotalMintedSupply - BurnedTokens - BotWallets - Locked`

[Max Supply](https://my-json-server.typicode.com/KittyInu/token-supply/circulating)

- Return: `TotalMintedSupply - BurnedTokens - BotWallets`

#### Definitions:

- `TotalMintedSupply`: Total number of tokens minted at launch. Fixed value of 1 trillion. 

- `BurnedTokens`: Total number of tokens sent to dead wallet address. 

- `BotWallets`: Wallets prevented from selling/transferring their tokens due to using automated buying methods at launch. 

- `Locked`: Tokens locked by team for future liquidity provisions. 