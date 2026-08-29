---
layout: default
title: Privacy Policy for framelad
permalink: /framelad/
---

# Privacy Policy for framelad

**Effective date:** 2026-06-18
**Last updated:** 2026-08-29
**App:** framelad

This Privacy Policy explains how the framelad Android application ("framelad", "the app", "we") handles your information. framelad is a **tool for RNG (random number generation) manipulation**, built on the open-source mGBA emulation core. It runs ROM files you provide, entirely on your device, and adds features to predict and influence in-app RNG outcomes.

> **Summary:** framelad has no servers and no user accounts. It collects, stores, transmits, and shares no personal data, and makes no internet connections of its own. The only network feature is optional *local link play*, device-to-device connections on your own local network that contact no servers.

---

## 1. Who we are

framelad is developed by **Twius**.
Contact: **twius.09@gmail.com**.

We do not operate any backend server, database, or cloud service for framelad. We never receive, store, or have access to your data.

---

## 2. Data stored on your device

framelad reads and writes files only on your own device, only with your explicit action, and never transmits them anywhere:

| Data | Where it lives | Purpose |
|------|----------------|---------|
| ROM files | A folder you choose via the Android system file picker (Storage Access Framework); a working copy is kept in the app's private storage | Loaded into the emulator to run |
| Battery save (`.sav`) files | The app's private storage, written automatically as you play; export and import through the file picker | Persist in-game save data |
| Save file backups | The app's private storage | Timestamped copies taken automatically before a save file sharing operation, so it can be undone |
| Save states | The app's private storage, each with a small picture of the emulated screen as it looked when you saved | Manual and automatic save and restore points, kept across app restarts |
| ROM photos | An image you pick with the system file picker, scaled down and copied into the app's private storage | An optional picture shown next to a ROM in your library |
| App settings | The app's private storage, and optionally a settings file you write or read through the file picker | Remember your preferences (theme, speed cap, autosave interval, control layout, last ROM folder, and so on) |
| Optional reference files you import | Files you choose with the file picker, copied into the app's private storage | Display names, labels, spawn data, and ROM profiles that you supply for the RNG features. All of it is text or numeric IDs you provide; the app bundles none of it |
| Temporary working files | The app's private cache | Short-lived copies used while importing a file or comparing two save files, replaced or removed as you keep using those features |

**About ROM photos.** If you choose a picture for a ROM, the app opens the standard Android file picker so you can select one. framelad receives only the single image you pick, makes a small copy of it in its own private storage, and never reads anything else from your photos. That copy is used only to draw the row in your library, it never leaves your device, and you can remove it in the app at any time.

All of this stays on your device. None of it is sent to us or to any third party, because the app never communicates with any server or internet service. framelad also opts out of Android's automatic cloud backup, so none of these files are copied to your Google account either.

---

## 3. Information shared with third parties

framelad shares **no** information with any third party. It contacts no external server.

The app's only network feature is **local link play**: an optional, user-initiated mode in which up to four devices on the *same local network* connect **to each other** to synchronize a live session. When you use it:

- Devices communicate over your local network only. One device acts as the host and passes session traffic between the others; with more than two participants this means the host relays, but every device involved is one you connected yourself. No internet service is involved, no third party sits in the path, and no data leaves your network.
- Sessions are advertised and discovered via Android's standard local network-service-discovery mechanism.
- The data exchanged is limited to what the feature needs: a 4-character room code, your device's name (shown to the other players in the lobby), the loaded ROM's 4-character header code (to warn about mismatches), and the emulated link traffic itself.
- Nothing from a link session is collected, logged, or transmitted anywhere else, and the connection ends when you disconnect or leave.

One further note, for completeness. The app's About section has a link to this policy. Tapping it hands the web address to whichever browser you have installed, and that browser loads the page as it would any other. framelad itself opens no connection and includes nothing about you. Apart from that one link, if you never use link play the app makes no network connections of any kind.

---

## 4. Permissions and why they are used

framelad requests access to files **only** through the Android Storage Access Framework, the standard system picker that lets *you* choose which folder or file the app may read. When you pick your ROM folder you grant access to that folder, so the app can list what is in it and read the ROM files and archives it finds there in order to show your library. It cannot reach anything outside the folders and files you have granted, and it requests no location permission and no access to contacts, camera, or microphone.

The following network-related permissions are declared **solely** for optional local link play:

| Permission | Why it is needed |
|---|---|
| `INTERNET` | Android requires this permission for *any* socket use, including purely local ones |
| `ACCESS_WIFI_STATE` | Discovering and maintaining device-to-device sessions on your local network |
| `CHANGE_WIFI_MULTICAST_STATE` | Local network-service discovery for link play |
| `ACCESS_NETWORK_STATE` | Detecting local network availability for link play |
| `WAKE_LOCK` | Keeping Wi-Fi responsive during a link session |

These five are the only permissions framelad declares.

---

## 5. Analytics, advertising, and tracking

framelad contains **no analytics SDKs, no advertising, and no third-party tracking**, and bundles no third-party data-collecting SDKs. The app is built on the open-source [mGBA](https://mgba.io/) emulation core, which likewise runs entirely on-device and performs no data collection. We do not profile you, and we do not sell or share personal data.

---

## 6. Data export, import, and deletion

**Export and import.** Battery save files and your app settings can each be written to, or read from, a location you choose with the Android file picker. Those files are created entirely on your device and are never sent to us or to any third party.

**Save file sharing.** framelad can open a second save file that you pick and move entities between it and your running game. Both files stay on your device throughout. Each is written through a temporary copy and checked before anything real is replaced, and a timestamped backup of both is taken first and kept in the app's private storage, so you can restore either one from inside the app.

**Deletion.** Because everything stays on your device, you remain in full control.

- Imported reference files (names, labels, spawn data, ROM profiles) and ROM photos can be removed inside the app at any time.
- ROM working copies, battery saves, save states and backups live in framelad's private storage. Clearing the app's data or uninstalling framelad removes all of them, along with every other file the app manages.
- Your original ROM files, and any save you exported yourself, stay wherever you keep them and are untouched by uninstalling. Delete those with your device's file manager.

---

## 7. Children's privacy

framelad is not directed to children under 13 (or the minimum age required in your jurisdiction). framelad collects no data from anyone, including children. Because no personal information is ever gathered, there is nothing that could be collected from a child under any applicable age threshold.

---

## 8. Security

Your data is stored in the app's private, sandboxed storage provided by Android. As with any device-stored data, keeping your device secure (screen lock, OS updates) is the best protection.

---

## 9. Changes to this policy

We may update this Privacy Policy from time to time. This page is the canonical version; the app links to it directly rather than shipping a copy of its own, so there is only ever one text to keep current. Material changes will be reflected by updating the "Last updated" date above and, where appropriate, within the app or its store listing. Because the app collects no data, any future change would only ever further clarify these terms.

---

## 10. Contact

Questions about this Privacy Policy? Contact **twius.09@gmail.com**.
