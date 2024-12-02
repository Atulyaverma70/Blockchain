# Blockchain
- Blockchain is the decentralized digital ledger technology. 
- It is used to store transactions which are immutable, transparent and secure. 
- It consist of chain of blocks which contain cryptographic hash of previous block.
- The Key fetures blockchain include:-
    - **Decentralized**- In this Blockchain data is distributed across network of computers, Instead of central location. It reduces the risk of single point of failure.
    - **Transparency**- All transactions of the blockchain visible to all the participants.
    - **Immutability**- It can't be changed if transaction once stored.
    - **Security**- It uses cryptographic technique to secure transactions and control access to the network. Consensus mechanism like POS and Pow ensures that only valid transactions added.
- Blockchain architecture-
    ![Blockchain Architecture](Blockchain-architecture-1.png)
- Blockchain Components:-
    - Blocks
    - Transactions
    - Decentralized Network
    - Consensus Mechanism
    - Cryptographic hashing
    - Public/Private keys
- Application of Blockchains:-
    - Cryptocurrency
    - Voting System
    - Healthcare
    - Supply Chain Management
    - Energy Trading
    - Real Estate
- Blockchain advantages:-
    - No single point of failure
    - No middle server required
    - cost reduction
    - Immutable
    - Blockchain is open
- Disadvantages of Blockchain:-
    - Verification is required for every transaction
    - Too much consumption of Power and electricity
    - Storage Problem 


# Consensus Mechanism
- CM are Protocol that are used to ensure agreement between participents on the validity of transactions.
- Some common consensus mechanism are:-
    - **Pow(Proof of work)**- it is an algorithm.
    - it require participants, known as miners, to solve mathmatical complex puzzle to add blocks in blockchain.
    - In validating this you have to need good investment , high graphic card,etc.
    - Bitcoin uses pow.
    - Less energy efficient.
    - **Pos(Proof of stake)**-Ethereum is shifted from pow to pos.
    - Pos select validators to valdate or create new blocks on the basis of amount of cryptocurrency they hold.
    - it is more decentralized.
    
    - it inhance the scalability.
    - Less energy consumption in comapre to pow.
    - **PoA(proof of authority)**- it has limited number of trusted validators.
    - **DPoS(delegated)**- depends on the basis of delegation of votes.

## Hyperledger
Hyperledger is an open-source initiative by the Linux Foundation aimed at advancing cross-industry blockchain technologies. It focuses on providing tools, frameworks, and libraries to build enterprise-grade blockchain applications
* fundamentals of hyperledger:
    * Modular architecture
        - it provide modularity and allow developer to play components like consensus algorithm, mebership service, cryptographic libraries.
    * Pemissioned Blockchain
        -  Only authorized participants can join and interact.
    *  Smart Contracts
        - Smart contracts in Hyperledger Fabric are called chaincode, implemented in languages like Go, Java, or Node.js.
    * Privacy and Confidentiality
        - Supports private data collections and channels to enable secure, confidential communication among specific participants.
    * Scalibility and performance
        - Designed to meet enterprise-level scalability and performance.
* Applications:
    * Supply chain mangement
    * Healthcare
    * Financial sevices
    * Identity verification

<hr>

## Transaction process
The transaction process in blockchain involves several key steps that ensure data integrity, transparency, and security.
* Processes
    * Transaction Initiation
        - A user initiates a transaction using their private key to sign the transaction date.
        - It include sender adress, Recipient adress, amount.
    * Transaction Broadcasting
        - signed transaction is broadcasted to the blockchain network.
    * Transaction Validation
        - Nodes (validators or miners) verify the transaction using consensus protocols.
    *  Transaction Inclusion in a Block
        - Valid transactions are grouped into a block.
    * Block Validation and Consensus
        - network reaches a consensus on the validity of the new block.
    * Transaction Confirmation
        - Once the block containing transaction it considered as confirmed.
    * Ledger Update
        - distributed ledger is updated across all nodes in the network.
    
<hr> 

