# Known Issues

This document tracks known issues, bugs, and performance limitations in the active WexSay Public Beta program. We are actively working to resolve these before the official Play Store release.

---

## 🛠️ Active Client Issues (Android App)

### 1. WebRTC calling Delay on Slow Networks
* **Description:** Voice and video calls can take up to 5-10 seconds to connect when one of the peers is on a weak 3G or heavily throttled connection.
* **Workaround:** Ensure you have a stable 4G, 5G, or Wi-Fi connection. We are tuning the ICE candidate gathering timeouts in the next release to speed up connections.
* **Tracking ID:** `#client-001`

### 2. Custom Emoji Rendering Lag on Lower-End Devices
* **Description:** Scrolling the custom emoji picker window on devices with less than 2 GB RAM can cause temporary frame drops (jank).
* **Workaround:** Tap slowly or close background applications. We are optimizing image caching and reducing rendering overhead in Jetpack Compose.
* **Tracking ID:** `#client-002`

### 3. Missing Auto-Updates (Package Name Constraint)
* **Description:** The beta application uses a temporary package name `com.expde.chitchat`. The final Google Play Store release will use a different package name.
* **Workaround:** Users will need to manually download and install the official Play Store package when released.
* **Tracking ID:** `#client-003`

---

## 🖥️ Active Administrative Panel Issues

### 1. Session Expiry Redirection Flash
* **Description:** When the admin dashboard session expires, the browser may briefly load the overview screen before redirecting to the login screen.
* **Workaround:** This is a visual bug and does not expose data. We are refining cookie verification checks on client mounts to prevent this flash.
* **Tracking ID:** `#admin-001`

---

## 📝 Reporting a New Issue
If you encounter an issue that is not listed here:
1. Ensure you are running the latest version of the WexSay beta APK.
2. Go to the [Issues](https://github.com/Wex-DE/WexSay/issues) section.
3. Open an issue using the **Bug Report Template** and provide as much detail as possible.
