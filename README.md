# 🚀 Using Metatransactions to Pay for Your Users' Gas

## 🌐 Overview
Welcome to a revolutionary way of interacting with the Ethereum blockchain! This repository contains a Solidity smart contract that showcases the power of metatransactions, enabling you to pay for gas costs on behalf of your users. This magic is made possible by having users sign a message off-chain, and a relayer broadcasting the transaction on-chain, footing the bill for the gas.

The repository includes two key contracts:

1. `RandomToken`: A simple yet powerful ERC20 token contract with a `freeMint` function. This function empowers anyone to mint an arbitrary amount of tokens to their address.

2. `TokenSender`: The star of the show! This contract verifies the signature and, if it's valid, transfers the specified amount of tokens from the sender to the recipient. This contract acts as the relayer in the metatransaction process.

## 🎩 Metatransactions
Metatransactions are the magic trick that allows users to interact with Ethereum contracts without needing to hold Ether. Instead, a third party (the relayer) pays for the gas. The user signs a message off-chain (indicating their intent to perform a certain action on-chain), and this signature is used to authenticate and execute the transaction on-chain.

## 🧪 Testing
The repository also includes a robust test script that uses the Mocha testing framework and the Chai assertion library. The test ensures that the `TokenSender` contract can successfully transfer tokens from one address to another given a valid signature from the sender.

## 🛠️ Installation
1. Clone the repository.
2. Install the dependencies by running `npm install`.
3. Compile the contracts by running `npx hardhat compile`.
4. Run the tests by running `npx hardhat test`.

## 🚀 Usage
1. Deploy the `RandomToken` and `TokenSender` contracts.
2. Mint some tokens to your address using the `freeMint` function in the `RandomToken` contract.
3. Approve the `TokenSender` contract to spend tokens on your behalf.
4. Sign a message to transfer tokens to a recipient.
5. Use the `transfer` function in the `TokenSender` contract to execute the transaction on your behalf.

## ⚠️ Note
This is a basic implementation and might not be secure for production use
