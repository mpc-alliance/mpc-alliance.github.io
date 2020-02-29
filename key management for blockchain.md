---
title: Key management in blockchain systems
parent: MPC Use Cases
grand_parent: Contents
has_children: true
nav_order: 1
---

# Key management in Blockchain Systems


Threshold signature scheme (TSS) is a sub field of MPC computing digital signatures in a distributed way. 
The natural way in which TSS can be put to use in a blockchain is by changing a blockchain client to generate keys and signatures using TSS. The term blockchain client refers to the set of commands executed by a full node. In practice, the TSS technology allows us to replace all private key related commands with distributed computations.

To explain it in more detail, we start by describing briefly how new addresses are created on the classical blockchain design.  Simply put, we can create a new address by generating a private key, and then computing the public key from the private key. Finally, the blockchain address is derived out of the public key.

Now, using TSS, we would have a set of n parties jointly computing the public key, each holding a secret share of the private key (the individual shares are not revealed to the other parties). From the public key, we can derive the address in the same way as in the traditional system, making the blockchain agnostic to how the address is generated. The advantage is that the private key is not a single point of failure anymore because each party holds just one part of it. 

The same can be done when signing transactions. In this case, instead of a single party signing with their private key, we run a distributed signature generation between multiple parties. So each party can produce a valid signature as long as enough of them are acting honestly. Again we moved from local computation (single point of failure) to an interactive one.

It is important to mention that the distributed key generation can be done in a way that allows different types of access structures: the general “t out of n” setting will be able to withstand up to t arbitrary failures in private key related operations, without compromising security.
