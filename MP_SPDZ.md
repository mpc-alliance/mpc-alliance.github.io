---
title: MP-SPDZ
parent: Systems
has_children: true
nav_order: 2
---

# MP-SPDZ

MP-SPDZ implements more than 30 MPC protocol variants, all of which
can be used with the same high-level programming interface based on
Python. This considerably simplifies comparing the cost of different
protocols and security models.

The protocols cover all commonly used security models
(honest/dishonest majority and semi-honest/malicious corruption) as
well as computation of binary and arithmetic circuits (the latter
modulo primes and powers of two). The underlying primitives employed
include secret sharing, oblivious transfer, homomorphic encryption,
and garbled circuits.

A particular focus of MP-SPDZ is the application to machine learning.
Currently this includes inference/classification for complex networks
such as ResNet and DenseNet as well as deep learning training with
fully-connected layers and softmax/sigmoid output activation.


#### Links
- [Software](https://github.com/data61/MP-SPDZ)
- [Paper](https://eprint.iacr.org/2020/521)
- [Reference](https://mp-spdz.readthedocs.org)
