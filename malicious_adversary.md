---
title: Malicious Adversary
parent: Security model
has_children: true
nav_order: 2
---

# Malicious Adversary

The malicious setting (or active security) is more realistic than the semi-honest setting. In the malicious setting players can do what ever they want to obtain private information of other parties inputs. This means they can arbitrarily deviate from the protocol in any way they feel.

The malicious setting comes in two variants. In the first variant called active-security-with-abort the honest players will abort the protocol when the adversary deviates from the protocol, or more realistically the honest players abort with overwhelming probability if the adversary deviates. In the second variant, called robust security, the honest players are able to continue with the protocol even though the malicious players have deviated from the protocol.

Active-security-with-abort can be obtained no matter how many parties one has, and no matter how many adversaries. However, the second variant of robust security can only be obtained when one has an honest majority; i.e. the number of honest parties is more than the number of dishonest parties. Thus in the important case of two party multi-party computation one can only obtain active-security-with-abort.