## MSP(membership service provider)
 Membership Service Provider (MSP) is a component responsible for managing the identities of participants in a blockchain network. It ensures that only authenticated and authorized members can perform actions within the network.

* Role of MSP
    * Identity Management: MSP handles the identities of all participants.
    * Authentication:
    * Authorization
* Type of MSP 
    * Local MSP: used by single node for its own identity.
    * Channel MSP: Defines the set of identities allowed to participate in a specific channel.
        * Ensures that only authorized participants can interact within the channel.
* Workflow of MSP in Hyperledger fabric
    * Enrollment
        - A participant requests a certificate from the Certificate Authority.
    * Transation signing
        - The participant uses their private key to sign transactions.
    * Access control
        - MSP checks if the participant's certificate is valid and complies with the network's policies.
    * Consensus Participation
        - Only nodes with valid identities managed by the MSP can participate in consensus mechanisms.
* Advantages
    - Security
    - Flexibility
    - Scalibility
    - Decentralization

<hr>

## Fabric gateway
The Fabric Gateway is an abstraction layer introduced in Hyperledger Fabric that simplifies how applications interact with blockchain networks.
* Key features of fabric gateway
    * Centralized transaction submission
        - Applications communicate with a single gateway peer rather than directly interacting with multiple peers for endorsements.
    * Simplified Client SDKs
        - The gateway removes the need for applications to handle low-level blockchain operations,
    * Improved application architecture
        - Reduces the application's responsibility to manage network topology and business logic, focusing solely on initiating transactions and querying the ledger.
    * Scalibility
        - Multiple clients can share a single gateway, improving scalability in enterprise networks.

* Workflow of fabric gateway
    * Application request
        - The client application connects to the gateway peer and sends a request
    * Endolrsement collection
        - Collects endorsements from the required peers.
    * Transaction Submission:
        - The gateway submits the endorsed transaction to the ordering service for inclusion in a block.
    * Block Validation and Commit:
        - The block containing the transaction is validated and committed to the ledger by peers.
    * Response to client
        - The gateway sends the transaction or query result back to the application.
    
* Benefits
    - Enhanced security
    - Reduce application management
    - Cross language support

## Challenges in hyperledger
* Complexity of Setup and Configuration
    -  Setting up a Hyperledger network is complex due to its modular architecture, requiring careful configuration of peers, orderers, Membership Service Providers (MSPs), and channels.
* Scalibility issue
    - Achieving high scalability in large networks can be challenging, especially as the number of peers, transactions, and participants increases.
* Limited Interoperability
    - Hyperledger framework are not  interoperable with other blockchains.
* Resource-Intensive
    - High infrastructure costs, limiting accessibility for smaller organizations
* Limited Developer Ecosystem
    - Fewer libraries, tools, and community resources available for development and troubleshooting.
* Data Privacy Management
    - Increased overhead for maintaining data confidentiality.
* Maintenance and Upgrades
    - Upgrading Hyperledger networks can be disruptive, as it may require downtime and careful migration of data and configurations.

## Endorsement policies
Endorsement policies in blockchain, specifically in Hyperledger Fabric, define the rules for validating transactions.
* Static Policies:
    - Fixed rules defined during chaincode deployment.
    - Examples:
        - AND: All specified organizations must endorse.
        - OR: Any one of the specified organizations can endorse.
        - N-Out-Of: A minimum number of specified organizations must endorse.

* Dynamic Policies:
    - Policies that can change dynamically based on the governance of the network (e.g., using smart contracts or administrative decisions).

## Hperledger fabric Network
A Hyperledger Fabric Network is a permissioned blockchain system designed for enterprise use cases. It is highly modular and flexible, enabling organizations to define their blockchain network structure and governance according to their specific needs.

* Key Components of a Hyperledger Fabric Network
    * Peers
        - Nodes in the network that maintain the ledger and execute smart contracts
    * Ordering Service
        - Provides a consensus mechanism to order transactions into blocks and deliver them to peers.
    * Membership Service Provider (MSP)
        - Manages identities of participants in the network using certificate
    * Ledger
        - Stores all the transaction
    * Channels
        - Private subnetwork within a fabric network
    * client application 
        - Interfaces used by users to interact with the blockchain network.

