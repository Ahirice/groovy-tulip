---
title: >-
  Overcoming Ethereum’s current UX, privacy and scalability limitations to
  redefine trust
description: >-
  What's next for Ethereum? Once progresses are made on privacy, UX and
  scalability, we're in for a complete redefinition of what trust…
date: '2019-07-09T10:46:48.144Z'
categories: []
keywords: []
slug: >-
  /overcoming-ethereums-current-ux-privacy-and-scalability-limitations-to-redefine-trust
excerpt: >-
  What's next for Ethereum? Once progresses are made on privacy, UX and
  scalability, we're in for a complete redefinition of what trust…
thumb_img_path: images/1__fEszowUMiJczj7N22OM2eg.jpeg
content_img_path: images/1__fEszowUMiJczj7N22OM2eg.jpeg
layout: post
---


On June 26, ConsenSys held a fascinating discussion addressing Ethereum's past, present and future: “Ecosystem For Next Generation dApps & What’s Possible on Ethereum Now” ([details](https://www.eventbrite.com/e/ecosystem-for-next-generation-dapps-whats-possible-on-ethereum-now-tickets-63444399908#)). After the usual introductions, the panellists discussed Ethereum’s current limitations and how to overcome them.

The questions of the audience and the host, Rune Bentien from ConsenSys led us through a discussion clearly highlighting the link between the UX, privacy and scalability issues.

### Meet the panel

The panel was well balanced, with builders from different Ethereum projects:

