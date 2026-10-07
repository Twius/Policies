---
layout: default
title: Privacy Policy for Sifdroid
permalink: /sifdroid/
nav_order: 6
---

# Privacy Policy for Sifdroid

**First published:** 2026-06-04<br>
**Last updated:** 2026-10-07

Sifdroid is a personal-finance documentation app: it records the accounts, income, expenses, transfers, investment holdings, and assets that you enter yourself. It does not execute trades or payments. This Privacy Policy explains how it handles your information. "We" and "us" mean Twius, the developer of Sifdroid.

{: .summary }
**In short:** Sifdroid works without servers or user accounts. Your financial records stay on your device, and only a few requests leave it. The app sends stock and crypto symbols to market-data providers to get prices, and dates to an exchange-rate provider to get the rates for those days. It also asks Google Play whether you own Sifdroid Pro, the app's optional in-app purchase, and Google's billing library sends Google diagnostics. Your balances, amounts, quantities, and notes are never sent anywhere.

## 1. Who we are {#who-we-are}

Sifdroid is developed by Twius (Anastasis Anastasi, an individual developer in Cyprus). You can reach us at [twius.09@gmail.com](mailto:twius.09@gmail.com).

There is no backend server, database, or cloud service behind Sifdroid. The app never sends us anything it stores, so we cannot see or access your app data. [Section 2](#what-we-receive) lists what we do receive.

## 2. What we receive {#what-we-receive}

We receive personal information in only these ways:

- **Emails you send us:** your email address and whatever you write or attach. We use them only to reply to you, and delete them once the matter is settled. Our email is provided by Google (Gmail), which may store it outside the EU, including in the United States. Google LLC is certified under the EU-US Data Privacy Framework.
- **Google Play sales records:** when you buy Sifdroid Pro, Google gives us its usual seller's record of the sale, such as the order number, date, price, device model, and your country, and in some countries your city and postcode. We can look up an order by the email address you paid with. It never includes your card details. We use it for support, refunds, and tax records, and keep it as long as tax law requires.
- **Crash reports:** if you have chosen to share usage and diagnostics data with Google, Google Play shows us reports of the app's crashes and freezes. They contain technical details such as the device model, the Android version, and where in the app the error happened, which can include an error message from the app. Google does not tell us who you are.

Under EU and UK data protection law, our legal basis is our legitimate interest in answering you and supporting the app, and our legal duty to keep tax records.

## 3. Data stored on your device {#data-on-device}

Everything Sifdroid stores is kept on your device. It is kept in a private SQLite database (`sifdroid.db`) and the app's private storage. That covers:

- Accounts you create (name, icon, and currency) and the transfers you record between them
- Transactions (income, expenses, and transfers), categories, and recurring rules
- Investment portfolio and watchlist entries: symbols, quantities, the prices you enter, and each holding's currency
- Your record of investment buys and sells, including quantity, price, and date
- Assets: name, description, category, currency, and the value you enter, plus the asset categories you create
- Totals the app has worked out from these records, and upcoming earnings dates for your reminders
- App settings, including your base currency, dashboard preferences (section order and which sections are shown or hidden), any API keys you provide, and whether Sifdroid Pro has been purchased
- Notification preferences

The app also keeps copies of public data it downloads, such as exchange-rate tables and company logos, so that screens still work offline.

None of it is sent to us, and nothing is sent to anyone else except as described in [section 4](#what-leaves). The app does not back up or sync anything to a server. Android's cloud backup is switched off for the app, so none of it is copied to your Google account. If you move to a new phone with a direct device-to-device transfer, Android may copy the app's data across.

## 4. What leaves your device {#what-leaves}

To show live market data and convert between currencies, Sifdroid contacts the following services directly from your device. Only what each lookup needs is sent: an asset symbol, or for exchange rates, a date or a range of dates, and for earnings dates, today's date and the date a year ahead. When you add a holding or a watchlist item, the app looks the symbol up as soon as you leave the symbol field, so whatever you typed there, finished or not, is sent to Finnhub or CoinGecko. Your amounts, quantities, balances, and notes are never sent.

| Service | Purpose | What is sent |
|---|---|---|
| **Finnhub** (finnhub.io) | Symbol search, stock price, earnings dates, basic financials, and company profile (name, listing currency, and logo URL) | Stock symbol (e.g. `AAPL`), including an unfinished one you typed while adding a holding or watchlist item, and your Finnhub API key |
| **CoinGecko** (coingecko.com) | Coin lookup, crypto price, 24h change, and market data (name, financials, and image URL) | Coin identifier, or the symbol you typed (e.g. `bitcoin`, `BTC`), and your CoinGecko API key, if you provided one |
| **Frankfurter** (frankfurter.dev) | Currency exchange rates, for today and for past days | A request for the US dollar rate table, either the latest one or the one for a past date or range of dates. Those dates are the days of your entries, transfers, and investment purchases in a currency other than your base currency. Your amounts and your base currency are not sent, and the conversion happens on your device |

When a stock or coin logo is shown, the app also downloads that image directly from the logo URL the provider returned, which may be the provider itself or a CDN host. That request shows the host which image you are loading, and so which stock or coin you follow, but never your balances, amounts, or quantities.

Every request, like any internet connection, also shows the provider your IP address. Because your API keys belong to your own provider accounts, Finnhub, and CoinGecko if you entered a key, can link your lookups to you. Finnhub is based in the United States and CoinGecko in Singapore, and Frankfurter runs on a global network, so requests may be handled outside your country. Your device connects to these providers directly. We do not send them anything ourselves, and we keep nothing from these requests. Each provider decides how long it keeps its own logs. Under EU and UK data protection law, our legal basis for these lookups is our legitimate interest in making the app's features work, including keeping exchange rates current. You can object by writing to us. Price lookups stop when you remove your investments and watchlist items, but the daily exchange-rate download stops only if you stop using the app.

Price lookups are made only when you have added investments or watchlist items, or use a feature that needs them. The latest exchange-rate table is downloaded about once a day when you open the app, even if you only use one currency. Past rates are downloaded only when your records use a currency other than your base currency.

Each provider handles the requests it receives under its own terms and privacy practices: see the [Finnhub privacy policy](https://finnhub.io/privacy-policy), the [CoinGecko privacy policy](https://www.coingecko.com/en/privacy), and the [Frankfurter website](https://frankfurter.dev/).

API keys you enter are stored locally on your device and are sent only to the provider they belong to, to authenticate your own requests.

The app also talks to Google Play about Sifdroid Pro (see [section 7](#purchases)), and Google's billing library sends Google diagnostics (see [section 6](#analytics)). If you have chosen to share usage and diagnostics data with Google, Android also sends Google a report when the app crashes or freezes. That report can sometimes include part of what the app was working on at the time (see [section 2](#what-we-receive)).

## 5. Permissions {#permissions}

These are the permissions Sifdroid uses, including the ones added by the Google and AndroidX libraries it is built with rather than by our own code.

| Permission | Why it is needed |
|---|---|
| `INTERNET` | To fetch live prices, exchange rates, and logo images from the providers listed above. Google's Play Billing library also uses it to send Google the billing diagnostics described in [section 6](#analytics). The app makes no other network requests |
| `POST_NOTIFICATIONS` | To show local reminders of upcoming earnings for the stocks you follow. Every notification is generated on your device; there is no push server |
| `RECEIVE_BOOT_COMPLETED` | To re-schedule your local reminders after the device restarts |
| `USE_BIOMETRIC` | For the optional **App lock**. Authentication is handled entirely by Android's `BiometricPrompt`, using your biometric or, as a fallback, your device PIN, pattern, or password. Sifdroid never sees or stores your fingerprint, face, PIN, or passcode |
| `USE_FINGERPRINT` | Added by the AndroidX biometric library for older Android versions, for the same optional app lock |
| `com.android.vending.BILLING` | Added by Google's Play Billing library, which handles the Sifdroid Pro purchase |
| `ACCESS_NETWORK_STATE` | Added by Google's event-reporting library, which Play Billing uses, to check for a connection before sending its diagnostics |
| `com.sifdroid.DYNAMIC_RECEIVER_NOT_EXPORTED_PERMISSION` | Added by the AndroidX core library. It is private to Sifdroid and only stops other apps from sending it internal messages |

Sifdroid requests no location, contacts, camera, or microphone permission. It also requests no storage or media permission: when you export or import a backup, Android's own file picker lets you choose where the file goes or which file to open, and the app is given access to that one file only.

Reminders are delivered through Android's alarm scheduler. The app never requests the exact-alarm permission. On Android 12 and later it uses inexact alarms unless Android itself allows exact ones; on earlier versions it uses the exact scheduling that is available there without any permission.

## 6. Analytics, advertising, and tracking {#analytics}

Sifdroid does not include analytics, advertising, third-party tracking, or crash reporting of its own. We do not profile you, and we do not sell your personal data or use it for advertising.

The only part of Sifdroid that sends diagnostics anywhere is Google's Play Billing library, which handles Sifdroid Pro. It ships with Google Play services components and Google's event-reporting library, which send Google diagnostics about the billing flow. Google decides what they contain and how they are used. We never receive them, and they contain none of your financial records.

## 7. Purchases {#purchases}

Sifdroid is free to install and free to use for everyday budgeting. Some features (investments, assets, and recurring transactions) are unlocked by Sifdroid Pro, an optional in-app purchase. Sifdroid Pro is a single one-time purchase. It is not a subscription, and the app does not show ads.

Google Play Billing processes the payment. Google runs the transaction and keeps a record of what you own, so it can be restored on any device where you are signed in. We never see your card details, and [Google's privacy policy](https://policies.google.com/privacy) governs how Google handles them.

Each time you open Sifdroid, or return to it from the background, it asks Google Play whether you own Sifdroid Pro, so that the right features are available. This check happens whether or not you have bought it, and it is also what the **Restore purchase** button uses after you reinstall the app or move to a new device. If it cannot reach Google Play, the app keeps using the answer it last received. From Google Play the app receives the product's details, such as its price, and whether you own it. The app sends nothing about the purchase to us. Google's sales record is described in [section 2](#what-we-receive). The only purchase information the app itself keeps is whether you own Sifdroid Pro. Google's billing library may briefly hold its own diagnostics on the device before sending them.

The [Terms of Use]({{ '/sifdroid/terms/' | relative_url }}) cover what the purchase includes and how refunds work.

## 8. Managing and deleting your data {#deletion}

**Export:** You can export your data from **Settings**, under **Data**. The app writes a single `.json` file with all of your data to a location you choose. Your app settings are deliberately left out, so the file never contains your API keys. The app never sends the file to us or to anyone else. If you save it to a cloud service such as Google Drive, that service stores it. It does contain your financial data, so store and share it carefully: anyone who can open it can read it.

**Import:** You can restore from a backup file you provide: a `.json` backup, or a `.zip` or CSV backup from an earlier version of the app. Savings goals and photos in an older backup are skipped, since the app no longer has either. Importing replaces the app's current data with the contents of the file.

Clearing the app's data in Android settings, or uninstalling Sifdroid, removes everything it keeps on your device. Your Sifdroid Pro purchase is separate: it belongs to your Google account rather than to the installed app, so it survives uninstalling and can be restored later. Any backup files you exported stay wherever you saved them, and you delete those yourself.

## 9. Your rights {#your-rights}

Data protection law gives you rights over the personal data an organisation holds about you, such as access, correction, erasure, and portability. We hold none of the data the app stores. Sifdroid does not use a server or accounts, so we have no copy to hand over, correct, or delete. Everything those rights would cover sits on your device, under your control: the export function gives you portability, and clearing the app's data or uninstalling the app gives you erasure.

For what we do receive (see [section 2](#what-we-receive)), you can ask us for a copy of it, ask us to correct or delete it, ask us to limit how we use it, or object to our using it, by writing to [twius.09@gmail.com](mailto:twius.09@gmail.com). Sales records we must keep for tax purposes are deleted when that period ends. You can also complain to the data protection authority where you live or work, or to ours, the [Cyprus Commissioner for Personal Data Protection](https://www.dataprotection.gov.cy).

Google processes your purchase, and its own billing diagnostics, as a separate controller, under [Google's privacy policy](https://policies.google.com/privacy). Rights over that data are exercised with Google. Sifdroid never sees your payment details.

## 10. Children's privacy {#children}

Sifdroid is not directed to children under 13, or under the minimum age that applies where you live. We do not knowingly collect personal information from children. If you think a child has sent us personal information, for example by email, tell us and we will delete it.

## 11. Security {#security}

Your data lives in the app's private storage, which Android keeps sandboxed from other apps.

You can turn on the optional **App lock**, opened with your biometric or your device PIN, pattern, or password, for another layer of protection. It locks again whenever the app is sent to the background or your screen turns off, and while it is locked, the app's contents are covered by a full-screen lock screen. While App lock is on, the app also keeps its contents out of the recent-apps preview and blocks screenshots.

Keeping the device itself secure, with a screen lock and current OS updates, remains the best protection for anything stored on it.

## 12. Changes to this policy {#changes}

We may update this policy from time to time. The version published at this address is always the current one, and the "Last updated" date at the top tells you when it last changed. If a change is material, we will point it out in the app's release notes and on its store listing before it applies to you.

## 13. Related documents {#related}

This policy covers what happens to your information. Your use of Sifdroid is also covered by the [Terms of Use]({{ '/sifdroid/terms/' | relative_url }}).

## 14. Contact {#contact}

Questions about this policy: [twius.09@gmail.com](mailto:twius.09@gmail.com).
