---
layout: default
title: Privacy Policy - Sifdroid
permalink: /sifdroid/
---

# Privacy Policy for Sifdroid

**Effective date:** 2026-06-04
**Last updated:** 2026-08-29
**App:** sifdroid

This Privacy Policy explains how the Sifdroid Android app handles your information. Sifdroid is a personal-finance documentation app: it records the income, expenses, savings goals, investment holdings, and assets that you enter yourself. It does not execute trades or payments.

In short: Sifdroid has no servers and no user accounts, and your financial data stays on your device. Two kinds of information do leave it. The app sends stock and crypto symbols and currency codes to third-party market-data providers to look up live prices, and it asks Google Play whether you own Sifdroid Pro, the app's optional in-app purchase. Your balances, amounts, holdings, notes, and goals are never sent anywhere.

## Who we are

Sifdroid is developed by Twius.
Contact: **twius.09@gmail.com**.

We do not operate any backend server, database, or cloud service for Sifdroid. We never receive or store your data, and we have no way to access it.

## Data stored on your device

Everything you enter is stored locally on your device, in a private SQLite database (`sifdroid.db`) and the app's private storage. This includes:

- Accounts you create (name and icon) and the transfers you record between them
- Transactions (income, expenses, transfers), categories, and recurring rules
- Savings goals, contributions, and any goal photo you select
- Investment portfolio and watchlist entries: symbols, quantities, the prices you enter, and each holding's currency
- Your record of investment buys and sells, including quantity, price, and date
- Assets: name, description, category, the value you enter, and any asset photo you select
- App settings, including your base currency, dashboard preferences (section order and which sections are shown or hidden), any API keys you provide, and whether Sifdroid Pro has been purchased
- Notification preferences

None of this is transmitted to us or to any third party for storage. Android backup is disabled for the app (`allowBackup="false"`), so it is not copied into cloud backups by the operating system.

## Information shared with third parties

To show live market data, Sifdroid contacts the following services directly from your device. Only the minimum lookup parameters are sent: an asset symbol or a currency code. Your amounts, quantities, balances, notes, and goals are never sent.

| Service | Purpose | What is sent |
|---|---|---|
| **Finnhub** (finnhub.io) | Stock price, earnings dates, basic financials, and company profile (name, listing currency, logo URL) | Stock symbol (e.g. `AAPL`) and your Finnhub API key |
| **CoinGecko** (coingecko.com) | Crypto price, 24h change, and market data (name, financials, image URL) | Coin identifier (e.g. `bitcoin`) and your CoinGecko API key, if you provided one |
| **Frankfurter** (frankfurter.app) | Daily currency exchange rates | A request for the US dollar rate table. Your own base currency is not sent; the conversion happens on your device |

When a stock or coin logo is shown, the app also downloads that image directly from the logo URL the provider returned, which may be the provider itself or a CDN host. Such a request necessarily reveals your device's IP address and which image you are loading to that host, but never your balances, amounts, or holdings.

These requests are made only when you have added investments or watchlist items, or use a feature that needs them. Each provider processes the request under its own privacy policy:

- Finnhub: https://finnhub.io/privacy-policy
- CoinGecko: https://www.coingecko.com/en/privacy
- Frankfurter: https://www.frankfurter.app/

API keys you enter are stored locally on your device and are sent only to the provider they belong to, to authenticate your own requests.

### Sifdroid Pro (optional in-app purchase)

