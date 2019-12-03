---
title: Launching Android at Monolith
description: >-
  Near daily we got emails, messages, telegrams, and feedback at events asking a
  simple question: When Android? Now is the time and learn…
date: '2019-10-25T16:17:00.637Z'
categories: []
keywords: []
slug: /launching-android-at-monolith
excerpt: >-
  Near daily we got emails, messages, telegrams, and feedback at events asking a
  simple question: When Android? Now is the time and learn…
thumb_img_path: /images/1__4TTgsCPAATeHo9sHQNjMvg.png
content_img_path: /images/1__4TTgsCPAATeHo9sHQNjMvg.png
layout: post
---


Near daily we got emails, messages, telegrams, and feedback at events asking a simple question: **When Android?**

It was a busy summer! 🌞

This post details our experiences in launching a Blockchain native wallet on top of the Android platform.

![](/images/0__JwC4AVBc8y0qfSCq.jpg)

#### **First Some Background ✅**

Monolith is a non-custodial banking alternative, powered by Ethereum. You can securely store Ethereum-based tokens in your own decentralised Monolith wallet. You can then exchange them to fiat and load them onto your Monolith Visa debit card.

This means that in order to deliver a great User Experience (UX), we have to enable users to seamlessly interact with both the decentralised world of Ethereum as well as the traditional financial world.

Monolith was conceived back in 2016 by our founders, Mel and David. After acquiring the appropriate licenses and partnerships, we set out to build what we thought the bank of the future should look like.

![](/images/0__M__tNhcLR__vU72g5n.jpg)

#### **Launching on iOS first 📲**

