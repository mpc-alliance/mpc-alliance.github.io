---
title: Scale-Mamba
parent: Systems
has_children: true
nav_order: 1
---

# SCALE-MAMBA

SCALE-MAMBA is a framework for true multi-party computation based on secret sharing over large finite fields and also over binary fields. It is secure in a active-security-with-abort model. The system contains multiple hooks to enable it to be utilized in close-to-real-life situations. 

MAMBA is the front end language. It compiles a Python-ish language into a bytecode representation. The bytecodes are fully specified in the documentation. 

SCALE is the runtime, it executes the secure protocol based on the bytecodes. 

The system is based on SPDZ for the large finite field computations, using TopGear for the offline phase. For binary fields the system uses a variant of the BMR protocol, called HSS, using Tiny-OT to produce the shared garbling of the circuits. It is possible to exchange data between the large prime finite field sharing and the binary sharing.


#### Links
- [Software](https://homes.esat.kuleuven.be/~nsmart/SCALE/)
