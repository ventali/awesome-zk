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
- [zkSNARKs in a nutshell](https://blog.ethereum.org/2016/12/05/zksnarks-in-a-nutshell/)
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

## Layer-2

- [An Incomplete Guide to Rollups](https://vitalik.ca/general/2021/01/05/rollup.html)
- [Why rollups + data shards are the only sustainable solution for high scalability](https://polynya.medium.com/why-rollups-data-shards-are-the-only-sustainable-solution-for-high-scalability-c9aabd6fbb48)

## Projects

### zk-VM

- [ZKVM book](https://hackmd.io/@liangcc/zkvmbook)
- [Introduction to zkEVM](https://hackmd.io/@yezhang/S1_KMMbGt)
- [appliedzkp](https://github.com/appliedzkp)
- [Matter Labs zkEVM](https://blog.matter-labs.io/unisync-a-port-of-uniswap-v2-on-the-zkevm-b12954748504)
- [Hermez zkEVM](https://blog.hermez.io/introducing-hermez-zkevm/)
- [Scroll](https://hackmd.io/@yezhang/S1sJ2cEWY)
  - [zkEVM](https://hackmd.io/@yezhang/S1_KMMbGt)
- [Sin7Y zkEVM](https://medium.com/@sin7y)

### ZK Applications

- [Zcash: a privacy-protecting, digital currency](https://z.cash/technology/)
- [Loopring Launches zkRollup Exchange](https://medium.com/loopring-protocol/loopring-launches-zkrollup-exchange-loopring-io-d6a85beeed21)
- [Tornado Cash: Introducing Private Transactions On Ethereum](https://tornado-cash.medium.com/introducing-private-transactions-on-ethereum-now-69fb059a14a1)
- [Semaphore: a privacy gadget built on Ethereum](https://medium.com/coinmonks/to-mixers-and-beyond-presenting-semaphore-a-privacy-gadget-built-on-ethereum-4c8b00857c9b)
- [Announcing Dark Forest: an MMO space-conquest game](https://blog.zkga.me/announcing-darkforest)

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