The bank of the future is accessible anywhere, so we started working on our mobile app. We built on iOS first due to its homogenous operating system distribution and the availability of the secure enclave on their devices. It’s a public secret at this point that building on iOS first is [generally easier](https://medium.com/@the_manifest/android-vs-ios-which-platform-to-build-your-app-for-first-22ea8996abe1) (with some exceptions).

We built our application in a cross-platform way using react-native. Our User Interfaces (UIs) were designed in a platform-agnostic way, whilst still respecting native elements and patterns such as UI components and controls. At such an early stage it made sense to prioritise go-to-market speed and iterative design over a platform-specific design.

We launched our invite-only iOS closed alpha in March, and [publicly on the App Store](https://apps.apple.com/gb/app/monolith-ethereum-wallet/id1389841315) in June. Our time exclusively on iOS helped us really nail down what a good onboarding experience feels like for our product and hammer out the kinks of interacting with something as nuanced as the Ethereum network.

![](/images/0__mgEKI36lruqawcUU.jpg)

#### **Creation of the Android squad 💪**

3rd of June, 2019. We had finally released on iOS and whilst we knew that we could probably get the Android app out relatively quickly. However, we needed to make sure to do in a way that protected our users.

Given the [diverse Android landscape](https://developer.android.com/about/dashboards), we got a team together and we defined our goal:

![](/images/0__yy90__1ERA4QIfuPe.jpg)

#### **Demystifying the Android landscape 🌪**

A key assumption in our security model is that customer keys are securely stored in their devices. On iOS, we could rely on the Secure Enclave. However, Android has a number of different Keystore implementations. Some are backed by the [Secure Element](https://www.justaskgemalto.com/en/what-is-a-secure-element/) (SE), [Trusted Execution Environment](https://dzone.com/articles/overview-tee-in-android) (TEE) and most recently [StrongBox](https://developer.android.com/about/versions/pie/android-9.0). Furthermore, not all manufacturers implement Android APIs consistently. We very quickly had a number of questions to answer. For example:

1.  What type of ECC signature schemes does Android natively support, if any?
2.  To generate the mnemonic, we use BIP39 which requires entropy of 32 bits. On iOS, we use the [PrimeRandom secure enclave API](https://developer.apple.com/documentation/security/ksecattrkeytypeecsecprimerandom). What are the alternatives for this on Android?
3.  Can we perform feature detection for devices that do not have a hardware Keymaster implementation (that back the [Keystore](https://source.android.com/security/keystore/features)) and restrict based on this? How? What are the different features to consider? Which ones would we restrict?
4.  \[…\] etc, etc, etc

So we got busy researching and prototyping:

![](/images/0__s0pPhot8MRRyHBZa.jpg)

Given our findings, the minimum OS level that we were comfortable with supporting was [Android Nougat](https://en.wikipedia.org/wiki/Android_Nougat) (API 24) as it introduced unified support for the Keystore interface in a manner that ensures that users don’t accidentally remove their private key whilst messing around with their biometrics.

#### **But what devices did our users have? ⁉️**

To get this answered we had a look through the Google Analytics data for our website. We then manually researched the minimum OS level available for Android for each device.

![](/images/0__0dmezN__payI5mysJ.jpg)

From this, we concluded that even though the global distribution dashboards estimated that only 58% of global users had Android Nougat or higher, with mostly European-based users, the number was closer to 85%. We also understood that this was going to get better over time, and we didn’t want to compromise on security.

#### **Building, Testing, Fixing 🤖**

The road ahead was now clearer. First, we had to make the existing functionality work on Android. While most of the react-native components worked straight out of the box, there were native bridges for a number of APIs including key generation and derivation, transaction signing and customer onboarding which needed to be built.

As soon as July came around, we had a basic version and asked our team members to test it in fury. 😀

Mel, our founder was demoing a (partially broken!) internal Android app on our [summer livestream on July the 10th](https://twitter.com/i/broadcasts/1OwGWkkAXwMGQ).

![](/images/0__HRpE7dF2FbymA1aW.jpg)

This phase of development actually took a bit longer than expected. It turned out that our app looked inconsistent on a couple of devices. Once we were confident with the security aspect of things, we released the app as a beta app to 100 community members in August.

We relied on [Instabug](https://instabug.com) and [Discord](https://discordapp.com/invite/BBtta3H?source=post_page---------------------------) to have meaningful conversations with our customers. Over the summer, product managers at Monolith personally responded to most customer messages, bug reports and suggestions! 😊

![](/images/0__8fpxkLr0cl4nFZVF.jpg)
![](/images/0__HvG5wpULcPZeK3sL.jpg)

Two months and 5 Android app iterations later, we were ready to launch!

#### **Sweet Victory ❤**

![](/images/0__arFd7DZNNZ__bYqEM.jpg)

As a team, we’ve gone through a lot to get here, but it’s clear that this is just the beginning. We’ll keep iterating on our product as we strive to understand our customers, and how they use our Wallet and Card in the real world. 🙏

Our goal is to one day be able to confidently ask them to close their bank accounts and live their financial lives on this new paradigm of Decentralised Finance. 🚀

We want to thank everyone who has supported us on this journey. 🎉

![](/images/0__Lf2__865R0oYBGeT3.jpg)

### **Summary**

1.  Building a secure non-custodial product in crypto is hard. We had to tread carefully when building cross-platform.
2.  We designed our app to be cross-platform from the beginning and built it on react-native.
3.  Since we relied on a number of native components, we launched on iOS first.
4.  After many iterations and fixing issues on iOS, we started building for Android.
5.  We defined the problem, investigated and found the right balance between user security and reach.
6.  We had our Android app live internally for a month and for two months in Beta.
7.  We launched in the Play Store and are moving quickly in delivering the next major version of our app.

**\-** [**🕸 Website**](https://monolith.xyz/) **|** [**🐦 Twitter**](https://twitter.com/monolith_web3) **|** [**🎮 Discord**](https://discord.gg/GN6gGEP) **|** [**👽 Reddit**](https://www.reddit.com/r/Monolith_Web3/) **|**[**✈️Telegram**](https://t.me/Monolith_Web3) **-**