# 🧩 Simple Go REST API

This is a simple RESTful API server built with Go (`net/http`) that supports basic user management operations:

- ✅ Create User
- 🔍 Get User by ID
- 🗑️ Delete User
- 🌐 Hello World Root Route

User data is stored **in-memory** using a map with a mutex for thread-safe access.

---

## 🛠️ Features

- Built with Go's standard library
- JSON request/response
- Thread-safe with `sync.RWMutex`
- Routes:
  - `GET /` – Hello world route
  - `POST /users` – Create a user
  - `GET /users/{id}` – Get a user by ID
  - `DELETE /users/{id}` – Delete a user by ID

---

## 📦 Requirements

- Go 1.18 or later installed on your system

---

## 🚀 Running the Server

1. Clone this repository:

   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. Run the Go server:

   ```bash
   go run main.go
   ```

3. Server will start at:

   ```
   http://localhost:8080
   ```

---

## 📬 API Endpoints

### ➕ Create User

- **URL:** `POST /users`
- **Body:**

```json
{
  "name": "John Doe"
}
```

- **Response:** `204 No Content`

---

### 🔍 Get User

- **URL:** `GET /users/{id}`
- **Response:**

```json
{
  "name": "John Doe"
}
```

- **Errors:**
  - `400 Bad Request` – Invalid ID
  - `404 Not Found` – User not found

---

### ❌ Delete User

- **URL:** `DELETE /users/{id}`
- **Response:** `204 No Content`

---

## ⚠️ Notes

- This API uses an in-memory map to store users, so **all data is lost when the server restarts**.
- This is a great learning project but not production-ready.
