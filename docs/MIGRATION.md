# Migration Guide — From Beta to Play Store Release

This guide explains how to migrate your account, data, and chats from the WexSay Public Beta application (`com.expde.chitchat`) to the official stable Google Play Store release (`com.wexde.wexsay`) when it launches.

---

## 🔍 Understanding the Package Constraints

During the testing phase, the application is packaged under a temporary testing ID:
* **Beta Package ID:** `com.expde.chitchat`
* **Stable Production Package ID:** `com.wexde.wexsay`

Because these are separate package IDs, the Android OS treats them as two completely different apps.
* Installing the Play Store version **will not overwrite** the Beta version.
* The Beta app **cannot receive auto-updates** to transition to the Play Store version.
* Both apps can technically run on your device at the same time, though we recommend uninstalling the Beta version once migration is complete.

---

## 💾 How Your Data is Preserved

You do not need to manually backup or export your chat database. All your data is securely stored on our centralized backend servers:
* Account profiles, contacts, and group associations.
* Private chat message logs and media attachments.
* Custom settings and support history.

---

## 🔄 Step-by-Step Migration Process

When the official Play Store app is released, follow these steps to migrate:

### Step 1: Install the Stable App
1. Open the Google Play Store on your Android device.
2. Search for **WexSay** (developed by WexDE) and install the application.

### Step 2: Log In with Your Existing Credentials
1. Open the newly installed WexSay app.
2. Select your country and enter the **same email/phone number** you used in the Beta application.
3. Verify your account via the standard verification steps (e.g., OTP code).

### Step 3: Verify Data Synchronization
1. Wait a few seconds for the app to sync with the backend.
2. Confirm that your contacts, active chats, and group memberships are fully restored.
3. Confirm that your profile picture and settings are updated.

### Step 4: Uninstall the Beta Application
1. Long-press the old WexSay Beta app icon on your device launcher.
2. Select **Uninstall** to remove the temporary package (`com.expde.chitchat`) and free up storage.
