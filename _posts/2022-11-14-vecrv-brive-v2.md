---
layout: post
title: veCRV Brive V2
date: 2022-10-27 06:45 -0800
categories: smart_contract
link: https://github.com/yearn/yearn-security/blob/master/disclosures/2022-11-01.md
---
Reward manipulation logic error.

> Disclaimer: The Yearn team did not write or deploy the original BribeV2 contract. However, as a heavy user of it, decided to act quickly to deploy a new contract so that operations could resume.
> During a routine check, irregularities were discovered in the amount of SPELL bribes being claimed by some users of the BribeV2 contract. Following analysis, it was determined to be an attacker exploiting a flaw in the way the contract calculates bribe allocations.
> The flaw causes bribes to be allocated based on each user's locked amount of CRV rather than allocating based on their veCRV balance.
> The attacker was found to have exploited this since September 2021, tricking the contract into awarding them higher allocations than they should deserve for the actual weight they contributed to a gauge.
> Other BribeV2 users were unknowingly subject to faulty bribe calculations due to the fact that lock time was not taken into account.
> Yearn developers patched the vulnerability and deployed a new version of the contract (yBribe) which properly allocates bribes to users.

- [Yearn's Bilateral Responsible Disclosure Agreements](https://github.com/yearn/yearn-security/blob/master/SECURITY.md#bilateral-responsible-disclosure-agreements)
- [Suspect TX](https://etherscan.io/tx/0x47e10eebda1b9afbabe622d3deece757d6d49a0510081635fc7dc21efe50aeeb)