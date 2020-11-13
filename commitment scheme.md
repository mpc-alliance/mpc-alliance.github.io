---
title: Commitment Scheme
parent: Basic Building Blocks
has_children: true
nav_order: 1
---

# Commitment Scheme



A commitment scheme abstracts the notion of a “locked box”: the contents of the box are hidden (without the key), but can be opened in only one way.
The two basic security properties of a commitment scheme are _hiding_ and _binding_. Loosely, hiding means that it is hard for an adversary to tell apart between two commitments and two separate messages. Binding roughly means that it is hard for an adversary that is given a commitment to come up with an identical commitment that opens to a different message.
