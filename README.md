# Node.js Backend API

A simple backend application built using **Node.js, Express, and MongoDB** with JWT authentication and basic CRUD operations for tasks.

---

## 🚀 Features

* User registration and login
* JWT-based authentication
* Create, read, update, delete (CRUD) tasks
* MongoDB database integration
* Middleware-based route protection
* Clean project structure (controllers, routes, models)

---

## 🛠️ Tech Stack

* Node.js
* Express.js
* MongoDB (Mongoose)
* JWT (Authentication)
* bcryptjs (Password hashing)
* dotenv

---

## 📁 Project Structure

```
node-backend/
├── src/
│   ├── config/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── app.js
│   └── server.js
├── .env
├── package.json
```

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone <repo-url>
cd node-backend
```

### 2. Install dependencies

```bash
npm install
```

### 3. Create environment file

Create a `.env` file in the root directory:

```env
PORT=5000
MONGO_URI=mongodb://localhost:27017/nodeapp
JWT_SECRET=secret123
```

### 4. Start MongoDB (local setup)

```bash
mongod
```

---

## ▶️ Run the application

### Development mode

```bash
npm run dev
```

### Production mode

```bash
npm start
```

---

## 📡 API Endpoints

### Auth Routes

#### Register User

```
POST /api/auth/register
```

#### Login User

```
POST /api/auth/login
```

---

### Task Routes (Protected)

#### Create Task

```
POST /api/tasks
Authorization: Bearer <token>
```

#### Get All Tasks

```
GET /api/tasks
Authorization: Bearer <token>
```

#### Update Task

```
PUT /api/tasks/:id
Authorization: Bearer <token>
```

#### Delete Task

```
DELETE /api/tasks/:id
Authorization: Bearer <token>
```

---

## 🔐 Authentication Flow

1. User registers or logs in
2. Server returns JWT token
3. Token is sent in request header:

   ```
   Authorization: Bearer <token>
   ```
4. Middleware verifies token before allowing access

---

## 🧠 What You Learn From This Project

* How backend architecture is structured
* How Express routing works
* JWT authentication flow
* MongoDB schema design
* Middleware usage
* Real-world API design

---

## 📌 Future Improvements

* Add refresh tokens
* Add role-based access control (Admin/User)
* Add Docker support
* Add unit testing
* Deploy on AWS / Render / Vercel

---

## 👨‍💻 Author

Built for learning backend development with Node.js 🚀
