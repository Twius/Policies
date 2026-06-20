---
layout: default
title: Privacy Policy — Sifdroid
permalink: /sifdroid/
---

# Privacy Policy for Sifdroid

**Effective date:** 2026-06-04
**Last updated:** 2026-06-18
**App:** sifdroid

This Privacy Policy explains how the Sifdroid Android application ("Sifdroid", "the app", "we") handles your information. Sifdroid is a personal-finance **documentation** app: it records income, expenses, savings goals, investment holdings, and assets that you enter yourself. It does not execute trades or payments.

> **Summary:** Sifdroid has no servers and no user accounts. All of your financial data stays on your device. The only information that ever leaves your device is the stock/crypto symbols and currency codes needed to look up live prices from third-party market-data providers — never your balances, amounts, holdings, notes, or goals.

---

## 1. Who we are

Sifdroid is developed by **Twius**.
Contact: **twius.09@gmail.com**.

We do not operate any backend server, database, or cloud service for Sifdroid. We never receive, store, or have access to your data.

---

## 2. Data stored on your device

All data you enter is stored **locally** on your device in a private SQLite database (`sifdroid.db`) and the app's private storage. This includes:

- Transactions (income, expenses, transfers), categories, and recurring rules
- Savings goals, contributions, and any goal photos you select
- Investment portfolio and watchlist entries (symbols, quantities, prices, and each holding's currency you enter)
- Assets (name, description, category, the value you enter, and any asset photo you select)
- App settings, including your base currency, dashboard preferences (section order and which sections are shown/hidden), and any API keys you provide
- Notification preferences

This data is **not** transmitted to us or to any third party for storage. Android backup is disabled for the app (`allowBackup="false"`), so this data is not copied into cloud backups by the operating system.

---

## 3. Information shared with third parties

To show live market data, Sifdroid contacts the following third-party services directly from your device. **Only the minimum lookup parameters are sent** — i.e. the asset symbol or currency code. Your amounts, quantities, balances, notes, and goals are never sent.

| Service | Purpose | What is sent |
|---|---|---|
| **Finnhub** (finnhub.io) | Stock price, earnings dates, basic financials, and company profile (name, listing currency, logo URL) | Stock symbol (e.g. `AAPL`) and your Finnhub API key |
| **CoinGecko** (coingecko.com) | Crypto price, 24h change, and market data (name, financials, image URL) | Coin identifier (e.g. `bitcoin`) and your CoinGecko API key, if provided |
| **Frankfurter** (frankfurter.app) | Daily currency exchange rates | Currency codes (e.g. `USD`, `EUR`) |

In addition, when a stock or coin **logo** is shown, the app downloads that image directly from the logo/image URL the provider returned (a provider or CDN host). Such a request necessarily reveals your device's IP address and which image you're loading to that host, but never your balances, amounts, or holdings.

These requests are only made when you have added investments/watchlist items or use related features. Each provider processes the request under **its own privacy policy**:

- Finnhub: https://finnhub.io/privacy-policy
- CoinGecko: https://www.coingecko.com/en/privacy
- Frankfurter: https://www.frankfurter.app/

API keys you enter are stored locally on your device and are sent only to their respective provider to authenticate your own requests.

---

## 4. Permissions and why they are used

- **Internet** — to fetch live prices and exchange rates from the providers listed above. No other network communication occurs.
- **Photos** — when you choose a photo for a savings goal or an asset, the app uses Android's **system photo picker**, which grants access to only the single image you pick. Sifdroid does **not** request broad storage or media permissions. The selected image is copied into the app's private storage and referenced locally; it is never uploaded.
- **Biometric / device credential (USE_BIOMETRIC)** — optional app lock. Authentication is handled entirely by Android's `BiometricPrompt`, using your biometric **or**, as a fallback, your device PIN/pattern/password. Sifdroid never sees or stores your fingerprint, face, PIN, or passcode.
- **Notifications (POST_NOTIFICATIONS)** — to show local reminders (earnings alerts, savings reminders, goal completion). All notifications are generated on-device; there is no push server.
- **Boot completed (RECEIVE_BOOT_COMPLETED)** — to re-schedule your local reminders after the device restarts. Reminders use the system's standard (inexact) alarm scheduling; the app does not request exact-alarm permissions.

---

## 5. Analytics, advertising, and tracking

Sifdroid contains **no analytics SDKs, no advertising, and no third-party tracking**. We do not profile you, and we do not sell or share personal data.

---

## 6. Data export, import, and deletion

- **Export:** You can export your data via Settings → Data → Export. The app writes a single **`.zip` archive** — containing a CSV data file of all your data **plus copies of any goal/asset photos you added** — to a location you choose. The file is created entirely on-device and is never sent to us or any third party. Because it contains your full financial data and your photos, store and share that file carefully; anyone who can open it can read your data.
- **Import:** You can restore from a backup file you provide (a `.zip` backup, or a plain CSV). Importing **replaces** the app's current data with the file's contents.
- **Deletion:** Because all data is local, you can permanently delete it by clearing the app's storage in Android settings or uninstalling the app. Uninstalling removes the local database and all associated data. Any backup files you exported live wherever you saved them and are deleted separately by you.

---

## 7. Children's privacy

Sifdroid is not directed to children under 13 (or the minimum age required in your jurisdiction). We do not knowingly collect personal information from children. Since no data is collected by us, no such data is processed on our side.

---

## 8. Security

Your data is stored in the app's private, sandboxed storage provided by Android. You may enable the optional app lock — unlocked with your biometric or your device PIN/pattern/password — for an additional layer of protection; it re-locks whenever the app is sent to the background or your screen turns off, and while the unlock prompt is showing the app's contents are obscured (blurred) so they are not visible behind it. As with any device-stored data, keeping your device secure (screen lock, OS updates) is the best protection.

---

## 9. Changes to this policy

We may update this Privacy Policy from time to time. Material changes will be reflected by updating the "Last updated" date above and, where appropriate, within the app or its store listing.

---

## 10. Contact

Questions about this Privacy Policy? Contact **twius.09@gmail.com**.
