# WexSay Public Beta Program

Welcome to the WexSay Public Beta Program! By participating in this program, you are helping the WexDE development team test, optimize, and secure our social messaging client before its general release on the Google Play Store.

This document details the goals, policies, and procedures of our testing phase.

---

## 🎯 Program Goals

1. **Device Compatibility:** Verifying that our Jetpack Compose UI layout and local storage functions render smoothly on all Android versions from Oreo (8.0) to Android 14+.
2. **WebRTC Calls Testing:** Auditing audio and video call quality under varied network speeds (3G, 4G, 5G, Wi-Fi) and resolving any codec/routing issues.
3. **Synchronization Verification:** Testing SQLite/Room local database synchronization routines when syncing edited or deleted message frames.
4. **Push Notifications Tuning:** Ensuring Firebase Cloud Messaging (FCM) alerts arrive instantly and do not drain background battery.

---

## ⚠️ Important Rules & Expectations

* **Pre-Release Software:** The beta application is in active development. You may experience occasional crashes, notification delays, or calling drops. We advise against using this for mission-critical operations.
* **No Auto-Updates:** The beta app uses the temporary package name `com.expde.chitchat`. **It will not automatically update to the stable Play Store version.** You will need to manually install the official version later.
* **Feedback is Crucial:** We ask that you report any bugs, calling failures, or visual bugs in the [Issues](https://github.com/Wex-DE/WexSay/issues) section of this repository.

---

## 🔄 Transitioning to Stable

When the stable version of WexSay is published on the Google Play Store:
1. We will post an official announcement here.
2. You will download the official app from the Google Play Store.
3. All your contacts, chat history, and accounts will be restored automatically when you log in, as all data is securely persisted on our backend database.
4. You can then safely uninstall the temporary beta app (`com.expde.chitchat`).
