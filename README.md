# Polygon Proof of Stake - POLY PROOF Advanced
# owner Gaurav Kumar Saini from CHANDIGARH UNIVERSITY
## Description

In this Assessment I will deploy an NFT collection on the Ethereum blockchain, map the collection to the Polygon network, and transfer assets using the Polygon Bridge. The project utilizes an image generation tool and implements ERC721A tokens. This Project is Part of My Metacrafters Blockchain Training.

## Features

- Generate a 5-item collection using DALLE 2 or Midjourney
- Store items on IPFS using pinata.cloud
- Deploy an ERC721A contract to the Goerli Ethereum Testnet
- Map the NFT collection using the Polygon network token mapper
- Script for batch mint all NFTs
- Implement approval and deposit of NFTs for transfer
- Test balanceOf on Mumbai

## Contracts
### Execution

Follow the steps below to execute the project:

1. **Generate a 5-item collection**: Use Lexica to generate a collection of 5 unique NFTs. Ensure that each NFT is distinct and represents your desired collection.
2. **Store items on IPFS**: Upload the generated NFT items to IPFS using pinata.cloud or a similar service. Obtain the IPFS hashes for each item to be used as the token URIs.
3. **Deploy the NFT Contract**: Deploy the MyNFT contract on the Ethereum network. During deployment, set a suitable name and symbol for the contract and provide a detailed prompt description for the NFTs.
   - Execute the command: `npx hardhat run scripts/deploy.js --network goerli`
5. **Implement promptDescriptionDetail function**: Enhance the MyNFT contract by implementing the `promptDescriptionDetail` function. This function should return a detailed description of the prompt used to generate the NFTs.
6. **Map the NFT collection**: Map the NFT collection on the Polygon network using the token mapper tool. This step is optional but can be helpful for visualizing and interacting with the collection on the Polygon network.
8. **Batch Mint NFTs**: Write a script to perform batch minting of all 5 NFTs. Utilize the `batchMint` function of the MyNFT contract to assign each NFT to a recipient address and set the corresponding IPFS hash as the token URI.
   - Execute the command: `npx hardhat run scripts/batchMint.js --network goerli`
9. **Batch Transfer NFTs to Polygon Mumbai**: Write a script to perform batch transferring of all 5 NFTs from the Ethereum network to the Polygon Mumbai network using the FxPortal Bridge. Ensure that the NFTs are approved for transfer and deposit them to the Bridge.
   - Execute the command: `npx hardhat run scripts/batchTransfer.js --network goerli`
10. **Approve NFTs for Transfer**: Implement the necessary steps to approve the NFTs for transfer from the Ethereum network to the Polygon Mumbai network.
11. **Deposit NFTs to the Bridge**: Perform the required operations to deposit the NFTs to the FxPortal Bridge. This step enables the secure transfer of the NFTs from the Ethereum network to the Polygon Mumbai network.
12. **Test balanceOf on Mumbai**: Test the `balance` function on the Polygon Mumbai network to verify the NFT balance of a specific address.
    
### MyNFT.sol

This contract represents the NFT collection and inherits from the ERC721A contract. It includes the following functions:

- `mint(uint256 quantity)`: Allows the owner to mint NFTs with the specified quantity.
- `promptDescription()`: Returns the prompt description for generating the NFT images.

## Setup

1. Clone the repository: `git clone https://github.com/cu-sanjay/Polygon-Proof-of-Stake`
2. Install the dependencies: `npm install`

## Configuration

1. Create a `.env` file in the root directory and provide the following information:
     `PRIVATE_KEY=<key>`

## Usage

1. Deploy the contract to the Goerli Ethereum Testnet:

   ```bash
   npx hardhat run scripts/deploy.js --network goerli
   ```
   
2. Mint NFTs:
   
   ```bash
   npx hardhat run scripts/batchMint.js --network goerli
   ```


3. Approve and transfer NFTs to Polygon Mumbai:
  ```bash
 npx hardhat run scripts/batchTransfer.js --network goerli
  ```
# video explanation 
https://www.loom.com/share/aff0c702836e47b58c7ef80a41384bda?sid=2feb84b6-3459-4db2-9bbb-fb5313ae349d
# thank you ...
