# 🚀 Social Media App

A scalable social media backend application built with **TypeScript, Node.js, and Express.js**, developed as part of my backend development journey with **Route Academy**.

The project focuses on implementing real-world backend concepts including authentication, authorization, friend management, real-time communication, caching, GraphQL, and secure user management.

---

## 🛠️ Tech Stack

* **Node.js**
* **Express.js**
* **TypeScript**
* **MongoDB**
* **Mongoose**
* **Redis**
* **JWT**
* **GraphQL**
* **Socket.IO**
* **bcrypt**
* **Zod**
* **Morgan**
* **CORS**

---

## ✨ Features

### 🔐 Authentication & Authorization

* User registration and login
* Password hashing using bcrypt
* JWT-based authentication
* Access & Refresh Tokens
* Token management using Redis
* Email verification using OTP
* Password validation
* Protected routes and authorization middleware

### 👥 User & Friend System

* User management
* Send friend requests
* Accept friend requests
* Friend request status management
* Prevent sending requests to yourself
* Handle pending and accepted requests

### ⚡ Real-Time Communication

Implemented real-time communication using **Socket.IO**.

Current functionality includes:

* User registration on the socket server
* User connection management
* Real-time event handling
* Sending messages through Socket.IO

### 🔎 GraphQL

The application also provides GraphQL functionality for flexible API querying.

Implemented operations include:

* Query friend requests
* Send friend requests
* Retrieve related user information

---

## 🗄️ Redis

Redis is used to improve performance and manage temporary authentication-related data.

Examples include:

* Refresh token management
* JWT session handling
* OTP storage
* OTP expiration
* Authentication-related rate limiting

---

## 🧩 Project Structure

```text
Social-Media-App/
│
├── config/
│
├── src/
│   ├── app/
│   ├── DB/
│   ├── middleware/
│   ├── modules/
│   │   ├── auth/
│   │   ├── user/
│   │   ├── post/
│   │   └── chat/
│   │
│   ├── graphql/
│   ├── socket/
│   └── index.ts
│
├── .gitignore
├── package.json
├── package-lock.json
├── tsconfig.json
└── README.md
```

> The exact internal structure may evolve as the project continues to grow.

---

## 🔑 Authentication Flow

The authentication system follows a token-based architecture:

```text
Client
  │
  ▼
Login / Signup
  │
  ▼
Authentication
  │
  ├── Access Token
  │
  └── Refresh Token
          │
          ▼
        Redis
```

Protected endpoints require a valid access token.

Refresh tokens are managed using Redis to support session control and token revocation.

---

## 📡 Real-Time Communication

Socket.IO is used to establish real-time communication between connected users.

```text
Client
   │
   │ Socket Connection
   ▼
Socket.IO Server
   │
   ├── Register User
   ├── Send Message
   └── Handle Events
```

---

## 📦 Installation

Clone the repository:

```bash
git clone <https://github.com/ahmedghanem111/Social-Media-App.git>
```

Navigate to the project:

```bash
cd social-media-app
```

Install dependencies:

```bash
npm install
```

---

## ⚙️ Environment Variables

Create your environment configuration according to the required services.

Example:

```env
PORT=3000

MONGO_URI=mongodb://127.0.0.1:27017/socialApp

JWT_ACCESS_SECRET=your_access_secret
JWT_REFRESH_SECRET=your_refresh_secret

REDIS_URL=your_redis_connection_string

EMAIL_USER=your_email
EMAIL_PASSWORD=your_email_password
```

---

## ▶️ Running the Project

### Development

```bash
npm run start:dev
```

### Build

```bash
npm run start:build
```

### Production

```bash
npm start
```

---

## 🧪 API Testing

The backend APIs can be tested using tools such as **Postman**.

Authentication endpoints and protected endpoints can be tested by providing the generated JWT access token in the request headers.

Example:

```text
Authorization: Bearer <access-token>
```

GraphQL operations can be tested through the GraphQL endpoint.

---

## 🎯 Learning Outcomes

Through this project, I practiced and applied several backend development concepts:

* Building RESTful APIs
* TypeScript with Express.js
* MongoDB database design
* Mongoose schemas and queries
* Authentication & Authorization
* JWT Access & Refresh Tokens
* Redis integration
* OTP-based verification
* GraphQL APIs
* Real-time communication with Socket.IO
* Middleware architecture
* Input validation
* Modular backend architecture
* API testing

---

## 🚀 Future Improvements

Possible future enhancements include:

* Complete one-to-one and group chat functionality
* Post reactions and comments
* Media upload and storage
* Notifications system
* Advanced feed algorithms
* Improved caching strategies
* Docker containerization
* API documentation with Swagger/OpenAPI
* Automated testing

---

## 👨‍💻 Author

**Ahmed Mohamed Abdelfatah**

Computer Science Student
Cairo University

Backend Developer | Node.js

---

## 📚 Training

Developed as part of my backend development journey with **Route Academy**.
