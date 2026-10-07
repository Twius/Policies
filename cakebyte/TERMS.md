---
layout: default
title: Terms of Use for Cakebyte
permalink: /cakebyte/terms/
nav_order: 3
---

# Terms of Use for Cakebyte

**First published:** 2026-09-15<br>
**Last updated:** 2026-10-07

These Terms of Use ("Terms") cover your use of the Cakebyte Android app ("Cakebyte", "the app"). "We" and "us" mean Twius, the developer of Cakebyte. Cakebyte is a no-root firewall. It uses Android's `VpnService` API to open a local tunnel on your device, then allows or blocks the traffic your apps send based on rules you set.

By installing or using Cakebyte, you agree to these Terms. If you do not agree, do not use the app.

{: .summary }
**In short:** Cakebyte is a firewall, not a privacy VPN. Your traffic is not sent through any server, and the app adds no encryption. Blocking is best effort, so some connections may still get through. If you block an app, expect parts of it to stop working. You choose what to block. The app is provided as is, though your rights under consumer law still apply.

## 1. Who these Terms are with {#who}

Cakebyte is developed and published by Twius (Anastasis Anastasi, an individual developer in Cyprus). You can reach us at [twius.09@gmail.com](mailto:twius.09@gmail.com).

The terms of the store you got the app from also apply, which is normally Google Play. Where those store terms and these Terms disagree about something the store handles, such as payment, refunds, or distribution, the store terms win, but they never reduce the refunds these Terms promise or your rights under consumer law.

You need to be at least 13 to use Cakebyte, or older if a higher minimum age applies where you live. If you are under 18, or under the age of adulthood where you live, a parent or guardian needs to agree to these Terms for you.

Nothing in these Terms takes away rights you have under the consumer protection law of the country where you live.

## 2. Your licence to use the app {#licence}

