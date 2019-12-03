---
title: The Coffee’s on Crypto ☕️ A deep dive into how your TokenCard will work
description: >-
  We’ve spent the past few weeks onboarding the first Tokenauts onto the
  TokenWallet alpha — 300 of you have already got involved, and we’re…
date: '2018-12-11T15:28:14.769Z'
categories: []
keywords: []
slug: /the-coffees-on-crypto-%EF%B8%8F-a-deep-dive-into-how-your-tokencard-will-work
excerpt: >-
  We’ve spent the past few weeks onboarding the first Tokenauts onto the
  TokenWallet alpha — 300 of you have already got involved, and we’re…
layout: post
---

We’ve spent the past few weeks onboarding the first Tokenauts onto the TokenWallet alpha — 300 of you have already got involved, and we’re looking to ramp that number up to 1,000 before the New Year, ahead of our test cards going live (🔌 keep your eyes peeled on Twitter over the next few days for updates on testing)…

We thought we’d take this opportunity to delve under the hood of the upcoming TokenCard, explaining exactly what happens when you spend your crypto, and how TokenCard payments work.

As many of you will already know, there are two parts to the Token equation. There’s the **TokenWallet**, and the **TokenCard**. At launch, your TokenCard will be a debit card, which means that you will need to exchange crypto from your TokenWallet and load your card with fiat before taking it for a spin. Please note that, for the future, we’re working toward integrating “Instant Authorization”, so you could spend straight from crypto to fiat without needing to top up in between.

#### Bridging crypto and fiat: How do we do it?

Let’s say that you want to top-up your TokenCard with 1 ETH worth of fiat from your TokenWallet — here’s what that would look like under the hood.

When you tap “Top Up”, you’re effectively authoring an Ethereum transaction to send 1 ETH from your TokenWallet, to your TokenCard account. This happens in two stages.

Firstly, that 1 ETH is sent to a Token Treasury float (for this to occur, we do some checks to make sure that e.g. you have enough ETH in your wallet). Once this is OK’ed, the second step sees us instructing our issuing partner to send fiat back the other way into your TokenCard account. The fiat will be credited to your account instantly, ready to spend.

![The TokenCard top-up flow, simplified](images/1__5EJSGKCd__er__RiIzv__yodg.png)
The TokenCard top-up flow, simplified

If you’re wondering how we work out the ETH to GBP (or your preferred currency), we will quote you a rate which you can accept or decline before we execute the trade. We’ll always aim to provide a fair and competitive market rate to you.

So you’ve topped up your TokenCard with fiat and want to spend it. Here’s how that happens:

#### Making an everyday payment

You’re starting the morning off with a coffee from an aptly named cafe, Coffee Place (this is known as the “Merchant”). You’re stood in line, shiny new TokenCard in tow. The coffee comes to £3 and you’re asked to put your card in the POS terminal.

You’ve just typed your PIN in, and here’s what happens next.

The Merchant (or more specifically, the POS terminal) creates an Authorization, kicking off the process by which your transaction will be approved or denied. The Authorization is instantly sent up the chain to an Acquirer, a bank that enables Merchants such as Coffee Place to process card payments.

At this point, the Acquirer will vet the transaction (usually on behalf of the Merchant) to see if there are any issues, e.g. to see if _that_ TokenCard is blocked. Assuming all is OK at this stage, the Authorization is sent even further up the chain, to the Card Networks (in Europe, these might include Visa, Mastercard, and American Express).

The Card Networks will generally pass the Authorization straight up the payment chain. This time: to the Processor. The Processor’s job here is to put the final checks in — making sure your TokenCard is active, that Coffee Shop is a legitimate merchant, and that you have £3 for that coffee. The Processor will typically own the ledger of money in and out, plus the balances of different cards — so they have a good grasp on whether or not you can buy your coffee from Coffee Shop.

![The coffee’s on crypto, in just a few seconds!](images/1__Ila4As2qP6r1djon1W3m5Q.gif)
The coffee’s on crypto, in just a few seconds!

Once the Authorization for your purchase is approved — every institution in the chain has given an “all good” message — it works its way back to the POS and “Approved” will flash on the screen. At this point you’re free to drink your coffee, which will still be piping hot, as the whole payment process takes just a few seconds.

#### What makes your TokenCard different

It’s our hope that spending with TokenCard feels familiar in all the important ways, but with an added bit of magic. For instance, you could instead buy your coffee with Contactless, or 3D Secure online payments (as for Apple Pay 🍎, we will not be supporting this initially — we’ll be working with our issuer to support this once cards are out).

If you’d rather pay in cash, you could simply withdraw from an ATM with your TokenCard, much like you would do with your payment cards today.

But we also differ from traditional money in a lot of ways.

When you exchange crypto from your TokenWallet into fiat in your TokenCard account, you have the security and peace of mind of locking in the rate you get, so there are no surprises when it comes to market movement. It’s also more economical in terms of Gas costs, as there are fewer computational processes involved in topping up, compared with making a number of smaller transactions on food and travel throughout the day.

And when spending, you’re always in the know _as it happens_. For every transaction, we’ll instantly debit your account and update your TokenCard — so when you spent your £3 at Coffee Shop in the example above, you’d be able to see your remaining balance instantly. With most traditional banks, it could take up to 72 hours to see this information.

So there you have it. When topping up your TokenCard, and spending it day-to-day, a lot goes on under the hood. For now, if you’d like to get involved in the Token Alpha, keep your eyes peeled [**@tokencard\_io**](https://twitter.com/tokencard_io) this week… 👀