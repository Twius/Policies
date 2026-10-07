---
layout: default
title: Privacy Policy for framelad
permalink: /framelad/
nav_order: 4
---

# Privacy Policy for framelad

**First published:** 2026-06-18<br>
**Last updated:** 2026-10-07

framelad is a tool for RNG (random number generation) manipulation, built on the open-source mGBA emulation core. It runs ROM files you provide, entirely on your device, and adds features to predict and influence in-app RNG outcomes. This Privacy Policy explains how it handles your information. "We" and "us" mean Twius, the developer of framelad.

{: .summary }
**In short:** framelad works without servers or user accounts. The app never sends us any of your data, and it makes no internet connections of its own, except to an address you type in for link play. The only network feature is optional link play, which shares your device's name and a few session details directly with the other devices in the session.

## 1. Who we are {#who-we-are}

framelad is developed by Twius (Anastasis Anastasi, an individual developer in Cyprus). You can reach us at [twius.09@gmail.com](mailto:twius.09@gmail.com).

There is no backend server, database, or cloud service behind framelad. The app never sends us anything it stores, so we cannot see or access your app data. [Section 2](#what-we-receive) lists what we do receive.

## 2. What we receive {#what-we-receive}

We receive personal information in only these ways:

- **Emails you send us:** your email address and whatever you write or attach. We use them only to reply to you, and delete them once the matter is settled. Our email is provided by Google (Gmail), which may store it outside the EU, including in the United States. Google LLC is certified under the EU-US Data Privacy Framework.
- **Google Play sales records:** when you buy framelad, Google gives us its usual seller's record of the sale, such as the order number, date, price, device model, and your country, and in some countries your city and postcode. We can look up an order by the email address you paid with. It never includes your card details. We use it for support, refunds, and tax records, and keep it as long as tax law requires.
- **Crash reports:** if you have chosen to share usage and diagnostics data with Google, Google Play shows us reports of the app's crashes and freezes. They contain technical details such as the device model, the Android version, and where in the app the error happened, which can include an error message from the app. Google does not tell us who you are.

Under EU and UK data protection law, our legal basis is our legitimate interest in answering you and supporting the app, and our legal duty to keep tax records.

## 3. Data stored on your device {#data-on-device}

Everything framelad stores is kept on your device. Most of it is kept in the app's private storage, and files you export go to places you choose with the Android file picker. That covers:

| Data | Where it lives | Purpose |
|---|---|---|
| ROM files | A folder you choose via the Android system file picker (Storage Access Framework); a working copy is kept in the app's private storage | Loaded into the emulator to run |
| Battery save (`.sav`) files | The app's private storage, written automatically as you play; export and import through the file picker | Persist in-game save data |
| Save file backups | The app's private storage; you can also export them through the file picker | Timestamped copies taken automatically before a save file sharing operation, so it can be undone. The 10 most recent pairs are kept |
| Save states | The app's private storage, each with a small picture of the emulated screen as it looked when you saved | Manual and automatic save and restore points, kept across app restarts |
| ROM photos | An image you pick with the system file picker, scaled down and copied into the app's private storage | An optional picture shown next to a ROM in your library |
| App settings | The app's private storage, and optionally a settings file you write or read through the file picker | Remember your preferences (theme, speed cap, autosave interval, control layout, last ROM folder, and so on) |
| Optional reference files you import | Files you choose with the file picker, copied into the app's private storage | Display names, labels, spawn data, and ROM profiles that you supply for the RNG features. All of it is text or numeric IDs you provide; the app bundles none of it |
| Import records | The app's private storage | The name of each file you imported, and which file each ROM working copy came from |
| Temporary working files | The app's private cache | Short-lived copies used while opening a ROM, importing a file, exporting a save, or comparing two save files, replaced or removed as you keep using those features |

**About ROM photos:** If you choose a picture for a ROM, the app opens the standard Android file picker so you can select one. framelad receives only the single image you pick, makes a small copy of it in its own private storage, and never reads anything else from your photos. That copy is used only to draw the row in your library, it never leaves your device, and you can remove it in the app at any time.

None of it is sent to us, and nothing is sent to anyone else except as described in [section 4](#what-leaves). The app does not back up or sync anything to a server. Android's cloud backup is switched off for the app, so none of it is copied to your Google account. If you move to a new phone with a direct device-to-device transfer, Android may copy the app's data across.

## 4. What leaves your device {#what-leaves}

framelad sends nothing to us or to any company, and it contacts no server, ours or anyone else's. It shares information only during link play, as described below.

The app's only network feature is link play: an optional mode, started only by you, in which up to four devices running framelad connect directly to each other to synchronise a live session. When you use it:

- Devices connect directly, with no server or relay in between. One device acts as the host and passes session traffic between the others. Normally this happens on your local network. If you type in an address with **Enter IP manually**, the app connects to that address wherever it is.
- While you host, the room is announced through Android's local network-service discovery, so every device on your network can see it, and anyone there running framelad can join the lobby until it is full. Link traffic is not encrypted, so use link play only on a network you trust, such as your home Wi-Fi.
- The data exchanged is limited to what the feature needs. The room's 4-character code and the host's local network address are announced on the network. If you join a room, the app sends your device's name as set in Android (or its model name, if no name is set) and the loaded game's 4-character header code. Everyone in the lobby sees the names of the devices that joined. The host's own name is never sent, and the host appears only as "Host". The emulated link traffic passes between the devices.
- Nothing from a link session is saved or sent anywhere else, and the connection ends when you disconnect or leave. The app writes only short technical notes, such as player numbers and connection errors, to Android's on-device system log; these never include your device name.

The app's About section contains outward links: to this policy, to the Terms of Use, to the framelad guide, and to the app's Play Store listing. Tapping one hands the address to your browser or store app; framelad opens no connection itself and includes nothing about you. Aside from a link you tap, the app makes no network connections at all unless you use link play. If you have chosen to share usage and diagnostics data with Google, Android also sends Google a report when the app crashes or freezes. That report can sometimes include part of what the app was working on at the time (see [section 2](#what-we-receive)).

## 5. Permissions {#permissions}

framelad requests access to files only through the Android Storage Access Framework, the standard system picker that lets you choose which folder or file the app may read. When you pick your ROM folder you grant read-only access to that folder, so the app can list what is in it and read the ROM files and archives it finds there to show your library. It cannot reach anything outside the folders and files you have granted.

framelad declares five permissions, all for optional link play, and the AndroidX libraries it is built with add one more:

| Permission | Why it is needed |
|---|---|
| `INTERNET` | Android requires this permission for any socket use, including purely local ones |
| `ACCESS_WIFI_STATE` | Declared for link play; the app does not currently use it to read anything |
| `CHANGE_WIFI_MULTICAST_STATE` | For local network-service discovery during link play |
| `ACCESS_NETWORK_STATE` | Declared for link play; the app does not currently use it to read anything |
| `WAKE_LOCK` | To keep Wi-Fi responsive during a link session |
| `com.framelad.DYNAMIC_RECEIVER_NOT_EXPORTED_PERMISSION` | Added by the AndroidX core library. It is private to framelad and only stops other apps from sending it internal messages |

framelad requests no location, contacts, camera, or microphone permission.

## 6. Analytics, advertising, and tracking {#analytics}

framelad does not include analytics, advertising, third-party tracking, or crash reporting of its own. We do not profile you, and we do not sell your personal data or use it for advertising.

framelad also bundles no third-party SDKs that collect data. It is built on the open-source [mGBA](https://mgba.io/) emulation core, which also runs entirely on your device and collects no data.

## 7. Managing and deleting your data {#deletion}

**Export and import:** Battery saves, save file backups, and your app settings can be written to a location you choose with the Android file picker, and battery saves and settings can be read back the same way. Save states cannot be exported. The app never sends these files to us or to anyone else. If you save one to a cloud service such as Google Drive, that service stores it.

**Save file sharing:** framelad can open a second save file that you pick and move entities between it and your running game. The app sends neither file anywhere. Each is written through a temporary copy and checked before anything real is replaced, and a timestamped backup of both is taken first and kept in the app's private storage, so you can restore either one from inside the app. Keep your own export as well. The [Terms of Use]({{ '/framelad/terms/' | relative_url }}) explain why.

**Deletion:** ROM photos can be removed inside the app at any time. Imported reference files (names, labels, spawn data, and ROM profiles) can be removed inside the app while their game is running. ROM working copies, battery saves, save states, and backups live in framelad's private storage.

Clearing the app's data in Android settings, or uninstalling framelad, removes everything it keeps on your device. Your original ROM files, and any save or settings file you exported yourself, stay wherever you keep them and are untouched by uninstalling. Delete those with your device's file manager.

## 8. Your rights {#your-rights}

Data protection law gives you rights over the personal data an organisation holds about you, such as access, correction, erasure, and portability. We hold none of the data the app stores. framelad does not use a server or accounts, so we have no copy to hand over, correct, or delete. Everything those rights would cover sits on your device, under your control: the export functions described above give you portability, and clearing the app's data or uninstalling the app gives you erasure.

For what we do receive (see [section 2](#what-we-receive)), you can ask us for a copy of it, ask us to correct or delete it, ask us to limit how we use it, or object to our using it, by writing to [twius.09@gmail.com](mailto:twius.09@gmail.com). Sales records we must keep for tax purposes are deleted when that period ends. You can also complain to the data protection authority where you live or work, or to ours, the [Cyprus Commissioner for Personal Data Protection](https://www.dataprotection.gov.cy).

If you bought framelad from Google Play, Google processes that purchase as a separate controller, under [Google's privacy policy](https://policies.google.com/privacy). Rights over that data are exercised with Google. framelad never sees your payment details.

## 9. Children's privacy {#children}

framelad is not directed to children under 13, or under the minimum age that applies where you live. We do not knowingly collect personal information from children. If you think a child has sent us personal information, for example by email, tell us and we will delete it.

## 10. Security {#security}

Your data lives in the app's private storage, which Android keeps sandboxed from other apps.

Keeping the device itself secure, with a screen lock and current OS updates, remains the best protection for anything stored on it.

## 11. Changes to this policy {#changes}

We may update this policy from time to time. The version published at this address is always the current one, and the "Last updated" date at the top tells you when it last changed. If a change is material, we will point it out in the app's release notes and on its store listing before it applies to you.

## 12. Related documents {#related}

This policy covers what happens to your information. Your use of framelad is also covered by the [Terms of Use]({{ '/framelad/terms/' | relative_url }}).

## 13. Contact {#contact}

Questions about this policy: [twius.09@gmail.com](mailto:twius.09@gmail.com).
