---
layout: post
title:  Team Finance
date:   2022-10-27 08:29 -0700
categories:
- smart_contract
network:
- Ethereum
amount: 15_800_000
link: https://rekt.news/teamfinance-rekt/
---

Lost $15.8M, of which $7M were recovered. Exploit due to pool migration function bug.

> @TeamFinance_ was exploited in https://etherscan.io/tx/0xb2e3ea72d353da43a2ac9a8f1670fd16463ab370e563b9b5b26119b2601277ce, leading to the loss of ~$15.8M for the protocol:  $11.5M (V2_USDC_CAW)+$1.7M(V2_USDC_TSUKA)+0.7M(V2_KNDX_WETH)+1.9M(V2_FEG_WETH).
> The protocol has a flawed migrate() that is exploited to transfer real UniswapV2 liquidity to an attacker-controlled new V3 pair with skewed price, resulting in huge leftover as the refund for profit. Also, the authorized sender check is bypassed by locking any tokens.
> The initial fund (1.76 ETH)  to launch the hack is withdrawn from @FixedFloat.

- [Peckshield Thread](https://twitter.com/peckshield/status/1585587858978623491)
- [Attack Tx](https://etherscan.io/tx/0xb2e3ea72d353da43a2ac9a8f1670fd16463ab370e563b9b5b26119b2601277ce)