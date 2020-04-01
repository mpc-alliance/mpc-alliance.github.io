---
title: Threshold Key Generation and Storage
parent: MPC Use Cases
grand_parent: Contents
has_children: true
nav_order: 2
---

# Threshold Key Generation and Storage


Multiparty computation (MPC) has gained considerable interest due to its inherent ability to protect cryptographic keys from theft or misuse. What’s often understated about MPC is that it is profoundly safer and simpler to administer than conventional models for private key generation and storage.

When used for key management, MPC software runs locally on the devices that are designated to participate in functions such as generation of key shares, partial signatures, key rotation, storage, recovery, suspension, and deletion. To minimize the risk of key theft or insider misuse, MPC supports threshold schemes where two or more honest parties must make their share of a key available for computation to use the key for a specific cryptographic operation.

What’s interesting about MPC-based key generation, use, and storage is that it natively generates a local share of a private key on each party’s device which is used locally for partial computations. The share never leaves the device and is never shared with any other party. Naturally, this reduces the risk of theft.

By generating keys in the form of key shares which are locally generated, used, and stored on each party’s device, there is no longer a need to generate, then shard, then distribute keys shares as is common with other schemes using Shamir Secret Sharing. The same is true when key shares need to be refreshed to deal with lost devices, personnel transitions, or routine security protocols. The new shares are once again locally generated and used by each MPC node, and locally stored on each party’s device.

Naturally, this local share generation and storage eliminates a lot of steps and risks for errors or compromise. When you consider the number of keys that may be required for a business, this characteristic of MPC introduces a dramatic reduction in operational complexity and risk.

Threshold-based MPC runs in a distributed fashion across the devices to execute the cryptographic operation. It does this without requiring any shares to be disclosed or collected and reassembled. So MPC again eliminates a massive amount of complexity and risk by eliminating these conventional key generation and storage related processes.

Dramatically simplified key generation, use, and storage is just one of the many compelling attributes of using MPC-based solutions for cryptographic key management.

Author: Frank Wiener [@Sepior](sepior.md)