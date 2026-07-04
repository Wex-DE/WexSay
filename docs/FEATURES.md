# WexSay Features Walkthrough

This document highlights the key features of the WexSay Android messaging client.

---

## 💬 Real-time Messaging
* **WebSocket Engine:** Persistent Socket.IO connections ensure instant delivery of messages with typing and read indicators.
* **Deleted Messages (Delete for Everyone):** Patched local database synchronizations clear message content from recipient devices instantly.
* **Forwarded Flag:** Messages forwarded from other conversations display a "Forwarded" tag to indicate shared content.
* **Reactions:** React to messages using standard and custom WebP animated emojis.

---

## 📞 Low-Latency calling
* **Voice & Video Calling:** Powered by native Android WebRTC libraries, supporting crystal clear calls.
* **Mute/Silence Controls:** Allows users to easily silence incoming rings by tapping volume controls, similar to modern messenger applications.
* **P2P Connection:** Media frames are routed directly peer-to-peer (P2P), ensuring minimum latency and optimal bandwidth usage.

---

## 🎨 Themes & Customizations
* **Wallpaper Customizer:** Choose from cosmic dark, neon lines, or obsidian backgrounds for individual chat rooms.
* **Animated Emojis:** Interactive WebP animations loaded via the AXEmojiView component for visually engaging reactions.
* **Dark Mode Support:** Clean contrast adjustments across all screens, preventing visual strain.

---

## 👥 Multi-Account Support
* **Up to 3 Accounts:** Add and configure three independent accounts (different phone numbers/emails) in the profile panel.
* **Instant Swapping:** Switch profiles with a single tap. The application clears cache data and re-establishes WebSocket sessions seamlessly.

---

## 🛡️ Privacy Controls
* **Phone Number Privacy:** Choose who can view your phone number (Everyone, Contacts, or Nobody).
* **Avatar Privacy:** Hide your profile picture from non-contacts or specify visual scopes.
* **Global Search Controls:** Toggle whether you can be discovered via email, phone, or username search queries.
