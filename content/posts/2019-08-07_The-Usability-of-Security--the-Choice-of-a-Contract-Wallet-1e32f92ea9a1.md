---
title: 'The Usability of Security: the Choice of a Contract Wallet'
description: How to design a wallet that stands the test of time? Make it smarter!
date: '2019-08-07T15:39:23.900Z'
categories: []
keywords: []
slug: /the-usability-of-security-the-choice-of-a-contract-wallet
excerpt: How to design a wallet that stands the test of time? Make it smarter!
thumb_img_path: images/1__zup3ifzvGX5hSsS2NWtGhQ.jpeg
content_img_path: images/1__zup3ifzvGX5hSsS2NWtGhQ.jpeg
layout: post
---


To hold cryptocurrency and interact with the decentralized services available on Ethereum, one needs a wallet. While the core features of a wallet seem pretty obvious (send and receive, duh!), the challenge lies with the implementation details. Just like a planes guidance system, a wallet is mission-critical software: it cannot stand a single failure, considering the dramatic consequences.

There are essentially two types of wallet with different ways to hedge against hacks, failure, or users’ negligence:

_ℹ️ Custodial (vs non-custodial) refers to who is actually keeping the funds. Are you the sole owner of your assets? -or are you trusting someone to safekeep them for you?_

1.  **Custodial wallets** focus on the user experience above all. Their UX is generally quite good, and they go as far as to include advanced asset recovery features in most instances. However, since you’re giving away the ultimate control of your currencies to the service provider, there are some risks. Namely — if they disappear, so does your money.
2.  **Non-custodial wallets** focus on staying decentralised and keeping the user in control. The user has ultimate control over their money, which hedges against hacks or the service provider disappearing. The flip side to this is that a greater responsibility rests with the user. Since the user is the sole owner of the private key, the service provider cannot help them recover access to funds should they lose them.

The reality is a little bit more nuanced than this dichotomy. There is a third type of wallet, which supports the integration of more safety and recovery features while keeping the whole process non-custodial and decentralised: **smart contract wallets**.

The idea is actually quite simple: you remain the sole owner of the keys, however, it’s possible to implement some logic as to the how, when, and to whom the funds are moved. Going a step further, you could even envision time/action-based fund recovery methods where you don’t lose access to your money even if you lose access to the seed.

### Standing the test of time

The Monolith smart contract wallet is professional-grade at its core; resilient enough to hold your funds without ever failing. Though this level of high security at a contract-level is already a feat, **safe & continuous access of our users to their funds for decades to come** is only the baseline.

To fulfil this vision, we need to **go farther than code**. We need to consider all the attack vectors, including those created by social engineering, or life’s risks, and hedge against them. Can an attacker empty the whole wallet as soon as he gains access, even if his transactions are obviously suspicious? What happens if one of our users loses his seed phrase? What happens if one dies?

All these edge-cases are eventually bound to happen to our users. Though we’re not saying we are ready to challenge death just yet —we’ve taken many situations into consideration on a product-level. The challenge for us is in avoiding any offering which would involve some form of custody over users’ funds, which is fundamentally against our principles and vision.

Which leads us to today’s topic — the choice of a contract wallet — an elegant solution which increases the overall safety of users’ funds while still keeping the product decentralized and non-custodial.

### The Benefits of a smart contract wallet

Since smart contract wallets bring the functionalities offered by smart contracts while replicating those of traditional wallets (access & transfer funds), the possibilities become near-endless. We will dive into the main one we’ve implemented and are exploring here at Monolith.

### Fund safety is paramount

There are essentially two ways to go around increasing users fund safety with a smart contract wallet. You can either reduce the number of assets exposed if a breach was to happen or provide additional features to recover funds if the seed phrase is lost. Even better, you can do both!

#### A/ Protect assets, even if the access is compromised

To reduce the exposure in case of attacks while preserving usability, we currently have two main features live and implemented in the contract wallet:

1.  **The Daily Limit** specifies a maximum daily limit for the entire contract. The amount can be denominated either in ETH or fiat currencies (using an oracle).
2.  **Address Whitelisting** defines a list of trusted addresses that are not affected by the daily limit. Any address (up to 5) can be used.

