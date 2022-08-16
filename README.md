# Building a DAO

![](https://i.imgur.com/6uXR2G9.png)

## What is a DAO?

DAO stands for **D**ecentralized **A**utonomous **O**rganization. You can think of DAOs as analogous to companies in the real world. Essentially, DAOs allow for members to create and vote on governance decisions.

In traditional companies, when a decision needs to be made, the board of directors or executives of the company are in charge of making that decision. In a DAO, however, this process is democratized, and any member can create a proposal, and all other members can vote on it. Each proposal created has a deadline for voting, and after the deadline the decision is made in favour of the voting outcome (YES or NO).

Membership in DAOs is typically restricted either by ownership of ERC20 tokens, or by ownership of NFTs. Examples of DAOs where membership and voting power is proportional to how many tokens you own include [Uniswap](https://uniswap.org) and [ENS](https://ens.domains). Examples of DAOs where they are based on NFTs include [Meebits DAO](https://www.meebitsdao.world/).

## Building our DAO

You want to launch a DAO for holders of your `CryptoDevs` NFTs. From the ETH that was gained through the ICO, you built up a DAO Treasury. The DAO now has a lot of ETH, but currently does nothing with it.

You want to allow your NFT holders to create and vote on proposals to use that ETH for purchasing other NFTs from an NFT marketplace, and speculate on price. Maybe in the future when you sell the NFT back, you split the profits among all members of the DAO.

## Requirements

- Anyone with a `CryptoDevs` NFT can create a proposal to purchase a different NFT from an NFT marketplace
- Everyone with a `CryptoDevs` NFT can vote for or against the active proposals
- Each NFT counts as one vote for each proposal
- Voter cannot vote multiple times on the same proposal with the same NFT
- If majority of the voters vote for the proposal by the deadline, the NFT purchase can then be executed

## What we will make

- To be able to purchase NFTs automatically when a proposal is passed, we need an on-chain NFT marketplace that you can call a `purchase()` function on. There exist a lot of NFT marketplaces out there, but to avoid overcomplicating things, we create a simplified fake NFT marketplace for this tutorial as the focus is on the DAO.
- We will also make the actual DAO smart contract using Hardhat.
- We will make the website using Next.js to allow users to create and vote on proposals

## Prerequisites

- Must have completed the [NFT-Collection Tutorial](https://github.com/AzureKn1ght/NFT-Collection)
- Must have some ETH to give to the DAO Treasury

--- 

## BUILD IT

### Smart Contract Development

We will start off with first creating the smart contracts

- `FakeNFTMarketplace.sol`
- `CryptoDevsDAO.sol`


### Frontend Development

Now, it's time to build the Frontend interface so users can create and vote on proposals from the website.

To develop the website, we will be using [Next.js](https://nextjs.org/), which is a meta-framework built on top of [React](https://reactjs.org/).


### Testing

- Create a couple of proposals
- Try voting `YAY` on one, and `NAY` on the other
- Wait for 5 minutes for their deadlines to pass
- Execute both of them
- Watch the balance of the DAO Treasury go down 


### Technologies Used 
- [Hardhat](https://hardhat.org/)
- [Solidity](https://soliditylang.org/)
- [Ethers.js](https://github.com/ethers-io/ethers.js/)
- [React](https://reactjs.org/)
- [Next.js](https://nextjs.org/)

--- 

## DEPLOY 🚀

What good is a website if you cannot share it with others? Let's deploy the dApp and share it with the world.

### Smart Contract 
https://goerli.etherscan.io/address/0x4Dda85D5Ad5A2a934e69CAAE0f7257d7839DDe4B

### Dapp Frontend
https://dao-tutorial-azurekn1ght.vercel.app/
