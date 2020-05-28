---
title: Shamir Secret Sharing
parent: Advanced Building Blocks
has_children: true
nav_order: 1
---

# Secret Sharing Schemes


A Secret Sharing Scheme (SSS) is a set of two protocols:
1. Distribution 
2. Reconstruction 

In Distribution, a dealer takes a secret `s` and distribute it to `n` parties. In Reconstruction, a subset of the parties reveal their secret shares in order to learn the secret `s`. It is guaranteed that if disallowed sets of parties will not be able to learn anything about the original secret.  

A Secret Sharing Scheme is associated to an Access Structure, this is the set of sets of parties which can recover the secret (or equivalently the set of sets of parties which cannot access the secret). Access structures are always monotonically increasing, i.e. if you add a party to a set which can access the secret then the bigger set can also access the secret. There are a number of different methods to perform secret sharing.

In multi-party computation we are usually interested in so-called Linear Secret Sharing Schemes (LSSSs) as they allow parties to locally compute linear functions of their secrets for free.

#### Shamir Secret Sharing

In Shamir Secret Sharing the number of parties which can be adversarial `t` is a threshold of the total number of parties `n`. In multi-party computation protocols one usually has either `t<n/2` or `t<n/3`. Shamir is a form of LSSS, and usually the one used to introduce concepts in introductory courses.

#### Replicated Secret Sharing

Another popular LSSS scheme is called Replicated Secret Sharing, this is less efficient (usually) than Shamir Sharing for threshold structures. However, with Replicated Secret Sharing one is able to represent any access structure.

#### Full Threshold Secret Sharing

The simplest secret sharing scheme is one in which all parties need to come together to recover the secret. This form of sharing is the basis of almost all multi-party computation protocols in the dishonest majority setting. In this secret sharing each party `P_i` has a value `x_i` with the actual secret being `x = x_1 + ... + x_n`.

