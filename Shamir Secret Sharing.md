---
title: Shamir Secret Sharing
parent: Advanced Building Blocks
grand_parent: Contents
has_children: true
nav_order: 1
---

# Shamir's Secret Sharing Scheme


Shamir's Secret Sharing Scheme (SSSS) is a set of two protocols:
1. Distribution 
2. Reconstruction 

In Distribution, a dealer takes a secret `s` and distribute it to `n` parties. In Reconstruction, a threshold of the parties (threshold `t` is set by the dealer) reveal their secret shares in order to learn the secret `s`. 
It is guaranteed that less that `t` parties will not be able to learn anything about the original secret.  