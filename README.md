# Secure-Authentication-Lab

# Secure Authentication Lab

## Project Overview

A small local authentication service demonstrating essential authentication security practices.

This project focuses on implementing secure authentication mechanisms, validating user input, protecting login endpoints, and managing user sessions.

### Security Features

- Password hashing
- Server-side input validation
- Rate limiting
- Generic authentication errors
- Secure session-cookie settings
- User logout functionality
- Automated security tests

---

## 1. Run Locally

### Step 1: Create a Virtual Environment

```bash
python -m venv .venv
```

### Step 2: Activate the Virtual Environment

**Windows:**

```bash
.venv\Scripts\activate
```

**macOS / Linux:**

```bash
source .venv/bin/activate
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Start the Application

```bash
python app.py
```

The service listens only on:

```text
http://127.0.0.1:5000
```

The local database is initialized automatically when the application starts.

---

## 2. Test the Authentication Service

### Step 1: Check Application Health

```bash
curl -i http://127.0.0.1:5000/health
```

This endpoint checks whether the authentication service is running.

### Step 2: Register a New User

```bash
curl -i -X POST http://127.0.0.1:5000/register \
  -H "Content-Type: application/json" \
  -d '{"username":"demo_user","password":"a-long-demo-password"}'
```

This request registers a new user with a username and password.

### Step 3: Login

```bash
curl -i -X POST http://127.0.0.1:5000/login \
  -H "Content-Type: application/json" \
  -d '{"username":"demo_user","password":"a-long-demo
