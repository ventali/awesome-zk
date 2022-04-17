<div align="center">
  <h1 align="center">Awesome Zero Knowledge</h1>
  <p align="center">
    <a href="https://github.com/sindresorhus/awesome">
      <img alt="awesome list badge" src="https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg">
    </a>
    <a href="https://github.com/ventali/awesome-zk/graphs/contributors">
      <img alt="GitHub contributors" src="https://img.shields.io/github/contributors/ventali/awesome-zk">
    </a>
    <a href="http://makeapullrequest.com">
      <img alt="pull requests welcome badge" src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat">
    </a>
  </p>

  <p align="center">A curated list of awesome ZK resources, libraries, tools and more.</p>
</div>

Table of Contents
=================

* [Basics](#basics)
* [Layer 2](#layer-2)
* [Projects](#projects)
  * [Zk\-VM](#zk-vm)
  * [Zk\-Layer1](#zk-layer1)
  * [Zk\-Layer2](#zk-layer2)
  * [Basic Computing](#basic-computing)
  * [Framework / SDK](#framework--sdk)
  * [Zk\-Applications](#zk-applications)
    * [Gaming](#gaming)
    * [Payment](#payment)
    * [Mixer](#mixer)
    * [KYC](#kyc)
    * [Wallet](#wallet)
    * [Crosschain](#crosschain)
    * [Marketplace](#marketplace)
    * [DeFi / DEX](#defi--dex)
    * [Tokens / NFT](#tokens--nft)
    * [Voting / Participation](#voting--participation)
  * [Hardware Acceleration](#hardware-acceleration)
  * [Trusted Execution Environment (TEE) Based Projects](#trusted-execution-environment-tee-based-projects)
* [Advanced Topics](#advanced-topics)
  * [PLONK](#plonk)
  * [Groth16](#groth16)
  * [Halo](#halo)
  * [Probabilistic Proof Systems](#probabilistic-proof-systems)
  * [Pinocchio](#pinocchio)
  * [Bulletproofs](#bulletproofs)
  * [Hash Functions](#hash-functions)
  * [Systems](#systems)
  * [Quadratic Span Programs](#quadratic-span-programs)
  * [Zether](#zether)
  * [Anonymous Zether](#anonymous-zether)
  * [Quisquis](#quisquis)
  * [Zk\-VM](#zk-vm-1)
* [Tools](#tools)
* [Auditing and Consulting](#auditing-and-consulting)
* [Discussions](#discussions)
* [Communities](#communities)

## Basics

- [Prerequisite understanding questions](https://0xparc.notion.site/Prerequisite-understanding-questions-c5ebb77a5cc049f39577ec9a7fb7b22c)
- Introduction
  - [Understanding ZKPs Through Illustrated Examples](https://blog.goodaudience.com/understanding-zero-knowledge-proofs-through-simple-examples-df673f796d99)
  - [Zero Knowledge Proofs: An Illustrated Primer](https://blog.cryptographyengineering.com/2014/11/27/zero-knowledge-proofs-illustrated-primer/)
  - [What are zk-SNARKs?](https://z.cash/technology/zksnarks/)
  - [ZKPs for Engineers: Introduction](https://blog.zkga.me/intro-to-zksnarks)
  - [Privacy in Cryptocurrencies: An Overview](https://medium.com/@yi.sun/privacy-in-cryptocurrencies-d4b268157f6c)
- Vitalik's blogs for STARKs
  - [Part 1: Proofs with Polynomials](https://vitalik.ca/general/2017/11/09/starks_part_1.html)
  - [Part 2: Thank Goodness It's FRI-day](https://vitalik.ca/general/2017/11/22/starks_part_2.html)
  - [Part 3: Into the Weeds](https://vitalik.ca/general/2018/07/21/starks_part_3.html)
- Explaining STARKs
  - [Part I: STARK Overview](https://aszepieniec.github.io/stark-anatomy/overview)
  - [Part II: Basic Tools](https://aszepieniec.github.io/stark-anatomy/basic-tools)
  - [Part II: FRI](https://aszepieniec.github.io/stark-anatomy/fri)
  - [Part IV: The STARK Polynomial IOP](https://aszepieniec.github.io/stark-anatomy/stark)
  - [Part V: A Rescue-Prime STARK](https://aszepieniec.github.io/stark-anatomy/rescue-prime)
  - [Part VI: Speeding Things Up](https://aszepieniec.github.io/stark-anatomy/faster)
- [zkSNARKs in a nutshell](https://blog.ethereum.org/2016/12/05/zksnarks-in-a-nutshell/)
- [Comments on paper: zkSNARKs in a Nutshell by Aaron](https://github.com/ventali/awesome-zk/tree/main/zk-intro)
- [An approximate introduction to how zk-SNARKs are possible](https://vitalik.ca/general/2021/01/26/snarks.html)
- Explaining SNARKs
  - [Part I: Homomorphic Hidings](https://electriccoin.co/blog/snark-explain/)
  - [Part II: Blind Evaluation of Polynomials](https://electriccoin.co/blog/snark-explain2/)
  - [Part III: The Knowledge of Coefficient Test and Assumption](https://electriccoin.co/blog/snark-explain3/)
  - [Part IV: How to make Blind Evaluation of Polynomials Verifiable](https://electriccoin.co/blog/snark-explain4/)
  - [Part V: From Computations to Polynomials](https://electriccoin.co/blog/snark-explain5/)
  - [Part VI: The Pinocchio Protocol](https://electriccoin.co/blog/snark-explain6/)
  - [Part VII: Pairings of Elliptic Curves](https://electriccoin.co/blog/snark-explain7/)
- Important landmarks for zk-SNARKs
  - [Succinct ZK](https://people.csail.mit.edu/vinodv/6892-Fall2013/efficientargs.pdf) - K92
  - [Succinct Non-Interactive ZK](https://people.csail.mit.edu/silvio/Selected%20Scientific%20Papers/Proof%20Systems/Computationally_Sound_Proofs.pdf) - M94
  - [“SNARK” terminology and characterization of existence](https://eprint.iacr.org/2011/443.pdf) - BCCT11
  - [Succinct NIZK without the PCP Theorem](http://www0.cs.ucl.ac.uk/staff/J.Groth/ShortNIZK.pdf) - Groth10
  - [Succinct NIZK without PCP Theorem & Quasi-linear prover time](https://eprint.iacr.org/2012/215.pdf) - GGPR13
  - [Verifiable Delay Function](https://eprint.iacr.org/2018/601.pdf)

## Layer 2

- [An Incomplete Guide to Rollups](https://vitalik.ca/general/2021/01/05/rollup.html)
- [Why rollups + data shards are the only sustainable solution for high scalability](https://polynya.medium.com/why-rollups-data-shards-are-the-only-sustainable-solution-for-high-scalability-c9aabd6fbb48)
- [Introducing zkSync: the missing link to mass adoption of Ethereum](https://medium.com/matter-labs/introducing-zk-sync-the-missing-link-to-mass-adoption-of-ethereum-14c9cea83f58)
- [Validity Proofs vs. Fraud Proofs](https://starkware.medium.com/validity-proofs-vs-fraud-proofs-4ef8b4d3d87a)
- [A Pre-consensus Mechanism by Leohio](https://ethresear.ch/t/a-pre-consensus-mechanism-to-secure-instant-finality-and-long-interval-in-zkrollup/8749)

## Projects

### Zk-VM

- [Matter Labs zkEVM](https://blog.matter-labs.io/unisync-a-port-of-uniswap-v2-on-the-zkevm-b12954748504)
- [Hermez zkEVM](https://blog.hermez.io/introducing-hermez-zkevm/)
- [Mir Protocol](https://mirprotocol.org/blog/Introducing-Mir)
- [Scroll](https://hackmd.io/@yezhang/S1sJ2cEWY)
  - [zkEVM](https://hackmd.io/@yezhang/S1_KMMbGt)
- [Sin7Y zkEVM](https://medium.com/@sin7y)
- [zCloak Space](https://zcloak.network/#/)
- [Circuits for zkEVM](https://github.com/appliedzkp/zkevm-circuits)

### Zk-Layer1

- [Aleo: A SDK for Zero-Knowledge Transactions](https://github.com/AleoHQ/aleo)
- [Iron Fish: the universal privacy layer for crypto](https://ironfish.network/)

### Zk-Layer2

- [Aztec: Scalable Privacy on Ethereum](https://aztec.network/)
- [StarkNet](https://starkware.co/starknet/)
- [Polygon Miden](https://polygon.technology/solutions/polygon-miden/)
- [Polygon Zero](https://polygon.technology/solutions/polygon-zero/)

### Basic Computing

- [Risc0: a zero-knowledge verifiable general computing platform](https://github.com/risc0/risc0)

### Framework / SDK

- [Espresso Systems](http://espressosys.com)

### Zk-Applications

#### Gaming

- [Dark Forest: an MMO space-conquest game](https://blog.zkga.me/announcing-darkforest) and their [ZK Circuit Walkthrough](https://blog.zkga.me/df-init-circuit)

#### Payment

- [Zcash: a privacy-protecting, digital currency](https://z.cash/technology/)
- [Monero: private, decentralized cryptocurrency](https://www.getmonero.org/)
- [Manta: a Plug and Play Private DeFi Stack](https://www.manta.network/) 
- [Mina: a payment system using a succinct blockchain](https://minaprotocol.com/wp-content/uploads/technicalWhitepaper.pdf)
- [SwapCT: Swap Confidential Transactions for Privacy-Preserving Multi-Token Exchanges](https://eprint.iacr.org/2021/631.pdf)
- [Zef: Low-latency, Scalable, Private Payments](https://zefchain.com/) and their [Slides](https://zefchain.com/papers/zef_slides.pdf)

#### Mixer

- [CoinJoin: an open-source way to mix bitcoins](https://coinjoin.io/en)
- [Tornado Cash: Introducing Private Transactions On Ethereum](https://tornado-cash.medium.com/introducing-private-transactions-on-ethereum-now-69fb059a14a1)

#### Identity

- [zkKYC](https://eprint.iacr.org/2021/907.pdf)
- [zCloak: DeFi KYC Gateway](https://app.zcloak.network/#/transfer)
- [Iden3: future-proof tech stack for self-sovereign identity](https://iden3.io/)
- [Polygon ID: identity system with programmable privacy](https://polygon.technology/polygon-id/)

#### Wallet

- [Argent (based on zkSync)](https://www.argent.xyz/)

#### Crosschain

- [ZkLink: cross chain amm swap protocol powered by ZK-Rollup](https://github.com/zkLinkProtocol/zklink-contracts)
- [Mystiko Network: Anonymous Protocol for a Cross-Chain Network](https://mystiko.network/whitepaper.pdf)
- [Penumbra: a shielded, cross-chain network](https://penumbra.zone/)
- [Zecrey: Bringing Cross-chain Privacy to Digital Assets](https://www.zecrey.com/)
- [Suez: move Eth to the Starknet ecosystem](https://suez.dev/)
- [ZKCross: a trustworthy cross-chain protocol built with multichain zkRollup](https://www.zkcross.org/)

#### Marketplace

- [Modulo Zero: on-chain solution for private data exchange](https://modulozero.xyz/) and their [Repo](https://github.com/nulven/EthDataMarketplace)

#### DeFi / DEX

- [Panther Protocol](https://www.pantherprotocol.io/resources/panther-protocol-v-1-0-1.pdf)
- [Loopring Launches zkRollup Exchange](https://medium.com/loopring-protocol/loopring-launches-zkrollup-exchange-loopring-io-d6a85beeed21)
- [Railgun: brings privacy to cryptocurrencies](https://www.railgun.org/#/)

#### Tokens / NFT

- [StealthDrop: Anonymous Airdrops using ZK proofs](https://github.com/nalinbhardwaj/stealthdrop)
- [ZKP Private Airdrop](https://github.com/a16z/zkp-merkle-airdrop-contracts) and their [Zk Merkle Airdrop Library](https://github.com/a16z/zkp-merkle-airdrop-lib)
- [Immutable X: the first layer-2 scaling solution for NFTs on Ethereum](https://www.immutable.com/)

#### Voting / Participation

- [Zero Knowledge Message Board by Nulven](https://github.com/nulven/zk-polling)
- [Semaphore: a privacy gadget built on Ethereum](https://medium.com/coinmonks/to-mixers-and-beyond-presenting-semaphore-a-privacy-gadget-built-on-ethereum-4c8b00857c9b)

### Hardware Acceleration

- [Hardware for ZKPs & VDFs with Supranational](https://www.supranational.net/)
  - [Practical SNARK-based VDF](https://zkproof.org/2021/11/24/practical-snark-based-vdf/)

### Trusted Execution Environment (TEE) Based Projects
- [Oasis Network](https://oasisprotocol.org/)
- [Secret Network](https://scrt.network/)

## Advanced Topics

### PLONK

- [Understanding PLONK](https://vitalik.ca/general/2019/09/22/plonk.html)
- [Permutations over Lagrange-bases for Oecumenical Noninteractive arguments of Knowledge](https://eprint.iacr.org/2019/953.pdf)

### Groth16

- [On the Size of Pairing-based Non-interactive Arguments](https://eprint.iacr.org/2016/260.pdf)

### Halo

- [Vitalik Buterin: Halo and more: exploring incremental verification and SNARKs without pairings](https://vitalik.ca/general/2021/11/05/halo.html) - Proof size reduction
- [Recursive Proof Composition without a Trusted Setup](https://eprint.iacr.org/2019/1021.pdf)

### Probabilistic Proof Systems

- [Georgetown University COSC 544 Class Notes](https://people.cs.georgetown.edu/jthaler/COSC544.html)

### Pinocchio

- [Pinocchio: Nearly Practical Verifiable Computation](https://eprint.iacr.org/2013/279.pdf)

### Bulletproofs

- [Bulletproofs: Short Proofs for Confidential Transactions and More](https://eprint.iacr.org/2017/1066.pdf)
- [Bulletproofs+: Shorter Proofs for Privacy-Enhanced Distributed Ledger](https://eprint.iacr.org/2020/735)

### Hash Functions

- [POSEIDON: A New Hash Function for Zero-Knowledge Proof Systems](https://eprint.iacr.org/2019/458.pdf)

### Systems

- [SNARKs for C: Verifying Program Executions Succinctly and in Zero Knowledge](https://eprint.iacr.org/2013/507.pdf)

### Quadratic Span Programs

- [Quadratic Span Programs and Succinct NIZKs without PCPs](https://eprint.iacr.org/2012/215.pdf)

### Zether

- [Zether: Towards Privacy in a Smart Contract World](https://eprint.iacr.org/2019/191.pdf)

### Anonymous Zether

- [MANY-OUT-OF-MANY PROOFS](https://eprint.iacr.org/2020/293.pdf)

### Quisquis

- [Quisquis: A New Design for Anonymous Cryptocurrencies](https://eprint.iacr.org/2018/990.pdf)

### Zk-VM

- [ZKVM book](https://hackmd.io/@liangcc/zkvmbook)
- [Introduction to zkEVM](https://hackmd.io/@yezhang/S1_KMMbGt)

### Slush: Fractal Scaling

- [Slush, a proposal for Fractal scaling](https://hackmd.io/@kalmanlajko/rkgg9GLG5#Our-trustless-bridging)

## Tools

- [Circom](https://docs.circom.io/getting-started/installation/)
- [Library: ZK-Garage/Plonk](https://github.com/ZK-Garage/plonk)

## Auditing and Consulting

- [ABDK](https://www.abdk.consulting/)
- [Least Authority](https://leastauthority.com/)

## Discussions

- [Why Dark Forest Matters: A Good Game, not a Crypto Game](https://mirror.xyz/omarmezenner.eth/gFCfCVwTfUU91SDXeROEaDQe4984nbFBIgv9QSY0r1U)
- [Six Moonshot ZK Applications](https://gubsheep.substack.com/p/six-moonshot-zk-applications?s=r)
- [The Strongest Crypto Gaming Thesis](https://gubsheep.substack.com/p/the-strongest-crypto-gaming-thesis?s=r)
- [Hardware Acceleration for Zero Knowledge Proofs](https://www.paradigm.xyz/2022/04/zk-hardware)
- [How do trusted setups work?](https://vitalik.ca/general/2022/03/14/trustedsetup.html)

## Communities

- [Harmony zkDAO](https://harmonyone.notion.site/zkDAO-Succinct-Private-Fair-2f14d3d954264bd38091b418fd6b9bd5)
- [Zero Knowledge University](https://zku.one/)
- [ZK Hash Bounties](https://www.zkhashbounties.info/)
- [Zero Knowledge Forum](https://zeroknowledge.fm/)
- [0xPARC: Program for Applied Research in Cryptography](https://0xparc.org/blog/program-for-applied-research)
- [ZPrize: accelerate zero-knowledge cryptography](https://www.zprize.io/)
- [zkMesh: a monthly newsletter](https://zkmesh.substack.com/)