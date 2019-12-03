---
title: "How-to: Interact with your TokenWallet using Etherscan \U0001F4F9"
description: "Hi Tokenauts \U0001F44B In this post we’ll walk through a couple of the ways in which TokenAlpha users can interact with their TokenWallet using…"
date: '2019-02-05T15:05:11.139Z'
categories: []
keywords: []
slug: /how-to-interact-with-your-tokenwallet-using-etherscan
excerpt: "Hi Tokenauts \U0001F44B In this post we’ll walk through a couple of the ways in which TokenAlpha users can interact with their TokenWallet using…"
thumb_img_path: images/1__x3z8zbGMhf4Le4OVmdVXqA.jpeg
content_img_path: images/1__x3z8zbGMhf4Le4OVmdVXqA.jpeg
layout: post
---


Hi Tokenauts 👋 In this post we’ll walk through a couple of the ways in which TokenAlpha users can interact with their TokenWallet using tools such as Etherscan and Metamask.

The powerful thing about this is that it really reflects our commitment to the **decentralised** aspect of what we’re building here at Token — we are indeed a means to store and access your funds, but if we were ever to go away, you’d still be able to access and interact with your wallet all the same. We’re really excited to show you this in practice!

In this post, we’ll be doing a couple of things using the “**Write Contract**” feature on Etherscan ⬇️

*   Transferring funds to a wallet of our choice
*   Filling up the TokenWallet Gas Tank

You’ll need a few things to get started ⬇️

*   Your TokenWallet with some ETH loaded in
*   [**Metamask**](https://metamask.io/) installed on your browser
*   [**Etherscan**](https://ropsten.etherscan.io/) open on your browser

### Connecting to Metamask

If you’re a TokenWallet Alpha user and have already deployed your Contract Wallet in the app, getting connected to Metamask takes no time at all. To connect, simply install the Metamask extension to your browser (at [**metamask.io**](http://metamask.io)) and make sure you’re connected to the Ropsten Test Network.

To log in, look out for “import account using seed phrase” — click this and enter your TokenWallet’s seed phrase. Wondering where to find your TokenWallet’s seed? Head to the “More (. . .)” tab in the app and tap “Backup Seed” to reveal it.

![Enter your seed phrase on this screen ⬆️](images/1__Z0jPFjXjnhOtwobyvJ38Pg.jpeg)
Enter your seed phrase on this screen ⬆️

Once you’ve connected your wallet to Metamask, you should be able to see an ETH balance — if you’re wondering why this balance is different to the balance on your TokenWallet, that’s because Metamask reads the Gas Tank’s balance, rather than your Contract Wallet. This is super important, as it means that your funds are better protected should your Gas Tank ever be compromised.

Go ahead and name your wallet in Metamask — we called ours “TokenCard #1” — and you’re good to go.

So you’re set up with Metamask and the TokenWallet — what’s next? We’re going to make use of Etherscan’s “Write Contract” feature to send some ETH!

![Metamask wallet and TokenWallet side-by-side ⬆️](images/1__YcVDNL2qq__J__3ZfyEZzb__A.jpeg)
Metamask wallet and TokenWallet side-by-side ⬆️

### Getting started with Etherscan

Open up a new window and head to [**ropsten.etherscan.io**](https://ropsten.etherscan.io), the version of Etherscan on the Ropsten test network. The first thing you’ll need to do is grab your wallet address from the app (highlighted below) and paste this into the search bar on Etherscan — this will load up the info on your TokenWallet.

In the example below, we’re using a newly deployed wallet, so we’ve got a blank canvas to play with. Before that, here’s a quick intro to some of the tabs on Etherscan:

**Code**: This is where you can view your Smart Contract source code — we’ve published and verified ours on Etherscan for you to check out.

**Read Contract**: This is where you’ll be able to query your Contract Wallet, checking for example if you have a certain address whitelisted.

**Write Contract** ᴮᵉᵗᵃ: This is where you’ll be able to execute transactions on your TokenWallet, for example topping up your Gas Tank. We’ll be using this today…

![Viewing your wallet in Etherscan ⬆️](images/1__AncG5XHw5781a5b5DpaVrw.jpeg)
Viewing your wallet in Etherscan ⬆️

### Send ETH to another wallet

Let’s get started by sending ETH from our wallet to another wallet! To do this, head to the **Write Contract** tab on Etherscan.

You’ll need to click “**Connect with Metamask**” in order to authorise transactions (safety first!) — we logged in earlier, so all we need to do is confirm that we’re happy to execute transactions.

![Connecting Etherscan to Metamask ⬆️](images/1__mRu1CayaKRAh6mQPrcoB__A.jpeg)
Connecting Etherscan to Metamask ⬆️

From there, head to **Transfer **— this is the name given to sending ETH through your TokenWallet — and fill in the details of your transaction:

**\_to**: The address of the wallet you’d like to send ETH to.

**\_asset**: As we’re sending ETH, we’ve put “0x0” into here.

**\_amount**: How much ETH you’d like to send. Etherscan requires that you input the value in Wei, which is the smallest denomination of ETH — sending 1 ETH would mean that we’d need to type in 1000000000000000000.

Once you’ve written in the values of your choice, click “**Write**”, and that’s it! You’ve just sent ETH from one address to another without needing to use your TokenWallet app. Even better, you’ll still be able to see the transaction in the “**Transactions**” tab in the app.

![Writing your first transaction 🎉](images/1__T86jZUPExOhcuRYxSoSX3w.jpeg)
Writing your first transaction 🎉

### Topping up your Gas Tank

Now that you’ve sent some ETH, next up is topping up your TokenWallet Gas Tank.

In the same way as sending ETH to a wallet, head to the “**Write Contract**” tab on Etherscan, and this time scroll down to **InitializeTopUpLimit**. Enter how much you’d like to top up your Gas Tank in the **\_amount** section (again, in Wei), then confirm this.

![Topping up your Gas Tank ⬆️](images/1__eNILK__QKJ8Iy1V__jl4vCxw.jpeg)
Topping up your Gas Tank ⬆️

Wait a few seconds for the transaction to go through… and… that’s it!

You’ll be able to see your top-up transaction reflected both in the **Transactions** screen on Etherscan and — if you pull down in the app to refresh — on the actual balance of your Gas Tank in the TokenWallet!

![Your newly updated Gas Tank ⬆️](images/1__LtTGsKJwcm__TKXUixE5HJg.jpeg)
Your newly updated Gas Tank ⬆️

So there you are; just a few ways in which you can interact with your TokenWallet on using tools such as Etherscan and Metamask! Give it a go yourself and let us know what you think on [**Twitter**](https://twitter.com/tokencard_io) and in our official [**Discord**](https://discord.gg/RhxpjpX) server.