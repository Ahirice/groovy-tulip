---
title: The age of the Consumer Contract Wallet
description: Today the Token team shows you what the future holds.
date: '2018-05-02T16:50:52.534Z'
categories: []
keywords: []
slug: /the-age-of-the-consumer-contract-wallet
excerpt: Today the Token team shows you what the future holds.
layout: post
thumb_img_path: /images/1__ZRJwzx9DrheMyVp__4r95hA.png
content_img_path: /images/1__ZRJwzx9DrheMyVp__4r95hA.png
---
---

Big things need to change for Ethereum to enter the global consciousness.

The world we are building towards will see users own assets of all classes from the tangible to the intangible. These assets will manifest themselves in the form of various token protocols on the Ethereum network. In the future all tokens from those that represent your PlayStation, your house and your gold to tokens that represent voting rights and even your own identity, will be held in your \[Token\] wallet, with functionality unimaginable today.

**In this future the user cannot be permitted to run any risk of losing their assets, however careless they might be.** The world as it exists today is no where close to this; all storage solutions suffer from critical vulnerabilities and severe compromises.

> We identify this risk as one of the core problems preventing the further proliferation of the technology into the mass market.

_Token is on the verge of launching the next gen platform that tackles these issues head on. The need for a wallet that reduces risk of loss to close to zero is paramount._ **_We’ve built it, it’s about time, it lies as the heart of our platform, and it’s called the Token Wallet._**

### Legacy wallet types and core weaknesses

Today there are roughly 4 ways to store digital assets. **None are ideal:**

#### Type 1 — Keypairs

