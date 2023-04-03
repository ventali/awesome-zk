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

  <p align="center">A curated list of awesome ZK resources, libraries, tools and more. For a ZK knowledge base, please see https://github.com/delendum-xyz/zk-knowledge </p>
</div>

### Telegram Group
Join the discussion [group chat](https://t.me/+9WAAmCpPRadjOTNh) with other developers and researchers

### Fellowship Program
If you are interested in working together with top experts to explore practical use cases of new research ideas, consider applying to our [fellowship program](https://delendum.xyz/fellow). The deadline for 2023 fellowship 2 application is March 15.

Table of Contents
=================

* [Basics](#basics)
  * [Mathematical Foundations](#mathematical-foundations)
* [Projects](#projects)
  * [Zk\-VM](#zk-vm)
  * [Zk\-Layer1](#zk-layer1)
  * [Zk\-Layer2](#zk-layer2)
  * [Transpiler](#transpiler)
  * [Computing Infrastructure](#computing-infrastructure)
  * [Framework / SDK](#framework--sdk)
  * [Zk\-Applications](#zk-applications)
  * [Hardware Acceleration](#hardware-acceleration)
  * [TEE Based Projects](#trusted-execution-environment-tee-based-projects)
* [Programming Languages](#programming-languages)
* [Programming Libraries](#programming-libraries)
* [Developer Tools](#tools)
* [Auditing and Consulting](#auditing-and-consulting)
* [Validator Services](#validator-services)
* [Books](#books)
* [Discussions](#discussions)
* [Communities](#communities)
* [Advanced Topics](#advanced-topics)

## Basics

- [Prerequisite understanding questions](https://0xparc.notion.site/Prerequisite-understanding-questions-c5ebb77a5cc049f39577ec9a7fb7b22c)
- [ZKP Overview: History, Proving Systems, Circuits, Compilers](https://zkp.science)
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
  - [Brainfuck STARK Tutorial](https://neptune.cash/learn/brainfuck-tutorial/)
- [zkSNARKs in a nutshell](https://blog.ethereum.org/2016/12/05/zksnarks-in-a-nutshell/)
- [The MoonMath Manual to zk-SNARKs](https://leastauthority.com/community-matters/moonmath-manual/)
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
- Circuit optimization
  - [Circuit Optimisation Handout](https://docs.google.com/document/d/1aZ1GUAJOBFuqD4GOo9HqAH8w4xJo7HM4Bjte5-wkdnU/edit)
- Introduction to Layer 2
  - [An Incomplete Guide to Rollups](https://vitalik.ca/general/2021/01/05/rollup.html)
  - [Why rollups + data shards are the only sustainable solution for high scalability](https://polynya.medium.com/why-rollups-data-shards-are-the-only-sustainable-solution-for-high-scalability-c9aabd6fbb48)
  - [Introducing zkSync: the missing link to mass adoption of Ethereum](https://medium.com/matter-labs/introducing-zk-sync-the-missing-link-to-mass-adoption-of-ethereum-14c9cea83f58)
  - [Validity Proofs vs. Fraud Proofs](https://starkware.medium.com/validity-proofs-vs-fraud-proofs-4ef8b4d3d87a)
  - [A Pre-consensus Mechanism by Leohio](https://ethresear.ch/t/a-pre-consensus-mechanism-to-secure-instant-finality-and-long-interval-in-zkrollup/8749)

### Mathematical Foundations

- [Introduction to Mathematical Cryptography](https://github.com/isislovecruft/library--/blob/master/cryptography%20%26%20mathematics/An%20Introduction%20to%20Mathematical%20Cryptography%20(2014)%20-%20Hoffstein%2C%20Pipher%2C%20Silverman.pdf)
- [Modern Computer Algebra](https://maths-people.anu.edu.au/~brent/pd/mca-cup-0.5.9.pdf)
- [Explicit-Formulas Database](http://hyperelliptic.org/EFD/)
- [Abstract Algebra](http://abstract.ups.edu/download/aata-20220728.pdf)
- [Algebraic Number Theory](https://kashanu.ac.ir/Files/Content/ANT.pdf)
- [Computational Introduction to Number Theory and Algebra](https://shoup.net/ntb/ntb-v2.pdf)
- [A Graduate Course in Applied Cryptography](https://crypto.stanford.edu/~dabo/cryptobook/BonehShoup_0_4.pdf)
- [Lattice Cryptography](https://eprint.iacr.org/2015/939.pdf)
- [The Design of Rijndael](https://cs.ru.nl/~joan/papers/JDA_VRI_Rijndael_2002.pdf)

More specific to ZK:

- [Elliptic Curves Number Theory And Cryptography](https://people.cs.nctu.edu.tw/~rjchen/ECC2012S/Elliptic%20Curves%20Number%20Theory%20And%20Cryptography%202n.pdf)
- [Pairings for Beginners](https://static1.squarespace.com/static/5fdbb09f31d71c1227082339/t/5ff394720493bd28278889c6/1609798774687/PairingsForBeginners.pdf)
- [Proofs, Arguments, and Zero-Knowledge](https://people.cs.georgetown.edu/jthaler/ProofsArgsAndZK.pdf)

## Projects

### Zk-EVM

- [Matter Labs zkEVM](https://blog.matter-labs.io/unisync-a-port-of-uniswap-v2-on-the-zkevm-b12954748504)
- [Hermez zkEVM](https://blog.hermez.io/introducing-hermez-zkevm/)
- [Scroll](https://hackmd.io/@yezhang/S1sJ2cEWY) and their [zkEVM](https://hackmd.io/@yezhang/S1_KMMbGt)
- [Appliedzkp: Circuits for zkEVM](https://github.com/appliedzkp/zkevm-circuits)
- [ConsenSys zkEVM](https://ethresear.ch/uploads/short-url/3DM8kjFfIG6PHXu4qpYpmujXgme.pdf) and their [gnark library](https://github.com/consensys/gnark)
- [TinyZKEVM](https://github.com/leonardoalt/tinyzkevm)
- [Sovereign Labs: zkEVM on Risc0](https://github.com/Sovereign-Labs/ethereum-vpm)

### Zk-VM

- [zCloak Space](https://zcloak.network/#/)
- [Delphinus zkWASM](https://delphinuslab.com/zk-wasm/) and their [github](https://github.com/DelphinusLab/zkWasm)
- [zkMove: bytecode VM](https://www.zkmove.net/) and their [github](https://github.com/young-rocks/zkmove)
- [zkRiscV: RV32I Risc-V instruction set](https://github.com/lucasgleba/zkRiscV)
- [OlaVM: An Ethereum compatible ZKVM](https://olavm.org/)
- [Tritron VM](https://github.com/TritonVM/triton-vm)
- [Risc0: a general purpose zkVM](https://github.com/risc0/risc0)
- [Miden: zero-knowledge virtual machine written in Rust](https://github.com/0xPolygonMiden/miden-vm)

#### Benchmarking

- [ZK System Benchmarking: compare the performance of different zero-knowledge proof libraries](https://github.com/delendum-xyz/zk-benchmarking)

### Zk-Layer1

- [Mir Protocol](https://mirprotocol.org/blog/Introducing-Mir)
- [Aleo: A SDK for Zero-Knowledge Transactions](https://github.com/AleoHQ/aleo)
- [Iron Fish: the universal privacy layer for crypto](https://ironfish.network/)
- [Mina: a payment system using a succinct blockchain](https://minaprotocol.com/wp-content/uploads/technicalWhitepaper.pdf)
- [Celo: EVM compatible proof-of-stake layer-1](https://celo.org/) and their [Light clients with ZKPs](https://zeroknowledge.fm/93-2/)
- [Zeeka Network: a light and scalable blockchain using ZKPs](https://hackmd.io/_Sw5u2lUR9GfBV5vwtoMSQ#Zeeka-Network---Whitepaper)
- [quark: decentralized state machine with STARK proofs](https://github.com/liamzebedee/quark-blockchain/blob/master/whitepaper.md)
- [Lelantus: transaction confidentiality and anonymity](https://lelantus.io)
- [Neptune: a new privacy layer-one blockchain](https://neptune.cash/)
- [DarkFi: a new Layer 1 blockchain, designed with anonymity at the forefront](https://dark.fi)
- [Espresso Systems: single-shot scaling & privacy solution](http://espressosys.com)

### Zk-Layer2

- [Aztec: Scalable Privacy on Ethereum](https://aztec.network/)
- [StarkNet: permissionless decentralized ZK-Rollup](https://starkware.co/starknet/)
- [Scroll: an EVM-equivalent zkRollup](https://scroll.io/)
- [zkSync: an EVM-compatible ZK Rollup](https://zksync.io)
- [Polygon Zero: a layer 2 scaling solution for Ethereum](https://polygon.technology/solutions/polygon-zero/)
- [Polygon Miden: a STARK-based, Zero-Knowledge rollup](https://polygon.technology/solutions/polygon-miden/)
- [Taikocha: a zkEVM-based general-purpose zkRollup network](https://taikocha.in/)
- [Twilight: Layer 2 for Private Computation](https://twilight.finance/)
- [Orbis: A Layer 2 ZK-Rollup Scaling Solution Built on Cardano](https://linktr.ee/orbisprotocol)
- [Radius: MEV-resistant ZK-Rollups with Practical VDE (PVDE)](https://ethresear.ch/t/mev-resistant-zk-rollups-with-practical-vde-pvde/12677)
- [ZEXE on Plasma: An implementation of ZEXE on Ethereum](https://devpost.com/software/zexe-on-ethereum)
- [Nightfall: Private Token Transaction on Ethereum](https://github.com/EYBlockchain/nightfall/blob/master/doc/whitepaper/nightfall-v1.pdf)

### Privacy Layer

- [Light Protocol: DeFi Privacy Infrastructure on Solana](https://www.lightprotocol.com/)

### Transpiler

- [Starlight: Generate a zApp from a Solidity contract](https://github.com/EYBlockchain/starlight/blob/master/doc/WRITEUP.md)
- [Warp: transpile Ethereum smart contracts to Cairo](https://github.com/NethermindEth/warp)
- [zkay: A Language for Private Smart Contracts on Ethereum](https://github.com/eth-sri/zkay)

### Computing Infrastructure

- [=nil;'s zkLLVM: LLVM-based zero-knowledge proof systems compiler](https://github.com/nilfoundation/zkllvm)
- [CirC: Compiler Infrastructure for Cryptosystems and Verification](https://github.com/circify/circ)
- [Trustless Labs: ZK-friendly Multi-rollup Architecture for Web3 Applications](https://trustless.org/)

### Framework / SDK

- [Adapt Framework: a toolkit for building end-to-end decentralized systems](https://www.adaptframework.solutions)
- [Atlas Protocol: Zero-Knowlege Blockchain Development Platform](http://atlaszk.com/ide)

### Zk-Applications

#### Gaming

- [Dark Forest: an MMO space-conquest game](https://blog.zkga.me/announcing-darkforest) and their [ZK Circuit Walkthrough](https://blog.zkga.me/df-init-circuit)
- [Isaac: a physics-powered onchain reality on Starknet](https://topology.gg/) and their [blog](https://www.guiltygyoza.xyz/2022/05/topology-isaac-defcon)
- [Crypto Maze: action-packed MMO](https://www.cryptomaze.app/)
- [Zordle: the first end-to-end web app built using Halo 2 ZK proofs](https://github.com/nalinbhardwaj/zordle)
- [zkSNARK-Sudoku: Sudoku verifier using zkSNARK and circom.](https://github.com/web3-master/zksnark-sudoku)
- [Leela vs the World: the first zkAI game](https://twitter.com/VsLeela)

#### Payment

- [Zcash: a privacy-protecting, digital currency](https://z.cash/technology/)
- [Monero: private, decentralized cryptocurrency](https://www.getmonero.org/)
- [Manta: a Plug and Play Private DeFi Stack](https://www.manta.network/) 
- [SwapCT: Swap Confidential Transactions for Privacy-Preserving Multi-Token Exchanges](https://eprint.iacr.org/2021/631.pdf)
- [Zef: Low-latency, Scalable, Private Payments](https://zefchain.com/) and their [Slides](https://zefchain.com/papers/zef_slides.pdf)
- [Anoma: A protocol for private, asset-agnostic digital cash](https://anoma.net/) and their [use of recursive zkps](https://anoma.net/blog/demystifying-recursive-zkp/)
- [ZETH: Integrating Zerocash on Ethereum](https://github.com/clearmatics/zeth)

#### Mixer

- [CoinJoin: an open-source way to mix bitcoins](https://coinjoin.io/en)
- [Tornado Cash: Introducing Private Transactions On Ethereum](https://tornado-cash.medium.com/introducing-private-transactions-on-ethereum-now-69fb059a14a1)
- [Otter Cash: A privacy layer for the Solana ecosystem](https://otter.cash/)
- [Mobius: Trustless Tumbling for Transaction Privacy](https://eprint.iacr.org/2017/881.pdf)
- [TumbleBit: An Untrusted Bitcoin-Compatible Anonymous Payment Hub](https://eprint.iacr.org/2016/575)
- [Mixcoin: Anonymity for Bitcoin with accountable mixes](https://eprint.iacr.org/2014/077.pdf)
- [CashShuffle: background coin shuffling for Bitcoin Cash](https://cashshuffle.com)
- [MicroMix: A noncustodial Ethereum mixer](https://github.com/privacy-scaling-explorations/mixer)
- [Juicer Protocol: trusted and secure ](https://github.com/wasmjuicer/juicer)

#### Identity

- [zkKYC: A solution concept for KYC without knowing your customer](https://eprint.iacr.org/2021/907.pdf)
- [zkID.app: A Privacy-Preserving Passport to the Web 3.0 World](https://zkid.app/)
- [Notebook: a zero-knowledge B2B2C identity protocol](https://notebook-6.gitbook.io/notebook-docs-1.0/)
- [Iden3: future-proof tech stack for self-sovereign identity](https://iden3.io/)
- [Polygon ID: identity system with programmable privacy](https://polygon.technology/polygon-id/)
- [Sealance: building financial compliance into digital currencies](https://www.sealance.io/)
- [Humanode: biologically verified human nodes for a fair financial system](https://humanode.io/)
- [OutDID: your zero-knowledge, decentralized KYC filter of blockchain users](https://www.outdid.io/)
- [IdentityBlockchain: state-certified electronic identities to establish blockchain identities](https://github.com/IdentityBlockchain)
- [Worldcoin: Privacy-Preserving Proof-of-Personhood Protocol](https://worldcoin.org/)
- [ZeroBiometrics: Privacy Preserving and Data Protection Face Authentication](https://zerobiometrics.com/)

#### Wallet

- [Argent: smart contract wallet based on zkSync](https://www.argent.xyz/)
- [Numio: Layer 2 focused wallet built on zkSync](https://www.numio.one/)
- [Zkopru: Affordable Ethereum Privacy Wallet](https://zkopru.network/)
- [Bunkyr: zero‑knowledge security without seed phrases or backup codes](https://bunkyr.com/)
- [Wasabi Wallet: non-custodial, privacy-focused Bitcoin wallet](https://wasabiwallet.io)

#### Trustless Bridge

- [=nil; Foundation's Solana and Mina to Ethereum zkBridge](https://nil.foundation)
- [Succinct Labs: the trust-minimized interoperability layer](https://www.succinct.xyz/)
- [Overeality: Infrastructure for Web3 Interoperability](https://overeality.io/home) and their [paper](https://overeality.io/zkBridge.pdf)

#### Crosschain

- [ZkLink: cross chain amm swap protocol powered by ZK-Rollup](https://github.com/zkLinkProtocol/zklink-contracts)
- [Mystiko Network: Anonymous Protocol for a Cross-Chain Network](https://mystiko.network/whitepaper.pdf)
- [Penumbra: a shielded, cross-chain network](https://penumbra.zone/)
- [Zecrey: Bringing Cross-chain Privacy to Digital Assets](https://www.zecrey.com/)
- [Suez: move Eth to the Starknet ecosystem](https://suez.dev/)
- [ZKCross: a trustworthy cross-chain protocol built with multichain zkRollup](https://www.zkcross.org/)
- [Electron Labs: ZK Light Clients for NEAR Rainbow Bridge](https://electronlabs.org/)
- [ZeroPool: a fully private multi-blockchain solution](https://zeropool.network/)
- [Raze Network: Multichain Privacy Middleware](https://www.raze.network/)
- [Zendoo: A zk-SNARK enabled verifiable cross-chain transfer protocol](https://www.horizen.io/zendoo/) and their [whitepaper](https://www.horizen.io/assets/files/Horizen-Sidechain-Zendoo-A_zk-SNARK-Verifiable-Cross-Chain-Transfer-Protocol.pdf)
- [DarkFi: applications and shielded cross-chain assets utilizing Halo 2](https://darkrenaissance.github.io/darkfi/architecture/overview.html)

#### Marketplace

- [=nil; Foundation's Proof Market: a decentralized proof market protocol](https://proof.market.nil.foundation)
- [Modulo Zero: on-chain solution for private data exchange](https://modulozero.xyz/) and their [Repo](https://github.com/nulven/EthDataMarketplace)
- [Ruby Protocol: Building a Cross-chain Cryptographic Infrastructure for Data Monetization](https://wiki.ruby.io/)
- [zkPoD: A decentralized system for data exchange](https://github.com/sec-bit/zkPoD-node)

#### Fiat On-ramp

- [Ladder: KYC on-ramp solution implementing an oraclized peer-to-peer protocol](https://www.ladderpay.xyz/)

#### User Profiling

- [FirstBatch: create a representation of your identity from your social data](https://firstbatch.xyz/)
- [Interep: verify users' reputation without exposing their identities](https://github.com/interep-project)

#### Data Infrastructure

- [=nil; \`DROP DATABASE \*: A database management system for blockchains enhanced by provable SQL](https://dbms.nil.foundation)
- [Filecoin: Zero Knowledge and the Filecoin Network](https://filecoin.io/blog/posts/zero-knowledge-and-the-filecoin-network/)
- [Nectar Protocol: Web3 infrastructure for healthcare](https://nectar.haus/) and their [documentation](https://github.com/NectarProtocol/documentation)
- [zk-SQL: ZK-based engine for self-sovereign SQL queries](https://github.com/timoth-y/zk-SQL)

#### State Attestation

- [Relic Protocol: the first provably secure source of historical data on chain](https://relicprotocol.com/)
- [Axiom: generate proofs for various computations completed previously on chain](https://www.axiomcrypto.xyz/)

#### Machine Learning

- [zk-MNIST: web frontend app + Jupyter notebook with ML model generation](https://github.com/0xZKML/zk-mnist) and their [demo](https://zkmnist.netlify.app/)
- [zkCNN: GKR-based zero-knowledge proof protocol for CNN model inference](https://github.com/TAMUCrypto/zkCNN) and their [paper](https://eprint.iacr.org/2021/673.pdf)
- [Modulus Labs: bringing powerful ML models on-chain](https://www.moduluslabs.xyz/) and their [blogs](https://medium.com/@ModulusLabs)
- [zkonduit: inference for deep learning models and other computational graphs in a zk-snark](https://github.com/zkonduit/ezkl)
- [ZK Machine Learning: truly private machine learning, with zk-SNARKs and blockchain](https://github.com/zk-ml/demo)

#### DeFi / DEX

- [Panther Protocol](https://www.pantherprotocol.io/resources/panther-protocol-v-1-0-1.pdf)
- [Loopring Launches zkRollup Exchange](https://medium.com/loopring-protocol/loopring-launches-zkrollup-exchange-loopring-io-d6a85beeed21)
- [Railgun: brings privacy to cryptocurrencies](https://www.railgun.org/#/)
- [EdgeSwap: Ethereum-based layer 2 trading protocol](https://www.edgeswap.io/)
- [ZigZag: ZK Rollup order book DEX](https://docs.zigzag.exchange/)
- [Mute: a ZK-Rollup based AMM exchange](https://mute.io/)

#### Tokens / NFT

- [StealthDrop: Anonymous Airdrops using ZK proofs](https://github.com/nalinbhardwaj/stealthdrop)
- [ZKP Private Airdrop](https://github.com/a16z/zkp-merkle-airdrop-contracts) and their [Zk Merkle Airdrop Library](https://github.com/a16z/zkp-merkle-airdrop-lib)
- [zk-NftMint: Mint an NFT if you know a secret](https://github.com/weijiekoh/zknftmint) and their [contract](https://goerli.etherscan.io/address/0xc4490d6407f81378c8d3620eA11092B2FC429Df2)
- [Immutable X: the first layer-2 scaling solution for NFTs on Ethereum](https://www.immutable.com/)

#### Voting / Participation

- [Semaphore: a privacy gadget built on Ethereum](https://medium.com/coinmonks/to-mixers-and-beyond-presenting-semaphore-a-privacy-gadget-built-on-ethereum-4c8b00857c9b)
- [zkC.R.E.A.M: Confidential Reliable Ethereum Anonymous Mixer](https://zkcre.am/)
- [Cabal: create credibly pseudonymous channels based on members' Ethereum activity](https://www.cabal.xyz/)
- [OVOTE: Offchain Voting with Onchain Trustless Execution](https://forum.aragon.org/t/we-present-ovote-offchain-voting-with-onchain-trustless-execution/3603) and their [document](https://forum.aragon.org/t/we-present-ovote-offchain-voting-with-onchain-trustless-execution/3603)
- [Scaffold-ETH: Prove Membership with Circom and Zero Knowledge](https://github.com/scaffold-eth/scaffold-eth-examples/tree/zk-prove-membership)
- [Vocdoni: A decentralized self sovereign governance platform](https://docs.vocdoni.io/) and their [architecture](https://docs.vocdoni.io/architecture/general.html)

#### Communication

- [Waku: a suite of privacy-preserving, peer-to-peer messaging protocols](https://waku.org)
- [Zero Knowledge Message Board by nulven, yush\_g](https://github.com/nulven/zk-message-board) and their [article](https://mirror.xyz/0x3FD6f213ae1B8a7B6bd8f14BE9BF316a5e5A5d28/VTGpmEYLKIslUPf66VQzHUneB0R7EhMpJJ_mGrMvTwY)
- [Double Blind: semi-anonymously sign messages for a group of people](https://github.com/doubleblind-xyz/double-blind) and their [documentation](https://double-blind.xyz/docs/#/)

#### Document Management

- [zkDocs: information attestation and verification workflows](https://github.com/a16z/zkdocs)

### Hardware Acceleration

- [Hardware for ZKPs & VDFs with Supranational](https://www.supranational.net/) and their [Practical SNARK-based VDF](https://zkproof.org/2021/11/24/practical-snark-based-vdf/)
- [PipeZK: Accelerating Zero-Knowledge Proof with a Pipelined Architecture](https://www.microsoft.com/en-us/research/uploads/prod/2021/05/isca21_pizk-60a269dbb1310.pdf)
- [Ingonyama: building a ZK processing unit](https://www.ingonyama.com/) and their [slides](https://drive.google.com/file/d/1VfLrC6CQinM3DCVfaAu_5qTOoc5eigue/view)
- [ZKAccel: Accelerated ZKP as a Service](https://inaccel.com/)
- [DZK: decentralized zero-knowledge proof platform](https://dzk.org/)
- [Cysic: Hardware Accelerating Zero-Knowledge Proof](https://cysic.xyz)

### Trusted Execution Environment (TEE) Based Projects

- [Oasis Network](https://oasisprotocol.org/)
- [Secret Network](https://scrt.network/)
- [Obscuro](https://www.obscu.ro/)
- [Phala](https://www.phala.network/en/)

### Fully Homomorphic Encryption (FHE) Based Projects

- [Zama](https://www.zama.ai/)

## Programming Languages 

| Name  | Ecosystem | Type | GitHub | Documentation | 
| ------------- |:-------------:|:-------------:|:-------------:|:-------------:|
| Cairo     | StarkNet    | STARK-provable programs for general computation  | https://github.com/starkware-libs/cairo-lang | https://cairo-lang.org/docs/ | 
| ZoKrates     | Python subset   | R1CS SNARKs Frontend | https://github.com/Zokrates/ZoKrates | https://zokrates.github.io |
| Leo      | Aleo     | Functional, statically-typed  | https://github.com/AleoHQ/leo | https://developer.aleo.org/developer/language/layout/ |
| Circom | Typed JS | Circuit compiler   | https://github.com/iden3/circom | https://docs.circom.io |
| Noir | Aztec | Private contract language  | https://github.com/noir-lang/noir | https://noir-lang.github.io/book/index.html
| Snarky | Mina | R1CS SNARKs OCaml frontend | https://github.com/o1-labs/snarky | / | 
| Zinc | zkSync | Turing-complete smart contract | https://github.com/matter-labs/zinc | / | 
| Juxiv | Anoma | Functional | https://github.com/anoma/juvix | https://juvix.readthedocs.io/en/latest/index.html | 
| ZKPDL | / | High-level | https://github.com/brownie/cashlib | http://cs.brown.edu/research/brownie/usenix10.pdf |
| zkVM | / | Stack machine with a string of bytecode representing ZkVM instructions | https://github.com/stellar/slingshot/tree/main/zkvm | https://github.com/stellar/slingshot/files/3164245/zkvm-whitepaper-2019-05-09.pdf | 
| lurk | Protocol Labs | Lurk is a statically scoped dialect of Lisp, influenced by Scheme and Common Lisp | https://github.com/lurk-lang/lurk-rs | https://github.com/lurk-lang/lurk/blob/master/spec/v0-1.md |

## Programming Libraries 

| Name  | Host Language | Features | GitHub |
| ------------- |:-------------:|:-------------:|:-------------:|
| Libsnark     | C++    | General-purpose proof systems, gadget libraries | https://github.com/scipr-lab/libsnark |
| Bulletproofs | Rust | Single-party proofs, online multi-party computation, R1CS  | https://github.com/dalek-cryptography/bulletproofs |
| Bellman     | Rust   | Circuit traits, primitive structures, basic gadget implementations | https://github.com/zkcrypto/bellman |
| gnark      | Go     | High level API with frontend and backend to design circuits | https://github.com/ConsenSys/gnark | 
| Arkworks | Rust | R1CS, curves, Groth16, finite field, curves | https://github.com/arkworks-rs | 
| Circomlib | Javascript | Circom templates | https://github.com/iden3/circomlib |
| libSTARK | C++ | ZK-STARK library | https://github.com/elibensasson/libSTARK | 
| plonky2 | rust | SNARK implementation based on techniques from PLONK and FRI | https://github.com/mir-protocol/plonky2 |
| plonk | rust | Pure Rust implementation of the PLONK ZKProof System | https://github.com/dusk-network/plonk |
| Spartan | rust | High-speed zkSNARKs without trusted setup | https://github.com/microsoft/Spartan |
| DIZK | Java | Distributed polynomial interpolation, Lagrange polynomials, multi-scalar multiplication | https://github.com/scipr-lab/dizk | 
| wasmsnark | Javascript | Generate zkSnark proofs and verify from web browser | https://github.com/iden3/wasmsnark | 
| jellyfish | rust | Rust Implementation of the PLONK ZKP System and Extensions | https://github.com/EspressoSystems/jellyfish |
| libiop | C++ | IOP-based zkSNARKs | https://github.com/scipr-lab/libiop | 
| Nova | rust | Recursive SNARKs without trusted setup | https://github.com/microsoft/Nova |
| plonky3 | rust | a toolkit for implementing polynomial IOPs (PIOPs), such as PLONK and STARKs | https://github.com/Plonky3/Plonky3 |

## Tools

### Plonk

- [plonkit: zkSNARK toolkit to work with circom DSL in PLONK proof system](https://github.com/fluidex/plonkit)
- [Plonk: A pure Rust PLONK implementation](https://github.com/ZK-Garage/plonk)

### ECDSA

- [zk-ECDSA: zkSNARKs for ECDSA](https://0xparc.org/blog/zk-ecdsa-1)

### Circuit Building Library

- [Circom: zkSnark circuit compiler](https://github.com/iden3/circom)
- [Arkworks: an ecosystem for developing with zkSNARKs](https://github.com/arkworks-rs)
- [ZoKrates: a toolbox for zkSNARKs on Ethereum](https://zokrates.github.io/)
- [Snarkjs: zkSNARK implementation in JavaScript & WASM](https://github.com/iden3/snarkjs)
- [RCC: Rust Circuit Compiler](https://github.com/delendum-xyz/rcc)

### Formal Verification

- [The State of Current Progress](https://delendum.xyz/2022/09/04/formal-verification-zk-constraint-systems.html#the-state-of-current-progress)
- [Ecne: an engine for verifying the soundness of R1CS constraints](https://github.com/franklynwang/EcneProject)
- [Picus: Symbolic Virtual Machine for Automated R1CS Verification](https://github.com/Veridise/Picus)
- [Papyrus: A Symbolic Execution Tool for Cairo](https://github.com/Veridise/Papyrus)

### Other Tools

- [zkREPL: an in-browser collaborative development environment](https://zkrepl.dev/)
- [crrl: Rust library for cryptographic research](https://github.com/pornin/crrl)
- [Shield: a development framework for circom developers](https://xord.notion.site/SHIELD-5306223ca4f745d19f54b9a5f4004cd6)

## Auditing and Consulting

- [ABDK](https://www.abdk.consulting/)
- [Least Authority](https://leastauthority.com/)
- [Hashcloak](https://hashcloak.com/)
- [Taurus](https://blog.taurushq.com/zero-knowledge-security/)
- [Common Prefix](https://www.commonprefix.com/)
- [ZK Labs](https://zklabs.io/#audits)
- [Diligence](https://consensys.net/diligence/)
- [Trail of Bits](https://www.trailofbits.com/)
- [Kudelski Security](https://kudelskisecurity.com/)

## Validator Services

- [ZK Validator](https://zkvalidator.com/)

## Books

- [Proofs, Arguments, and Zero-Knowledge](https://people.cs.georgetown.edu/jthaler/ProofsArgsAndZK.pdf) (Justin Thaler, 2022)
- [A Graduate Course in Applied Cryptography](http://toc.cryptobook.us/book.pdf) (Dan Boneh and Victor Shoup, 2020)

## Discussions

- [Why Dark Forest Matters: A Good Game, not a Crypto Game](https://mirror.xyz/omarmezenner.eth/gFCfCVwTfUU91SDXeROEaDQe4984nbFBIgv9QSY0r1U)
- [Six Moonshot ZK Applications](https://gubsheep.substack.com/p/six-moonshot-zk-applications?s=r)
- [A Socratic Dialogue to Come Up With a Secure ZK Message Board Architecture](https://mirror.xyz/0x3FD6f213ae1B8a7B6bd8f14BE9BF316a5e5A5d28/VTGpmEYLKIslUPf66VQzHUneB0R7EhMpJJ_mGrMvTwY)
- [The Strongest Crypto Gaming Thesis](https://gubsheep.substack.com/p/the-strongest-crypto-gaming-thesis?s=r)
- [Hardware Acceleration for Zero Knowledge Proofs](https://www.paradigm.xyz/2022/04/zk-hardware)
- [How do trusted setups work?](https://vitalik.ca/general/2022/03/14/trustedsetup.html)
- [10 zkApps Use Cases on Mina Protocol](https://blog.o1labs.org/10-snapps-use-cases-on-mina-83e646010e52)
- [Programming Languages in ZKP](https://medium.com/@delendum/thoughts-of-programming-languages-in-zkp-c906e96f056e)

## Communities

- [Harmony zkDAO](https://harmonyone.notion.site/zkDAO-Succinct-Private-Fair-2f14d3d954264bd38091b418fd6b9bd5)
- [Zero Knowledge University](https://zku.one/)
- [ZK Hash Bounties](https://www.zkhashbounties.info/)
- [Zero Knowledge Forum](https://zeroknowledge.fm/)
- [0xPARC: Program for Applied Research in Cryptography](https://0xparc.org/blog/program-for-applied-research)
- [ZPrize: accelerate zero-knowledge cryptography](https://www.zprize.io/)
- [zkMesh: a monthly newsletter](https://zkmesh.substack.com/)
- [ZKHack Discord](https://discord.com/invite/tHXyEbEqVN): Read, discuss, and implement ZK in Rust/Python (Fridays at 11:30ET)
- [ZKP Discussion Group Chat by Delendum](https://t.me/+gucKN1RBchMxMjVh): idea sharing, seeking advice/review/co-publish

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

### Elliptic Curve

- [2-chains of elliptic curves](https://eprint.iacr.org/2021/1359.pdf)
- [A survey of elliptic curves for proof systems](https://eprint.iacr.org/2022/586.pdf)
- [ECFFT: Fast Polynomial Algorithms over all Finite Fields](https://arxiv.org/abs/2107.08473)

### Slush: Fractal Scaling

- [Slush, a proposal for Fractal scaling](https://hackmd.io/@kalmanlajko/rkgg9GLG5#Our-trustless-bridging)

### DIZK: Distributed ZKP
- [DIZK: A Distributed Zero Knowledge Proof System](https://eprint.iacr.org/2018/691.pdf)

### Network Privacy
- [Dandelion: Redesigning the Bitcoin Network for Anonymity](https://arxiv.org/pdf/1701.04439.pdf)
- [A Flexible Network Approach to Privacy of Blockchain Transactions](https://arxiv.org/pdf/1807.11338.pdf)
