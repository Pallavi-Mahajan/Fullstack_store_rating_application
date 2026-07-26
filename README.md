# 🏪 Fullstack Store Rating Application

A full-stack web application that allows users to rate stores, view average ratings, and manage ratings. The application is built using **React.js**, **Node.js (Express)**, and **MySQL** with JWT-based authentication.

---

## 📌 Features

### User Authentication
- User Registration
- Secure Login using JWT
- Password hashing using bcrypt

### User Roles
- **Admin**
- **Normal User**
- **Store Owner**

### Store Management
- View all available stores
- Display average rating for each store
- Normal users can submit and update ratings (1–5)
- Users can view their previously submitted ratings

### Security
- JWT Authentication
- Password hashing with bcrypt
- Role-based authorization
- Input validation

---

## 🛠️ Tech Stack

### Frontend
- React.js
- Axios
- CSS

### Backend
- Node.js
- Express.js
- JWT Authentication
- bcryptjs
- CORS

### Database
- MySQL

---

## 📂 Project Structure

```
Fullstack_Store_Rating_Application/
│
├── frontend/
│   ├── App.js
│   └── package.json
│
├── backend/
│   ├── server.js
│   └── package.json
│
├── database/
│   └── Database.sql
│
└── README.md
```

---

## 🗄️ Database Schema

### Users Table

| Column | Type |
|---------|------|
| id | INT |
| name | VARCHAR(60) |
| email | VARCHAR(100) |
| password_hash | VARCHAR(255) |
| address | VARCHAR(400) |
| role | admin / normal / store_owner |

---

### Stores Table

| Column | Type |
|---------|------|
| id | INT |
| name | VARCHAR(60) |
| email | VARCHAR(100) |
| address | VARCHAR(400) |
| owner_id | INT |

---

### Ratings Table

| Column | Type |
|---------|------|
| id | INT |
| user_id | INT |
| store_id | INT |
| rating | INT (1–5) |

---

## ⚙️ Installation

### 1. Clone Repository

```bash
git clone https://github.com/Fullstack_Store_Rating_Application.git

cd Fullstack_Store_Rating_Application
```

---

### 2. Setup Database

Open MySQL and execute:

```sql
source Database.sql;
```
---

### 3. Backend Setup

Navigate to backend folder.

```bash
cd backend
```

Install dependencies.

```bash
npm install
```

Required packages:

```bash
npm install express mysql2 bcryptjs jsonwebtoken cors
```

Update database credentials inside `server.js`.

Also change the JWT secret.

Start backend server.

```bash
node server.js
```

Server runs on:

```
http://localhost:4000
```

---

### 4. Frontend Setup

Navigate to frontend.

```bash
cd frontend
```

Install dependencies.

```bash
npm install
npm install axios
```

Start React application.

```bash
npm start
```

Application runs on:

```
http://localhost:3000
```

---

## 🔗 API Endpoints

### Register

```
POST /api/register
```

---

### Login

```
POST /api/login
```

---

### Get All Stores

```
GET /api/stores
```

Requires JWT Token.

---

### Submit Rating

```
POST /api/stores/:id/rate
```

Requires JWT Token.

---

## 🔐 Authentication

After login, the server returns a JWT token.
Include the token in every protected request.

---

## ⭐ Rating Rules

- Rating must be between **1 and 5**
- One rating per user for each store
- Existing ratings can be updated
- Average rating is calculated automatically

---

## 🚀 Future Enhancements

- Admin Dashboard
- Store Owner Dashboard
- Search Stores
- Filter Stores
- Pagination
- Responsive UI
- Profile Management
- Password Reset
- Email Verification
- Docker Deployment

---

## 👩‍💻 Author

  **Pallavi Mahajan**

---