The defacto and most raw method of storage, a **keypair**, if compromised does nothing to prevent an attacker from taking every last Gwei. The root of much worry and sleepless nights for big hodlers. Keypairs also don’t offer any recourse or protection if the user loses or forgets their seed. I have old friends who’ve lost [dearly](https://www.coindesk.com/early-bitcoin-adopter-calls-multi-sig-solutions-750-btc-theft/) because of keypair shortcomings, and we don’t wish this on anyone.

#### Type 1b — Hardware wallets

**Hardware wallets** essentially airgap a keypair, they offer an increased level of security but at the expense of usability with a high barrier to entry. They fall short in bringing crypto to the masses and frankly we will probably never see regular users walking around with ledgers dangling around their necks.

They are nice, but ultimately half-way solutions and symptoms of a larger problem. Our goal is enable anyone, anywhere to join this revolution and be properly setup in minutes not days with no upfront cost.

#### **Type 2 — Multi-sig wallets**

**Multiple signature wallets** (Multi-sig), require multiple keys (ideally different people or companies) to sign a transaction before it can be completed.

On Ethereum this functionality has been recreated with smart contracts. The Ethereum Foundation, Consensys, Gnosis, and (tragically) Parity, have all built their own implementations.

These **Institutional Contract Wallets** are designed to serve projects or companies that hold large amounts of funds and need to share and limit control internally. **They are not at all suitable for regular users, in addition to being notoriously hard to use.**

_Sidenote: even custodial counterparties like_ [_BitGo_](https://www.coindesk.com/bitfinex-bitcoin-hack-know-dont-know/) _cannot be relied upon._

#### Type 3 — Custodial wallets

The _inadequacy_ of the above storage types, as well as _laziness_ and _consumer apathy_ drives many to store their funds in the control of third party, primarily exchanges. These **custodial wallets**, become large centralized targets for attackers. _Withdrawal issues, fractional reserves and catastrophic loss are still all too_ [_common_](https://en.wikipedia.org/wiki/Cryptocurrency_and_security#Exchanges) _in the industry._ Trust is often misplaced.

Finally, custodial wallets undermine the point of cryptocurrency to little benefit. Being in control of your own funds is one of the things that makes the tech so powerful. Exchanges serve largely as storage for less sophisticated users, only a small percentage of funds they store are actually exchanged. **It should thus be considered an embarrassment to our industry that we are incapable of building an attractive, yet technically sound consumer product.**

> Quite simply put, crypto users will experience that “what if” sense of paranoia you get thinking about your funds just sitting there on an address or on an exchange. Over the years I’ve felt it more times than I dare mention. One day you might log in and it could all be gone; somewhere something might have gone wrong. Profound change is needed.

![Upcoming London Underground release](/images/1__Xcyx96Br4emBaf6QwUyxfA.png)
Upcoming London Underground release

### Token Wallet: The First Consumer Contract Wallet

**Globally Distributed Digitally Embedded Immutable Security in the form of Ethereum smart contracts is the final frontier.** It literally cannot get better than this. We expect attacks on crypto users and platforms to become more sophisticated as time goes on. The need has never been bigger.

Today we put forth our proposal for the first consumer grade smart contract wallet. It has been designed to hold a user’s ETH and tokens, and it governs its own security with simple to understand rules configured by the end user. These rules are directly programmed into the smart contract and are enforced by the EVM.

The Token Wallet is the first of what we call Consumer Contract Wallets for the masses. It has been engineered to meet the following design requirements:

1.  To greatly reduce risk of an attacker draining assets
2.  To prevent asset loss in the case of user negligence (e.g. key loss) \[v0.2 feature\]
3.  Allow users to be the only custodians of their own funds
4.  Eliminate need for expensive physical hardware
5.  Retain actual usability of funds (not locked up and practically inaccessible)
6.  To do all of the above from within a consumer grade mobile UI

![Part of the whitelisting process. First image shows the bottom of the main view with a smart contract security overview. (Images are of a pre-release version and are unbranded)](/images/1__ZRJwzx9DrheMyVp__4r95hA.png)
Part of the whitelisting process. First image shows the bottom of the main view with a smart contract security overview. (Images are of a pre-release version and are unbranded)

### **v0.1 high level spec**

Version 1 will allow a user to call the following functions on their contract:

**Address Whitelisting**

*   This function allows the user to enter into their smart contract wallet a few addresses that they trust as safe withdrawal destinations. The smart contract will then allow uncapped withdrawal to _only_ these addresses.
*   These addresses could be anything the user trusts from an exchange address, to a backup in a safety deposit box to their mums wallet.  
    Any time they want to withdraw an amount that exceeds the Daily Limit (see below) they will have do so to one of these addresses.
*   These addresses can only be written _once_ by the user to their contract and cannot be changed until v0.2 lands.

**Daily Limit**

*   For all non-whitelisted destinations the user can specify a maximum daily limit for the entire contract. This effectively allows the user to restrict the amount leaving their wallet to a desired amount per day.
*   The amount can be denominated in fiat with the use of a basic oracle (ex. $500/day). Future versions might allow limits in absolute values (ex. 1 ETH/day), in percentages (ex. 5%/day). But we believe fiat denominations to be a better UX.

#### **Hypothetical Scenario: Alice ($25k in ETH)**

Alice was negligent of her seed and an attacker gains access to it. The attacker is attempting to withdraw funds from Alice’s contract wallet.

Alice’s whitelist prevents the attacker from withdrawing all funds to themselves. The attacker stands to gain nothing from withdrawing to Alice’s addresses. The attacker is thus limited to the Daily Limit, which Alice had set to $1000/day.

Upon Alice being informed of the illegitimate withdrawal of $1000 in ETH, she then withdraws the rest of her assets ($24k) to one of her whitelisted addresses.

Dramatic loss was prevented and Alice learnt a fair lesson, she creates a new seed and moves on. In all traditional wallets as well as hardware wallets, Alice’s funds would have been completely drained.

> **We believe that purest technical solution and the most intuitive user experience are not mutually exclusive.** _At Token we strive to benefit the layman as well as the veteran hardened crypto nuts (like ourselves). We are excited to announce the Token Wallet and we can’t wait to put it in your hands so that you can help us iterate towards building the foundations for the future of crypto._

![Let’s hunt some bugs..](/images/1__Y9eq20Al3fa1grqyvqZMgA.png)
Let’s hunt some bugs..

#### Practical notes:

*   We will demo _things_ at Money2020 (so come)
*   The early Alpha for the Token Wallet will be available for download the week after Money2020
*   Starting next week users will be coming into our offices to test the app in person
*   Token Card launches once we are confident in the integrity of the app

#### Discussion and questions we want answered (eventually):

*   We want to learn a lot in the coming weeks (and months) about how we should go about things
*   This app will be riddled with bugs, this is fine, let’s hunt them together. We will rapidly iterate and improve through the app together with your help
*   The first version of the contract wallet is not perfect. The user-set rules might not be the ultimate ones. We are aware of this. In order to build the best we need your feedback.
*   The blogpost above details the ultimate vision for Contract Wallets being the holy grail of storing funds. It will take many iterations for us to reach this vision.
*   The introduction of a new standard does not go without its hurdles. It took users close to a decade to get used to the idea of a wallet with keys to store your crypto. We are now trying to get them to move to the next get with a Contract Wallet.
*   How do we reduce the learning curve and make sure that people understand?
*   Do people even care about understanding what is going on under the hood?
*   Should we have a more modular approach where the user chooses to deploy themselves?
*   The integrity of the code is paramount to us. Audits are planned, and we will painstakingly go through many version, much testing, large bug bounty programs before we are confident to label our system 1.0

Through all of this, with your help, five years from now it should be unthinkable for anyone to store their digital assets in something other than a smart contract wallet. Let’s get there together and ride this dragon into the sunset.

Much love ❤

~ Token Team

**\-** [**🕸 Website**](https://monolith.xyz/) **|** [**🐦 Twitter**](https://twitter.com/monolith_web3) **|** [**🎮 Discord**](https://discord.gg/GN6gGEP) **|** [**👽 Reddit**](https://www.reddit.com/r/Monolith_Web3/) **|**[**✈️Telegram**](https://t.me/Monolith_Web3) **-**