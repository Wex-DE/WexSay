# Backend API Specifications (REST & WebSockets)

This document provides technical documentation for the WexSay REST API and WebSocket events.

---

## 🔒 Authentication

All protected REST API requests must include the JWT token in the request headers:

`Authorization: Bearer <access_token>`

For the Administration Panel dashboard, authentication is securely handled using `HttpOnly` cookie exchanges (`adminToken`).

---

## 📡 REST Endpoints

### 1. Authentication Service

#### `POST /api/v1/auth/register`
* **Description:** Register a new user account.
* **Payload (JSON):**
  ```json
  {
    "phone_number": "+8801700000000",
    "email": "user@example.com",
    "password": "secure_password",
    "name": "John Doe",
    "username": "johndoe"
  }
  ```
* **Response (201 Created):**
  ```json
  {
    "status": "success",
    "data": {
      "user": { "id": "uuid-v4", "username": "johndoe", "is_verified": false }
    }
  }
  ```

#### `POST /api/v1/auth/login`
* **Description:** Log into an existing user account.
* **Response (200 OK):** Returns authentication access token and refresh token details.

---

### 2. User & Contacts Service

#### `GET /api/v1/users/profile/:username`
* **Description:** Fetch user profile details.
* **Privacy Controls:** Sensitive attributes (such as `email`) are scrubbed for other users. `phone_number` and `profile_picture` are filtered dynamically depending on the target user's privacy configurations.

#### `POST /api/v1/users/contacts/sync`
* **Description:** Upload phone suffixes to discover matching contacts.

---

## 🔌 WebSocket Events (Socket.IO)

Clients connect to the real-time server using:
`wss://api.wexsay.com`

### 1. Client to Server (Emit)

* **`join_room`:** Attach client socket to a chat room room ID.
  ```json
  { "conversation_id": "uuid-v4" }
  ```
* **`send_message`:** Send a message payload.
  ```json
  {
    "conversation_id": "uuid-v4",
    "content": "Hello!",
    "message_type": "text"
  }
  ```

### 2. Server to Client (Listen)

* **`receive_message`:** Emitted when a new message is delivered to an active room.
* **`message_status_update`:** Emitted when a message state changes (e.g. `delivered`, `seen`, or `deleted`).
