# Supported Devices

WexSay is designed to support a wide range of Android devices. However, hardware differences in audio codecs, camera sensors, and screen densities can affect performance. This document lists verified and supported device profiles.

---

## 📱 Hardware Requirements

### Minimum Requirements
* **Android OS:** 8.0 (API Level 26 - Oreo)
* **RAM:** 2 GB
* **CPU:** Quad-Core 1.4 GHz
* **Storage:** 150 MB free space (for app installation only; media storage varies)
* **Features:** Front camera (for video calls), microphone, Google Play Services (or MicroG for notifications).

### Recommended Requirements
* **Android OS:** 11.0 (API Level 30) or higher
* **RAM:** 4 GB or higher
* **CPU:** Octa-Core 2.0 GHz or higher (e.g. Snapdragon, MediaTek Dimensity)
* **Storage:** 500 MB+ free space
* **Features:** Front camera, microphone, secure hardware keystore (for encrypted storage).

---

## 🧪 Verified Device List

The following devices have been tested by the WexDE QA team and are verified to run WexSay without issues:

| Manufacturer | Model | Android Version Tested | Status | Notes |
| :--- | :--- | :---: | :---: | :--- |
| **Google** | Pixel 7 / 7 Pro | Android 13 / 14 |  ✅ Verified  | Smooth performance, instant calls |
| **Google** | Pixel 5 | Android 11 / 12 |  ✅ Verified  | Fully compatible |
| **Samsung** | Galaxy S22 / S23 | Android 12 / 13 / 14 |  ✅ Verified  | Excellent video calling performance |
| **Samsung** | Galaxy A34 / A54 | Android 13 |  ✅ Verified  | Responsive UI performance |
| **Xiaomi** | Redmi Note 11 / 12 | Android 11 / 12 |  ✅ Verified  | Fully compatible |
| **Realme** | Narzo 50 | Android 11 / 12 |  ✅ Verified  | Fully compatible |
| **OnePlus** | 10 Pro | Android 12 / 13 |  ✅ Verified  | Smooth performance |

---

## ⚠️ Known Compatibility Exceptions

* **Custom ROMs (without GCSF/MicroG):** Devices running LineageOS or GrapheneOS without Google services will run the app, but push notifications will experience polling delays.
* **Android Go Edition:** Devices with less than 2 GB RAM running Android Go may experience layout redraw lags during custom emoji rendering.
* **Huawei Devices (without GMS):** EMUI devices lacking Google Play Services will run the app, but notification badges and push receipts are subject to polling intervals.
