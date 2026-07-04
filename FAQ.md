# Frequently Asked Questions (FAQ)

Here are answers to the most common questions regarding the WexSay Public Beta program.

---

## 📦 Download & Installation

### Q: Where can I download the latest WexSay app?
**A:** You can always download the latest beta release directly from the [GitHub Releases](https://github.com/Wex-DE/WexSay/releases) page of this repository.

### Q: Why does my phone say "Unsafe App Blocked" or "Unknown Sources" when installing the APK?
**A:** Because WexSay is distributed as an independent APK package rather than through the Google Play Store, Android's Play Protect flags it as an "unknown source". This is normal. Tap **"Install anyway"** to proceed.

---

## 🛡️ Security & Privacy

### Q: Is my data safe during the Public Beta?
**A:** Yes. Your chats, media attachments, and settings are stored on our secure PostgreSQL backend servers. All transmissions are encrypted using TLS 1.3 (HTTPS/WSS) protocols.

### Q: Are my credentials encrypted on my phone?
**A:** Yes. Beginning with v1.0.0-beta.2, all local configurations, session keys, and profiles are encrypted using AES-256 GCM encryption keys managed by the hardware Android Keystore.

---

## 🚀 Beta Program & Play Store Release

### Q: Will the beta app automatically update when the Play Store version is released?
**A:** **No.** The beta app uses a temporary package name (`com.expde.chitchat`). The Play Store release will use our official package name (`com.wexde.wexsay`). Because of this, you must manually install the Play Store app when it is launched.

### Q: Will I lose my chat history when migrating to the Play Store version?
**A:** **No.** Since your chat history, contacts, and account details are stored on our servers, logging into the Play Store app with your registered email/phone number will immediately restore all your chats and settings.

### Q: How do I report bugs?
**A:** If you find a bug, please go to the [Issues](https://github.com/Wex-DE/WexSay/issues) tab on this repository and open an issue using the Bug Report template.

---

## 👥 Accounts & Profile Settings

### Q: Can I run multiple accounts in WexSay?
**A:** Yes. WexSay features an account multi-tenancy manager. You can configure and swap between up to three different accounts in the profile settings panel.
