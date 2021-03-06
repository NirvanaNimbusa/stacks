# Stacks FAQ 

Note this is an *ongoing Stacks FAQ* and can continue to be updated by various community and entity leaders. Please feel free to add question and answer suggestions via GitHub issues in the Stacks repository here - thanks! 

## **Blockchain state post mainnet launch**

While Stacks 2.0 code has undergone significant testing (public testnets running for ~8 months; multiple security audits; bug bounties), like any complex software (~200K lines of code!) and protocol, there can be latent or emergent bugs (remember the early days of [Bitcoin](https://en.wikipedia.org/wiki/History_of_bitcoin) and [Ethereum](https://medium.com/mycrypto/the-history-of-ethereum-hard-forks-6a6dae76d56f)). See [this post](https://forum.stacks.org/t/500-blocks-into-the-stacks-2-0-mainnet/11606) for a summary of salient updates following the first 500 blocks, and this general [status update](https://blog.stacks.co/stacks-2-status-update). You can also view this [Stacks status page](https://stacks-status.com/ ). 

Additional details: We’ve crafted a proposal for dealing with any CRITICAL issues post-launch: critical meaning there’s active or imminent threat to the network security or assets. For everything else, we will follow the SIP process (outlined in [SIP-000](https://github.com/blockstack/stacks-blockchain/blob/master/sip/sip-000-stacks-improvement-proposal-process.md)).

Regarding critical but non-consensus-breaking updates (e.g. a crash on the networking path):

- The Stacks Foundation, working with Stacks core developers, will publish a new release on Github.
- Anyone running a Stacks 2.0 node SHOULD upgrade. This would be just a routine software update, no impact to chainstate.

Regarding critical, consensus-breaking updates (e.g. an exploit is discovered in PoX or Clarity):

- The Stacks Foundation, working with Stacks core developers, will publish a new release on Github.
- Anyone running a Stacks 2.0 node MUST upgrade. This will be a hard-fork of the chain.
- In the first month or two immediately post launch, miners should anticipate and be prepared to (frequently) upgrade their nodes to:
    - Incorporate fixes for critical issues in the first category.
    - Incorporate regular updates that are not-critical, but still useful: for instance, improvements in logging, configuration management, monitoring etc.
 
 ## Stacks Token
 
 **What is the connection between Stacks and Bitcoin?**

The Stacks 2.0 blockchain brings (a) scalable transactions and (b) general-purpose smart contracts to Bitcoin without modifying Bitcoin. Stacks miners use Bitcoin to mine newly minted Stacks, while Stacks holders can lock their STX in consensus to earn Bitcoin, making STX a unique crypto asset that is natively priced in BTC and distributes BTC earnings.

Further details: The Clarity language, a secure and predictable smart contract language, goes live with Stacks 2.0 mainnet launch. It was developed by Princeton and MIT scientists over the last two years. Clarity makes it much harder to have smart contract bugs and allows developers to write logic around Bitcoin state directly. We believe bringing smart contracts directly to Bitcoin can make BTC more valuable as it can be put to productive use instead of being a passively held asset. 

**What can I do with STX?** 

STX are consumed when apps interact with [Clarity](https://clarity-lang.org/) smart contracts and users register blockchain-based names across hundreds of Blockstack apps. You can also Stack STX tokens to receive BTC rewards in a process called Stacking. 

## Stacking 

**What is Stacking?**

Stacking is the first consensus mechanism between two blockchains - in this case, the Bitcoin blockchain and Stacks blockchain. Stacking rewards network participants a base cryptocurrency, like Bitcoin, for locking up a newer cryptocurrency, like STX. Stackers participate in PoX consensus by sending  useful information to the network in Stacking transactions. 

Further details: We encourage you to read the technical overview available in the [whitepaper](https://gaia.blockstack.org/hub/1AxyPunHHAHiEffXWESKfbvmBpGQv138Fp/stacks.pdf) and to review this [blog post](https://blog.blockstack.org/stacking-earnings-model/) with a breakdown of potential earnings.  An overview of Stacking can be viewed at stacks.org/stacking

**What is the minimum to participate in Stacking?**

Stacking minimums are dynamic minimum based on participation levels. There are also several options for Stacking. See stacks.org/stacking for more info on Stacking partners, or visit Hiro.so/wallet to Stack via the Stacks wallet. 

- Users can pool their STX together to meet the minimum threshold using the delegate transactions. (Note that the minimum is dynamic and subject to change.) For example, third parties like OKCoin, Staked, and others anticipate enabling users to participate in Stacking even if they don't individually own the minimum threshold amount of STX. More info available on Stacks.org/stacking.

- For further info on Stacking protocol minimums via the wallet, see the [Stacking summary page](https://github.com/blockstack/stacks/blob/master/stacking.md) and [SIP-007](https://github.com/blockstack/stacks-blockchain/blob/master/sip/sip-007-stacking-consensus.md)
- For live updates on network minimums, see the Stacking API end point [here](https://stacks-node-api.mainnet.stacks.co/v2/pox) (NOTE: these are subject to change up until the end of the “prepare” phase of stacking.)

**When do Stacking rewards start?** 

Stacking rewards will be initiated following the first stacking cycle on the Stacks network, around end Jan. 2021 and paid out mid Feb. 2021. 

Further details: Upon launch, STX holders will be able to participate in the first Stacking cycle to test setup. BTC rewards are anticipated to start in following rewards cycle starting around the end of Jan. 2021. During the first reward cycle the network essentially getting up to speed and an anticipated beginning phase for the network.

## **Stacks Mining**

**Why would a miner spend BTC to mine STX?**

Simple arbitrage between the value of STX on exchanges and STX minted by mining. 

Earlier this year we introduced a limited mining bonus that gives early miners even more than 1000 STX/block in the early weeks of the system.
    - Specifically the STX mining schedule is:
        - Years 0-4: 1000 STX/block
        - Years 4-8: 500 STX/block
        - Years 8-12: 250 STX/block
        - Years 12+: 125 STX/block
    - See the Whitepaper for updated token economics. 

**How can I calculate the amount of BTC required for mining for one week?** 

See this community built [calculator](https://friedger.github.io/mining-calculator) There are lots of moving parts, but this calculator should help you get the gist of it.

**What are the minimum hardware requirements for mining?**

Just about any VPS or home PC will work - “mining” is not a compute intensive operation for stacks. That said, you need at least enough storage (currently 350GB) to hold bitcoin mainnet and 5GB/ish +/- per day in bandwidth.
    1. Stacks-node hardware requirements
    2. Bitcoind hardware requirements
    
**Where can I learn more about STX mining?**

- [Mining Docs](https://docs.blockstack.org/start-mining/mainnet) 
- https://stacks101.com/stx-mining-faq/
- Comprehensive document of community-compiled [mining questions](https://paper.dropbox.com/doc/Stacks-2.0-Mining-Questions--BDjmfvyQCysQI_2cIuhmmi0GAg-63CU2wD4zQsiiU6XPUtlr) 

## Accessing Stacks 2.0 Apps 

**How will the launch of Stacks 2.0 impact Stacks applications?** 

In the immediate term, users’ experiences with Stacks login, usernames, and existing applications may be impacted. That is, users may be asked to authenticate their Stacks IDs and log back into apps at some point. However, the launch of Stacks 2.0 will generally result in several upgrades to Stacks applications, including improvements to the Stacks login and wallet experiences. More info on developer upgrades in progress [here](https://forum.stacks.org/t/apps-support-upon-launch-of-stacks-2-0-mainnet/11526/2). 

Note this is an *ongoing Stacks FAQ* and can continue to be updated by various community and entity leaders. Please feel free to add question and answer suggestions via GitHub issues in the Stacks repository here - thanks! 

Also see [Stacks docs](https://docs.blockstack.org/understand-stacks/overview), [Forum](https://forum.stacks.org/), and [Discord](https://discord.gg/C8ycHu4)! 
