---
title: MPC-based Solution for Key Protection
parent: MPC Use Cases
has_children: true
nav_order: 3
---

# MPC-based Solution for Key Protection

The emergence of blockchain technology makes self-sovereign finance become possible where users can access their funds directly without the permission from the banking system. This is similar to the concept of returning power to the people. However, users have lost private keys which are needed to access their assets. Therefore, key management plays a significant role for digital asset protection. In this article, we will introduce an MPC-based solution for key protection.


## Background

For general users, it is not easy to secure their own key, let alone understand what a private key is. The blockchain user experience is very different from the current password system. For example, there is no way for others to help key recovery if you lost your private key or the mnemonic code. Decentralization is good that only the owner with the key can move the fund, but it shifts the responsibility to the users. There are many new custodian services offering better user experiences to improve usability, but users still need to trust a third party and give up complete control over their assets. An ideal key management design should simultaneously consider security, usability and liability.

Besides, cryptocurrencies are notorious for their vulnerability to theft from exchanges. Since exchanges are in charge of safekeeping of assets from users, they have become a target for hackers. Improper key management and poor system implementation at the exchange may increase the risk of asset theft. Therefore, securing digital assets is becoming an important topic that is worthy of more public attention.


## Threshold signature scheme (TSS)

Recently, TSS has attracted much attention for private key protection and cryptocurrency wallet design. TSS, a special application of threshold cryptography, dramatically decreases the risk of private key management. Compared to multi-signature, TSS offers shorter signatures and better privacy. Moreover, TSS provides native multi-signature capability and can be executed off-chain. Most importantly, TSS does not save private keys on servers and provides risk control as well as separation of duties. These significant advantages make TSS suitable for implementing hot wallets without revealing private keys.

In TSS, there are three phases as follows to generate a signature.

1. **Key Generation**: In this phase, all participants run a cryptographic process called distributed key generation (DKG) to determine a shared public and private key. After the process, each participant will have a secret share, which can be used for signing later. The secret share should be secured safely by each participant.
2. **Signing**: In this phase, each participant generates and exchanges some required information for the signing algorithm with the secret share created in the key generation process. Then, each participant takes the message as an input to generate a digital signature. During the signing process, it is important to ensure no private key will be able to be reconstructed.
3. **Verification**: The signature verification is run by the same way as the particular signing scheme such as ECDSA does. The goal is to ensure the signature can be verified by the same public key.


## Multi-party computation (MPC)

MPC is a subfield of cryptography and can be described as the problem of n players needing to compute an agreed function of their inputs in a secure way while ensuring correctness and ensuring inputs remain private. In addition, secure multi-party computation (sMPC) can provide a security guarantee even if malicious players attack the protocol. In other words, sMPC can achieve joint control to disperse risk among the participants without a single point of failure. This property is very helpful for key management to reduce risk.

Besides, MPC is suitable to design flexible policy checking to serve financial institutions. For example, a customer wants to transfer a transaction. The banking verification process then requires a banking teller to sign and then obtain approval from a manager. More importantly, MPC can achieve a (t, n)-threshold scheme which is similar to multi-signature.


## Potential advantages

Armed with this technology, there are several potential possibilities to design a cryptocurrency wallet or a custody service. Since secret shares can be generated in a centralized or distributed way, it can be used to design flexible access structures. Furthermore, the scheme supports disaster recovery to reconstruct the signature if users lose access to their secret share. These features make the system more practical and improve the user experience.


## Conclusion

Blockchain technology is at an early stage, and basic infrastructure and related tools are in development. Despite there being several cryptocurrency wallet solutions, we are still far from exploring the possibilities. TSS, an MPC-based solution for key protection, can be a powerful building block to develop threshold cryptosystems.


## Further reading

1. [Fast Multiparty Threshold ECDSA with Fast Trustless Setup](https://eprint.iacr.org/2019/114.pdf)
2. [Fast Secure Multiparty ECDSA with Practical Distributed Key Generation and Applications to Cryptocurrency Custody](https://eprint.iacr.org/2018/987.pdf)
3. [Threshold ECDSA from ECDSA Assumptions: The Multiparty Case](https://eprint.iacr.org/2019/523.pdf)
4. [Bandwidth-efficient threshold EC-DSA](https://eprint.iacr.org/2020/084)
5. [Threshold Signatures Explained](https://academy.binance.com/security/threshold-signatures-explained)


Author: Chang-Wu Chen [@AMIS](amis.md)
