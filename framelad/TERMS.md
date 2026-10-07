---
layout: default
title: Terms of Use for framelad
permalink: /framelad/terms/
nav_order: 5
---

# Terms of Use for framelad

**First published:** 2026-09-15<br>
**Last updated:** 2026-10-07

These Terms of Use ("Terms") cover your use of the framelad Android app ("framelad", "the app"). "We" and "us" mean Twius, the developer of framelad. framelad is a tool for RNG (random number generation) manipulation, built on the open-source mGBA emulation core. It runs ROM files that you provide, entirely on your device.

By installing or using framelad, you agree to these Terms. If you do not agree, do not use the app.

{: .summary }
**In short:** framelad supplies no ROMs or game content. You bring your own ROM files and you are responsible for having the right to use them. Some features write to your save data, so back it up. Predictions are best effort, not guaranteed. The app is provided as is, though your rights under consumer law still apply.

## 1. Who these Terms are with {#who}

framelad is developed and published by Twius (Anastasis Anastasi, an individual developer in Cyprus). You can reach us at [twius.09@gmail.com](mailto:twius.09@gmail.com).

The terms of the store you got the app from also apply, which is normally Google Play. Where those store terms and these Terms disagree about something the store handles, such as payment, refunds, or distribution, the store terms win, but they never reduce the refunds these Terms promise or your rights under consumer law.

You need to be at least 13 to use framelad, or older if a higher minimum age applies where you live. If you are under 18, or under the age of adulthood where you live, a parent or guardian needs to agree to these Terms for you.

Nothing in these Terms takes away rights you have under the consumer protection law of the country where you live.

## 2. Your licence to use the app {#licence}

