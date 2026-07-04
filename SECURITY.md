# Security Policy

We are committed to keeping WexSay secure and maintaining the confidentiality of our users. This document outlines how to report security vulnerabilities responsibly and our security update policies.

---

## Supported Versions

Only the latest active Public Beta release is supported for security updates.

| Version | Supported |
| :--- | :---: |
| >= 1.0.0-beta.2 |   ✅   |
| < 1.0.0-beta.2  |   ❌   |

---

## Reporting a Vulnerability

> [!CAUTION]
> **Please do NOT report security vulnerabilities via public GitHub issues.** Public issues expose the exploit immediately, putting other testers at risk.

If you discover a security vulnerability in the WexSay Android client, admin panel, or backend API, please report it privately:

1. **Email Us:** Send a detailed security report to `security@wexsay.com` (or the WexDE security contact).
2. **Provide Details:** Include a description of the vulnerability, steps to reproduce, and a proof-of-concept (PoC) if available.
3. **PGP Encryption (Optional):** You can encrypt your report using our public PGP key (available upon request or via our security contact page).

### Our Commitment
* We will acknowledge receipt of your report within 24 hours.
* We will provide a timeline for resolving the issue and keep you updated throughout the patching process.
* We will credit you in our [Credits](CREDITS.md) or release notes once the patch is live, unless you prefer to remain anonymous.

---

## Security Practices in WexSay

* **Transit Security:** All network requests and WebSocket frames use TLS 1.3 (HTTPS/WSS) to prevent eavesdropping. Cleartext traffic is disabled on the Android client manifest.
* **Storage Security:** In-app preferences, access tokens, and sensitive data are encrypted on-device using AES-256 GCM wrapper keys managed by the Android Keystore system.
* **Validation Hardening:** Uploaded files are validated on the backend using strict MIME-type and extension mapping to block malicious payload uploads.
* **Graceful Crash Handling:** Server exceptions are caught, database connection pools are closed safely, and instances are gracefully rebooted to prevent data leaks.
