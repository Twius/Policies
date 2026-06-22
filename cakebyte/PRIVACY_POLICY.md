---
layout: default
title: Privacy Policy — Cakebyte
permalink: /cakebyte/
---

# Privacy Policy for Cakebyte

**Effective date:** 2026-06-09
**Last updated:** 2026-06-22
**App:** cakebyte

This Privacy Policy explains how the Cakebyte Android application ("Cakebyte", "the app", "we") handles your information. Cakebyte is a **firewall** app for Android: it lets you allow or block individual apps' network access, block IP addresses and ranges, and review connection activity — all on your device.

> **Summary:** Cakebyte has no servers and no user accounts. It collects, transmits, and shares no personal data — everything it generates stays on your device. Cakebyte uses Android's local VPN API only to filter traffic on-device; no traffic is ever routed to an external server. The one exception is your **optional one-time purchase**, which — like every paid app on the Play Store — is processed by Google Play solely to unlock the Pro features. It carries none of your firewall activity and does not track you.

---

## 1. Who we are

Cakebyte is developed by **Twius**.
Contact: **twius.09@gmail.com**.

We do not operate any backend server, database, or cloud service for Cakebyte. We never receive, store, or have access to your data. If you buy the Pro upgrade, the payment is handled entirely by Google Play — we never see or store your payment details.

---

## 2. Data stored on your device

All data the app generates is stored **locally** on your device in a private SQLite database and the app's private storage. This includes:

- **Firewall rules** — which apps are allowed or blocked on WiFi and mobile data
- **IP blocklist** — IP addresses and CIDR ranges you have chosen to block for all apps, with an optional label (such as the name of the app you blocked the address from)
- **Connection logs** — domains, IP addresses, ports, and timestamps of network connections made by apps on your device
- **Firewall alerts** — system events such as firewall crashes, VPN conflicts, and permission revocations
- **App settings** — your preferences such as firewall recovery, roaming behaviour, and notification settings

This data is **not** transmitted to us or to any third party. There are no servers, no cloud sync, and no backups created by us.

---

## 3. Information shared with third parties

Cakebyte does **not** share any information with third parties for analytics, advertising, or profiling. Apart from completing a purchase you choose to make (see **Purchases** below), it contacts no external server at runtime — there is no cloud sync, no analytics, and no advertising.

**Purchases (Google Play Billing).** Cakebyte's core firewall is free. The Pro features are unlocked by a single, optional one-time purchase after a free 14-day trial (no subscription). If you choose to buy, the purchase is processed by **Google Play Billing** — Google's standard payment system used by all paid apps on the Play Store. Google handles the transaction and records your entitlement so it can be restored on your devices; we never receive or store your payment details. The app contacts Google Play only to complete or restore a purchase — never to transmit your firewall rules, connection logs, or any other activity. Your trial status is tracked locally on your device. How Google processes payments is governed by Google's own privacy policy.

Cakebyte bundles a static copy of the [StevenBlack/hosts](https://github.com/StevenBlack/hosts) unified hosts blocklist (MIT License) to identify known tracking domains. This list is included in the app at build time and is never fetched at runtime; no data is sent to or received from any external server as a result of it.

---

## 4. Permissions and why they are used

| Permission | Why it is needed |
|---|---|
| `QUERY_ALL_PACKAGES` | To display the full list of installed apps so you can set firewall rules for each one |
| `BIND_VPN_SERVICE` | To intercept network traffic locally on-device for firewall enforcement |
| `FOREGROUND_SERVICE` | To keep the firewall running while the app is in the background |
| `RECEIVE_BOOT_COMPLETED` | To restart the firewall automatically after the device reboots, if enabled |
| `POST_NOTIFICATIONS` | To show firewall status and blocked connection alerts |
| `ACCESS_NETWORK_STATE` | To detect when you switch between WiFi and mobile data |
| `WAKE_LOCK` | To keep packet forwarding responsive while the screen is off so background streaming does not stall, when "Keep awake for streaming" is enabled |
| `com.android.vending.BILLING` | To process the optional one-time in-app purchase that unlocks Pro features, through Google Play |

**VPN usage:** Cakebyte uses Android's `VpnService` API to create a local VPN tunnel. All traffic interception happens entirely on your device. Cakebyte is not a VPN service — no traffic is routed to any external server.

---

## 5. Analytics, advertising, and tracking

Cakebyte contains **no analytics SDKs, no advertising, and no third-party tracking**, and uses no crash-reporting tools. We do not profile you, and we do not sell or share personal data. The only third-party component in the app is Google Play Billing, used solely to process the optional purchase described above; it performs no advertising or behavioural tracking within Cakebyte.

---

## 6. Data logging, deletion, and control

- **Activity logging:** Connection logging is on by default. When you turn off **Activity logging** in settings, connections are not recorded to your device at all.
- **Deletion:** You can delete all connection logs and firewall alerts at any time from within the app. Connection logs for a specific app are also deleted automatically when that app is uninstalled or disabled on your device. Uninstalling Cakebyte removes all locally stored data.

---

## 7. Children's privacy

Cakebyte is not directed to children under 13 (or the minimum age required in your jurisdiction). We do not knowingly collect personal information from children. Since no data is collected by us, no such data is processed on our side.

---

## 8. Security

Your data is stored in the app's private, sandboxed storage provided by Android. As with any device-stored data, keeping your device secure (screen lock, OS updates) is the best protection.

---

## 9. Ownership and purchases

Cakebyte's core firewall is free to use. The Pro features (such as detailed connection logs, per-app activity statistics, and alerts) are unlocked by a single **one-time purchase** after a free 14-day trial. There are **no subscriptions, no recurring fees, and no ads.**

Your purchase is permanent. It is tied to your Google account and can be restored on any device where you are signed in. We will never remotely disable, restrict, or revoke features you have unlocked, and we will never sell or share your data.

---

## 10. Changes to this policy

We may update this Privacy Policy from time to time. Material changes will be reflected by updating the "Last updated" date above and, where appropriate, within the app or its store listing.

---

## 11. Contact

Questions about this Privacy Policy? Contact **twius.09@gmail.com**.
