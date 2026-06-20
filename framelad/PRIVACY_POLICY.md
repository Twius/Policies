---
layout: default
title: Privacy Policy — framelad
permalink: /framelad/
---

# Privacy Policy for framelad

**Effective date:** 2026-06-18
**Last updated:** 2026-06-18
**App:** framelad

This Privacy Policy explains how the framelad Android application ("framelad", "the app", "we") handles your information. framelad is a **tool for RNG (random number generation) manipulation**, built on the open-source mGBA emulation core. It runs ROM files you provide, entirely on your device, and adds features to predict and influence in-app RNG outcomes.

> **Summary:** framelad has no servers and no user accounts. It collects, stores, transmits, and shares no personal data, and never connects to the internet. The only network feature is optional *local link play* — a direct device-to-device connection on your own local network that contacts no servers.

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
| Battery save (`.sav`) files | The app's private storage (saved automatically as you play); export/import via the file picker | Persist in-game save data |
| Save states | The app's private storage | Manual and automatic save/restore points (kept across app restarts) |
| App settings | The app's private storage | Remember your preferences (theme, FPS cap, autosave interval, last ROM folder, etc.) |
| Optional names file | A file you choose via the file picker, copied to the app's private storage | Display names you supply for numeric IDs shown in the RNG features; removable in-app at any time |
| Optional RNG data file | A JSON file you choose via the file picker, copied to the app's private storage | Reference data you supply for the RNG prediction list; numeric IDs only |

All of this stays on your device. None of it is sent to us or to any third party, because the app never communicates with any server or internet service.

---

## 3. Information shared with third parties

framelad shares **no** information with any third party. It never connects to the internet and contacts no external server.

The app's only network feature is **local link play**: an optional, user-initiated mode in which two devices on the *same local network* connect **directly to each other** to synchronize a live session. When you use it:

- Devices communicate peer-to-peer over your local network only. No server, relay, or internet service is involved, and no data leaves your network.
- Sessions are advertised and discovered via Android's standard local network-service-discovery mechanism.
- The data exchanged is limited to what the feature needs: a 4-character room code, your device's name (shown to the other players in the lobby), the loaded ROM's 4-character header code (to warn about mismatches), and the emulated link traffic itself.
- Nothing from a link session is collected, logged, or transmitted anywhere else, and the connection ends when you disconnect or leave.

If you never use link play, the app makes no network connections of any kind.

---

## 4. Permissions and why they are used

framelad requests access to files **only** through the Android Storage Access Framework — the standard system picker that lets *you* choose which folder or file the app may read. The app cannot access any file you have not explicitly selected. It requests no location permission and no access to contacts, camera, microphone, or other sensitive data.

The following network-related permissions are declared **solely** for optional local link play:

| Permission | Why it is needed |
|---|---|
| `INTERNET` | Android requires this permission for *any* socket use, including purely local ones |
| `ACCESS_WIFI_STATE` | Discovering and maintaining device-to-device sessions on your local network |
| `CHANGE_WIFI_MULTICAST_STATE` | Local network-service discovery for link play |
| `ACCESS_NETWORK_STATE` | Detecting local network availability for link play |

---

## 5. Analytics, advertising, and tracking

framelad contains **no analytics SDKs, no advertising, and no third-party tracking**, and bundles no third-party data-collecting SDKs. The app is built on the open-source [mGBA](https://mgba.io/) emulation core, which likewise runs entirely on-device and performs no data collection. We do not profile you, and we do not sell or share personal data.

---

## 6. Data export, import, and deletion

- **Export / import:** Battery save files can be exported and imported via the Android file picker to locations you choose. Files are created entirely on-device and are never sent to us or any third party.
- **Deletion:** Because all data stays on your device, you remain in full control. You can delete any ROM, save file, save state, or imported names file through your device's file manager or in-app, and clearing the app's data or uninstalling it removes all app-managed files.

---

## 7. Children's privacy

framelad is not directed to children under 13 (or the minimum age required in your jurisdiction). framelad collects no data from anyone, including children. Because no personal information is ever gathered, there is nothing that could be collected from a child under any applicable age threshold.

---

## 8. Security

Your data is stored in the app's private, sandboxed storage provided by Android. As with any device-stored data, keeping your device secure (screen lock, OS updates) is the best protection.

---

## 9. Changes to this policy

We may update this Privacy Policy from time to time. Material changes will be reflected by updating the "Last updated" date above and, where appropriate, within the app or its store listing. Because the app collects no data, any future change would only ever further clarify these terms.

---

## 10. Contact

Questions about this Privacy Policy? Contact **twius.09@gmail.com**.