**Together, these two simple mechanisms greatly reduce the potential impact of an attack.** In a worst-case scenario, even if your seed was compromised, the daily limit restricts the damage that can be done on the first day of the attack. By then, you’ll have found out about the compromise, and will have moved your assets out quickly thanks to the whitelisted addresses.

#### B/ Recover lost assets

While the solutions we presented so far are well-conceived and efficient, they don’t solve the million-dollar problem: **what happens when a user loses his seed, be it by death or negligence**? So far the answer has had to do with the custodial vs non-custodial debate.

Since custodial wallets have access to users’ funds, they can sometimes provide a solution for this issue. The user (or his family) can re-verify his identity in the hopes of recovering the funds. On the non-custodial side, we couldn’t really do much better than a “Sorry, that sucks!” until very recently.

Indeed, having a **contract wallet opens an array of possibilities to finally solve this challenge without requiring custody over users’ funds.** We’re now seeing the light at the end of the tunnel and studying the different methods we could use to offer a credible answer to this issue.

One of the most promising is the [dead man’s switch](https://blockonomi.com/cryptocurrency-inheritance/#Dead_Mans_Switch).

Through regular usage of the wallet (such as a card top-up), users will be automatically sending “keep-alive” signals. If they don’t, the contract assets can be recovered on another address, as defined in the contract. With this mechanism, the assets can be safe even if one forgets or loses one’s seed phrase.

### The price of sovereignty

When it comes to downsides of contract wallets, there are two key issues which arise.

The first is the increased complexity involved in the development of decentralised applications (compared to a centralised/custodial solution).

The second is the gas costs: since everything happens on chain (including the contract deployment), there will inevitably be an Ethereum transaction cost attached. Depending on the operation, the cost can vary with the initialization transaction (required to deploy a new instance of the contract wallet) being among [the most costly.](https://hackernoon.com/costs-of-a-real-world-ethereum-contract-2033511b3214)

### Make it yours!

Now, here’s the coolest part about contract wallet: **you don’t have to handle all the minutiae of the deployment on your own.** Someone else can give you the tools to do it by yourself, and streamline the process.

While onboarding the Monolith app, we walk you through it. The only thing we ask of you is to write down and secure your seed; once it’s done the contract deployment is seamless and takes just a single tap.

![TokenCard app contract wallet deployment](https://cdn-images-1.medium.com/max/800/1*ZRvdZFVobMr0vi051B3vCg.gif)

While this doesn’t look like much from the pure app perspective, what happens in the background is quite awesome:

1.  You secure a seed that only you know,
2.  Thanks to the seed, you can sign your contract initialisation,
3.  You now have access to a smart contract wallet where you are in sole possession of the seed.

_ℹ️ We mentioned the gas cost of this transaction earlier. In our current process, we decided to cover it to streamline the user experience._

### Surviving its own disappearance

We insisted quite a bit on the non-custodial dimension of our service: we share **a conviction that you, and only you, should be able to control your assets.** Despite a price paid in terms of additional responsibility, it comes with many benefits, including one big we haven’t covered yet.

… You own your keys, which means no worries, ever! Yes, even if Monolith was to disappear, you could simply input your seed in another service and move your assets around.

[➡️ Get started with Monolith](https://monolith.app.link/0Jvily1Co1)

All things considered, this is the core benefit of decentralised and non-custodial services: you don’t have to trust anyone, not even the service provider. We don’t know about you, but to us, this is what DeFi looks like.

If you are curious about the underlying mechanics of our contract wallet, feel free to check [the code and the audits on GitHub](https://github.com/tokencard/contracts).

— Team Monolith

**\-** [**🕸 Website**](https://monolith.xyz/) **|** [**🐦 Twitter**](https://twitter.com/monolith_web3) **|** [**🎮 Discord**](https://discord.gg/GN6gGEP) **|** [**👽 Reddit**](https://www.reddit.com/r/Monolith_Web3/) **|**[**✈️Telegram**](https://t.me/Monolith_Web3) **-**