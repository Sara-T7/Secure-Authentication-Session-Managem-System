

# Authentication System

A secure authentication system built with **Node.js, Express.js, MySQL, HTML, CSS, and JavaScript**.

## Features

* Strong password validation
* Brute-force protection with rate limiting and account lockout
* JWT access tokens with rotating refresh tokens
* Google Sign-In
* Suspicious login detection using IP address and user-agent
* Active session management and session revocation
* Password hashing with bcrypt

## Technology Stack

* **Frontend:** HTML, CSS, JavaScript
* **Backend:** Node.js, Express.js
* **Database:** MySQL (XAMPP)
* **Authentication:** JWT, Refresh Tokens, Google Identity Services
* **Security:** bcrypt, rate limiting, account lockout

## Setup

### 1. Database

Start MySQL from XAMPP and run:

```text
backend/db/schema.sql
```

This creates the required database and tables.

### 2. Backend

```bash
cd backend
npm install
cp .env.example .env
npm start
```

Configure the required database, JWT, Google OAuth, and CORS variables in `.env`.

The backend runs on:

```text
http://localhost:4000
```

### 3. Frontend

```bash
cd frontend
npx serve -l 5500
```

Configure the Google Client ID in:

```text
frontend/js/config.js
```

Then open:

```text
http://localhost:5500
```

## Project Structure

```text
auth-system/
├── backend/
├── frontend/
└── README.md
```

## Security

Passwords are hashed using bcrypt. Access tokens are short-lived, while refresh tokens are securely stored using HTTP-only cookies and rotated after use. Login attempts are protected through rate limiting and account lockout mechanisms.
