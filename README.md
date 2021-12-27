
### Kitty Inu Token Supply API

Currently implemented with my JSON Server as a temporary solution to create api endpoints for circulating, total, and max supply of the token.

#### Endpoints

##### Syntax

```
https://my-json-server.typicode.com/KittyInu/token-supply/<endpoint>
```

Values for `endpoint`:

- `total`
- `circulating`
- `max`

[Total Supply](https://my-json-server.typicode.com/KittyInu/token-supply/total)

> Total Supply is the total amount of coins in existence right now (minus any coins that have been verifiably burned). ([source](https://coinmarketcap.com/faq/))

- Return: `MaxSupply - BurnedTokens - BotWallets`

[Circulating Supply](https://my-json-server.typicode.com/KittyInu/token-supply/circulating)

> Circulating Supply is the best approximation of the number of coins that are circulating in the market and in the general public's hands. ([source](https://coinmarketcap.com/faq/))

- Return: `MaxSupply - BurnedTokens - BotWallets - Locked`

[Max Supply](https://my-json-server.typicode.com/KittyInu/token-supply/max)

> Max Supply is the best approximation of the maximum amount of coins that will ever exist in the lifetime of the cryptocurrency. ([source](https://coinmarketcap.com/faq/))

- Return: 1 Trillion tokens (constant)


#### Definitions

- `MaxSupply`: Total number of tokens minted at launch. Fixed value of 1 trillion. 

- `BurnedTokens`: Total number of tokens sent to dead wallet address. 

- `BotWallets`: Wallets prevented from selling/transferring their tokens due to using automated buying methods at launch. 

- `Locked`: Tokens locked by team for future liquidity provisions. 