---
layout: default
title: Privacy Policy for Sifdroid
permalink: /sifdroid/
---

# Privacy Policy for Sifdroid

**Effective date:** 2026-06-04
**Last updated:** 2026-09-24
**App:** sifdroid

This Privacy Policy explains how the Sifdroid Android app handles your information. Sifdroid is a personal-finance documentation app: it records the accounts, income, expenses, transfers, investment holdings, and assets that you enter yourself. It does not execute trades or payments.

> **In short:** Sifdroid has no servers and no user accounts, and your financial data stays on your device. Only a few requests leave it. The app sends stock and crypto symbols to market-data providers to get prices, and dates to an exchange-rate provider to get the rates for those days. It also asks Google Play whether you own Sifdroid Pro, the app's optional in-app purchase. Your balances, amounts, holdings, and notes are never sent anywhere.

## 1. Who we are

Sifdroid is developed by Twius.
Contact: **twius.09@gmail.com**.

We do not operate any backend server, database, or cloud service for Sifdroid. We never receive or store your data, and we have no way to access it.

## 2. Data stored on your device

Everything you enter is stored locally on your device, in a private SQLite database (`sifdroid.db`) and the app's private storage. This includes:

- Accounts you create (name, icon, and currency) and the transfers you record between them
- Transactions (income, expenses, transfers), categories, and recurring rules
- Investment portfolio and watchlist entries: symbols, quantities, the prices you enter, and each holding's currency
- Your record of investment buys and sells, including quantity, price, and date
- Assets: name, description, category, currency, and the value you enter, plus the asset categories you create
- App settings, including your base currency, dashboard preferences (section order and which sections are shown or hidden), any API keys you provide, and whether Sifdroid Pro has been purchased
- Notification preferences

The app also keeps copies of public data it downloads, such as exchange-rate tables and company logos, so that screens still work offline.

None of this is transmitted to us or to any third party for storage. Android backup is disabled for the app (`allowBackup="false"`), so it is not copied into cloud backups by the operating system.

## 3. Information shared with third parties

To show live market data and convert between currencies, Sifdroid contacts the following services directly from your device. Only what each lookup needs is sent: an asset symbol, or for exchange rates, a date or a range of dates. When you add a holding, the app looks the symbol up as you type, so whatever is in the symbol field is sent to Finnhub or CoinGecko while you are still typing it. Your amounts, quantities, balances, and notes are never sent.

| Service | Purpose | What is sent |
|---|---|---|
| **Finnhub** (finnhub.io) | Symbol search, stock price, earnings dates, basic financials, and company profile (name, listing currency, logo URL) | Stock symbol (e.g. `AAPL`), including what you have typed so far while looking one up, and your Finnhub API key |
| **CoinGecko** (coingecko.com) | Coin lookup, crypto price, 24h change, and market data (name, financials, image URL) | Coin identifier, or the symbol you typed (e.g. `bitcoin`, `BTC`), and your CoinGecko API key, if you provided one |
| **Frankfurter** (frankfurter.dev) | Currency exchange rates, for today and for past days | A request for the US dollar rate table, either the latest one or the one for a past date or range of dates. Those dates are the days of your entries, transfers, and investment purchases in a currency other than your base currency. Your amounts and your base currency are not sent, and the conversion happens on your device |

When a stock or coin logo is shown, the app also downloads that image directly from the logo URL the provider returned, which may be the provider itself or a CDN host. Such a request necessarily reveals your device's IP address and which image you are loading to that host, but never your balances, amounts, or holdings.

Price lookups are made only when you have added investments or watchlist items, or use a feature that needs them. The latest exchange-rate table is downloaded about once a day when you open the app, even if you only use one currency. Past rates are downloaded only when your records use a currency other than your base currency. Each provider processes the request under its own privacy policy:

- Finnhub: https://finnhub.io/privacy-policy
- CoinGecko: https://www.coingecko.com/en/privacy
- Frankfurter: https://frankfurter.dev/

API keys you enter are stored locally on your device and are sent only to the provider they belong to, to authenticate your own requests.

### Sifdroid Pro (optional in-app purchase)

