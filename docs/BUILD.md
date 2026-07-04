# Compilation & Build Guide (Private Codebase)

This guide documents the procedures for compiling and building the WexSay Android application from the private source code repository.

---

## 🛠️ Build Requirements

* **Android Studio:** Ladybug (2024.2.1) or higher.
* **JDK:** Java Development Kit 17 (configured as Gradle JDK).
* **Android SDK:** API Level 36 (compileSdk) / Build Tools 36.0.0.
* **Gradle Wrapper:** Version 9.2.1.
* **KSP Devtools:** Kotlin Symbol Processing plugins.

---

## 🔑 Project Configurations

Before compiling the application, ensure the following local configurations are configured:

### 1. google-services.json
Obtain the Firebase App Configuration file from the Firebase Console under Project Settings and place it in the application's root app module:
`app/google-services.json`

### 2. local.properties
Define the local path to your Android SDK installation in the root project directory:
`sdk.dir=C\:\\Users\\YourUsername\\AppData\\Local\\Android\\Sdk`

---

## 🚀 Building via Command Line (Gradle)

Open a terminal or command prompt in the root of the private repository and run the following Gradle commands:

### 1. Clean the Build Cache
Ensure old build artifacts are cleared before compiling:
```bash
./gradlew clean
```

### 2. Compile and Verify Kotlin Sources
Run full Kotlin and Java compiler checks:
```bash
./gradlew compileDebugSources
```

### 3. Generate Release APK (Split Architectures)
Build the release binaries optimized for distribution:
```bash
./gradlew assembleRelease
```
The compiled output files will be generated in:
`app/build/outputs/apk/release/`

* `app-universal-release.apk` (Recommended; supports all architectures)
* `app-arm64-v8a-release.apk` (For modern 64-bit devices)
* `app-armeabi-v7a-release.apk` (For older 32-bit devices)
