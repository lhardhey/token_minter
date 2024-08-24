# Token Minting DApp

This DApp allows users to mint their own tokens on the Ethereum blockchain. Users can specify the name, symbol, and initial supply of the tokens they wish to create.

## Features

- **Token Creation**: Users can create a new token by specifying its name, symbol, and initial supply.
- **Inspection**: Users can inspect the list of created tokens.

## Prerequisites

- Node.js
- NPM or Yarn
- Ethers.js
- Cartesi Rollup Server

## Setup

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/token-minting-dapp.git
    cd token-minting-dapp
    ```

2. Install dependencies:
    ```bash
    npm install
    ```
    or
    ```bash
    yarn install
    ```

3. Create a `.env` file with the following content:
    ```
    ROLLUP_HTTP_SERVER_URL=http://your-rollup-server-url
    ```

4. Start the DApp:
    ```bash
    node index.js
    ```

## How It Works

### Token Creation

The DApp listens for requests to create a token. Users must provide the token name, symbol, and initial supply. If the request is valid, the token is created and stored.

### Token Inspection

Users can inspect the list of created tokens by sending an inspection request. The DApp will return the current state of all tokens.

## API Endpoints

- **Advance State**: Handles the creation of a new token.
- **Inspect State**: Allows inspection of the current list of tokens.

## Code Overview

- `hex2Object(hex)`: Converts a hexadecimal string to an object.
- `obj2Hex(obj)`: Converts an object to a hexadecimal string.
- `handle_advance(data)`: Handles the token creation logic.
- `handle_inspect(data)`: Handles the inspection logic.
- `handlers`: Maps request types to their respective handlers.
- `finish`: Continuously polls the Rollup Server for new requests.
