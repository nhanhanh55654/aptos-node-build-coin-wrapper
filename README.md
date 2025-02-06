
# Aptos Node Build & Coin Wrapper

## Overview

`aptos-node-build-coin-wrapper` is a Node.js project designed to interact with the Aptos blockchain using the Move programming language. This project provides utilities for building and deploying Aptos nodes and managing coin transactions on the Aptos network.

## Features

-   Setup and deploy an Aptos node.
    
-   Manage Aptos coin transactions.
    
-   Interact with smart contracts written in Move.
    
-   REST API integration for blockchain interactions.
    
-   Fully compatible with the Aptos blockchain ecosystem.
    

## Prerequisites

Before setting up the project, ensure you have the following installed:

-   [Node.js](https://nodejs.org/) (version 16 or higher recommended)
    
-   Aptos CLI for managing the blockchain
    
-   Move CLI for smart contract development
    

## Installation

Clone the repository and install dependencies:

```
git clone https://github.com/nhanhanh55654/aptos-node-build-coin-wrapper.git
cd aptos-node-build-coin-wrapper
npm install
```

## Configuration

Create a `.env` file in the root directory and add the following environment variables:

```
APTOS_NODE_URL=<Your_Aptos_Node_URL>
PRIVATE_KEY=<Your_Private_Key>
FAUCET_URL=<Aptos_Faucet_URL>
```

## Usage

### Start the Application

```
npm start
```

### Deploy a Smart Contract

1.  Write a Move smart contract in the `contracts` directory.
    
2.  Use the following command to compile and publish the contract:
    
    ```
    aptos move publish --profile default
    ```
    

### Send a Coin Transaction

Use the provided API or script to send Aptos coins:

```
const { sendCoin } = require('./src/coin');

sendCoin('<receiver_address>', 100)
  .then(response => console.log('Transaction Successful:', response))
  .catch(error => console.error('Transaction Failed:', error));
```

## API Endpoints

The project provides REST API endpoints for interacting with Aptos:

-   `POST /send-coin` – Transfer coins to another account.
    
-   `GET /account/:address` – Retrieve account details.
    
-   `POST /deploy` – Deploy a Move smart contract.
    

## Contributing

Feel free to contribute to the project by submitting pull requests or reporting issues.

## License

This project is licensed under the MIT License.
