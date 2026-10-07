---
layout: default
title: Privacy Policy for Cakebyte
permalink: /cakebyte/
nav_order: 2
---

# Privacy Policy for Cakebyte

**First published:** 2026-08-29<br>
**Last updated:** 2026-10-07

Cakebyte is a firewall app for Android. It lets you allow or block network access for individual apps, block IP addresses and ranges, and look at what your apps have been connecting to. This Privacy Policy explains how it handles your information. "We" and "us" mean Twius, the developer of Cakebyte.

{: .summary }
**In short:** Cakebyte works without servers or user accounts. Nothing it records about you is sent anywhere, apart from what an occasional crash report may contain. The only network requests the app makes are to Google, for the Pro upgrade and the billing library's diagnostics, and to GitHub, when you update the tracker list.

## 1. Who we are {#who-we-are}

Cakebyte is developed by Twius (Anastasis Anastasi, an individual developer in Cyprus). You can reach us at [twius.09@gmail.com](mailto:twius.09@gmail.com).

There is no backend server, database, or cloud service behind Cakebyte. The app never sends us anything it stores, so we cannot see or access your app data. [Section 2](#what-we-receive) lists what we do receive.

## 2. What we receive {#what-we-receive}

We receive personal information in only these ways:

- **Emails you send us:** your email address and whatever you write or attach. We use them only to reply to you, and delete them once the matter is settled. Our email is provided by Google (Gmail), which may store it outside the EU, including in the United States. Google LLC is certified under the EU-US Data Privacy Framework.
- **Google Play sales records:** when you buy Cakebyte Pro, Google gives us its usual seller's record of the sale, such as the order number, date, price, device model, and your country, and in some countries your city and postcode. We can look up an order by the email address you paid with. It never includes your card details. We use it for support, refunds, and tax records, and keep it as long as tax law requires.
- **Crash reports:** if you have chosen to share usage and diagnostics data with Google, Google Play shows us reports of the app's crashes and freezes. They contain technical details such as the device model, the Android version, and where in the app the error happened, which can include an error message from the app. Google does not tell us who you are.

Under EU and UK data protection law, our legal basis is our legitimate interest in answering you and supporting the app, and our legal duty to keep tax records.

## 3. Data stored on your device {#data-on-device}

Everything Cakebyte stores is kept on your device. It is kept in a private SQLite database, a settings file, and, if you update the tracker list, a copy of that list, all in the app's private storage. That covers:

- **Firewall rules:** which apps you have allowed or blocked on Wi-Fi and mobile data
- **IP blocklist:** the addresses and CIDR ranges you have blocked for all apps, each with an optional label (often the name of the app you blocked it from)
- **Connection logs:** domains, IP addresses, ports, and timestamps for the connections your apps make
- **Usage counts:** hourly and daily totals of each app's connections and blocked connections (see [section 8](#deletion))
- **Firewall alerts:** events like a firewall crash, a conflict with another VPN app, or a revoked permission
- **Pro status:** when your trial started and whether you own Cakebyte Pro
- **App settings:** your preferences, such as recovery behaviour, roaming behaviour, **Activity logging**, **Keep history for**, **Keep awake for streaming**, and App Lock
- **Tracker list:** the copy you downloaded, if you have updated the tracker list (see [section 4](#what-leaves))

To show you your apps, Cakebyte reads the list of apps installed on your device and keeps a rule entry for each one. That list never leaves the device.

None of it is sent to us, and nothing is sent to anyone else except as described in [section 4](#what-leaves). The app does not back up or sync anything to a server. Android's cloud backup is switched off for the app, so none of it is copied to your Google account. If you move to a new phone with a direct device-to-device transfer, Android may copy the app's data across.

## 4. What leaves your device {#what-leaves}

Nothing, apart from the Pro checks and purchase described in [section 7](#purchases), the billing diagnostics described in [section 6](#analytics), and the tracker list update described below. At runtime the app contacts no server of ours, because there isn't one. If you have chosen to share usage and diagnostics data with Google, Android also sends Google a report when the app crashes or freezes. That report can sometimes include part of what the app was working on at the time (see [section 2](#what-we-receive)).

Cakebyte bundles a copy of the [StevenBlack/hosts](https://github.com/StevenBlack/hosts) blocklist (MIT License) so it can recognise known tracking domains. That file ships inside the app and is read from local storage, and no lookup you make is sent anywhere. If you tap update on the tracker list in settings and confirm, the app downloads the latest version of the list from GitHub and uses it instead. It never does this on its own. The request contains nothing about your connections. Like any web request, it shows GitHub your IP address, and it identifies itself only as "Cakebyte". GitHub handles it under its [privacy statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).

**VPN usage:** Cakebyte uses Android's `VpnService` API to open a local tunnel so it can inspect packets on the device. The tunnel starts and ends on your device. Traffic you allow goes where your apps send it, and Cakebyte never routes it through a VPN server, ours or anyone else's.

## 5. Permissions {#permissions}

| Permission | Why it is needed |
|---|---|
| `QUERY_ALL_PACKAGES` | To display the full list of installed apps so you can set firewall rules for each one |
| `BIND_VPN_SERVICE` | To intercept network traffic locally on-device for firewall enforcement |
| `BIND_QUICK_SETTINGS_TILE` | To show the optional Quick Settings tile that turns the firewall on and off |
| `INTERNET` | To forward the traffic your apps send, once the firewall has allowed it, and to download the tracker list when you update it. Google's billing library also uses it to send its diagnostics (see [section 6](#analytics)). Cakebyte sends none of your data anywhere |
| `FOREGROUND_SERVICE` | To keep the firewall running while the app is in the background |
| `FOREGROUND_SERVICE_CONNECTED_DEVICE` | Android 14 and later require every foreground service to declare a type. Cakebyte's firewall service uses the connected-device type, which needs this permission |
| `RECEIVE_BOOT_COMPLETED` | To restart the firewall automatically after the device reboots, if it was on before the reboot |
| `POST_NOTIFICATIONS` | To show firewall status and alerts about crashes, VPN conflicts, and revoked permissions |
| `ACCESS_NETWORK_STATE` | To detect when you switch between Wi-Fi and mobile data |
| `CHANGE_NETWORK_STATE` | Android requires it before the firewall service can use the connected-device foreground-service type |
| `WAKE_LOCK` | To keep packet forwarding responsive while the screen is off so background streaming does not stall, when **Keep awake for streaming** is on |
| `USE_BIOMETRIC` | To unlock the app with your fingerprint, face, or device PIN, pattern, or password when the optional App Lock (**Settings > Security > Require unlock**) is on. Android does the authentication itself; Cakebyte never receives or stores your biometric data |
| `com.android.vending.BILLING` | To process the optional one-time in-app purchase that unlocks Pro features, through Google Play |
| `com.cakebyte.DYNAMIC_RECEIVER_NOT_EXPORTED_PERMISSION` | Added by the AndroidX core library. It is private to Cakebyte and only stops other apps from sending it internal messages |

Cakebyte requests no location, contacts, camera, or microphone permission.

## 6. Analytics, advertising, and tracking {#analytics}

Cakebyte does not include analytics, advertising, third-party tracking, or crash reporting of its own. We do not profile you, and we do not sell your personal data or use it for advertising.

The only part of Cakebyte that sends diagnostics anywhere is Google's Play Billing library, which handles Cakebyte Pro. It ships with Google Play services components and Google's event-reporting library, which send Google diagnostics about the billing flow. Google decides what they contain and how they are used. We never receive them, and they contain none of your firewall rules or connection logs.

## 7. Purchases {#purchases}

The firewall itself is free and stays free. Cakebyte Pro adds the detailed connection log, per-app statistics, the alert history, and the IP blocklist, and you get a 14-day trial before deciding. Cakebyte Pro is a single one-time purchase. It is not a subscription, and the app does not show ads.

Google Play Billing processes the payment. Google runs the transaction and keeps a record of what you own, so it can be restored on any device where you are signed in. We never see your card details, and [Google's privacy policy](https://policies.google.com/privacy) governs how Google handles them.

Each time the app starts, including when Android starts it in the background, it asks Google Play whether you own Cakebyte Pro and what it costs, and it completes or restores a purchase when you ask. From Google Play the app receives the product's details, such as its price, and whether you own it. The app sends nothing about the purchase to us. Google's sales record is described in [section 2](#what-we-receive). Your trial status is kept on your device and never uploaded. Your firewall rules and connection logs are never part of that exchange.

The [Terms of Use]({{ '/cakebyte/terms/' | relative_url }}) cover what the purchase includes and how refunds work.

## 8. Managing and deleting your data {#deletion}

Connection logging is on by default. Turn off **Activity logging** in settings and the app stops recording connections altogether.

Connection logs are deleted automatically once a day after they pass the period set under **Keep history for** (7 days by default). If you choose **Forever**, logs older than 30 days are still deleted once they take up more than 500 MB. Alerts are kept until you delete them or clear the app's data. You can also wipe the connection logs at any time with **Clear all data now** in settings. Cakebyte Pro users, and anyone still in the trial, can delete the alert history on the Alerts screen. Logs belonging to an app you uninstall are removed automatically the next time you open the app list or start the firewall.

One thing that wipe does not cover: the per-app counts your connection logs are rolled up into. There are two of these: an hourly one, kept for 60 days, and a daily one, which is not pruned at all. Each row holds an app's package name, which hour or day it covers, how many connections that app made, and how many were blocked. Neither contains domains, addresses, or anything about what a single connection was for. They stay on your device like everything else.

Turning **Activity logging** off stops the roll-ups too, not only the connection logs. While it is off, no connections are recorded and nothing is aggregated. Alerts are still kept, and automatic cleanup pauses.

Clearing the app's data in Android settings, or uninstalling Cakebyte, removes everything it keeps on your device.

## 9. Your rights {#your-rights}

Data protection law gives you rights over the personal data an organisation holds about you, such as access, correction, erasure, and portability. We hold none of the data the app stores. Cakebyte does not use a server or accounts, so we have no copy to hand over, correct, or delete. Everything those rights would cover sits on your device, under your control: you can clear the connection logs from inside the app, turn logging off so nothing is recorded in the first place, and clear the app's data or uninstall the app to remove everything.

For what we do receive (see [section 2](#what-we-receive)), you can ask us for a copy of it, ask us to correct or delete it, ask us to limit how we use it, or object to our using it, by writing to [twius.09@gmail.com](mailto:twius.09@gmail.com). Sales records we must keep for tax purposes are deleted when that period ends. You can also complain to the data protection authority where you live or work, or to ours, the [Cyprus Commissioner for Personal Data Protection](https://www.dataprotection.gov.cy).

Google processes your purchase, and its own billing diagnostics, as a separate controller, under [Google's privacy policy](https://policies.google.com/privacy). Rights over that data are exercised with Google. Cakebyte never sees your payment details.

## 10. Children's privacy {#children}

Cakebyte is not directed to children under 13, or under the minimum age that applies where you live. We do not knowingly collect personal information from children. If you think a child has sent us personal information, for example by email, tell us and we will delete it.

## 11. Security {#security}

Your data lives in the app's private storage, which Android keeps sandboxed from other apps.

App Lock is an optional extra, switched on with **Settings > Security > Require unlock**. When it is on, Cakebyte asks for authentication when you open it, and again if it has sat in the background for more than about 30 seconds, so someone holding your unlocked phone cannot change your firewall rules or read your connection logs. It ships off by default.

Android handles the authentication itself, through its biometric and device-credential APIs. Cakebyte stores no credentials and never sees your fingerprint or face data. While App Lock is on, the app also hides its contents from the recents screen.

The Quick Settings tile respects App Lock. Whether or not App Lock is on, it can turn the firewall on. If Cakebyte does not have VPN permission yet, the tile opens the app instead. While App Lock is on, turning the firewall off from the tile opens the app and asks you to unlock it first.

Keeping the device itself secure, with a screen lock and current OS updates, remains the best protection for anything stored on it.

## 12. Changes to this policy {#changes}

We may update this policy from time to time. The version published at this address is always the current one, and the "Last updated" date at the top tells you when it last changed. If a change is material, we will point it out in the app's release notes and on its store listing before it applies to you.

## 13. Related documents {#related}

This policy covers what happens to your information. Your use of Cakebyte is also covered by the [Terms of Use]({{ '/cakebyte/terms/' | relative_url }}).

## 14. Contact {#contact}

Questions about this policy: [twius.09@gmail.com](mailto:twius.09@gmail.com).
