---
title: GMW protocol
parent: Protocols
has_children: true
nav_order: 3
---

# GMW Protocol



classical MPC protocol of Goldreich, Micali, and Wigderson (GMW), which uses a boolean-circuit representation for the function being computed and is secure against a semi-honest adversary controlling any number of corrupted parties.

The protocol can be generlized to arithmetic circuits as well.

The GMW protocol should be distingushed from the GMW Compiler which shows it is possible to convert protocol secure for [semi-honest](semi_honest_adversary.md) into one secure for [malicious](malicious_adversary.md).