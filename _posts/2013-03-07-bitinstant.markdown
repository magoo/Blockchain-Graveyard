---
layout: post
title:  "BitInstant"
date:   2013-03-07 11:52:03 -0700
categories: bitcoin breach
link: http://archive.is/NtRDX
---
The attacker contacted our domain registrar at Site5 posing as me and using a very similar email address as mine, they did so by proxying through a network owned by a haulage company in the UK whom I suspect are innocent victims the same as ourselves. Armed with knowledge of my place of birth and mother's maiden name alone (both facts easy to locate on the public record) they convinced Site5 staff to add their email address to the account and make it the primary login (this prevented us from deleting it from the account). We immediately realized what was going on, and logged in to change the information back. After changing this info and locking the attacker out, overnight he was able to revert my changes and point our website somewhere else. Site5 is denying any damages, but we suspect this was partly their fault.

After gaining access, they redirected DNS by pointing the nameservers to hetzner.de in germany, they used hetzner's nameservers to redirect traffic to a hosting provider in ukraine. By doing this, he locked out both my login and Gareths's login and they used this to hijack our emails and reset the login for one exchange (VirWox), enabling them to gain access and steal $12,480 USD worth of BTC. No other exchanges were affected due to either Mult Factor Authentication, OTP, Yubikey's and auto lockdowns.

The hacker was also able to pull a few hours of internal company emails. However due to mandatory PGP encrytion between members of our company and tools like Cryptocat, sensitive information was not breached.