Sifdroid is free to install and free to use for everyday budgeting. Some features (investments, assets, and recurring transactions) are unlocked by **Sifdroid Pro**, an optional one-time in-app purchase processed entirely by Google Play under [Google's privacy policy](https://policies.google.com/privacy). There is no subscription.

Each time you open Sifdroid, or return to it from the background, it asks Google Play whether Sifdroid Pro has been purchased on your account, so that the right features are available. This check happens whether or not you have bought it, and it is also what the "Restore purchase" button uses after you reinstall the app or move to a new device. If it cannot reach Google Play, the app keeps using the answer it last received.

Sifdroid never sees or stores your payment details, such as your card number or billing address. From Google Play it receives only whether the purchase exists. That single yes-or-no answer is the only purchase-related information kept on your device, and nothing about it is sent to us; we have no server to send it to.

## 4. Permissions and device access

These are the permissions Sifdroid uses, including the ones added by the Google and AndroidX libraries it is built with rather than by our own code.

- **Internet:** to fetch live prices, exchange rates, and logo images from the providers listed above, and to let Google Play process and verify the Sifdroid Pro purchase. The app makes no other network requests.
- **Notifications (POST_NOTIFICATIONS):** to show local reminders of upcoming earnings for the stocks you follow. Every notification is generated on your device; there is no push server.
- **Boot completed (RECEIVE_BOOT_COMPLETED):** to re-schedule your local reminders after the device restarts.
- **Biometric (USE_BIOMETRIC, plus the legacy USE_FINGERPRINT that the AndroidX biometric library adds for older Android versions):** the optional app lock. Authentication is handled entirely by Android's `BiometricPrompt`, using your biometric or, as a fallback, your device PIN, pattern, or password. Sifdroid never sees or stores your fingerprint, face, PIN, or passcode.
- **Billing (com.android.vending.BILLING) and network state (ACCESS_NETWORK_STATE):** added by Google's Play Billing library and its dependencies, which handle the Sifdroid Pro purchase and need to know whether the device is online.

Sifdroid requests no location permission, no contacts permission, and no storage or media permission.

When you export or import a backup, Android's own file picker lets you choose where the file goes or which file to open, and the app is given access to that one file only. No storage permission is involved.

Reminders are delivered through Android's alarm scheduler. The app never requests the exact-alarm permission. On Android 12 and later it uses inexact alarms; on earlier versions it uses the exact scheduling that is available there without any permission.

## 5. Analytics, advertising, and tracking

Sifdroid itself contains no analytics SDK, no advertising, and no tracking. We do not profile you, and we do not sell or share personal data. We receive nothing at all about your use of the app, because there is nowhere for it to be received.

Google's Play Billing library is the exception. It ships with Google Play services components and Google's own event-reporting library, and uses them to send Google diagnostics about the billing flow. That is Google's processing, not ours, and it carries none of your financial data.

## 6. Data export, import, and deletion

- **Export:** You can export your data from Settings, under Data. The app writes a single `.json` file with all of your data to a location you choose. Your app settings are deliberately left out, so the file never contains your API keys. The file is created entirely on your device and is never sent to us or to anyone else. It does contain your financial data, so store and share it carefully: anyone who can open it can read it.
- **Import:** You can restore from a backup file you provide: a `.json` backup, or a `.zip` or CSV backup from an earlier version of the app. Savings goals and photos in an older backup are skipped, since the app no longer has either. Importing replaces the app's current data with the contents of the file.
- **Deletion:** Because everything is local, you can delete it permanently by clearing the app's storage in Android settings, or by uninstalling the app. Uninstalling removes the local database and everything in it. Your Sifdroid Pro purchase is separate: it belongs to your Google account rather than to the installed app, so it survives uninstalling and can be restored later. Any backup files you exported stay wherever you saved them, and you delete those yourself.

## 7. Your rights

Data protection law gives you rights over personal data an organisation holds about you: access, correction, erasure, portability. We hold none. Sifdroid has no server and no account system, so there is no copy on our side to hand over, correct or delete. Everything those rights would cover sits on your device, under your control: the export function is your portability, and clearing the app's storage or uninstalling is your erasure.

Google processes your purchase, and its own billing diagnostics, as a separate controller. Rights over that data are exercised with Google, under [Google's privacy policy](https://policies.google.com/privacy).

## 8. Children's privacy

Sifdroid is not directed to children under 13, or the minimum age required in your jurisdiction. We do not knowingly collect personal information from children. Since we collect no data at all, no such data is processed on our side.

## 9. Security

Your data lives in the app's private, sandboxed storage, provided by Android. You can enable the optional app lock, opened with your biometric or your device PIN, pattern, or password, for another layer of protection. It re-locks whenever the app is sent to the background or your screen turns off, and while it is locked the app's contents are covered by a full-screen lock screen and kept out of the system's recent-apps preview. Keeping the device itself secure, with a screen lock and current OS updates, remains the best protection for anything stored on it.

## 10. Related documents

This policy covers what happens to your information. The [Terms of Use](/Policies/sifdroid/terms/) cover the rest: what the app does, what it does not promise, and the Sifdroid Pro purchase.

## 11. Changes to this policy

We may update this Privacy Policy from time to time. Material changes will be reflected by updating the "Last updated" date above and, where appropriate, within the app or its store listing.

## 12. Contact

Questions about this Privacy Policy? Contact **twius.09@gmail.com**.
