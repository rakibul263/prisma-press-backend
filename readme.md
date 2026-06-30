# 🚀 Prisma Press Backend

A modern, scalable, and modular Blog REST API built with **Express.js**, **TypeScript**, **Prisma ORM**, and **PostgreSQL**.

This project provides complete backend functionality for a blogging platform including authentication, user management, posts, comments, role-based authorization, and admin statistics.

---

## ✨ Features

### 🔐 Authentication
- User Registration
- User Login
- JWT Access Token
- Refresh Token
- HTTP-Only Cookie Authentication
- Password Hashing using bcrypt

### 👤 User Management
- Register User
- Get Logged-in User Profile
- Update Profile
- Profile Photo
- User Bio

### 📝 Blog Posts
- Create Post
- Update Post
- Delete Post
- Get Single Post
- Get All Posts
- Pagination
- Search
- Filter
- Sorting
- Featured Posts
- Draft / Published / Archived Status
- View Counter

### 💬 Comments
- Create Comment
- Edit Own Comment
- Delete Own Comment
- Get Comment
- Get Author Comments
- Comment Moderation (Admin)

### 🛡 Authorization
- JWT Authentication
- Role Based Access Control
- USER Role
- ADMIN Role

### 📊 Admin Dashboard
- Total Users
- Total Posts
- Published Posts
- Draft Posts
- Archived Posts
- Total Comments
- Approved Comments
- Total Views

---

# 🛠 Tech Stack

| Technology | Usage |
|------------|------|
| Express.js | Backend Framework |
| TypeScript | Programming Language |
| Prisma ORM | Database ORM |
| PostgreSQL | Database |
| JWT | Authentication |
| bcrypt | Password Hashing |
| Cookie Parser | Cookie Handling |
| CORS | Cross-Origin Resource Sharing |
| dotenv | Environment Variables |

---

# 📁 Project Structure

```
src/
│
├── app/
│   ├── modules/
│   │   ├── auth/
│   │   ├── user/
│   │   ├── profile/
│   │   ├── post/
│   │   └── comment/
│   │
│   ├── middleware/
│   ├── routes/
│   ├── utils/
│   ├── helpers/
│   └── errors/
│
├── prisma/
│
├── generated/
│
├── server.ts
└── app.ts
```

---

# ⚙️ Installation

Clone the repository

```bash
git clone https://github.com/your-username/prisma-press-backend.git
```

Move into the project

```bash
cd prisma-press-backend
```

Install dependencies

```bash
npm install
```

or

```bash
pnpm install
```

---

# 🔑 Environment Variables

Create a `.env` file in the project root.

```env
DATABASE_URL=

PORT=3000

APP_URL=

BCRYPT_SALT_ROUNDS=

JWT_ACCESS_SECRET=

JWT_REFRESH_SECRET=

JWT_ACCESS_EXPIRES_IN=

JWT_REFRESH_EXPIRES_IN=
```

---

# ▶️ Running the Project

Development

```bash
npm run dev
```

or

```bash
pnpm dev
```

Build

```bash
npm run build
```

Run Production

```bash
npm start
```

---

# 📌 API Endpoints

## Authentication

| Method | Endpoint |
|---------|----------|
| POST | `/api/auth/login` |
| POST | `/api/auth/refresh-token` |

---

## Users

| Method | Endpoint |
|---------|----------|
| POST | `/api/users/register` |
| GET | `/api/users/me` |
| PUT | `/api/users/my-profile` |

---

## Posts

| Method | Endpoint |
|---------|----------|
| GET | `/api/posts` |
| GET | `/api/posts/:postId` |
| GET | `/api/posts/my-posts` |
| GET | `/api/posts/stats` |
| POST | `/api/posts` |
| PATCH | `/api/posts/:postId` |
| DELETE | `/api/posts/:postId` |

---

## Comments

| Method | Endpoint |
|---------|----------|
| GET | `/api/comments/:commentId` |
| GET | `/api/comments/author/:authorId` |
| POST | `/api/comments` |
| PATCH | `/api/comments/:commentId` |
| DELETE | `/api/comments/:commentId` |
| PATCH | `/api/comments/:commentId/moderate` |

---

# 🔍 Post Filtering

Supports

- Search
- Tags
- Featured
- Status
- Author
- Pagination
- Sorting

Example

```
GET /api/posts?search=prisma&page=1&limit=10&sortBy=createdAt&sortOrder=desc
```

---

# 🔒 Security

- Password Hashing (bcrypt)
- JWT Authentication
- HTTP Only Cookies
- Protected Routes
- Role-Based Authorization
- Global Error Handler
- Prisma Error Handling

---

# 📈 Future Improvements

- Request Validation
- Rate Limiting
- Unit Testing
- Integration Testing
- Logging System
- Docker Support
- CI/CD Pipeline
- Swagger Documentation

---

# 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push your branch
5. Open a Pull Request

---

# 👨‍💻 Author

**MD Rakibul Hasan**

If you like this project, don't forget to ⭐ the repository.