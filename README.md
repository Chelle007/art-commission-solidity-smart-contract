# ArtCommissionContract

## Description

ArtCommissionContract is a smart contract written in Solidity that facilitates art commission agreements between artists and clients.

## Features

- **Secure Escrow Management:** The contract holds funds in escrow until the completion or cancellation of the commission, ensuring that both parties fulfill their obligations.
- **Artwork Submission:** Artists can submit completed artwork to the contract, providing transparency and accountability in the commission process.
- **Revision Requests:** Clients can request revisions to the artwork, allowing for iterative improvements and ensuring satisfaction with the final product.
- **Contract Cancellation:** In case of disputes or dissatisfaction, contracts can be cancelled, with funds refunded to the appropriate parties according to predefined rules.

## Contract Structure

The contract includes the following state variables and functions:

- **State Variables:**
  - `artist`: Address of the artist.
  - `client`: Address of the client.
  - `serviceProvider`: Address of the service provider (deployer of the contract).
  - `totalCost`: Total cost of the commission.
  - `escrowBalance`: Balance held in escrow.
  - `revisionCount`: Number of revisions requested.
  - `maxRevisions`: Maximum number of revisions allowed.
  - `ipfsHash`: IPFS hash of the submitted artwork.
  - `ipfsHashHistory`: History of IPFS hashes.
  - `isCancelled`: Flag indicating if the contract is cancelled.
  - `isCompleted`: Flag indicating if the contract is completed.
  - `artFinished`: Flag indicating if the artwork is finished.
  - `revisionRequested`: Flag indicating if a revision is requested.

- **Functions:**
  - `makeFullPayment`: Client makes full payment to escrow with fee deduction.
  - `submitArtwork`: Artist submits completed artwork.
  - `approveArtwork`: Client approves the artwork, releasing funds to the artist.
  - `cancelContract`: Handle contract cancellation and refund with fee deduction.
  - `requestRevision`: Client requests a revision.
  - `submitRevisedArtwork`: Artist submits a revised version of the artwork.
  - `checkContractStatus`: Check the status of the contract.

## Usage

To deploy the contract and interact with it, you can use tools such as Remix IDE, Truffle, or Hardhat. After deploying the contract, clients and artists can interact with it using Ethereum wallets such as MetaMask.

## License

This contract is released under the MIT License.
