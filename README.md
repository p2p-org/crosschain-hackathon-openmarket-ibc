# OpenMarket - NFT marketplace over IBC #


***Note*** : This repository was created for the cross-chain hackathon results estimation convenience


**OpenMarket demo video:** 

**OpenMarket Demo websites:** 
- Zone #1 https://demo-ibc0.openmarket.one
- Zone #2 https://demo-ibc1.openmarket.one

OpenMarket is a decentralized marketplace for non-fungible tokens (NFT) trading. It is part of the Сosmos ecosystem and can be used to trade the non-fungible asset of any blockchain in it. This is done using the IBC protocol which, among other things, allows cryptocurrency and NFTs to be transferred between blockchains.

To start trading, tokens used by other blockchains are transferred via IBC protocol to OpenMarket Blockchain, where all the trading (e.g. flat sale ar an auction) takes place. After trading is done, tokens are transferred via IBC protocol to the target blockchain, not necessarily the one from which they originated. 

The usual applications for non-fungible tokens are representing art, game items, tickets, licenses, and identity. Those use cases can be implemented using forthcoming NFT functionality of Cosmos Hub and Binance Chain, or general-purpose smart contract platforms in the ecosystem like Agoric. 

Another area of application for NFT is decentralized finance. Tokens in them can be used to trade names and monikers, manage staking reward rights, resell Collateralized Debt Positions (CDPs) for stablecoins and much more. In the Cosmos ecosystem, Starname Network, Kava, Nervos are among the decentralized financial projects. A rarer variant of NFTs application is a decentralized autonomous organization (DAO), namely using NFT for DAO votes, managed accounts, vested tokens. 


From a technical point of view, OpenMarket consists of three interacting elements:

* Protocol: Tendermint+cosmos-sdk based blockchain that stores basic token information and runs all trading logic (putting up a token for sale, purchase, transfer, etc.). Stored in [marketplace](https://github.com/p2p-org/marketplace/tree/feat/hack-ibc-nft) and [modules](https://github.com/corestario/modules/tree/hack-ibc) repos.
* Data Warehouse (DWH) collects information about tokens from blockchain and constantly updates it, as well as aggregates NFT metadata located on external servers. Stroed in [DWH](https://github.com/p2p-org/dwh/tree/hack-ibc-docker) repo.
* The interface (web, mobile or CLI) allows you to send transactions to the blockchain and also receives and displays the information collected by DWH to users. Stored in [openmarket-sdk](https://github.com/p2p-org/openmarket-sdk) and [openmarket-demo](https://github.com/p2p-org/openmarket-demo/tree/dev) repos.

Most interesting part blockchain-wise is [NFT IBC Packet module](https://github.com/p2p-org/marketplace/tree/feat/hack-ibc-nft/x/nftIBC).

