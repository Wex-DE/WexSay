# Project Structure (High-Level Overview)

To keep our core code secure and proprietary, this public repository does not host the source code files. Instead, it serves as the distribution platform, bug tracker, and community guide.

This document outlines the organization of our private repository files for developers, auditors, and contributors to understand our project's modular design.

---

## 📁 Repository Directory Layout (Private Monorepo)

```
├── admin-frontend/         # Next.js 15 Administrative Panel dashboard
│   ├── public/             # Static assets and themes
│   └── src/
│       ├── app/            # Next.js pages and layouts (dashboard, users, themes)
│       ├── store/          # Zustand auth and dashboard state managers
│       └── utils/          # Axios API configuration
│
├── backend/                # Node.js Express & WebSocket API Backend
│   ├── src/
│   │   ├── config/         # Postgres connection pool, Redis client, Firebase Admin
│   │   ├── controllers/    # Route controllers (admin, chat, user, support)
│   │   ├── database/       # DB schema migrations and seeding logic
│   │   ├── middleware/     # Auth checks, RBAC controls, and rate limiters
│   │   ├── models/         # Sequelize database models (User, Message, Group)
│   │   ├── routes/         # REST API endpoints mapping
│   │   └── sockets/        # Real-time WebSocket connection handlers
│   └── uploads/            # Local media storage directory
│
└── app/                    # Native Android Mobile Application
    ├── build.gradle.kts    # Project-level dependencies and configs
    └── src/main/
        ├── AndroidManifest.xml # Permissions and component declarations
        ├── java/com/expde/chitchat/
        │   ├── calling/    # WebRTC voice/video calling services
        │   ├── database/   # Room local SQLite persistence classes (DAOs)
        │   ├── network/    # Retrofit API interface and SocketManager callbacks
        │   ├── ui/         # Jetpack Compose UI screens (HomeScreen, ChatScreen)
        │   ├── utils/      # TokenManager, CallLogHelper, EmojiHelper
        │   └── viewmodel/  # Architecture view models (ChatViewModel, HomeViewModel)
        └── res/            # UI resources (Drawables, layouts, strings)
```

---

## 🔒 Confidential & Ignored Files

The following configuration files are explicitly excluded from tracking in our private version control systems to ensure credentials are never exposed:
* `backend/.env` (Backend port, database URL, JWT secret keys, and email keys).
* `backend/firebase-adminsdk.json` (Firebase Cloud Messaging private service account key).
* `app/google-services.json` (Mobile client Firebase app association keys).
* `app/local.properties` (Local Android SDK paths).