*   [Mischa Tuffield](https://twitter.com/mischat) is the CTO of [TokenCard](https://tokencard.io/), a participatory banking solution offering the only non-custodial smart contract wallet paired with a debit card.
*   [Christine Perry](https://twitter.com/christineRPM) started as dApp developer, became frustrated by the current clunkiness and speed of Ethereum and decided to do something about it by joining [SKALE Labs.](https://skalelabs.com/)
*   [Raphael Mazet](https://twitter.com/raph_alice) — started his career as a lobbyist, trying to create an advocacy platform for citizens. He realised that transparency was necessary to raise money for social funding, so he co-founded [Alice](https://alice.si/), a blockchain-powered platform for transparent social impact.
*   [Joe Andrews](https://twitter.com/jaosef) is the Product Lead of the leading privacy solutions on Ethereum, the [Aztec Protocol](https://www.aztecprotocol.com/).
*   [Alex Batlin](https://www.linkedin.com/in/batlin/) is the founder and CEO of [Trustology](https://www.trustology.io/), a custodial wallet solution geared for institutional and high-value investors.

![Ecosystem For Next Generation dApps & What’s Possible on Ethereum Now — at ConsenSys London’s offices](images/1__GMk1yzMD7b9WppwPIVf7AQ.jpeg)
Ecosystem For Next Generation dApps & What’s Possible on Ethereum Now — at ConsenSys London’s offices

///**Disclaimer**: You’ll find below my (Brice from TokenCard) notes from the event, organised into a few main themes. Keep in mind that this was a panel discussion, and some adjustments were necessary to make it readable. I reached out to each speaker before publishing the article to make sure the content presented here matched their vision.///

### Alex Batlin: trustlessness VS UX?

Before we jump into Ethereum, our main topic today, let’s start with a common theme of the discussion: trust.

Alex presented a fascinating perspective addressing Ethereum and DLTs’ impact on current trust paradigms. In his view, we could say that **banks are “mass producers of trust”**: they offer the same standardised agreements to many, and so far people feel mostly safe in their relationship with their banks.

However, **innovation is being stifled by the mass production of trust**: not everyone fits one of the few boxes offered by their bank or insurance service. That’s precisely where Ethereum and smart contracts can play a role. They enable **a new paradigm for trust: the “mass customisation of trust”**.

As Alex noted, we are all making weird assumptions about trust: for instance, we tend to trust a Ledger Wallet to safeguard our cryptos, despite having little visibility over their software stack. We feel safe, even if the UX is unsatisfying: we trade usability for security.

> We have to be pragmatic about what we mean by trust

Alex assets that we don’t have to be purists about completely removing the need for trust in the services we use, as it often comes at the expense of UX. The goal is not zero-trust but **enough trust minimisation for the users to be comfortable using the service.**

He thinks decentralisation matters to avoid arbitrary central control (as we can see on centralised social networks) yet it cannot preempt the UX, which is a necessity for adoption.

### Raphael Mazet: How to nurture trust?

As an ex-lobbyist now working on Alice, a solution using blockchain to bring more transparency to social funding, Raphael holds a practical and exciting take on trust in the context of solidarity.

![[Alice](https://alice.si/)](images/1__xc4h1r1lqQtWT6OBb1tKog.png)
[Alice](https://alice.si/)

He presented Alice’s solution to solve the issue of the lack of trust in Non-governmental Organisations (NGO)s: **how to achieve complete transparency when collecting donations and realising projects?**

On stage, he introduced a test project providing free school lunches to kids in Uganda. **Transparency is achieved by a mix of on-chain solutions and traditional authority figures (teachers)**. Here’s how it works:

Each teacher is provided with a smartphone that includes a cryptocurrency wallet; the children get an NFC-enabled chip as their own wallet.

In the morning, when the kids arrive at school, they load their wallet by tapping their NFC-chip on the teacher’s phone. They each pick a kitty that acts a 2FA mechanism. At lunch, they tap their NFC-chip again on the payment device to cover their expenses.

While the solution is still being worked out, it’s already quite elegant as it provides a **fully auditable trail**, on chain. Indeed, people who donated to the NGO can see:

1.  If the kids went to school, when they arrived and how many of them were there (when the teachers load their wallet in the morning).
2.  How many kids are getting their lunch and when (the spend transaction on the kids’ wallet)

### Mischa Tuffield: The bank you don’t need to trust

Rather than nurturing trust, can we simply abstract it? Through his experience with TokenCard, Mischa expanded on the paradigm shift Ethereum enabled: the ability to develop **services that do not require their trust**, and yes, even a bank alternative!

> Regulations are here to ensure the absence of systemic risk for society.

![[TokenCard](http://tokencard.io)](images/1__N__FypNtfHizWhru7n7pFZw.png)
[TokenCard](http://tokencard.io)

While developing a trustless service comes with additional complexity, it also provides several unique benefits:

*   Since no one but the user can access its funds, it **eliminates the possibility of an insider attack**, be it caused by a rogue employee or a brutal change of policy after a company buyout.
*   In terms of regulation, being non-custodial is an advantage. As Mischa states it, regulations are here to “ensure the absence of systemic risk for society”. In that sense, regulators are enthusiastic about a reserveless bank — since it’s **a bank that poses no threat to its users’ funds**.
*   However, being non-custodial is not sufficient to solve the issues with current banks. Indeed, trust minimisation involves going even further. He asserts that providing a **participatory experience** and exploring new revenues structures is key to bridging the gaps with users.
*   To ensure the experience provided by TokenCard is participatory and inclusive, TKN (TokenCard's native token) is a **protocol token**. Each usage of the service contributes to backing the token and holders can claim their share of the revenues generated.

### Joe Andrews: Privacy is necessary for UX

Joe developed a very pragmatic take on the necessity for privacy: instead of coming at it from a maximalist perspective; he pointed out **the usability issues that stem from a lack of privacy.**

> What happens if you want to get your salary on chain?

Indeed, the transparency of Ethereum’s blockchain is welcome when it’s used to track NGO contributions, but what happens if you want to get your salary on chain?

Do you simply accept that your employers and your colleagues will be able to see what you do with it? What about the people you transact with, in your daily usage of Ethereum? Are you comfortable sharing your whole transaction history with them?

![[Aztec Protocol](https://www.aztecprotocol.com/)](images/1__VwfwPChd52uu7a8HlPcVXA.png)
[Aztec Protocol](https://www.aztecprotocol.com/)

Aztec provides a solution to address these issues. The protocol offers an implementation of zero-knowledge transactions along with stealth addresses to provide full anonymity on Ethereum. It can be used to create confidential representations (called “notes”) of existing digital assets.

However, as Joe pointed out, **fixing the lack of privacy on-chain is not sufficient**. Privacy is an issue that starts from the very first purchase of cryptocurrencies. Most holders had to pass and submit official documents (KYC) to exchange services, with little to no visibility on how their personal data is handled.

### Mischa, Christine & Raphael: Ethereum’s limitations

As Mischa mentioned, when overcoming privacy issues, Ethereum developers still have to solve another significant blocker when bringing their app to the market: gas costs. While developers understand the necessity to pay for network costs, a problem arises when **there is no predictability over that cost.**

Indeed, **the Ether (ETH) price is not stable, which increases the complexity of managing gas**. Developers have a hard time predicting the marginal costs of what they are building, as there are two distinct factors affecting transaction cost:

1.  The overall network usage: a fast transaction can cost anything ranging from 5 to 20 gwei depending on the current network workload.
2.  The changing price of ETH: since gwei is a denomination of ETH, its value follows the same price fluctuations as ETH.

Together, these factors can lead to massive fluctuations in the cost of a given operation performed at two different times.

However, it’s not all grim for Ethereum! As Raphael demonstrated, a lot of progress has been made in a couple of years, and **it’s now easier than ever to develop new projects on Ethereum** thanks to the protocols and frameworks built by the community.

### Christine Perry: Building for a dApp dev

The Ethereum ecosystem now realises how critical UX is. Usability is still sub-par, considering that the onboarding of any dApp requires the user to have Metamask and some ETH, which currently translates to **dozen of steps before a crypto-newcomer can get started**.

However, as seen before, Ethereum’s usability issue is dual:

1.  We need a quick, convenient and easy way to onboard users on dApps.
2.  We also need a streamlined onboarding for dApp developers who have to deal with both their users UX issues and their dApp scalability problem.

![[SKALE Labs](https://skalelabs.com/)](images/1__A1PWvssjo8tvfXEjewlDyA.png)
[SKALE Labs](https://skalelabs.com/)

To ease scaling up a dApp, SKALE Network, a layer-2 solution, provides developers with sidechains that are fully decentralized, have high throughput, and are configurable to the needs of the dApp. Importantly — SKALE is very easy to deploy to and allows to scale smart contracts, run decentralized on-chain storage, and much more.

### Alex: Trust in a B2B context

To conclude, let’s go back to the chronology of our event. The last question addressed to the panel was about B2B — an audience member wanted to know the potential of blockchain in that setting, and the current usages. Since Trustology was the most B2B-focused company in the panel, Alex tackled this one and provided yet another insightful perspective.

![[Trustology](https://www.trustology.io/)](images/1__h6jqkD__fE5zYRaIko__DRCw.png)
[Trustology](https://www.trustology.io/)

He thinks that **DLTs excel at minimising/eliminating the trust required by different participants to transact and work with one another**.  With that in mind, he sees massive potential for DLTs in the international trade settlement as it provides an elegant solution to the problem of trust between geographically disparate corporates.

> The traditional international markets are not efficient at all

Indeed, as Alex pointed out, the traditional international markets are not efficient at all. **It takes around ten years to bring a financial product like a security to the market**. On the other hand, DLTs can slash both the cost and the delay of launching a security and other financial product, all around the globe.

We hope this article helped you understand the current limits and what's next for Ethereum. To go further, you can watch the full panel discussion here \[1:36:00\]:

If you are in London, you can check the next events organized by ConsenSys, here:

[**ConsenSys (@ConsenSys) | Twitter**  
_The latest Tweets from ConsenSys (@ConsenSys). ~Not giving away ETH~ Blockchain studio building decentralized…_twitter.com](https://twitter.com/ConsenSys "https://twitter.com/ConsenSys")[](https://twitter.com/ConsenSys)

See you in Ether!

— Team TokenCard

**\-** [**🕸 Website**](https://monolith.xyz/) **|** [**🐦 Twitter**](https://twitter.com/monolith_web3) **|** [**🎮 Discord**](https://discord.gg/GN6gGEP) **|** [**👽 Reddit**](https://www.reddit.com/r/Monolith_Web3/) **|**[**✈️Telegram**](https://t.me/Monolith_Web3) **-**