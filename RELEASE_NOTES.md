# Release Notes — WexSay Public Beta

Welcome to the public release page for WexSay. Below you will find the release notes for our latest beta builds.

---

## WexSay v1.0.0-beta.2 (Pre-Release)
**Date:** July 1, 2026  
**Build Target:** Android 8.0+ (API 26+)  
**Temporary Package Name:** `com.expde.chitchat`  
**Security Status:** Audited and Hardened  

### Release Overview
This pre-release focuses heavily on core security improvements, startup optimization, and resolving real-time database sync bugs in multi-device messaging environments.

### 🛡️ Critical Security & Privacy Hardening
* **Encrypted Shared Preferences:** Device access tokens and local configurations are now encrypted utilizing 256-bit AES cryptographic wrappers. Standard XML SharedPreferences are automatically migrated and wiped on first boot.
* **HTTPS Enforcement:** Blocked cleartext (non-encrypted HTTP) connections across all client activities, reducing exposure to Man-in-the-Middle (MitM) attacks.
* **User Email Privacy:** Refactored search and directory endpoints to prevent exposure of other users' email addresses.

### ⚡ Performance & Synchronization Fixes
* **Deleted Message Sync:** Patched SQLite room synchronization. Recipient screens now instantly clear text and display `"This message was deleted"` when a sender triggers "Delete for Everyone".
* **Start-Up Sync Refactoring:** Removed heavy user database scans from Node.js startup threads to keep API response times optimal.
* **Admin Login Visibility:** Redesigned text fields and settings pages inside the administration panel to support comfortable contrast ratios in both Day and Night modes.

### 📦 APK Assets (Universal & Split)
Download the appropriate package for your device architecture:
* `wexsay-universal-release.apk` (Supports all architectures; recommended)
* `wexsay-arm64-v8a-release.apk` (Optimized for modern 64-bit devices)
* `wexsay-armeabi-v7a-release.apk` (Optimized for older 32-bit devices)

---

## WexSay v1.0.0-beta.1 (Pre-Release)
**Date:** June 15, 2026  
**Build Target:** Android 8.0+  

### Release Overview
Initial public release containing core UI elements, real-time messaging engine, and calling infrastructure.
* Dynamic WebSocket chat connection.
* WebRTC voice and video calls.
* Visual customizer for chat screens.