Sifdroid is free to install and free to use for everyday budgeting. Some features (investments, assets, unlimited savings goals, and recurring transactions) are unlocked by **Sifdroid Pro**, an optional one-time in-app purchase processed entirely by Google Play under [Google's privacy policy](https://policies.google.com/privacy). There is no subscription.

Each time the app starts, it asks Google Play whether Sifdroid Pro has been purchased on your account, so that the right features are available. This check happens whether or not you have bought it, and it is also what the "Restore purchase" button uses after you reinstall the app or move to a new device.

Sifdroid never sees or stores your payment details, such as your card number or billing address. From Google Play it receives only whether the purchase exists. That single yes-or-no answer is the only purchase-related information kept on your device, and nothing about it is sent to us; we have no server to send it to.

## Permissions and device access

Sifdroid's installed app declares the following permissions. Some are added automatically by the Google and AndroidX libraries it uses, rather than requested by our own code, so they are listed here too.

- **Internet:** to fetch live prices, exchange rates, and logo images from the providers listed above, and to let Google Play process and verify the Sifdroid Pro purchase. The app makes no other network requests.
- **Notifications (POST_NOTIFICATIONS):** to show local reminders (earnings alerts, savings reminders, goal completion). Every notification is generated on your device; there is no push server.
- **Boot completed (RECEIVE_BOOT_COMPLETED):** to re-schedule your local reminders after the device restarts.
- **Biometric (USE_BIOMETRIC, plus the legacy USE_FINGERPRINT that the AndroidX biometric library adds for older Android versions):** the optional app lock. Authentication is handled entirely by Android's `BiometricPrompt`, using your biometric or, as a fallback, your device PIN, pattern, or password. Sifdroid never sees or stores your fingerprint, face, PIN, or passcode.
- **Billing (com.android.vending.BILLING) and network state (ACCESS_NETWORK_STATE):** added by Google's Play Billing library and its dependencies, which handle the Sifdroid Pro purchase and need to know whether the device is online.

Sifdroid requests no location permission, no contacts permission, and no storage or media permission.

When you choose a photo for a savings goal or an asset, no permission is involved: the app opens Android's picker, which may be the system photo picker or a gallery app you choose, and receives access to only the single image you pick. That image is copied into the app's private storage and referenced locally. It is never uploaded.

Reminders are delivered through Android's alarm scheduler. The app never requests the exact-alarm permission. On Android 12 and later it uses inexact alarms; on earlier versions it uses the exact scheduling that is available there without any permission.

## Analytics, advertising, and tracking

Sifdroid itself contains no analytics SDK, no advertising, and no tracking. We do not profile you, and we do not sell or share personal data. We receive nothing at all about your use of the app, because there is nowhere for it to be received.

One qualification, for completeness. Google's Play Billing library, used for the Sifdroid Pro purchase, ships with Google Play services components and with Google's own event-reporting library, and it uses them to send diagnostic information about the billing flow to Google. That is Google's processing under [Google's privacy policy](https://policies.google.com/privacy), not ours, and it carries none of your financial data. Those components also include ones the app never calls, such as the location component that the billing library lists as a dependency. Since Sifdroid requests no location permission, your location cannot be read.

## Data export, import, and deletion

- **Export:** You can export your data from Settings, under Data. The app writes a single `.zip` archive, containing a CSV file of your data plus copies of any goal or asset photos you added, to a location you choose. Your app settings are deliberately left out, so the archive never contains your API keys. The file is created entirely on your device and is never sent to us or to anyone else. It does contain your financial data and your photos, so store and share it carefully: anyone who can open it can read it.
- **Import:** You can restore from a backup file you provide, either a `.zip` backup or a plain CSV. Importing replaces the app's current data with the contents of the file.
- **Deletion:** Because everything is local, you can delete it permanently by clearing the app's storage in Android settings, or by uninstalling the app. Uninstalling removes the local database and everything in it. Your Sifdroid Pro purchase is separate: it belongs to your Google account rather than to the installed app, so it survives uninstalling and can be restored later. Any backup files you exported stay wherever you saved them, and you delete those yourself.

## Children's privacy

Sifdroid is not directed to children under 13, or the minimum age required in your jurisdiction. We do not knowingly collect personal information from children. Since we collect no data at all, no such data is processed on our side.

## Security

Your data lives in the app's private, sandboxed storage, provided by Android. You can enable the optional app lock, opened with your biometric or your device PIN, pattern, or password, for another layer of protection. It re-locks whenever the app is sent to the background or your screen turns off, and while it is locked the app's contents are covered by a full-screen lock screen and kept out of the system's recent-apps preview. Keeping the device itself secure, with a screen lock and current OS updates, remains the best protection for anything stored on it.

## Changes to this policy

We may update this Privacy Policy from time to time. Material changes will be reflected by updating the "Last updated" date above and, where appropriate, within the app or its store listing.

## Contact

Questions about this Privacy Policy? Contact **twius.09@gmail.com**.
