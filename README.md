## Modular 2-2019

# Scatter Wallet Basic Integration

## Contents

<!-- TOC START min:1 max:3 link:true update:true -->
- [scatter wallet test](#scatter-wallet-test)
  - [Table of Contents](#table-of-contents)
  - [1 | Description](#1--description)
  - [2 | Roadmap](#2--roadmap)
    - [2.1 Minimal Viable Product (MVP)](#21-minimal-viable-product-mvp)
  - [3 | Getting Started](#3--getting-started)
    - [3.1 Installing](#31-installing)
    - [3.2 Running](#32-running)

<!-- TOC END -->


## 1 | Description

Testing the ability to integrate Scatter wallet, particularly, the Signature Provider.

## 2 | Roadmap

### 2.1 Minimal Viable Product (MVP)

**Status:** _Complete_

* [x] Connect Scatter to React
* [x] Be able to send a transaction


## 3 | Getting Started

### 3.1 Installing

**Client**

Clone or download the repository.

Inside of `./client` Install dependencies.

```
npm install || yarn
```

**Blockchain**

Deploy the `eosio.token` contract found inside the `./eos` directory. Instructions found in the EOS website:
https://developers.eos.io/eosio-home/docs/token-contract.

This application requires Scatter, https://get-scatter.com/, and a local EOS blockchain, https://developers.eos.io/eosio-home/docs/setting-up-your-environment. Once the local blockchain node is running on port 8888, add the localhost EOS testnet to Scatter (Settings > Network) using settings found in http://localhost:8888/v1/chain/get_info.

Create 2 accounts.

1. Create 2 public, private key pairings with `cleos create key`. Save these keys
2. Add account names to those keys with `cleos create account eosio <account name> <EOS public key>`. Name one of these accounts `james`, or change the account name `james` in `App.js` to the account name you created.  

Add those accounts to Scatter in the local testnet with each account's private key.

Using `eosio.token` contract, create and issue EOS tokens to the accounts you created.


### 3.2 Running

Inside of `./client`

For Web:

```
npm run web || yarn web
```

For Mobile:

```
npm run start || yarn start || exp start
```
