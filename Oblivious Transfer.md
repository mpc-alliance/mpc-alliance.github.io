---
title: Oblivious Transfer
parent: Advanced Building Blocks
grand_parent: Contents
has_children: true
nav_order: 2
---

# Oblivious Transfer



Oblivious Transfer (OT) is a cryptographic primitive in which a sender transfers some of potentially many pieces of information to a receiver.
The sender doesn't know which pieces of information have been transferred.

Oblivious transfer is central to many of the constructions for secure multiparty computation.
In its most basic form, the sender has two secret messages as inputs,`m_0,m_1`; the receiver has a choice bit `c` as input.
At the end of the 1-out-of-2 OT protocol, the receiver should only learn message `m_c`, while the sender should not
learn the value of the receiver's input `c`.
