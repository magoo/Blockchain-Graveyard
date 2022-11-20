---
layout: post
title: Skyward Finance
date: 2022-11-01 05:04 -0800
categories: smart_contract
link: https://twitter.com/BlockSecTeam/status/1587998109648683010
---
Insufficient parameter validation. $3.2M lost. Smart contracts in Near blockchain.

> The root cause is in function redeem_skyward (https://github.com/skyward-finance/contracts/blob/master/skyward/src/treasury.rs#L158), which is used to redeem the treasury from the protocol.
> However, the function does not check whether the provided token_account_ids are duplicated. In this case, the attacker is able to redeem the treasury tokens multiple times with the same skyward share withdrawn once.

- [Exploit TX](https://explorer.near.org/transactions/92Gq7zehKPwSSnpoZ7LGGtSmgmBb4wP2XNDVJqUZRGqz)