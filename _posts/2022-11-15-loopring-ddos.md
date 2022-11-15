---
layout: post
title: Loopring DDoS
date: 2022-11-04 21:00 -0800
categories:
- cloud_infrastructure_breach
link: https://loopring.org/#/post/loopring-ddos-attack-post-mortem
---
DDoS attack on Loopring L2 chain. The Loopring gateway on AWS was targeted.

> On November 4 (GMT+8) at 21:00 hrs Loopring was targeted with an aggressive DDoS attack. During the incident, the rate per second (RPS) was significantly increased. The Loopring gateway was unable to handle such an overwhelming volume of requests resulting in the unavailability of the services.
>  22:07 Nov 4th Loopring contacted AWS security engineers for additional support.
> This DDoS attack only prevented Loopring from providing external services; it had no impact on the security of assets on Loopring. During the attack, the Loopring relayer continued to generate ZKP blocks and submitted them to the Ethereum blockchain.
> This event served as a good reminder to devote additional resources and layers of protection by leveraging AWS services. Loopring, in coordination with AWS, will implement a more robust security architecture for future challenges.
> The majority of Loopring's external services are built on AWS. Loopring will leverage AWS's security capability to better mitigate future potential security threats. Following this incident, Loopring will work more closely with AWS to identify risks and deploy improved shielding and protection, ensuring that our customers receive a robust service.