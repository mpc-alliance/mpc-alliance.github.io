---
title: GMW protocol
parent: Protocols
has_children: true
nav_order: 3
---

# GMW Protocol



This is a classical MPC protocol of Goldreich, Micali, and Wigderson (GMW), which uses a boolean-circuit representation for the function being computed and is secure against a semi-honest adversary controlling any number of corrupted parties. The basic, semi-honest protocol, uses [Oblivious Transfer](Oblivious Transfer.md) to execute the boolean gates. 

The protocol can be generlized to arithmetic circuits as well.

The GMW protocol should be distingushed from the GMW Compiler which shows it is possible to convert protocol secure for [semi-honest](semi_honest_adversary.md) into one secure for [malicious](malicious_adversary.md). This utilizes zero-knowledge proofs to stop any party from deviating from the correct protocol.

The term GMW is often used for a protocol which combines the two techniques together into an `n`-party multi-party computation protocol which is actively secure.
