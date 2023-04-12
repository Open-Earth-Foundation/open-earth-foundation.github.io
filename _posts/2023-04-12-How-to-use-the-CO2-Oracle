---
layout: post
title: "How to use a CO2 Oracle in a Smart Contract"
date: 2023-04-12
author: Adit P
tags: Oracles Ethereum Social Cost of Carbon
---

## What's a smart contract?

A smart contract is a self-executing computer program that automatically executes the terms of a contract when certain pre-defined conditions are met. It is typically implemented on a blockchain platform, such as Ethereum, and is designed to facilitate, verify, and enforce the negotiation and performance of a contract without the need for intermediaries, such as lawyers or banks.

Smart contracts can be used in a wide range of applications, including supply chain management, financial transactions, real estate, and digital identity verification. They are programmed to automatically trigger actions based on specific conditions, such as transferring funds when a certain condition is met or releasing goods once a payment has been received.

Smart contracts are considered to be secure, transparent, and tamper-proof, as all transactions are recorded on a blockchain and cannot be altered without consensus from the network. This makes them an ideal tool for automating complex business processes and reducing the need for intermediaries, while also increasing trust and transparency in transactions.


## Why do I need an Oracle?

In the context of blockchain technology, an oracle is a mechanism that provides off-chain data to a smart contract. It serves as a bridge between the blockchain and the outside world, enabling smart contracts to access information that is not available on the blockchain, such as stock prices, weather data, and sports scores.

Oracles work by gathering information from external sources and then transmitting that information to the blockchain network. Once the information is received by the smart contract, it can be used to trigger actions, such as executing a payment or updating a record on the blockchain.

There are different types of oracles, including centralized oracles, which rely on a single source of information, and decentralized oracles, which use multiple sources of information to ensure accuracy and prevent manipulation. Some oracles also use cryptographic techniques to ensure the authenticity and integrity of the data being transmitted.

Oracles play a crucial role in enabling smart contracts to interact with the real world and expand their functionality beyond the capabilities of the blockchain network. However, they also introduce new security risks, such as the possibility of malicious actors manipulating the data being transmitted to the blockchain. As a result, the development of secure and reliable oracle solutions is an active area of research and innovation in the blockchain space.


## What's the CO2 Oracle?

Open Earth Foundation's CO2 Oracle is a centralized oracle that makes the social cost of carbon availible for consumption in smart contracts. It provides the costs in 2023 dollars.

## How do I use the CO2 Oracle?

The fastest way is with our pre-setup smart contract located: [here](https://remix.ethereum.org/Open-Earth-Foundation/co2-pricing/blob/main/apps/smartcontracts/demo.sol).

There relevant lines for retrieving a single data point is:
```
req.add(
  "get",
  "https://co2pricingjulia.openearth.dev/?year=2025&prtp=0.01"
);

req.add("path", "");
```
Here we specify that we want the year to be 2025 and we are using a pure rate of time parameter of 1%. In a real smart contract, you would change these variables to be dynamic to best accomplish your goals.

# How do I run a smart contract?

Deplying a smart contract is easy with Remix! Deploying smart contracts to the blockchain is a bit outside the scope of this blog post, but we would reccomend using one of the many guides, [such as this one](https://www.geeksforgeeks.org/steps-to-execute-solidity-smart-contract-using-remix-ide/), to see how best to deploy your smart contract!

It's important to note that the oracle you use will be dependant on your chosen blockchain. The smart contract is curently configured for the Sepolia testnet on Ethereum, though since this contact is written in solidity, it is compatible with any EVM based blockchain.
