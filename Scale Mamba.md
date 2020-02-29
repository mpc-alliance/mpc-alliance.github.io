---
title: Scale Mamba
parent: Systems
grand_parent: Contents
has_children: true
nav_order: 1
---

# SCALE MAMBA


([_source_](https://github.com/MPC-SoK/frameworks/wiki/SCALE-MAMBA)) SCALE-MAMBA is a framework for true multi-party computation. It is secure in a malicious model (that is, the computation will abort with a malicious adversary) and it supersedes the SPDZ language. It uses an arithmetic model of computations (ie over a large finite field) but the protocol itself uses a hybrid approach (diverging far from the original circuit models).

MAMBA is the front end. It compiles a Python-ish language to a bytecode representation. The bytecodes are fully specified in the documentation (see below). SCALE executes the secure protocol on bytecodes. It uses three distinct types of pre-processing data to execute the secure protocol.


#### Links
- [Software](https://homes.esat.kuleuven.be/~nsmart/SCALE/)
