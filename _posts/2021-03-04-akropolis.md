---
layout: post
title: akropolis
date: 2020-11-13 14:31 -0800
categories: smart_contract
link: https://www.notion.so/akropolis/Akropolis-Hack-Update-10f48dfa44a544e5a7b24f298c759c6d
---
> Started at 11:50:41 AM +UTC, 12 November 2020, Akropolis was attacked by exploiting its flawed handling of the deposit logic in its SavingsModule smart contract. The hack results in a loss of 2,030,841.0177 DAI from the affected YCurve and sUSD pools. The stolen funds are currently held [here](https://etherscan.io/address/0x9f26ae5cd245bfeeb5926d61497550f79d9c6c1c): https://etherscan.io/address/0x9f26ae5cd245bfeeb5926d61497550f79d9c6c1c. The account has been blacklisted.

> This incident was due to a bug in the protocol without (1) validating the supported tokens and (2) enforcing reentrancy protection on the deposit logic. The exploitation leads to a large number of pooltokens minted without being backed by valuable assets. The redemption of these minted pooltokens is then exercised to drain about 2.0mn DAI from the affected Curve Y and Curve sUSD pools.