Cakebyte is **licensed to you, not sold**. You get a non-exclusive, non-transferable licence to install and use it, for personal or work use, on devices you own or control. It lasts until it ends as described in [section 15](#ending).

You may not:

- redistribute, resell, sublicense, rent, or lend the app;
- reverse engineer, decompile, or disassemble the app, or otherwise try to get at its source code, unless the law says you may or the licence of an open-source component inside the app allows it (see [section 10](#open-source));
- modify or patch the app to unlock paid features without paying for them, or help anyone else do so;
- use the app to interfere with a network, device, or account you do not own or are not allowed to configure, or to get around a security or monitoring control someone else is entitled to put on the device;
- remove or hide any copyright, licence, or attribution notice.

Cakebyte and its source code are proprietary, except for the open-source components described in [section 10](#open-source). Copyright (c) 2026 Twius. All rights reserved.

## 3. What Cakebyte is not {#not-a-vpn}

Cakebyte uses the `VpnService` API because that is the only way an app can filter traffic on Android without root access. It is not a VPN in the usual sense, and you should not use it as one.

Cakebyte does not send your traffic through a server. The tunnel starts and ends on your device, and the app adds no encryption, so it does not hide your traffic from your mobile operator, your internet provider, or the sites you connect to, all of whom see what they would see anyway. It does not change your IP address or your apparent location, so it will not get you around regional blocks.

It is also not an antivirus, malware scanner, ad blocker, or parental control app.

Its actual job is narrow. For each app, on Wi-Fi and on mobile data, it either lets a connection out or blocks it.

## 4. Blocking is not guaranteed {#blocking-not-guaranteed}

Cakebyte applies your rules by inspecting packets on the device. A blocked DNS query gets an NXDOMAIN reply, a blocked TCP connection gets reset, and blocked UDP gets an ICMP error back.

**We cannot promise that blocking always works.** A connection you blocked may still get through, and a connection you allowed may be cut off. This happens for a few reasons:

- Android routes some traffic outside the tunnel. The operating system's own traffic, parts of some carrier services, and certain system components are not covered by it.
- Cakebyte only forwards TCP and UDP, so anything else, such as ping, fails even for apps you allowed.
- Android may stop the app. Battery optimisation, a manufacturer's power management, or a crash will all do it, and while the app is not running your traffic flows as normal, unless you use **Always-on VPN (Android)** (see [section 5](#blocking-breaks)).
- Working out which app owns a connection relies on Android APIs that are not always accurate or available, and a connection Cakebyte cannot match to an app is let through.
- Another VPN app, a work profile, or a device policy can take priority over it.

**If a connection getting through would put you at real risk, do not rely on Cakebyte alone.** It controls how ordinary apps behave. It will not stop software that is deliberately trying to get around it.

## 5. Blocking things will break them {#blocking-breaks}

Blocking an app's network access stops parts of that app working. That is what the app is for, and it is your decision to make.

**You are responsible for what you block and for what happens as a result.** A blocked app may fail to sync or refuse to open at all. Two-factor codes may not arrive. Banking and payment apps usually stop working completely. A backup can quietly stop running without telling you, and a download can finish corrupted.

Two cases deserve extra thought.

**Emergency features:** Blocking system apps, messaging apps, or location services can interfere with emergency alerts, emergency location, or your ability to reach someone when you need to. Emergency calls over the mobile network do not go through this app, but anything that reaches help over the internet does. Think carefully before blocking something you might need in an emergency.

**Always-on VPN (Android):** This option under **Firewall recovery** hands over to Android's always-on VPN setting with "Block connections without VPN" turned on. While that is on, your device has no internet whenever Cakebyte is not running, including after a crash, during an app update, or when you turn the firewall off in Cakebyte. That is what the setting is meant to do. You turn it on and off in Android's VPN settings, not in Cakebyte.

## 6. The tracker list {#tracker-list}

Cakebyte ships with a copy of the [StevenBlack/hosts](https://github.com/StevenBlack/hosts) blocklist so it can flag connections to known tracking domains. Other people maintain that list, not us.

The copy is fixed when the app version is built. You can replace it with the latest version from settings, which downloads it from GitHub. The app never updates it on its own. Either way, it can be out of date. It will miss some trackers, and it will flag some domains you would not call trackers yourself. Treat the labels as a hint rather than a verdict. We do not check the list and we do not control what goes on it. We are not responsible for its contents, or for decisions you make based on it.

## 7. Other VPN apps {#other-vpns}

Android only lets one VPN app be active at a time. Starting Cakebyte disconnects any other VPN you are running, and starting another VPN disconnects Cakebyte. The app will usually notice and tell you, but it cannot prevent it.

If you rely on another VPN for privacy or for work access, remember that Cakebyte replaces it rather than running alongside it. The exception: if you use **Always-on VPN (Android)**, Android will not let another VPN take over until you switch that setting off.

## 8. Your data {#your-data}

Everything Cakebyte keeps, including your rules, blocklists, connection logs, and alerts, stays on your device, in the app's private storage. We do not run a server or keep a copy. The [Privacy Policy]({{ '/cakebyte/' | relative_url }}) explains this in full.

That has a consequence: **if you lose your device, it is damaged beyond repair, you reset it, clear the app's data, or uninstall the app, your Cakebyte data is gone for good.** We cannot recover it, because we never had it. If you move to a new phone with Android's direct device-to-device transfer, the app's data may be copied across.

You can clear connection logs from inside the app whenever you want, and you can turn logging off entirely. Connection logs show what your apps talk to, which can reveal a lot about you. Anyone who can get into your phone can read them.

Keeping your device secure is up to you. App Lock (**Settings > Security > Require unlock**) adds a layer on top of your screen lock, but it does not replace one.

## 9. Purchases {#purchases}

The firewall itself is free and stays free. The detailed connection log, per-app statistics, the alert history, and the IP blocklist are part of a paid unlock called Cakebyte Pro, and you get a free 14-day trial first. If the trial ends without a purchase, IP addresses you blocked stay blocked, but you need Cakebyte Pro to see or remove them. Cakebyte Pro is a single one-time purchase, not a subscription, and it does not renew.

- Google Play handles the payment, not us. We never see your card details.
- Within 48 hours of buying, you can ask Google Play for a refund. After that, contact us. We will refund you where the law requires, for example if Cakebyte Pro does not work as described.
- The purchase belongs to your Google account rather than to the installed app. It survives uninstalling, and you can restore it from inside the app.
- Trial status is stored only on your device, not with your Google account, so reinstalling, clearing the app's data, or moving to a new device can reset it.
- We will not take a feature you have paid for and charge for it again.

If something you bought does not unlock, try **Restore purchase** on **Settings > Cakebyte Pro** first, then contact us at the address in [section 19](#contact).

## 10. Open-source components {#open-source}

Cakebyte includes open-source software written by other people: mainly Google's AndroidX and Jetpack Compose libraries, Kotlin and its coroutines library from JetBrains, and Okio from Square, all under the Apache License 2.0, and the StevenBlack/hosts blocklist under the MIT License. Google's Play Billing library and the Google Play services components it uses are not open source. Google provides them under its own terms, the Android Software Development Kit License. Some smaller libraries that come with them, such as Google's event-reporting library, are open source under the Apache License 2.0. Each component keeps its own licence, and nothing in these Terms takes away a right those licences give you.

The list of components and their licence texts are in the app under **Settings > About > Open source licenses**.

## 11. No affiliation {#no-affiliation}

Cakebyte is an independent app. It is not affiliated with, associated with, endorsed by, or sponsored by Google, or by the maintainers of the StevenBlack/hosts list or the makers of any app, service, or domain named in Cakebyte or in that list. All trademarks and names belong to their owners.

## 12. Changes to the app {#changes-to-app}

We may update Cakebyte and change its features. We change or remove a feature only for a valid reason, such as a change to Android or Google Play, a security problem, a service the app relies on closing, or keeping the app working. If a change removes something you paid for, or makes it much worse, we will tell you before it happens, in the app's release notes and on its store listing, and you can ask for a refund within 30 days of that notice or of the change, whichever is later.

We may also stop offering Cakebyte. If we discontinue it, we stop updating and offering it, but the copy you have keeps working. We do not promise to keep it working with any particular device, Android version, network type, or manufacturer's power management behaviour. If you paid for Cakebyte Pro, we will provide the updates the law requires for as long as you can reasonably expect them.

Your data is on your device rather than with us, so discontinuing the app does not delete it.

## 13. No warranty {#no-warranty}

**Cakebyte is provided "as is" and "as available", with no warranty of any kind, express or implied, including any implied warranty of merchantability, fitness for a particular purpose, non-infringement, accuracy, security, or uninterrupted and error-free operation.**

We do not promise that the app will block any particular connection, that it will always attribute a connection to the right app, that it will keep running, that it will not interfere with other software on your device, or that its logs, statistics, and tracker labels are accurate or complete.

If you paid for Cakebyte Pro, you have legal rights if it is faulty or not as described, and these Terms do not affect them. None of this removes rights you have under consumer protection law where you live. Where that law applies, these disclaimers apply only as far as it allows.

## 14. Limits on our liability {#liability}

Nothing in these Terms limits our liability for death or personal injury caused by our negligence, for fraud, or for anything else the law does not let us limit.

Apart from that, we are only responsible for loss that is a foreseeable result of our breaking these Terms or failing to use reasonable care and skill. As far as the law allows, we are not responsible for lost profit, a missed message or notification, a missed opportunity, or an interrupted service, whether they arise from using Cakebyte, from a connection being blocked or allowed, from relying on something the app showed you, or from not being able to use it at all. Our total liability to you is limited to the greater of what you paid for Cakebyte Pro and €50. This limit does not affect your rights if Cakebyte Pro is faulty or not as described.

## 15. Ending your licence {#ending}

You can end your licence at any time by uninstalling the app. We can end it only if you seriously or repeatedly break these Terms, for example by cracking paid features or redistributing the app. If you turned on **Always-on VPN (Android)**, switch it off in Android's VPN settings before you uninstall Cakebyte or clear its data, or your device may be left with no network access. Sections [4](#blocking-not-guaranteed), [5](#blocking-breaks), [6](#tracker-list), [10](#open-source), [13](#no-warranty), [14](#liability), [17](#governing-law), and [18](#privacy) still apply after the licence ends.

## 16. Changes to these Terms {#changes}

We only change these Terms for a good reason, such as a change in the law, in Google Play's rules, or in how the app works. The version published at this address is always the current one, and the "Last updated" date at the top tells you when it last changed. If a change matters, we will tell you at least 30 days before it takes effect, in the app's release notes and on its store listing. If you do not agree, stop using the app. If the change takes away something you paid for, you can ask for a refund.

## 17. Governing law {#governing-law}

These Terms are governed by the law of Cyprus. If you are a consumer, you keep the protection of the mandatory laws of the country where you live, and you can bring a claim in the courts of Cyprus or in any court your local law lets you use. If you use Cakebyte for work, the courts of Cyprus decide any dispute. If a court finds part of these Terms unenforceable, the rest still applies. If someone else takes over Cakebyte, we may transfer these Terms to them. Your rights stay the same.

## 18. Privacy {#privacy}

What the app does with information on your device is covered separately in the [Privacy Policy for Cakebyte]({{ '/cakebyte/' | relative_url }}).

## 19. Contact {#contact}

Questions about these Terms: [twius.09@gmail.com](mailto:twius.09@gmail.com).
