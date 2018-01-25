---
layout: post
title:  "Poloniex"
date:   2014-03-04 11:52:03 -0700
categories: application
link: https://bitcointalk.org/index.php?topic=499580
---

Poloniex is a Bitcoin exchange that has been operating since 2014. In March of 2014, an Application Vulnerability was exploited and
caused a loss of 97 BTC (a 12.3% loss on the exchange). The reported cause of the hack was that they did not properly check for a negative account balance
while processing multiple, simultaneous withdrawals.

> The hacker found a vulnerability in the code that takes withdrawals. The hacker discovered that if you place several withdrawals
> all in practically the same instant, they will get processed at more or less the same time. This will result in a negative
> balance, but valid insertions into the database, which then get picked up by the withdrawal daemon.
>
> What Will Be Done to Prevent Further Exploits?
>
> Withdrawals and order creation have been switched to a queued method, where the first step is to add the task to a global
> execution queue that is processed sequentially. Each step of critical database operations is verified before proceeding, and such
> operations are in the process of being converted to transactions. I have hired additional developers to help with tightening up
> security at Poloniex, as well as created a bug bounty.
