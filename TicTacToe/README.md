<p align="center">
    <picture>
        <source media="(prefers-color-scheme: dark)" srcset=".docs/tictactoe-logo-dark-theme.png">
        <img alt="SwayApps TicTacToe Logo" width="400px" src=".docs/tictactoe-logo-light-theme.png">
    </picture>
</p>

<p align="center">
    <a href="https://crates.io/crates/forc/0.60.0" alt="forc">
        <img src="https://img.shields.io/badge/forc-v0.60.0-orange" />
    </a>
    <a href="https://crates.io/crates/fuel-core/0.26.0" alt="fuel-core">
        <img src="https://img.shields.io/badge/fuel--core-v0.26.0-yellow" />
    </a>
    <a href="https://crates.io/crates/fuels/0.62.0" alt="forc">
        <img src="https://img.shields.io/badge/fuels-v0.62.0-blue" />
    </a>
</p>

## Overview

An on-chain TicTacToe game, where two players compete to align 3 markers in a row. The game consists of a 3x3 grid.
The game has been won if three markers were aligned in a row. Otherwise, it's a draw.

More information can be found in the [specification](./SPECIFICATION.md).

## Project structure

The project consists of a smart contract.

```sh
TicTacToe
├── tictactoe-contract
│   ├── src/main.sw
│   └── tests/harness.rs
├── src
│   ├── package.json
│   ├── index.html
│   └── main.tsx
├── README.md
└── SPECIFICATION.md
```

## Running the project

### User interface

In order to run the subsequent commands change into the following directory `/path/to/TicTacToe/app/<here>`.

#### Run the frontend application

```bash
pnpm install
pnpm project-setup
```

You will need to install the [Fuel wallet](https://wallet.fuel.network/docs/install/) in order to interact with the application. Now you can open your browser and interact with the tic-tac-toe contract through the frontend.  To play connect two of your wallet accounts and switch between them so each can take their turn.  If you want to run this locally you will need to modify the `chainConfig.json` file to fund your wallet locally.  Add your wallet address and give it some amount of asset id 0x0000...0000.

### Project

In order to run the subsequent commands change into the following directory `/path/to/TicTacToe//<here>`.

#### Program compilation

```bash
forc build --locked
```

#### Running the tests

Before running the tests the programs must be compiled with the command above.

```bash
cargo test --locked
```
