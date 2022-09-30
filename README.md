# Hardhat FundMe

This is my first project I deployed to web3, special thanks to [Patrick Collins](https://twitter.com/PatrickAlphaC) and for freeCodeCamp on this [course](https://www.youtube.com/watch?v=gyMwXuJrbJQ).

The project comes with a smart contract, a test for that contract, a sample script that deploys that contract. It also comes with a variety of other tools, preconfigured to work with the project code.

## Requirements
* [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
* [Node.js](https://nodejs.org/en/download/)
* [yarn](https://classic.yarnpkg.com/lang/en/docs/install/)

## Setup
```shell
git clone https://github.com/3bodymo/hardhat-fund-me.git
cd hardhat-fund-me
yarn
```

## Interact with the contract on a testnet or mainnet
1. At first, you have to setup environment variables.
* You'll want to set your [`GOERLI_RPC_URL`](https://www.alchemy.com/overviews/private-rpc-endpoint) and [`PRIVATE_KEY`](https://metamask.zendesk.com/hc/en-us/articles/360015289632-How-to-export-an-account-s-private-key) as environment variables in **.env** file.

## Usage

### Deploy
To deploy on **Hardhat Network**
```shell
yarn hardhat deploy
```
To deploy on testnet like [**Goerli Network**](https://goerli.etherscan.io)
```shell
yarn hardhat deploy --network goerli
```
To deploy on [**localhost Network**](https://hardhat.org/hardhat-network/docs/overview), at first run a node in separate terminal
```shell
yarn hardhat node
```
then, run the following command
```shell
yarn hardhat deploy --network localhost
```

### Testing
To make the test on the hardhat network
```shell
yarn hardhat test
```
To run staging test, that will run on testnet network
```shell
yarn hardhat test --network goerli
```

### Test Coverage
```shell
yarn hardhat coverage
```

### Estimate gas
* At first, you have to setup [`ETHERSCAN_API_KEY`](https://info.etherscan.com/api-keys/) and [`COINMARKETCAP_API_KEY`](https://coinmarketcap.com/api/) as environment variables in **.env** file.
* Then, make sure that `gasReporter` in `hardhat.config.js` are enabled.
```shell
yarn hardhat test
```

### Run fund script
```shell
yarn hardhat node &
yarn hardhat run scripts/fund.js --network localhost
```

### Run withdraw script
```shell
yarn hardhat node &
yarn hardhat run scripts/withdraw.js --network localhost
```

## Demo
![](https://github.com/3bodymo/hardhat-fund-me/blob/main/demo.gif)


