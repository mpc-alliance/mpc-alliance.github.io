---
title: Yao protocol
parent: Protocols
has_children: true
nav_order: 2
---

# Yao Protocol

The basic passively secure protocol consists of 6 steps as follows:

1. The underlying function (e.g., in the millionaires' problem, comparison function) is described as a Boolean circuit with 2-input gates. The circuit is known to both parties. This step can be done beforehand by a third-party.
2. Alice [garbles](garbled_circuit.md) (encrypts) the circuit. We call Alice the garbler.
3. Alice sends the garbled circuit to Bob along with her encrypted input.
4. Bob through oblivious transfer receives Alice's encrypted circuit and input. In terms of the definition from above, Bob is the receiver and Alice the sender at this oblivious transfer.
5. Bob evaluates (decrypts) the circuit and obtains the encrypted outputs. We call Bob the evaluator.
6. Alice and Bob communicate to learn the output.

In descriptions one often sees Alice referred to as the circuit Constructor, and Bob as the circuit Evaluator.

To obtain active security the overall protocol description becomes more complex. Being a two-party protocol it is impossible to obtain a robust multi-party computation protocol from Yao.

The n-party version of this protocol is often referred to as the [BMR](bmr.md) protocol.


