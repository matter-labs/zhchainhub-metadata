# ZKchainHub-metadata

## Overview

Metadata files for mainnet and testnet to be used in the [ZKChainHub-backend](https://github.com/defi-wonderland/ZKchainHub-backend) configuration

## Adding new chains

### chains.json

This file contains an array of Chain metadata. To add a new one, follow the following interface:

```json
{
    "chainId": 324, // mandatory
    "name": "ZKsyncERA", // mandatory
    "iconUrl": "https://s2.coinmarketcap.com/static/img/coins/64x64/24091.png", // optional
    "publicRpcs": [
        "https://mainnet.era.zksync.io",
        "https://zksync.drpc.org",
        "https://zksync.meowrpc.com"
    ], //optional,
    "explorerUrl": "https://explorer.zksync.io/", // optional
    "websiteUrl": "https://zksync.io/", // optional
    "launchDate": 1679626800, // mandatory
    "chainType": "Rollup", // "Rollup" | "Validium"
    "baseToken": {
        "name": "Ether", // mandatory
        "symbol": "ETH", // mandatory
        "type": "native", // "native" | "erc20"
        "contractAddress": null, // null if "native", address if "erc20"
        "imageUrl": "https://coin-images.coingecko.com/coins/images/279/large/ethereum.png?1696501628", // optional
        "decimals": 18 // mandatory
    }
}
```

## Adding new tokens

### tokens.json

This file contains an array of Token metadata. To add a new one, follow the following interface:

```json
{
    "name": "0x Protocol Token", //mandatory
    "symbol": "ZRX", //mandatory
    "contractAddress": "0xE41d2489571d322189246DaFA5ebDe1F4699F498", // null if "native", address if "erc20"
    "imageUrl": "https://assets.coingecko.com/coins/images/863/large/0x.png?1696501996", //optional
    "type": "erc20", // "native" | "erc20"
    "decimals": 18 //mandatory
}
```

## Contributing

ZKchainHub was built with ❤️ by [Wonderland](https://defi.sucks).

Wonderland is a team of top Web3 researchers, developers, and operators who believe that the future needs to be open-source, permissionless, and decentralized.

[DeFi sucks](https://defi.sucks), but Wonderland is here to make it better.

## License

The primary license for the boilerplate is MIT. See the [`LICENSE`](./LICENSE) file for details.