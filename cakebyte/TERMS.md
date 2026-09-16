---
layout: default
title: Terms of Use for Cakebyte
permalink: /cakebyte/terms/
---

# Terms of Use for Cakebyte

**Effective date:** 2026-09-15
**Last updated:** 2026-09-16
**App:** cakebyte

These Terms of Use ("Terms") cover your use of the Cakebyte Android app ("Cakebyte", "the app"). Cakebyte is a no-root firewall. It uses Android's `VpnService` API to open a local tunnel on your device, then allows or blocks the traffic your apps send based on rules you set.

By installing or using Cakebyte, you agree to these Terms. If you do not agree, do not use the app.

> **In short:** Cakebyte is a firewall, not a privacy VPN. Your traffic is not sent through any server and the app does not encrypt it. Blocking is best effort, so some connections may still get through. If you block an app, expect parts of it to stop working. You choose what to block, and the app is provided as is.

## 1. Who we are

Cakebyte is developed and published by **Twius**.
Contact: **twius.09@gmail.com**.

The terms of the store you got the app from also apply, which for Cakebyte normally means Google Play. Where the store's terms and these Terms disagree about something the store handles, such as payment, refunds or distribution, the store's terms win.

## 2. Your licence to use the app

Cakebyte is **licensed to you, not sold**. You get a personal, non-exclusive, non-transferable, revocable licence to install and use it on devices you own or control, for your own personal and non-commercial use.

You may not:

- redistribute, resell, sublicense, rent or lend the app.
- reverse engineer, decompile or disassemble the app, or otherwise try to get at its source code. This does not apply where the law says it cannot, or where the licence of an open-source component inside the app allows it (see section 10).
- modify or patch the app to unlock paid features without buying them, or help anyone else do so.
- remove or hide any copyright, licence or attribution notice.
- use the app to interfere with a network, device or account you do not own or are not allowed to configure, or to get around a security or monitoring control someone else is entitled to put on the device.

Cakebyte and its source code are proprietary. Copyright (c) 2026 Twius. All rights reserved.

## 3. What Cakebyte is not

Cakebyte uses the `VpnService` API because that is the only way an app can filter traffic on Android without root access. It is not a VPN in the usual sense, and you should not use it as one.

Cakebyte does not send your traffic through a server. The tunnel stays on your device. It does not encrypt your traffic or hide it from your mobile operator, your internet provider, or the sites you connect to, all of whom see what they would see anyway. It does not change your IP address or your apparent location, so it will not get you around regional blocks.

It is also not an antivirus or malware scanner, not an ad blocker for ads shown inside apps, and not parental control software.

Its actual job is narrow. For each app, on WiFi and on mobile data, it either lets a connection out or blocks it.

## 4. Blocking is not guaranteed

Cakebyte applies your rules by inspecting packets on the device. A blocked DNS query gets an NXDOMAIN reply, a blocked TCP connection gets reset, and blocked UDP gets an ICMP error back.

**We cannot promise that blocking always works.** A connection you blocked may still get through, and a connection you allowed may be cut off. This happens for a few reasons:

- Android routes some traffic outside the tunnel. The operating system's own traffic, parts of some carrier services, and certain system components are not covered by it.
- An app may fall back to a protocol or transport that Cakebyte does not handle.
- Android may stop the app. Battery optimisation, a manufacturer's power management, or a crash will all do it, and while the app is not running your traffic flows as normal.
- Working out which app owns a connection relies on Android APIs that are not always accurate or available.
- Another VPN app, a work profile or a device policy can take priority over it.

**If a connection getting through would put you at real risk, do not rely on Cakebyte alone.** It controls how ordinary apps behave. It will not stop software that is deliberately trying to get around it.

## 5. Blocking things will break them

Blocking an app's network access stops parts of that app working. That is what the app is for, and it is your decision to make.

**You are responsible for what you block and for what happens as a result.** A blocked app may fail to sync or refuse to open at all. Two-factor codes may not arrive. Banking and payment apps usually stop working completely. A backup can quietly stop running without telling you, and a download can finish corrupted.

Two cases deserve extra thought.

**Emergency features.** Blocking system apps, messaging apps or location services can interfere with emergency alerts, emergency location, or your ability to reach someone when you need to. Emergency calls over the mobile network do not go through this app, but anything that reaches help over the internet does. Think carefully before blocking something you might need in an emergency.

**The hard kill switch.** This mode uses Android's own always-on VPN setting with "block connections without VPN" turned on. While it is on, your device has no internet at all whenever Cakebyte is not running, including after a crash or an app update. That is what the setting is meant to do. You switch it off in Android's VPN settings, not in Cakebyte.

## 6. The tracker list

