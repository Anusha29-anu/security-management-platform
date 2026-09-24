# Security Management Platform

A security management web application for managing tenant-level users, campaigns, and security events with role-based access control.

## Overview

This project includes:
- React + Vite frontend
- Node.js + Express backend
- PostgreSQL data layer
- JWT authentication
- Role-based authorization
- Tenant-scoped operations

## Features

### Authentication
- Login with email and password
- JWT-based session handling
- Token stored in browser localStorage

### Dashboard
- Total users
- Total campaigns
- Open security events
- High / critical events
- Recent activity overview

### Campaign Management
- View campaigns
- Search campaigns
- Filter by status
- Pagination
- Create campaign
- Update campaign
- Delete campaign
- Assign users
- Remove users

### Security Events
- View event type, severity, status, description, and timestamp
- Filter by severity and status
- Pagination support

### Users
- View tenant users
- Display name, email, and role
- Roles: ADMIN, MANAGER, USER

### Role-Based Access
- ADMIN: full access
- MANAGER: campaign and operational management
- USER: restricted read / assigned access

## Tech Stack

### Frontend
- React
- Vite
- JavaScript

### Backend
- Node.js
- Express.js
- PostgreSQL
- JWT
- bcrypt

## Project Structure

```text
security-management-platform/
├── backend/
│   ├── src/
│   ├── package.json
│   ├── .env.example
│   └── .env
├── frontend/
│   ├── src/
│   ├── package.json
│   └── vite.config.js
├── .gitignore
└── README.md
```

## Prerequisites

- Node.js 18+
- PostgreSQL database
- npm

## Backend Setup

1. Open the backend folder:

```bash
cd backend
```

2. Install dependencies:

```bash
npm install
```

3. Configure environment variables:

```bash
cp .env.example .env
```

Then update the values in `.env` for your PostgreSQL and JWT settings.

Example:

```env
PORT=5000
DB_HOST=localhost
DB_PORT=5433
DB_NAME=security_management
DB_USER=postgres
DB_PASSWORD=your_password
JWT_SECRET=your_secret_key
```

4. Start the backend server:

```bash
npm run dev
```

The API runs on:
- http://localhost:5000

## Frontend Setup

1. Open the frontend folder:

```bash
cd frontend
```

2. Install dependencies:

```bash
npm install
```

3. Start the frontend app:

```bash
npm run dev
```

The frontend runs on:
- http://localhost:5173

## Default Login

Use valid tenant user credentials that exist in the database. The app expects a real user record with a matching email and password hash.

## Notes

- The backend enforces authentication and role-based authorization.
- The frontend UI reflects those permissions but does not replace backend security checks.
- This project is a focused implementation for tenant security management and follows a simple, professional admin-dashboard structure.

## License

This project is for educational and demonstration purposes.
