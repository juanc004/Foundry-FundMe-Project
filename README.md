# Foundry FundMe Project

This contract was developed as part of the Cyfrin Updraft Foundry Fundamentals course. It allows users to fund a contract with a minimum USD value in ETH and enables the owner to withdraw the funds. The project uses Chainlink for reliable price feeds and supports zkSync for layer-2 scaling. Designed to improve Foundry and Solidity skills, it is intended for testing on Anvil, Sepolia, and zkSync networks.


## Features

- **Crowdfunding:** Users can fund the contract with ETH.
- **Minimum Funding Requirement:** Ensures a minimum amount of USD equivalent in ETH is sent.
- **Owner Withdrawal:** Only the contract owner can withdraw the funds.
- **Chainlink Price Feeds:** Uses Chainlink oracles to fetch the ETH/USD price.
- **zkSync Support:** Supports zkSync for transactions.

## Installation

### Prerequisites

- [Foundry](https://github.com/foundry-rs/foundry) - Ethereum development environment.
- [Node.js](https://nodejs.org/) and npm - For zkSync CLI.
- An Ethereum wallet (e.g., MetaMask).

### Steps

1. Clone the repository:
   ```zsh
   git clone https://github.com/juanc004/Foundry-FundMe-Project.git
   cd Foundry-FundMe-Project
   ```

2. Install dependencies and build the project:
   ```zsh
   make all
   ```

3. Update .env variables with your respective values:
   ```env
    SEPOLIA_RPC_URL=<YOUR_SEPOLIA_RPC_URL>
    PRIVATE_KEY=<YOUR_PRIVATE_KEY>
    ETHERSCAN_API_KEY=<YOUR_ETHERSCAN_API_KEY>
    SENDER_ADDRESS=<YOUR_PUBLIC_ADDRESS>
    DEFAULT_ANVIL_KEY=<YOUR_DEFAULT_ANVIL_KEY>
    DEFAULT_ZKSYNC_LOCAL_KEY=<YOUR_DEFAULT_ZKSYNC_LOCAL_KEY>
   ```

## Usage

**Note: This is a testing contract and should not be used for live purposes with real funds.**

### Deployment

To deploy the contract on different networks:

**On Anvil:**

Start Anvil in a separate terminal:
```zsh
make anvil
```

Deploy the contract:
```zsh
make deploy CHAIN=anvil
```

**On Sepolia:**
```zsh
make deploy CHAIN=sepolia
```

### Funding the Contract

To fund the contract on different networks:

**On Anvil:**

```zsh
make fund Chain=anvil
```

**On Sepolia:**
```zsh
make fund Chain=sepolia
```

### Withdrawing Funds

To withdraw funds as the contract owner on different networks:

**On Anvil:**

```zsh
make withdraw CHAIN=anvil
```

**On Sepolia:**
```zsh
make withdraw CHAIN=sepolia
```

## Testing

To run tests:

```zsh
make test
```

```zsh
make zktest
```

