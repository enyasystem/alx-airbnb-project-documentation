# 📄 Backend Requirements Specification – Airbnb Clone

This document outlines the **technical and functional requirements** for the core backend features of the Airbnb Clone project. It covers API endpoints, input/output data formats, validation rules, and performance criteria.

---

## 🔐 1. User Authentication

### ✅ Functional Requirements
- Users should be able to register, log in, and log out.
- Tokens should be used for session management (e.g., JWT).
- Passwords must be hashed before storage.
- Users must verify email before full access.

### 🔗 API Endpoints

| Method | Endpoint           | Description              |
|--------|--------------------|--------------------------|
| POST   | /api/v1/register   | Register new user        |
| POST   | /api/v1/login      | Authenticate user        |
| POST   | /api/v1/logout     | Log user out             |
| GET    | /api/v1/profile    | Get user profile (auth)  |

### 📝 Input/Output

**POST /api/v1/register**
```json
Input:
{
  "email": "user@example.com",
  "password": "securepass123"
}
Output:
{
  "message": "Registration successful. Verify your email."
}
