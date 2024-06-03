# Blockchain Voting System

Welcome to the Blockchain Voting System project! This repository is part of the Introduction to Blockchain course at the University of Eastern Finland. I am using the `sanattaori/techdot Aadhar` and `HeikkiLu/blockchain_voting` projects as a base, adding my own modifications and features to build a blockchain-based voting system.

## Running the Project

Follow these steps to run the project locally.

### 1. Clone the Project
Clone the repository to your local machine:
```bash
git clone https://github.com/laenol/Voting
```

### 2. Install Dependencies
Navigate into the project directory and install the necessary dependencies:
```bash
npm install
```
Install additional dependencies:
```bash
npm install ethereumjs-testrpc web3
npm install solc
```
Install `ganache-cli` globally. Ganache is a tool for creating a local blockchain for fast development with Ethereum:
```bash
npm install -g ganache-cli
```

### 3. Initialize the Database
Initialize the SQLite database by running:
```bash
node init_db.js
```

### 4. Configure Ganache
Change the Ganache address in `blockchain_voting/index.js`:

- Open `blockchain_voting/index.js`
- Find line 48 (`web3.setProvider(new web3.providers.HttpProvider('http://ganache:8545'));`)
- Change `'http://ganache:8545'` to `'http://localhost:8545'`

Change the hostname in `blockchain_voting/check_ganache_availibility.js`:

- Open `blockchain_voting/check_ganache_availibility.js`
- Find line 6 (`hostname: 'ganache',`)
- Change `'ganache'` to `'localhost'`

### 5. Run Ganache
Start Ganache to create the local blockchain:
```bash
ganache-cli
```

### 6. Run the Project
Start the project by running in the project file:
```bash
node index.js
```

### Default Credentials
Use the following default credentials to log in:
- **Username:** `admin`
- **Password:** `password`

## Explanation

- **Cloning the Project:** Copies the project repository to your local machine.
- **Installing Dependencies:** Installs the necessary software libraries required to run the project.
- **Initializing the Database:** Sets up the database that will store the voting data.
- **Configuring Ganache:** Ensures the project connects to the local blockchain created by Ganache.
- **Running Ganache:** Starts the local blockchain environment for testing and development.
- **Running the Project:** Launches the voting system application.

This step-by-step guide should make it easy to set up and run the Blockchain Voting System on your local machine. Enjoy exploring the world of blockchain-based voting!
