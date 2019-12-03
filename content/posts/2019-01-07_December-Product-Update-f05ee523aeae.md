---
title: December Product Update
description: "Hello Tokenauts \U0001F44B We’re starting 2019 off with a quick update on how our Product and Engineering team rounded off 2018. We’ve been…"
date: '2019-01-07T19:24:04.033Z'
categories: []
keywords: []
slug: /december-product-update
excerpt: "Hello Tokenauts \U0001F44B We’re starting 2019 off with a quick update on how our Product and Engineering team rounded off 2018. We’ve been…"
layout: post
thumb_img_path: /images/1__QZzleVC1__BZvzYgU87vlqA.png
content_img_path: /images/1__QZzleVC1__BZvzYgU87vlqA.png
---

Hello Tokenauts 👋 We’re starting 2019 off with a quick update on how our Product and Engineering team rounded off 2018. We’ve been working on a two big projects concurrently — first up, getting the Smart Contracts tightened up and pushed to Ropsten, and secondly, working on card KYC and issuance.

If you check out our product timeline @ [ProductPlan](https://app.productplan.com/p/WKmCZlrSDYGGdjB9HtBUJZKA9Cl6PCXD), here’s what’s changed:

1.  Move to Ropsten testnet
2.  TokenCard onboarding and order process

#### **Lifting off on Ropsten**

As our Community is aware, we have been putting a lot of resource into ensuring that our Contract Wallet is robust — putting it through rigorous testing internally and with auditors before shipping. Toward the end of December, we pushed it from our own internal network to the Ropsten testnet!

In a nutshell, this is an incredibly exciting milestone for the team as it allows us to get a feel of how the wallet operates in a live environment. For example, where our own internal network used “Proof of Authority”, Ropsten is secured by “Proof of Work” just like mainnet Ethereum. Moreover, moving to Ropsten will put our app under more stress — it is more erratic and vulnerable to attacks — so will be a real proving ground ahead of our move to mainnet.

For users, this importantly means that you can now [interact with your wallet](https://ropsten.etherscan.io/) on Ropsten using tools such as Etherscan, where you’ll also be able to see the contract [source code](https://ropsten.etherscan.io/address/0xc3c09ac893caa9eb238b6313d943af6c64036427#code). We really recommend that you check out Mischa’s description of the Contract Wallet on [Gist](https://gist.github.com/mischat/ca899c58bca9b89b7a9969c56a7b7b01) for the nitty gritty. Mischa will be putting more information on the contracts out there in the near future — including the full repository and details on a bug bounty.

![Interacting with your TokenWallet on [Etherscan](https://ropsten.etherscan.io/)](/images/1__VTHQrA6TxEW2y5f6lMW7vw.png)
Interacting with your TokenWallet on [Etherscan](https://ropsten.etherscan.io/)

#### **KYC and ordering TokenCard**

As some of our community will already have [seen on Twitter](https://twitter.com/tokencard_io/status/1073543521703993344), we began last month with a working end-to-end onboarding flow for TokenCard applicants! The initial implementation focuses on two parts:

**Step #1**: Selfie verification, address checking, and confirming that you’re good to receive a card.

**Step #2**: Making an API call to our issuer to send the card!

Having this up and running is a big development milestone from three points of view. From a **regulation** point of view, having the onboarding process set-up allows us to do Client Due Diligence (CDD), a process that helps us validate that _you’re you_, and that you can receive a card. From a **tech** perspective, we’ve working with third parties — we’ve chosen to go with _Onfido, Passfort and ComplyAdvantage_ — that best fits with what we’re building now and for the future. Finally, from a **usability** perspective, we’re really excited about the result; an onboarding process that is as frictionless as possible — certainly within the crypto space — and takes just a few minutes to complete!

For now, our goal within Product and Engineering is to continue along the two strands of developing the Smart Contract (we’re looking to do one final audit before pushing to mainnet Ethereum), and getting everything ready on the card side. Whilst this is going on, we’ll be inviting more people into the Token Alpha so that we get as much feedback as we can before applying the finishing touches.

Want to see what all the fuss is about? Sign up to the Token Alpha [HERE](http://eepurl.com/ga21Yn).

Thanks!