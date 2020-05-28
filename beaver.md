---
title: Beaver Based Protocols
parent: Protocols
has_children: true
nav_order: 3
---

# Beaver Based-Protocols

A large number of modern protocols are based on the Beaver's circuit randomization concept. Here an MPC protocol is broken into two phases; an offline phase into which so-called multiplication triples are produced, and an online phase in which the actual function is evaluated. If we let `[a]` denote the secret sharing of a value `a`, then the offline phase produces triples of the form `([a], [b], [c])` where `c = a*b`.  The offline phase can often be used to produce other forms of correlated randomness.

Whilst the offline phase is function and input independent, and requires usually public key operations, the online phase is executed once the function and inputs are known. This phase consumes the Beaver Triples and evaluates the function.

Active security is obtained by using a form of authenticated secret sharing, in the full threshold case this is obtained by using secret sharings of Message-Authentication-Codes on each secret shared value.

There are a number of protocols in this family depending on the type of underlying arithmetic supported, and the means to generate the Beaver triples.



#### Tiny-OT

Originally a two party protocol, this protocol uses [Oblivious Transfer](Oblivious Transfer.md) to produce the triples in the offline phase. The Tiny-OT protocol evaluates on boolean values. Tiny-OT forms the basis of many modern BMR protocols.


#### SPDZ

This is an n-party full threshold protocol for any finite field. The offline phase is usually based on using Homomorphic Encryption, although a variant based on Tiny-OT is possible (in which case one says the protocol uses MASCOT as the offline phase). The modern Homomorphic Encryption based offline phase comes in three variants HighGear, LowGear and TopGear depending on the type of encryption scheme and zero-knowledge proof used.

#### SPDZ2k

This is a variant of SPDZ which applies to secret sharing over the ring `Z_{2^k}`. The offline phase can either be based on Oblivious Transfer or Homomorphic Encryption.


