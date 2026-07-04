# Versioning Strategy

WexSay releases adhere strictly to [Semantic Versioning 2.0.0](https://semver.org/spec/v2.0.0.html). 

---

## 🏷️ Version Format

Our release versions use the following structure:

$$\text{MAJOR.MINOR.PATCH[-PRERELEASE]}$$

* **MAJOR:** Increment when you make incompatible API changes or structural migrations (e.g. package ID switch).
* **MINOR:** Increment when you add functionality in a backwards-compatible manner (e.g. new features like call log filters).
* **PATCH:** Increment when you make backwards-compatible bug fixes or security patches (e.g. SQLite database sync fixes).
* **PRERELEASE:** Tag appended to indicate public testing builds (e.g. `-beta.1`, `-beta.2`).

---

## 🚀 Release Classifications

### 1. Pre-Releases (Beta builds)
* **Format:** `v1.0.0-beta.X`
* **Purpose:** Public testing packages distributed as standalone APKs.
* **Update Frequency:** As bugs are identified and resolved by QA or reported by community members.

### 2. Stable Releases (General Availability)
* **Format:** `v1.0.0`
* **Purpose:** Production-ready packages published on the Google Play Store.
* **Update Frequency:** Scheduled feature updates and audited builds.

### 3. Hotfixes
* **Format:** `v1.0.1`
* **Purpose:** Emergency patches released to resolve critical crashes or zero-day security vulnerabilities.
* **Update Frequency:** Instant release upon validation of fix.
