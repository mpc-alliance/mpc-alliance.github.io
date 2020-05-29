---
title: BMR protocol
parent: Protocols
has_children: true
nav_order: 4
---

# BMR Protocol


The BMR protocols adapt the main idea of [Yao’s](yao.md) [Garbled Circuit](garbled_circuit.md) to a multi-party setting. The basic idea is that another MPC protocol is used to generate an `n`-party garbling, and then each player independently evaluate the circuit. To obtain active security one needs to utilize an actively secure base MPC protocol, and in addition utilize a method to ensure the evaluation phase reveals any deviations from the protocol. In modern BMR protocols the underlying MPC protocol is usually based on the `n`-party variant of Tiny-OT. 
