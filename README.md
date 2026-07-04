# WexSay — Secure Social Messaging for Android

<p align="center">
  <img src="https://raw.githubusercontent.com/Wex-DE/WexSay/main/assets/banner.png" alt="WexSay Banner" width="100%" max-width="800px">
</p>

<p align="center">
  <a href="https://github.com/Wex-DE/WexSay/releases"><img src="https://img.shields.io/github/v/release/Wex-DE/WexSay?include_prereleases&label=Public%20Beta&color=blue&style=flat-square" alt="GitHub pre-release version"></a>
  <img src="https://img.shields.io/badge/Platform-Android%208.0%2B-green?style=flat-square" alt="Platform Supported">
  <img src="https://img.shields.io/badge/License-Apache%202.0-orange?style=flat-square" alt="License Apache 2.0">
  <a href="https://github.com/Wex-DE/WexSay/issues"><img src="https://img.shields.io/github/issues/Wex-DE/WexSay?color=red&style=flat-square" alt="GitHub Issues"></a>
  <a href="https://github.com/Wex-DE/WexSay/discussions"><img src="https://img.shields.io/github/discussions/Wex-DE/WexSay?color=purple&style=flat-square" alt="GitHub Discussions"></a>
</p>

---

## Introduction

Welcome to the official public testing and release repository for **WexSay**, a modern, high-performance social messaging application for Android. Developed by the engineering team at **WexDE**, WexSay is designed to provide secure, low-latency, and media-rich communication.

This public repository serves as the central hub for the WexSay Beta program. Since our core application and backend codebase remain proprietary, this space is dedicated to distribution, public tracking of issues, feature proposals, changelogs, and community discussions.

