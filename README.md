# Simple Onion Routing Network

## Overview
This project implements a simple onion routing network where messages are securely transmitted through multiple nodes before reaching the final destination. The system ensures privacy by encrypting messages at each hop.

## Features
- Start multiple nodes and users.
- Register nodes with a central registry.
- Send and receive encrypted messages.
- RSA and symmetric encryption support.
- Forward messages through a defined network circuit.
- Simple API routes for retrieving message details.

## Project Structure
```
Simple-Onion-Routing-Network-TD4/
│── src/
│   ├── crypto.ts   # Cryptographic functions
│   ├── network.ts  # Network and routing logic
│   ├── registry.ts # Node registration logic
│── __test__/
│   ├── tests/
│   │   ├── onionRouting.test.ts  # Tests for onion routing
│── package.json
│── README.md
```

## Installation
1. Clone the repository:
   ```sh
   git clone <repository-url>
   cd Simple-Onion-Routing-Network-TD4
   ```
2. Install dependencies:
   ```sh
   npm install
   ```

## Usage
### Starting the Network
To start the network with a specified number of nodes and users, modify the network initialization script accordingly.

### API Endpoints
The system provides the following API routes:
- **Node Routes:**
  - `GET /getLastReceivedEncryptedMessage`
  - `GET /getLastReceivedDecryptedMessage`
  - `GET /getLastMessageDestination`
  - `GET /getPrivateKey`
- **User Routes:**
  - `GET /getLastReceivedMessage`
  - `GET /getLastSentMessage`

## Cryptographic Functions
The cryptographic module provides functions for:
- RSA key generation (`generateRsaKeyPair`)
- RSA encryption and decryption (`rsaEncrypt`, `rsaDecrypt`)
- Symmetric key generation (`createRandomSymmetricKey`)
- Symmetric encryption and decryption (`symEncrypt`, `symDecrypt`)
- Key import/export functions

## Running Tests
The project includes automated tests using Jest.
To run tests, use:
```sh
npm run test
```
### Current Test Status
✔ **27 Passed Tests**
✎ **5 TODO Tests** (Hidden tests need implementation)

## Future Improvements
- Implement additional hidden tests.
- Enhance security mechanisms.
- Optimize message forwarding performance.

## License
This project is licensed under the MIT License.

