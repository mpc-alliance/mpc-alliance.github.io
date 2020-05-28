---
title: BGW/CCD Protocol
parent: Protocols
has_children: true
nav_order: 3
---

# BGW/CCD Protocols

In the case of threshold secret sharing with `t<n/2` (resp. `t<n/3`) one can obtain semi-honest (resp. robust actively) secure multi-party computation protocols over a finite field of `p` elements with `p>n` using Shamir Sharing and the BGW/CCD protocol. The protocol family can be extended to an arbitrary `Q2` (resp. `Q3`) access structures in a relatively straight forward manner. The protocol is interesting as it can protect against adversaries with infinite computing power.

The protocol for semi-honest adversaries, i.e. when `t<n/2`, is relatively efficient, but the robust protocol, i.e. when `t<n/3`, is relatively costly requiring Verifiable Secret Sharing and a player elimination strategy. In modern instantiations aiming for active security one normally targets active-security-with-abort, which is easier to achieve.  If we restrict to active-security-with-abort then we can obtain a protocol with `t<n/2`, but which requires us to make cryptographic assumptions; i.e. it is no longer secure against adversaries with infinite computing power.