framelad is **licensed to you, not sold**. You get a non-exclusive, non-transferable licence to install and use it, for personal or work use, on devices you own or control. It lasts until it ends as described in [section 14](#ending).

You may not:

- redistribute, resell, sublicense, rent, or lend the app;
- reverse engineer, decompile, or disassemble the app, or otherwise try to get at its source code, unless the law says you may or the licence of an open-source component inside the app allows it (see [section 9](#open-source));
- remove or hide any copyright, licence, or attribution notice.

framelad and its source code are proprietary, except for the open-source components described in [section 9](#open-source). Copyright (c) 2026 Twius. All rights reserved.

## 3. Game files you supply {#game-files}

**framelad does not include ROM files or game content, such as graphics, sound, text, or names.** To work with the games it supports, it includes only numeric technical details, such as memory addresses and ID numbers. Unless you import names yourself, it shows numeric identifiers rather than names. Everything else the app operates on is supplied by you.

You are solely responsible for:

- obtaining any ROM file or save file you load into the app;
- ensuring you have the legal right to possess and use those files in your jurisdiction;
- any data or image you supply, including names, labels, tables, profiles, and ROM photos.

Only use framelad with ROM and save files you have the legal right to use. Laws on this differ by country and we do not advise you on them. We do not provide, host, link to, or endorse any source for obtaining game files.

## 4. Features that modify your save data {#save-data}

**Some framelad features write to the save data of the ROM you have loaded, not only read from it.** Save files are modified in place while the app is running. Save file sharing also writes to the second save file you pick, wherever you keep it. The app backs up both files first, but keep your own copy too.

Because of this:

- **Back up your save files before using any feature that modifies them.** The app provides an export function for this purpose.
- Modifying save data can produce results the original software did not anticipate, including data the game cannot read correctly.
- Loading a save state replaces the emulated system's state and may discard progress made since that state was created.

**You use these features at your own risk.** If a game cannot read a save the app changed as you asked, or you lose a save you did not back up, we may not be able to help you recover it. [Section 13](#liability) explains what we are responsible for.

## 5. Predictions and analysis {#predictions}

framelad's analysis features estimate future RNG outcomes by modelling how the software you load generates them. **These estimates are best effort and are not guaranteed to be correct.**

Accuracy depends on factors including the exact software you load, its revision, data you have supplied, and conditions inside the running software that the app does not model. Some outcomes are not predictable in principle, and the app indicates this where it can. Nothing in the app is a promise of a particular result.

## 6. Link play {#link-play}

framelad can connect directly to other devices running framelad, normally on your own local network. If you type in an address, it connects to that address wherever it is. Session traffic passes only between the participating devices, one of which acts as host. No server of ours is involved at any point, and we do not see, store, or have access to anything exchanged.

Link traffic is not encrypted, and anyone on the same network can see an open room and join its lobby. You are responsible for the networks you join and the devices you connect to. Data reaching your device during a link session comes from another participant, not from us, and we make no representation about it.

## 7. Your data {#your-data}

Everything framelad keeps, including your saves, save states, and imported data, stays on your device, in the app's private storage. We do not run a server or keep a copy. The [Privacy Policy]({{ '/framelad/' | relative_url }}) explains this in full.

That has a consequence: **if you lose your device, it is damaged beyond repair, you reset it, clear the app's data, or uninstall the app, your framelad data is gone for good.** We cannot recover it, because we never had it. If you move to a new phone with Android's direct device-to-device transfer, the app's data may be copied across.

Your original ROM files, and any save or settings file you exported yourself, stay wherever you keep them. Exporting your saves is the way to keep a copy that does not depend on the app. Save states cannot be exported.

Keeping your device secure is up to you.

## 8. Purchases {#purchases}

framelad is a paid app. You pay once, through Google Play.

- Google Play handles the payment, not us. We never see your card details.
- Within 48 hours of buying, you can ask Google Play for a refund. After that, contact us. We will refund you where the law requires, for example if framelad does not work as described.
- The purchase belongs to your Google account rather than to the installed app. You can reinstall framelad from Google Play at no extra cost.

## 9. Open-source components {#open-source}

framelad includes open-source software written by other people: most significantly the mGBA emulation core, which is licensed under the Mozilla Public License 2.0, along with Google's AndroidX and Jetpack Compose libraries and Kotlin and its coroutines library from JetBrains, under the Apache License 2.0. Each component keeps its own licence, and nothing in these Terms takes away a right those licences give you. The source code of the mGBA files, at the exact version framelad uses, is available from the [mGBA project](https://github.com/mgba-emu/mgba/tree/92621ea01d7a809b0cd3b1a687f30f0ea8db7c7a).

The list of components and their licence texts are in the app under **☰ > System > About > Open source licences**, which you can open while a game is running.

## 10. No affiliation {#no-affiliation}

framelad is an independent app. It is not affiliated with, associated with, endorsed by, or sponsored by Google, or by the mGBA project, any hardware manufacturer, any game publisher, or the developer of any software you may choose to run with it. All trademarks and names belong to their owners.

## 11. Changes to the app {#changes-to-app}

We may update framelad and change its features. We change or remove a feature only for a valid reason, such as a change to Android or Google Play, a security problem, or keeping the app working. If a change removes something you paid for, or makes it much worse, we will tell you before it happens, in the app's release notes and on its store listing, and you can ask for a refund within 30 days of that notice or of the change, whichever is later.

We may also stop offering framelad. If we discontinue it, we stop updating and offering it, but the copy you have keeps working. We do not promise to keep it working with any particular file, device, or Android version. If you paid for framelad, we will provide the updates the law requires for as long as you can reasonably expect them.

Your data is on your device rather than with us, so discontinuing the app does not delete it.

## 12. No warranty {#no-warranty}

**framelad is provided "as is" and "as available", with no warranty of any kind, express or implied, including any implied warranty of merchantability, fitness for a particular purpose, non-infringement, accuracy, security, or uninterrupted and error-free operation.**

We do not promise that predictions will be correct, that features which modify save data will produce a result the game can read, that the app will run any particular ROM file, or that its analysis and save-editing features will support it.

If you paid for framelad, you have legal rights if it is faulty or not as described, and these Terms do not affect them. None of this removes rights you have under consumer protection law where you live. Where that law applies, these disclaimers apply only as far as it allows.

## 13. Limits on our liability {#liability}

Nothing in these Terms limits our liability for death or personal injury caused by our negligence, for fraud, or for anything else the law does not let us limit.

Apart from that, we are only responsible for loss that is a foreseeable result of our breaking these Terms or failing to use reasonable care and skill. As far as the law allows, we are not responsible for a lost save that a backup would have protected, or for lost progress or lost time, whether they arise from using framelad, from relying on something the app showed you, or from not being able to use it at all. Our total liability to you is limited to the greater of what you paid for framelad and €50. This limit does not affect your rights if framelad is faulty or not as described.

## 14. Ending your licence {#ending}

You can end your licence at any time by uninstalling the app. We can end it only if you seriously or repeatedly break these Terms, for example by redistributing the app or sharing copies of it. Export any saves you want to keep before you uninstall. Sections [3](#game-files), [4](#save-data), [5](#predictions), [6](#link-play), [9](#open-source), [12](#no-warranty), [13](#liability), [16](#governing-law), and [17](#privacy) still apply after the licence ends.

## 15. Changes to these Terms {#changes}

We only change these Terms for a good reason, such as a change in the law, in Google Play's rules, or in how the app works. The version published at this address is always the current one, and the "Last updated" date at the top tells you when it last changed. If a change matters, we will tell you at least 30 days before it takes effect, in the app's release notes and on its store listing. If you do not agree, stop using the app. If the change takes away something you paid for, you can ask for a refund.

## 16. Governing law {#governing-law}

These Terms are governed by the law of Cyprus. If you are a consumer, you keep the protection of the mandatory laws of the country where you live, and you can bring a claim in the courts of Cyprus or in any court your local law lets you use. If you use framelad for work, the courts of Cyprus decide any dispute. If a court finds part of these Terms unenforceable, the rest still applies. If someone else takes over framelad, we may transfer these Terms to them. Your rights stay the same.

## 17. Privacy {#privacy}

What the app does with information on your device is covered separately in the [Privacy Policy for framelad]({{ '/framelad/' | relative_url }}).

## 18. Contact {#contact}

Questions about these Terms: [twius.09@gmail.com](mailto:twius.09@gmail.com).
