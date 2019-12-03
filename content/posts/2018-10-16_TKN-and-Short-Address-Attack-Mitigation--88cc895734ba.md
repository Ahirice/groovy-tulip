---
title: 'TKN and Short Address Attack Mitigation:'
description: 'Severity: High'
date: '2018-10-16T08:41:45.323Z'
categories: []
keywords: []
slug: /tkn-and-short-address-attack-mitigation
excerpt: 'Severity: High'
layout: post
---

*   Severity: High
*   Impact: ~0.12% of all TKN (approximately 50,000) stuck in around 15 unique Smart Contracts on chain
*   User Action Required: It is important that people do not send any more TKN to Smart Contracts for the time being

_It should be noted that this issue only impacts tokens that are stored within certain multisig wallets, and not all wallets are affected by the issue. If your TKN is stored on an address, there is no issue._

As some of our TKN holders already know, we’ve discovered an issue with how the TKN ERC20 contract mitigates against the short address attack. We’ve done some investigative work and are aware of this impacting older versions of the Gnosis MultiSig wallet and the Parity MultiSig wallet.

Currently, TKN held within these wallets cannot be “sent out” after being “sent in”; they are in essence stuck. We’re already looking into this issue as the highest priority.

We’ve put together this blog post to outline exactly what happened, and what we are doing about it.

**What happened**

In the Ethereum Virtual Machine (EVM) there is an issue known to be able to cause transactions to become vulnerable to the “[Short Address Attack” (SAA)](https://vessenes.com/the-erc20-short-address-attack-explained/). Given that the EVM CALL operation pads parameters with 0’s up to 32 bytes in length, it was deemed that there is a chance that Smart Contracts that transfer ERC20 tokens could be susceptible to the SAA. TL;DR, an SAA is when a contract receives less data than it was expecting, with inadequate or no validation being performed on the length of transaction payload — this could have been abused to “trick” smart contracts into performing malicious transactions.

To mitigate the risk of such attacks the author of our TKN ERC20 Contract put in protection that checked for the validity of transfers by performing a check on the length of the transaction — think of the validation as asking “is this _exactly_ the minimum length needed to perform the transaction?” in an attempt to protect TKN holders from the Short Address Attack; see Line 86 of [TKNs ERC20 Smart Contract](https://etherscan.io/address/0xaaaf91d9b90df800df4f55c205fd6989c977e73a#code).

Why was this important? It meant that the TKN holders were not susceptible to the Short Address Attack.

Unfortunately, certain multisig wallets such as Gnosis and Parity handle transactions a little differently than the manner prescribed by the ERC20 specification, padding each transaction payload. This means that, rather than having a transaction payload that is shorter than expected (as is the case with SAA), the transaction payload ends up being longer than expected. As a result, our “_exactly_” validation becomes too strict, causing the transaction to fail and the TKN to get “stuck” in the said smart contract.

**What we’re doing about it**

We’ve taken this issue seriously, and will take steps to ensure that this does not cause problems for TKN holders in the future.

For now:

*   We’ll be reissuing any stuck TKN to affected holders as the TKN that is currently stuck within these Smart Contracts can’t be retrieved (see the _“What you can do”_ section below)

Gnosis have also published [an update themselves on GitHub](https://github.com/gnosis/MultiSigWallet/blob/master/contracts/MultiSigWallet.sol#L242-L262), acknowledging the padding issues [and putting provisions in place so that it does not happen again in the future](https://github.com/gnosis/MultiSigWallet/commit/e1b25e8632ca28e9e9e09c81bd20bf33fdb405ce). The folk at OpenZeppelin have also removed their payload size check in their Smart Contract Library code, one can follow the discussion on their github account [— https://github.com/OpenZeppelin/zeppelin-solidity/commit/e33d9bb41be136f12bc734aef1aa6fffbf54fa40](https://github.com/OpenZeppelin/zeppelin-solidity/commit/e33d9bb41be136f12bc734aef1aa6fffbf54fa40) .

**What you can do**

If you are the owner of a Smart Contract Wallet and your TKN is “stuck” as a result of this issue, don’t panic, your TKN is stuck forever, but we will reissue you with other TKN asap.

In order for us to reissue your TKN please send us a signed message (see below for instructions) with the following caption to **hello@tokencard.io** so that we know it’s _you_ requesting the TKN:

“_I, owner of Smart Contract \[insert wallet address here\], would like to receive my stuck TKN in a new address, which I own, \[insert new wallet address here\].”_

You can easily create a signed message using My Ether Wallet’s “[**Sign a Message**](https://www.myetherwallet.com/signmsg.html)” tool:

![](images/0__nWzGV2Ypo__LiYuxx.jpg)
![](images/0__4SL430SSRzt9T5z0.jpg)

If you are messaging us regarding a MultiSig Contract, we require that all the owners (or the minimum required number of owners as dictated by the Multisig wallet) also sign a similar message. We’ll then send the new address any stuck TKN.

We’re sorry for the inconvenience caused by this, and are working to fix it quickly and comprehensively. We will continue to update our community — through our blog, on [**Twitter**](https://twitter.com/tokencard_io), [**Reddit**](https://www.reddit.com/r/TokenCard/), and our [**Community Discord**](http://discord/).

**More questions?**

I’ll be on Discord to answer any questions tomorrow (Wednesday October 17th) between 2–3pm BST.

Thanks,

Mischa — CTO @ Token