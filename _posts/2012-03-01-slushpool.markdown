---
layout: post
title:  "Slush's Pool"
date:   2012-03-01 11:52:03 -0700
categories:
- server_hot_wallet_breach
- cloud_provider_breach
link: http://archive.is/e5lt
---
A breach at Linode was the root cause here and there's plenty of information to understand the breach. [Credentials for a customer support team member](http://archive.is/tRQ9) were used and eight Linode customers were compromised for having affliations to bitcoin.

After accessing the customer support interface, the attacker was able to access the individual account interface for their victims and change root passwords on customer's machines. To apply this root password change, servers were rebooted.

A VP at Linode [responded](http://pastebin.com/UW7iT5fj).

>Somebody hacked my backup machine with pool data hosted on Linode and steal 3094 BTC ("hot" coins ready for payouts). Cold backup was not affected in any way by this hack.

> It looks that also user database has been compromised. Although passwords are stored in SHA1 with salt, I strongly recommend to change your password on the pool immediately.

>Robery of Bitcoins has no impact to pool users, I'm covering the loss from my own income (although it means that many months of my work is wasted  Roll Eyes ).