Cakebyte ships with a copy of the [StevenBlack/hosts](https://github.com/StevenBlack/hosts) blocklist so it can flag connections to known tracking domains. Other people maintain that list, not us.

The copy is fixed when the app version is built and is never updated while the app runs. It can be out of date. It will miss some trackers, and it will flag some domains you would not call trackers yourself. Treat the labels as a hint rather than a verdict. We do not check the list and we do not control what goes on it. We are not responsible for its contents, or for decisions you make based on it.

## 7. Other VPN apps

Android only lets one VPN app be active at a time. Starting Cakebyte disconnects any other VPN you are running, and starting another VPN disconnects Cakebyte. The app will usually notice and tell you, but it cannot prevent it.

If you rely on another VPN for privacy or for work access, remember that Cakebyte replaces it rather than running alongside it.

## 8. Your data

Your rules, blocklists, connection logs and alerts all stay on your device, in the app's private storage. We run no server and keep no copy. The [Privacy Policy](/Policies/cakebyte/) explains this in full.

That has a consequence: **if you lose your device, reset it, or uninstall the app, your Cakebyte data is gone for good.** We cannot recover it, because we never had it.

You can clear connection logs from inside the app whenever you want, and you can turn logging off entirely. Keeping the device itself secure is up to you. App Lock adds a layer on top of your screen lock, but it does not replace one.

Connection logs show what your apps talk to, which can reveal a lot about you. Anyone who can get into your phone can read them.

## 9. Cakebyte Pro

The firewall itself is free and stays free. The detailed connection log, per-app statistics, alerts and the IP blocklist are part of a paid unlock called **Cakebyte Pro**. You get a free 14-day trial first. After that it is a single one-time purchase, not a subscription, and it does not renew.

- Google Play handles the payment, not us. We never see your card details.
- Refunds go through Google Play under its own policy. Any refund rights you have by law are unaffected.
- The purchase belongs to your Google account rather than to the installed app. It survives uninstalling, and you can restore it from inside the app.
- Trial status is stored on your device. Reinstalling, clearing the app's data or moving to a new device can affect a trial already in progress.
- What Pro includes may change as the app develops. We will not take a feature you have paid for and charge for it again, though features can be added, changed or dropped as described in section 11.

If something you bought does not unlock, try the restore option in the app first, then contact us at the address in section 17.

## 10. Open-source components

Cakebyte includes open-source software written by other people. Mainly that is Google's AndroidX and Jetpack Compose libraries and Google Play Billing, plus Kotlin and its coroutines library from JetBrains, all under the Apache License 2.0, and the StevenBlack/hosts blocklist under the MIT License. Their own licences still govern them, and nothing in these Terms takes away a right those licences give you.

The full list and the licence texts are in the app under **Settings > About > Open source licenses**.

## 11. Changes to the app

We may change, update or discontinue Cakebyte or any part of it at any time. We do not promise to keep supporting any particular device, Android version, network type or manufacturer's power management behaviour.

Your data sits on your device rather than with us, so discontinuing the app does not delete it.

## 12. No warranty

**Cakebyte is provided "as is" and "as available", with no warranty of any kind**, express or implied. That includes any implied warranty of merchantability, fitness for a particular purpose, non-infringement, accuracy, security, or uninterrupted and error-free operation.

We do not promise that the app will block any particular connection, that it will always attribute a connection to the right app, that it will keep running, that it will not interfere with other software on your device, or that its logs, statistics and tracker labels are accurate or complete.

None of this removes rights you have under consumer protection law where you live. Where that law applies, these disclaimers only go as far as it allows.

## 13. Limits on our liability

As far as the law allows, we are not liable for indirect, incidental, special, consequential or punitive damages. Nor are we liable for lost data, lost profit, a missed message or notification, a missed opportunity, an interrupted service or any similar loss, whether it arises from using Cakebyte, from a connection being blocked or allowed, from relying on something the app displayed, or from not being able to use the app at all.

Where liability cannot be excluded, it is capped at the amount you paid for the app.

## 14. Ending this licence

The licence ends automatically if you break these Terms, and you can end it yourself at any time by uninstalling the app. If you turned on the hard kill switch, switch it off in Android's VPN settings before you uninstall, or your device may be left with no network access. Sections 4, 5, 12, 13 and 16 still apply after the licence ends.

## 15. Changes to these Terms

We may update these Terms. The version published at this address is always the current one, and the "Last updated" date at the top tells you when it changed. If you carry on using the app after a change, you accept the updated version.

## 16. Privacy

What the app does with information on your device is covered separately in the [Privacy Policy for Cakebyte](/Policies/cakebyte/).

## 17. Contact

Questions about these Terms: **twius.09@gmail.com**.
