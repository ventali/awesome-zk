## Comments on paper: zkSNARKs in a Nutshell

[zkSNARKs in a nutshell](https://blog.ethereum.org/2016/12/05/zksnarks-in-a-nutshell/) is a great introductory article for people unfamiliar with zero knowledge proofs. However, it might have skipped too many important, basic concepts for people unfamiliar with this subject, or cryptography in general. 

My comments focus on (1) providing some recent articles that explain basic concepts in detail, using plain languages; (2) sharing a few issues I identified in the article, and equations that I think would benefit from more clarifications; (3) providing some pointers to research papers, for readers who want to delve deep into how and why; (4) providing some pointers to recent developments on some of the "future possibilities" outlined in this article.

## Section: Overview

### p.1. A) Encoding as a polynomial problem

See also https://electriccoin.co/blog/snark-explain5/ (From Computations to Polynomials). This part is actually quite advanced and non-intuitive. I would suggest reading about the other parts before getting to this.

### p.1. B) Succinctness by random sampling

See also https://electriccoin.co/blog/snark-explain2/, which has a more intuitive explanation, with step-by-step hypothetical examples using Alice and Bob.


### p.1. C) Homomorphic encoding / encryption

Here https://electriccoin.co/blog/snark-explain/ offers a very detailed explanation. Some privacy ML research papers also do a good job explaining this. For example, https://eprint.iacr.org/2018/662.pdf (notably, many authors of this paper are doing research in cryptography and formal verification these days)

### p.1. D) Zero Knowledge

See also https://electriccoin.co/blog/snark-explain3/ and the subsequant section. 


## Section 1: RSA and Zero-Knowledge Proofs

### p.2. Re: Security of RSA and the choice of (p-1)(q-1)

A lot of things are skipped here. For readers without a cryptography background or unfamiliar with the innerworkings of RSA, here are two articles explainig how it works and why (p-1)(q-1) is picked here.

- https://doctrina.org/How-RSA-Works-With-Examples.html 
- https://doctrina.org/Why-RSA-Works-Three-Fundamental-Questions-Answered.html#wruiwrtt . 

I picked these two articles over numerous lecture slides on RSA that anyone can find on Google, because they (1) use plain language wherever possible; (2) offer contexts in practice and examples; (3) do not overuse greek symbols;

### p.2. Re: Definition of homomorphic operations

The paper states "In general, two operations are homomorphic if you can exchange their order without affecting the result."

This explanation can be confusing. "Exchanging order without affecting the result" is generally understood as a multiplicative property, e.g. A x B = B x A. What the author is trying to say here is homomorphic functions satisfy that f(a).f(b) = f(a.b), where f is the homomorphic function and . is some operation that combines two elements (e.g. a and b). I think Wikipedia offers a better explanation https://www.wikiwand.com/en/Homomorphism

## Section 1.1: Interactive Verification

### p.3. Re: Definition of soundness and completeness

> The generally desired properties are that no prover can convince the verifier about a wrong statement (soundness) and there is a certain strategy for the prover to convince the verifier about any true statement (completeness)

To be precise, "there is a certain strategy" really means "there must always exist a (constructive) way". Existence of a strategy is insufficient.

### p.3. Re: Definition of "ARguments"

> ARguments: the verifier is only protected against computationally limited provers. Provers with enough computational power can create proofs/arguments about wrong statements (Note that with enough computational power, any public-key encryption can be broken). This is also called “computational soundness”, as opposed to “perfect soundness”

"Computationally limited" really means "computers with finite computing powers, constrained by today's technologies and costs in practice". It should not be interpreted as "slow computers".

"Enough computational power" here really means "theoretically possible, but not feasible whatsoever for practical purposes" 

### p.4. Re: Definition of "setup string"

"Setup string" is an undefined term. Under the context of this section, "setup string" means the result of a function applied to the "witness string", such that it is not feasible to infer the "witness string" from the result, and the result is still sufficient for the verifier to verify the validity of the statement the prover wants to prove (in the above example, the transfer of balance)

## Section 2.1: P and NP

### p.4. Re: Basic definitions

This chapter is fairly basic for people with computer science background. But for those without, they could really use a lot more explanations. At least one person told me they spent a lot of time trying to understand what is discussed here, but find it very difficult. 

I suggest reading Chapter 3 Growth of Functions and Chapter 34 NP-completeness of Introduction to Algorithms, 3rd Edition. A free PDF version appears to be online here: https://web.iiit.ac.in/~pratik.kamble/storage/Algorithms/Cormen_Algorithms_3rd.pdf

### p.5. Re: P and NP problems in practice

> P is considered the class of “feasible” problems and indeed, for non-artificial problems, k is usually not larger than 4.
> 
> ...
> 
> Roughly speaking, if you only have to compute some value and not “search” for something, the problem is almost always in P. If you have to search for something, you mostly end up in a class called NP.

Note that P is generally considered feasible, it does not mean most feasible problems are in P. Many problems in practice cannot be solved in polynomial time but are solved nonetheless using techniques such as branch and bound, A*, etc. Many practical graph problems also have k greater than 4 - it really depends on the problem.

Although it is true that a search problem is generally verifiable in polynomial time (thus NP), it does not imply search problem is universally harder than problems that compute a value. An interesting problem to read about is [graph isomophism](https://www.wikiwand.com/en/Graph_isomorphism_problem). The [time complexity article](https://www.wikiwand.com/en/Time_complexity) on Wikipedia also offers a more comprehensive view.

## Section 2.2: The Class NP

### p.5. Re: SAT - an example of NP problem

This is a classic problem taught in computer science class in almost everywehre (as an medium-level / advanced subject for undergrads). For readers unfamiliar with this problem, half a page of explanation is very unlikely to be enough. It is worth spending some time on the [Wikipedia article](https://www.wikiwand.com/en/Boolean_satisfiability_problem), because it is used for analyzing numerous other problems.


## Section 2.3: P = NP? (p.6)

> Oh and just as a side note, if you can prove the converse, that P and NP are equal, apart from also winning that amount, there is a big chance that cryptocurrencies will cease to exist from one day to the next. The reason is that it will be much easier to find a solution to a proof of work puzzle, a collision in a hash function or the private key corresponding to an address. Those are all problems in NP and since you just proved that P = NP, there must be a polynomial-time program for them.

It's a fun thing to say "the world as we knew would cease to exist if P=NP....", but most proofs are not constructive, therefore it may have very limited implications in practice. That means, one can prove a statement, but the proof offers no insight on how to reduce (convert) problems between P and NP. An interesting related example is [Kolmogrov Complexity](https://www.wikiwand.com/en/Kolmogorov_complexity). We know it exists. We know it is exceedingly useful for compression and [AI](http://hutter1.net/ait.htm). We can prove so many results with it. But we also know (and can prove) it is incomputable.

## Section 2.4: NP-Completeness (p.6)

> For any NP-problem L there is a so-called reduction function f, which is computable in polynomial time such that
> 
> L(x) = SAT(f(x))
> 
> Such a reduction function can be seen as a compiler...

This is discussed in a lot  more detail in Introduction to Algorithms. See the chapters I referred to previously.

## Section 2.5: Reduction Example (p.7)

> We will now construct a reduction from SAT to PolyZero and thus show that PolyZero is also NP-complete

The example is not very beginner friendly, but overall what it is trying to do is to construct a function that translates between the two problems, i.e. with same input, they give the same output. The existence of such translation means the two problems are equivalent, that is one can be "reduced" to the other.

## Section 3: Quadratic Span Programs

### p.8. Re: QSP circuits and generic computations

I think readers could benefit from some high level descriptions. For example, what "circuit" means, how they are related to polynomials, how they work. I recommend this as a reference for beginners: https://electriccoin.co/blog/snark-explain5/ 

### p.9. Re: Zero points of polynomials

> Checking a polynomial identity only at a single point instead of at all points of course reduces the security, but the only way the prover can cheat in case th − vawb is not the zero polynomial is if she manages to hit a zero of that polynomial, but since she does not know s and the number of zeros is tiny (the degree of the polynomials) when compared to the possibilities for s (the number of field elements), this is very safe in practice

Although it is intuitive, this is not a trivial result. See: https://www.wikiwand.com/en/Lagrange%27s_theorem_(number_theory)

## Section 4: The zkSNARK in Detail (p.9)

> The encryption E used there has a certain homomorphic property, which allows the prover to compute E(v(s)) without actually knowing vk(s).

See also references to the "hiding" analogy in https://electriccoin.co/blog/snark-explain/

## Section 4.1: The zkSNARK in Detail (p.10)

> The more important part, though, is the question whether the prover can somehow come up with values A, B that fulfill the check e(A, gα) = e(B, g) but are not E(f(s)) and E(αf(s))), respectively. The answer to this question is “we hope not”. Seriously, this is called the “d-power knowledge of exponent assumption” and it is unknown whether a cheating prover can do such a thing or not. This assumption is an extension of similar assumptions that are made for proving the security of other public-key encryption schemes and which are similarly unknown to be true or not

"d-power knowledge of exponent assumption" was "recently" introduced in 2010 by Groth. See https://www.iacr.org/archive/asiacrypt2010/6477323/6477323.pdf. See also discussions in https://eprint.iacr.org/2019/148.pdf. It was actually considered a non-standard assumption. I think more serious readers would want to know to what extent the assumption holds and why we can use something that we only "hope" a cheater would not break it.

## Section 4.2 A SNARK for the QSP Problem

### p.12. Re: Injective function, free elements, and choice of coefficients

> There was an injective function....which restricts the values of a_1, ... ,a_m, b_1, ... ,b_m. Since m is relatively large, there are numbers which do not appear in the output of f for any input

Recall that a_i b_i has to equal to certain value based on f and the input string. See definition in p.8. Previously the definition was stated, but never explained. Perhaps the chapters should be reorganized a bit. 

What the paragraph is trying to say is perhaps not obvious for people are unfamiliar with injective function and how it is generally used to construct proofs. It should be explained that, the purpose of the construction here is to define a way we can choose coefficients such that it won't collide with inputs and make the proofs so much easier. i.e. avoid the use of a small subset of numbers in {1, ... m} (that are mapped by f) that are not "free". Most elements are "free" (to be used) because m is large.

### p.13. Re: Equations (1)-(3) for verifier confirmation

The equations themselves make mathematical sense, but I am still confused by the explanations provided in the paragraph on what it is trying to achieve. Perhaps it is necessary to borrow more explanations from the QSP paper to provide more context. 

TODO: Let's write it up step-by-step later, and with proper references to definitions before


## Section 5: Tradeoff between Input and Witness Size

### p.14. Re: Hasing complex statements to reduce input to constant size

The high level idea is sound but the math looks very confusing. Definition of H is ambiguous here. 

TODO: Let's rewrite this later.

## Section 6: How is this Relevant to Ethereum

### p.15. Re: Challenges of using zero knowledge for computation on Ethereum

> On Ethereum, zkSNARKs would not be limited to a single computational problem, but instead, everyone could set up a zkSNARK system for their specialized computational problem without having to launch a new blockchain. 

To make the problem even more challenging, the computations performed on Ethereum are much more complex than those on zCash (simple asset transfers). It's like jumping from calculator to first generation of personal computers.

### p.15. Re: zkSNARK in a Generic virtual machine

> It is also possible to do things like adding a zkSNARK system for a “generic virtual machine”. This would not require a new setup for a new use-case in much the same way as you do not need to bootstrap a new blockchain for a new smart contract on Ethereum.

At least three teams are taking up this challenge over the last 2-3 years and have made remarkable progress. See zkEVM references in README of this repository.


## Section 6.1: Getting zkSNARKs to Ethereum

This paper has not discussed using zkSNARK to prove transactions on layer 2, which at this time, appears to be the "mainstream" approach taken by Ethereum community for scaling. It is not suprising because the paper was written before layer 2 really became a thing. Nonethless, readers could find more information in zk-rollup section of the main README file in this repository.   