* How it work
    * Transaction Proposal:
        - A user submits a transaction request to the network.
    * Simulation and Endorsement:
        - Selected peers (endorsers) check the request by simulating it using smart contracts and give signed approvals.
    * Submission to Ordering Service:
        - The approved transaction is sent to the ordering service, which organizes transactions.
    * Block Creation:
        - The ordering service groups transactions into blocks and sends them to all peers.
    * Validation and Commitment:
        - Peers check if the transaction follows the rules and add valid ones to the ledger.
    * Ledger Update:
        - The blockchain records the transaction, and the current state is updated.

<hr>

## TXO Model
The TXO (Transaction Output) model is a fundamental concept used in blockchain systems, particularly in Bitcoin and similar cryptocurrencies. It represents the way transactions are structured and how value is transferred between participants in the network.

* Key components
    * UTXO (Unspent Transaction Output):
        - A UTXO is an output from a previous transaction that has not been spent yet.
        - It acts as the input for a future transaction.
    * Inputs:
        - References to one or more UTXOs from previous transactions that are being spent in the current transaction.
    * Outputs:
        - New UTXOs created by the transaction, representing the transferred value to recipients.
    * Transaction:
        - A transaction in the TXO model takes UTXOs as inputs, consumes them, and creates new UTXOs as outputs.

* How it works
    * Creating UTXOs:
        - When a transaction is made, it creates outputs (UTXOs) that can later be used as inputs for new transactions.
        - Example: Alice sends 1 BTC to Bob. This creates a UTXO of 1 BTC for Bob.
    * Spending UTXOs:
        - To make a transaction, a user must spend existing UTXOs by referencing them in the transaction's inputs.
        - UTXOs can only be spent once, ensuring double-spending is prevented.
    * Change UTXO:
        - If the UTXO being spent is larger than the transaction amount, the difference is sent back to the sender as a "change" UTXO.

<hr>

## Identity mixer
A mixer (also known as a tumbler) is a service or tool used to enhance the privacy of cryptocurrency transactions.

* How Mixers Work
    * Input Collection:
        - Users send their cryptocurrency (e.g., Bitcoin, Ethereum) to the mixer.
    * Obfuscation:
        - The mixer combines and breaks down the funds into smaller amounts.
        - It randomly distributes these smaller amounts to the intended recipients through multiple transactions, often with delays.
    * Output Distribution:
        - Users receive an equivalent amount of cryptocurrency from the pool but not from their original input.
        - The output is sent to a new address specified by the user.

* Types of Blockchain Mixers
    * Centralized Mixers:
        - Operated by a single entity.
        - Users trust the service provider to handle their funds and maintain privacy.
        - Risk: Trust issues and potential for regulatory scrutiny.
    * Decentralized Mixers:
        - Operate without a central authority, using smart contracts or peer-to-peer protocols.
        - Example: CoinJoin or Tornado Cash.
        - Advantage: Greater trustlessness and resistance to censorship.
* Advantages
    * Privacy enhancement
    * Protection against survillance

<hr>

## Smart contract
A smart contract is a self-executing contract with the terms of the agreement between buyer and seller being directly written into lines of code.

* Key Features of Smart Contracts:
    * Self-Execution: They run automatically without the need for intermediaries.
    * Immutable: Once deployed, the code cannot be changed, ensuring trust and security.
    * Decentralized: They are distributed across all nodes in the blockchain, making them tamper-proof.
    * Transparent: The code and transaction history can be accessed by all participants, ensuring transparency.
* How Smart Contracts Work:
    * Trigger Event: A predefined condition or event occurs, which triggers the contract.
    * Execution: The smart contract code is executed to perform the specified actions (e.g., transferring funds, verifying data).
    * Validation: The contract verifies that all conditions are met before executing the actions.
    * Completion: The contract performs the necessary operations and updates the blockchain ledger.
* Blockchain Platforms for Smart Contracts:
    * Ethereum
    * Hyperledger fabric

<hr>



