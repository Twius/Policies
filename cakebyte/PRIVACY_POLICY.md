---
layout: default
title: Privacy Policy for Cakebyte
permalink: /cakebyte/
---

# Privacy Policy for Cakebyte

**Effective date:** 2026-08-29
**Last updated:** 2026-08-29
**App:** cakebyte

Cakebyte is a firewall app for Android. It lets you allow or block network access
for individual apps, block IP addresses and ranges, and look at what your apps have
been connecting to. This policy describes what it does with the information it handles.

The short version: Cakebyte has no servers and no accounts. Nothing it records about
you is sent anywhere. The only network request the app itself makes is to Google Play,
and only when you buy or restore the Pro upgrade.

## 1. Who we are

Cakebyte is developed by Twius. You can reach us at twius.09@gmail.com.

There is no backend server or cloud service behind Cakebyte. We hold no copy of your
data because we never receive one. If you buy the Pro upgrade, Google Play handles the
payment and we never see your card details.

## 2. What the app stores on your device

Cakebyte keeps its data in a private SQLite database inside the app's own sandboxed
storage. That covers:

- **Firewall rules**: which apps you have allowed or blocked on WiFi and mobile data
- **IP blocklist**: the addresses and CIDR ranges you have blocked for all apps, each with an optional label (often the name of the app you blocked it from)
- **Connection logs**: domains, IP addresses, ports and timestamps for the connections your apps make
- **Firewall alerts**: events like a firewall crash, a conflict with another VPN app, or a revoked permission
- **App settings**: your preferences, such as recovery behaviour, roaming behaviour and which notifications you want

None of it is transmitted to us or to anyone else. We create no backups and run no sync.

## 3. What leaves your device

Nothing, apart from the purchase described in section 7.

Cakebyte contains no analytics SDK and no advertising. Nothing reports crashes back to
us either. It does not profile you, and there is no data for us to sell even if we
wanted to. At runtime the app contacts no server of ours, because there isn't one.

It does bundle a static copy of the [StevenBlack/hosts](https://github.com/StevenBlack/hosts)
blocklist (MIT License) so it can recognise known tracking domains. That file ships
inside the app and is read from local storage. Nothing is fetched at runtime, and no
lookup you make is sent anywhere.

**VPN usage.** Cakebyte uses Android's `VpnService` API to open a local tunnel so it
can inspect packets on the device. It is not a VPN service in the usual sense: your
traffic is never relayed through a server we or anyone else operates.

## 4. Permissions

| Permission | Why it is needed |
|---|---|
| `QUERY_ALL_PACKAGES` | To display the full list of installed apps so you can set firewall rules for each one |
| `BIND_VPN_SERVICE` | To intercept network traffic locally on-device for firewall enforcement |
| `INTERNET` | To forward the traffic your apps send, once the firewall has allowed it. Cakebyte itself sends no data anywhere |
| `FOREGROUND_SERVICE` | To keep the firewall running while the app is in the background |
| `FOREGROUND_SERVICE_CONNECTED_DEVICE` | The foreground-service type that Android 14 and later requires for a VPN service |
| `RECEIVE_BOOT_COMPLETED` | To restart the firewall automatically after the device reboots, if enabled |
| `POST_NOTIFICATIONS` | To show firewall status and blocked connection alerts |
| `ACCESS_NETWORK_STATE` | To detect when you switch between WiFi and mobile data |
| `CHANGE_NETWORK_STATE` | To bring the local VPN tunnel up and down as your device moves between networks |
| `WAKE_LOCK` | To keep packet forwarding responsive while the screen is off so background streaming does not stall, when "Keep awake for streaming" is enabled |
| `USE_BIOMETRIC` | To unlock the app with your fingerprint, face, or device PIN/pattern/password when the optional App Lock is enabled. Authentication is performed entirely by Android; Cakebyte never receives or stores your biometric data |
| `com.android.vending.BILLING` | To process the optional one-time in-app purchase that unlocks Pro features, through Google Play |

## 5. Logging and deletion

Connection logging is on by default. Turn off **Activity logging** in settings and the
app stops recording connections altogether.

You can wipe the connection logs and the alert history from inside the app whenever you
want. Logs belonging to a particular app are also dropped automatically if you uninstall
or disable that app.

One thing that wipe does not cover: Cakebyte keeps a small daily roll-up per app,
holding nothing but connection and block counts. There are no domains, addresses or
timestamps in it. It stays on your device like everything else, and uninstalling
Cakebyte clears it along with the rest.

## 6. App Lock and device security

Everything lives in the app's private storage, which Android keeps sandboxed from other
apps. Beyond that the usual advice applies: a screen lock and current OS updates protect
device-stored data better than anything an app can do for you.

**App Lock** is an optional extra. Switch it on and Cakebyte asks for authentication
when you open it, and again if it has sat in the background for more than about 30
seconds, so someone holding your unlocked phone cannot change your firewall rules or
read your connection logs. It ships off by default.

Android handles the authentication itself, through its biometric and device-credential
APIs. Cakebyte stores no credentials and never sees your fingerprint or face data. While
App Lock is on, the app also hides its contents from the recents screen.

## 7. Purchases

The firewall itself is free. Pro adds the detailed connection log, per-app statistics
and alerts, and you get a 14-day trial before deciding. Unlocking it is a single
one-time purchase. There is no subscription and there are no ads.

Google Play Billing processes the payment, the same system behind every paid app on the
Play Store. Google runs the transaction and keeps a record of what you own so it can be
restored on any device where you are signed in. We never receive or store your payment
details, and Google's own privacy policy governs how it handles them. Your trial status
is tracked locally and never uploaded.

The app talks to Google Play for one reason: to complete or restore a purchase. Your
firewall rules and connection logs are never part of that conversation.

Your purchase is permanent. We will not remotely disable or restrict anything you have
unlocked.

## 8. Children

Cakebyte is not aimed at children under 13, or under whatever minimum age applies where
you live. We do not knowingly collect information from children. Since we collect
nothing from anyone, there is nothing on our side to process.

## 9. Changes to this policy

We may revise this policy occasionally. When something material changes, the
"Last updated" date above changes with it, and where it matters we will say so in the
app or on the store listing.

## 10. Contact

Questions about any of this: twius.09@gmail.com
