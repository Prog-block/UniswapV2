# UniswapV2

Uniswap is a decentralized exchange (DEX). And thus aims to be an alternative to centralised exchanges. It is based on various smart contracts, which enable the exchange of tokens. Currently there are 3 versions of Uniswap. This repo deals with the second version i.e UniswapV2.

### Code Comprehension: 

This project helped me to develop a deep understanding of this complex codebase by analyzing and comprehending it. This project also provided valuable insights into the inner workings of decentralized exchanges.


### Architecture Overview:

![alt text](image.png)


### Core:

1. UniswapV2ERC20 – an extended ERC20 implementation that’s used for LP-tokens. It additionally implements EIP-2612 to support off-chain approval of transfers.
2. UniswapV2Factory – similarly to V1, this is a factory contract that creates pair contracts and serves as a registry for them. The registry uses create2 to generate pair addresses–we’ll see how it works in details.
3. UniswapV2Pair – the main contract that’s responsible for the core logic. It’s worth noting that the factory allows to create only unique pairs to not dilute liquidity.

### Periphery:

1. UniswapV2Router: Main entrypoint for the Uniswap UI and other web and decentralized applications working on top of Uniswap.

2. UniswapV2Library: Collection of helper functions that implement important calculations

### Tooling:

Foundry is used to compile and test the contracts.

### Commands:

Contracts can be compiled with:
```bash
forge build
```

Tests can be deployed with:
```bash
forge test
```

Enjoy building✌️