> [!IMPORTANT]
> **This is a Public Beta release.** The application is in active development. Features are subject to change, and you may encounter bugs. Please review the [Beta Program Warning](#critical-beta-program-warning) before installation.

---

## Key Features

* **High-Performance Messaging:** Powered by a customized real-time WebSocket architecture ensuring instant delivery.
* **Low-Latency calling:** Native WebRTC calling infrastructure supporting voice and video calls with optimal network routing.
* **Smart FAQ Suggestions:** Integrated administrative assistance allowing users to query automated systems for quick answers.
* **Visual Theme Engine:** Advanced customization settings including personalized chat backgrounds and custom emojis.
* **Privacy Controls:** Fine-grained settings for managing phone number visibility, last seen status, and profile picture access.
* **Account Multi-tenancy:** Built-in multi-account manager allowing users to swap between up to three accounts seamlessly.

---

## Why WexSay?

WexSay is engineered from the ground up for responsiveness and modern Android design patterns. By utilizing Jetpack Compose for a fully declarative UI, Kotlin Coroutines for async operations, and a highly optimized local SQLite (Room) database for offline-first caching, WexSay delivers a fluid, battery-efficient, and premium user experience even on budget devices.

---

## Screenshots

<p align="center">
  <img src="https://raw.githubusercontent.com/Wex-DE/WexSay/main/assets/screenshots/screenshot_home.png" alt="Home Screen" width="30%">
  <img src="https://raw.githubusercontent.com/Wex-DE/WexSay/main/assets/screenshots/screenshot_chat.png" alt="Chat Screen" width="30%">
  <img src="https://raw.githubusercontent.com/Wex-DE/WexSay/main/assets/screenshots/screenshot_profile.png" alt="Profile Screen" width="30%">
</p>

---

## APK Download & Installation

The latest pre-release testing packages (APK) can be downloaded directly from the GitHub Releases page.

### [➡️ Download Latest WexSay Beta APK](https://github.com/Wex-DE/WexSay/releases)

### Basic Installation Steps
1. Navigate to the [Releases](https://github.com/Wex-DE/WexSay/releases) section and download the latest universal or architecture-specific APK.
2. Open the downloaded `.apk` file on your Android device.
3. If prompted, enable the **"Install from Unknown Sources"** permission for your browser or file manager.
4. Follow the on-screen installer prompts to complete setup.

---

## Critical Beta Program Warning

Please read this section carefully before joining the testing program.

* **Temporary Package Name:** The current beta app is distributed under the temporary package name `com.expde.chitchat`.
* **Play Store Migration:** The stable production release will be published on the Google Play Store under a different official package name.
* **No Auto-Updates:** Due to the package name change, **this beta app will not automatically update to the stable Play Store version.** You will need to manually install the official Play Store app when it is released.
* **Data Safety:** All your profile details, servers, and chat histories are securely stored on our backend databases. When migrating to the official Play Store app later, logging in with your credentials will automatically restore your chats.
* **Bug Reports:** As this is pre-release software, bugs, calling issues, or notification delays may occur. Report any bugs in the [Issues](https://github.com/Wex-DE/WexSay/issues) section.

For more details on migration, please read our [Migration Guide](MIGRATION_GUIDE.md).

---

## System Requirements

| Parameter | Minimum Requirement | Recommended |
| :--- | :--- | :--- |
| **OS Version** | Android 8.0 (API Level 26 - Oreo) | Android 11.0 (API Level 30) or higher |
| **RAM** | 2 GB | 4 GB or higher |
| **Architecture** | ARMv7, ARM64, x86, x86_64 | ARM64 (arm64-v8a) |
| **Network** | 3G / Stable Internet | 4G / 5G / High-speed Wi-Fi |

---

## Android Permissions Explanation

WexSay requires the following system permissions to operate. You will be prompted to grant them as they are needed:

* **Contacts (`READ_CONTACTS`):** Used to sync and discover contacts who are already using WexSay.
* **Camera (`CAMERA`):** Required for capturing photos, videos, and scanning QR codes for web login.
* **Audio (`RECORD_AUDIO`):** Required for voice messages and WebRTC audio calling.
* **Notifications (`POST_NOTIFICATIONS`):** Used on Android 13+ to deliver push notifications for incoming messages and calls.
* **Location (`ACCESS_FINE_LOCATION`):** Required for sharing your live location in chats (only active when sharing).
* **Storage (`READ_MEDIA_IMAGES`, `READ_MEDIA_VIDEO`):** Used to select and upload media files to your chats.

---

## Known Issues

Before reporting a bug, check our [Known Issues](KNOWN_ISSUES.md) page to see if it is already tracked. Current major active items include:
* Occasional audio routing delays when connecting WebRTC calls over slow mobile data (3G).
* In-app status transitions (Online/Offline) showing minor sync lag under unstable networks.

---

## Project Roadmap

We are working toward our official v1.0 release. Key milestones include:
* **Q3 2026:** Expanded calling configuration settings and stable notifications tuning.
* **Q4 2026:** Finalization of Play Store packaging and data migration validation.
* **2027:** Future plans for secure desktop and web clients.

For the full roadmap, refer to [ROADMAP.md](ROADMAP.md).

---

## Contributing & Reporting Issues

Even though the source code of the Android application is proprietary, you can help improve WexSay by contributing to the community!

* **Bug Reports:** Open an issue using our [Bug Report Template](.github/ISSUE_TEMPLATE/bug_report.md) if you encounter any app crashes or unexpected behaviors.
* **Feature Requests:** Submit proposals for new features or styling tweaks using the [Feature Request Template](.github/ISSUE_TEMPLATE/feature_request.md).
* **Discussions:** Ask questions, share ideas, and chat with other beta testers in [GitHub Discussions](https://github.com/Wex-DE/WexSay/discussions).

Please read our [Contributing Guidelines](CONTRIBUTING.md) and [Code of Conduct](CODE_OF_CONDUCT.md) before participating in the community.

---

## Security Responsible Disclosure

We take user privacy and security seriously. If you discover a security vulnerability in the WexSay client or backend api:
* **Do NOT open a public issue.**
* Please report it privately to our security team according to the guidelines in [SECURITY.md](SECURITY.md).

---

## License & Credits

The documentation, assets, issue templates, and scripts in this public repository are licensed under the **Apache License 2.0**. See the [LICENSE](LICENSE) file for details.

The WexSay application binary relies on open-source libraries. For detailed acknowledgments, refer to [CREDITS.md](CREDITS.md) and [ACKNOWLEDGEMENTS.md](ACKNOWLEDGEMENTS.md).

---

<p align="center">
  Developed with ❤️ by the <b>WexDE Team</b>.<br>
  © 2026 WexDE. All rights reserved.
</p>