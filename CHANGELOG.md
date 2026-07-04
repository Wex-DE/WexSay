# Changelog

All notable changes to the public releases of WexSay will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [1.0.0-beta.2] - 2026-07-01

### Added
* Support for Google Cloud/Firebase service account rotation.
* Multi-account swapping capability supporting up to 3 active account profiles in parallel.
* Visual themes tab in admin configurations to support dynamic chat background customizations.
* Robust local SQLite (Room) database synchronization handling recipient view message deletes.

### Changed
* Refactored network layer to block cleartext HTTP communication, enforcing HTTPS channels exclusively.
* Upgraded local device credential storage to AES-256 EncryptedSharedPreferences.
* Optimized database initial sync procedures to prevent Event Loop blockages on startup.

### Fixed
* Fixed a critical sync issue where recipient devices failed to update deleted message statuses in chat views.
* Fixed text visibility contrast issues in Day mode on admin panel input bars and tables.
* Fixed empty vertical layout gaps in Themes setup view.

---

## [1.0.0-beta.1] - 2026-06-15

### Added
* First public beta package release of WexSay (`com.expde.chitchat`).
* Core WebRTC audio/video call integration with in-app native dialer support.
* Modern Jetpack Compose UI layout featuring slide-out menus and custom emoji panels.
* In-app automated support assistant matching FAQ suggested replies.
* Real-time push notification receiver powered by Firebase Cloud Messaging (FCM).
