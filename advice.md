---
layout: page
title: Starting a BTC/ETH company?
permalink: /advice/
---

This project was created to get your attention and point you to security resources.


1. Protect key material. Your servers will be accessed.
2. Be defensive against application vulnerability. You will have bugs.
3. Protect all authentication to your cloud infrastructure (2Fac, Strong + Unique Passwords). Your employees will re-use passwords and bad guys will get them.
4. Limit the exposure of funds with cold storage, HSMs, and Multi-Signature transactions.
5. Design for collusion whenever possible for sensitive or high value operations.

If this seems intimidating, here's some advice!

### Bitcoin Specific Advice

- [Cold Storage][CS] can reduce the impact of a security breach from 100% to a configurable percentage. After this, reduce your risk of a large hot wallet even further with cryptographic hardware or multisignature transactions.
- After reducing the amount of funds you'd store in a "Hot Wallet", use multisignature transactions to secure a hot wallet even further.
- Use an [HSM][HSM] that will protect key material and make it extremely hard to make a transaction that cannot be audited. It will also defend greatly against insider threats.

### General Security

These are practices that are common at any company, not just a blockchain company.

- [Starting up Security][SUS] is advice for company wide security.

- [Product Security][SUSSPS] and [Modern Product Security][MPS] discuss the development of a secure product.

- [Investigating Account Takeover][SUSSATO] discusses the massive amounts of phishing, malware, and other attacks that will directly target and steal from your customers.
- [Preventing Account Takeover][SUSSPAT] will discuss the automated ways you can prevent takeover of your customer accounts.

- [Bounty Launch Lessons][SUSBB] and [Bug Bounty 5 Years In][BBFYI] will help you start a bug bounty program from scratch.

- [Red Teams][SUSRT] will help you simulate a worst case incident scenario before it happens.

- [Scott Roberts from Github][IRDEAD] writes about hunting for adversaries on your infrastructure. [Ryan Huber from Slack][DSA] discusses approaches to alerting.

- [Security Breach 101][SUSSSB] will help you understand the complex coordination of an incident in progress.

- [Coinbase's security][CBS] should also act as a reference model for your own security program.

### About

This started as `bitcoin_breaches.txt` on my laptop. After 30 or so entries, I figured this would help bring [Starting Up Security][SUSS] to the BTC / ETH community. A much more broad list exists [here at bitcointalk][bitcointalk] that includes scams and fraud.

Feel free to suggest additions to the graveyard or advice section in pull requests.

[bitcointalk]: https://bitcointalk.org/index.php?topic=83794.0
[SUSS]: https://medium.com/starting-up-security
[SUS]: https://medium.com/starting-up-security/starting-up-security-87839ab21bae#.m120kdhur
[SUSSPS]: https://medium.com/starting-up-security/starting-up-security-85382451ae2e#.i290cvwdn
[SUSSATO]: https://medium.com/starting-up-security/investigating-account-takeover-21514954aa8f#.3mu9v6es0
[SUSSPAT]: https://medium.com/starting-up-security/preventing-account-takeover-c914fa07fb45#.lf7dzfy9m
[SUSBB]: https://medium.com/starting-up-security/bounty-launch-lessons-c7c3be3f5b#.wx2pkfjt3
[SUSRT]: https://medium.com/starting-up-security/red-teams-6faa8d95f602#.r40mml4re
[SUSSSB]: https://medium.com/starting-up-security/security-breach-101-b0f7897c027c
[BBFYI]: https://medium.com/@collingreene/bug-bounty-5-years-in-c95cda604365#.96dca24fk
[IRDEAD]: https://sroberts.github.io/2015/04/14/ir-is-dead-long-live-ir/
[MPS]: https://medium.com/@collingreene/modern-application-security-6fe53d7fc055#.2ul67qgbn
[DSA]: https://slack.engineering/distributed-security-alerting-c89414c992d6#.dkuulzsyr
[CBS]: https://medium.com/the-coinbase-blog/how-coinbase-builds-secure-infrastructure-to-store-bitcoin-in-the-cloud-30a6504e40ba#.yec4b2bbv
[CS]: https://en.bitcoin.it/wiki/Cold_storage
[HSM]: https://gemini.com/blog/your-bitcoin-wallet-may-be-at-risk-safenet-hsm-key-extraction-vulnerability/
