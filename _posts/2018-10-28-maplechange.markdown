---
layout: post
title:  "MapleChange"
date:   2018-10-28 11:52:03 -0700
categories: 
- application
link: https://www.ibtimes.com/cryptocurrency-exchange-maplechange-hacked-exit-scam-allegations-surface-2728232
---
There are heavy accusation of an exit scam, so I delayed the posting of this breach.

> Due to a bug, some people have managed to withdraw all the funds from our exchange. We are in the process of a thorough investigation for this. We are extremely sorry that it has to come to end like this. Until the investigation is over, we cannot refund anything.

A [follow up tweet](https://pastebin.com/PZD3Qb35) includes a post mortem:

> The method `unlock_and_sub_funds` has proper conditionals, immediately raising exceptions if the sub amount goes below the balance of the user. In this case, even if the malformed/exploited order did get processed, it would stop here, properly throwing an error in our logs and allowing us to properly investigate. However, the perpetuators knew exactly how this code would run, and as a result abused it using a series of accounts, as you notice in order.rb (https://github.com/peatio/peatio/blob/6fe7e960a12c40053370cb25cdd0968b67041aa0/app/models/order.rb), the call `strike` both calls `hold_account.unlock_and_sub_funds` (removing funds from one account) and adding it onto `expect_account`. If properly executed, this exploit could continue to subtract funds from one account and add onto the other one with no limitations. This is primarily the cause of the bug.

So, the best estimate is that it is an application vulnerability (if it indeed was not an exit scam). This would be typical of the occurrences of race conditions and other ledger related application bugs in the graveyard.
