# Simple Voting DApp (Decentralized Application)

![Solidity](https://img.shields.io/badge/Solidity-%5E0.8.0-blue)
![Ethereum](https://img.shields.io/badge/Ethereum-Smart%20Contract-brightgreen)
![License](https://img.shields.io/badge/License-MIT-orange)

This project is a **Simple Voting DApp** built using Solidity, designed to help you learn the basics of smart contract development on Ethereum. It demonstrates key concepts such as state variables, mappings, events, and access control.

The project implements a **basic voting system** where:
- The owner of the contract can add candidates.
- Voters can vote for their preferred candidate.
- Each voter can vote only once.

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Technologies Used](#technologies-used)
4. [How It Works](#how-it-works)
5. [Getting Started](#getting-started)
   - [Prerequisites](#prerequisites)
   - [Installation](#installation)
   - [Deployment](#deployment)
6. [Usage](#usage)
7. [Contributing](#contributing)
8. [License](#license)
9. [Acknowledgements](#acknowledgements)

---

## Project Overview

This project is a **Simple Voting System** where:
- The owner of the contract can add candidates.
- Voters can vote for their preferred candidate.
- The system ensures that each voter can vote only once by tracking their address.

The project is designed to be beginner-friendly and introduces key Solidity concepts like **mappings**, **modifiers**, and **events**.

---

## Features

- **Add Candidates**: Only the contract owner can add candidates to the voting system.
- **Vote for Candidates**: Voters can vote for their preferred candidate.
- **Prevent Duplicate Voting**: Each voter can vote only once.
- **View Results**: Anyone can view the number of votes each candidate has received.

---

## Technologies Used

- **Solidity**: The smart contract is written in Solidity (version ^0.8.0).
- **Remix IDE**: Used for testing and deploying the contract.
- **Ethereum**: The contract is deployed on the Ethereum blockchain (testnet or mainnet).
- **GitHub**: For version control and collaboration.

---

## How It Works

### Voting Mechanism

1. **Add Candidates**:
   - The contract owner can add candidates using the `addCandidate` function.

2. **Vote for Candidates**:
   - Voters can vote for a candidate by calling the `vote` function and specifying the candidate's ID.
   - The contract checks if the voter has already voted using a `mapping(address => bool)`.

3. **Prevent Duplicate Voting**:
   - Each voter's address is stored in a mapping after they vote.
   - If a voter tries to vote again, the transaction will revert with an error message.

4. **View Results**:
   - Anyone can call the `getCandidate` function to view the details of a candidate, including their vote count.

### Smart Contract Functions

- **`addCandidate(string memory _name)`**: Adds a new candidate (owner-only).
- **`vote(uint _candidateId)`**: Allows a voter to vote for a candidate.
- **`getCandidate(uint _candidateId)`**: Returns details of a candidate.

---

## Getting Started

### Prerequisites

- Basic knowledge of Solidity and Ethereum.
- [Metamask](https://metamask.io/) or another Ethereum wallet.
- [Remix IDE](https://remix.ethereum.org/) for testing and deployment.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/simple-voting-dapp.git
   cd simple-voting-dapp
  '''
2. Open the project in Remix IDE or your preferred Solidity development environment.

### Deployment

1. Compile the `SimpleVoting.sol` contract in Remix.
2. Deploy the contract to an Ethereum testnet (e.g., Goerli) or mainnet using Remix or a tool like Hardhat/Truffle.
3. Interact with the contract using Remix or a custom frontend.

### Usage

### Step 1: Add Candidates

- Call `addCandidate("Alice")` to add a candidate named Alice.
- Call `addCandidate("Bob")` to add a candidate named Bob.

### Step 2: Vote for Candidates

- Voter A calls `vote(1)` to vote for Alice.
- Voter B calls `vote(2)` to vote for Bob.

### Step 3: Check Results

- Call `getCandidate(1)` to see Alice's vote count.
- Call `getCandidate(2)` to see Bob's vote count.

### Contributing

Contributions are welcome! If you'd like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch:  
   ```sh
   git checkout -b feature/YourFeatureName
   ```
3. Commit your changes:  
   ```sh
   git commit -m 'Add some feature'
   ```
4. Push to the branch:  
   ```sh
   git push origin feature/YourFeatureName
   ```
5. Open a pull request.

### License

This project is licensed under the MIT License. See the [`LICENSE`](./LICENSE) file for details.

### Acknowledgements

This project was created as part of learning Solidity and Ethereum development.

Special thanks to the Ethereum community for providing excellent resources and tools.



