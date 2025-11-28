# User Authentication System

## 🔐 MERN Stack Authentication with JWT & Bcrypt

A secure, full-stack user authentication system built with the MERN (MongoDB, Express.js, React.js, Node.js) stack. This project implements industry-standard security practices including JWT tokens, bcrypt password hashing, and HTTP-only cookies.

![MERN Stack](https://img.shields.io/badge/Stack-MERN-green)
![License](https://img.shields.io/badge/License-MIT-blue)

## ✨ Features

- 🔐 **Secure Authentication**: JWT-based authentication with HTTP-only cookies
- 🔒 **Password Encryption**: Bcrypt hashing for secure password storage
- 👤 **User Management**: Complete registration, login, and profile management
- 🛡️ **Protected Routes**: Frontend and backend route protection
- 📱 **Responsive UI**: React with Bootstrap for modern, mobile-friendly design
- 🎨 **Toast Notifications**: User-friendly notifications with React Toastify
- 🗄️ **MongoDB Database**: Efficient data storage with Mongoose ODM

## 🛠️ Technologies Used

### Frontend
- **React.js** - UI library
- **React Router** - Navigation
- **React Bootstrap** - UI components
- **React Toastify** - Notifications
- **Vite** - Build tool

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **Mongoose** - ODM
- **JWT** - Authentication tokens
- **Bcrypt.js** - Password hashing

## 📋 Prerequisites

Before running this project, make sure you have:

- Node.js (v14 or higher)
- MongoDB Atlas account (or local MongoDB)
- Git

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/bradtraversy/mern-auth.git
cd mern-auth
```

### 2. Set Up Environment Variables

Create a `.env` file in the root directory:

```env
NODE_ENV=development
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key_here
```

### 3. Install Dependencies

```bash
# Install backend dependencies
npm install

# Install frontend dependencies
cd frontend
npm install
cd ..
```

### 4. Run the Application

```bash
# Run both frontend and backend (development mode)
npm run dev

# Run backend only
npm run server

# Run frontend only
cd frontend
npm run dev
```

The application will run on:
- Frontend: http://localhost:3000
- Backend: http://localhost:5000

## 📁 Project Structure

```
mern-auth/
├── backend/
│   ├── config/
│   │   └── db.js
│   ├── controllers/
│   │   └── userController.js
│   ├── middleware/
│   │   ├── authMiddleware.js
│   │   └── errorMiddleware.js
│   ├── models/
│   │   └── userModel.js
│   ├── routes/
│   │   └── userRoutes.js
│   ├── utils/
│   │   └── generateToken.js
│   └── server.js
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── package.json
│   └── vite.config.js
├── .env
├── .gitignore
├── package.json
└── README.md
```

## 🔑 API Endpoints

### Authentication Routes

| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| POST | `/api/users/auth` | Login user | No |
| POST | `/api/users` | Register user | No |
| POST | `/api/users/logout` | Logout user | Yes |
| GET | `/api/users/profile` | Get user profile | Yes |
| PUT | `/api/users/profile` | Update user profile | Yes |

## 🎯 Key Features Explained

### JWT Authentication
- Tokens stored in HTTP-only cookies for security
- Automatic token validation on protected routes
- Refresh token mechanism

### Password Security
- Passwords hashed with bcrypt before storage
- Never stored in plain text
- Secure password comparison

### Protected Routes
- Frontend: React Router guards
- Backend: Custom middleware
- Automatic redirect for unauthorized access

## 🌐 Deployment

### Deploy Frontend (Vercel)

1. Build the frontend:
```bash
cd frontend
npm run build
```

2. Deploy to Vercel:
- Go to [Vercel](https://vercel.com)
- Import your GitHub repository
- Set root directory to `frontend`
- Add environment variable: `VITE_API_URL=your_backend_url`
- Deploy

### Deploy Backend (Render)

1. Push code to GitHub
2. Go to [Render](https://render.com)
3. Create new Web Service
4. Connect GitHub repository
5. Set environment variables:
   - `MONGO_URI`
   - `JWT_SECRET`
   - `NODE_ENV=production`
6. Deploy

## 🔧 Configuration

### MongoDB Setup

1. Create account at [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
2. Create new cluster
3. Get connection string
4. Add to `.env` file

### Environment Variables

```env
# Server Configuration
NODE_ENV=development
PORT=5000

# Database
MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/dbname

# JWT Secret (use a strong random string)
JWT_SECRET=your_super_secret_jwt_key_here
```

## 📝 Usage Example

### Register New User
```javascript
// POST /api/users
{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "password123"
}
```

### Login
```javascript
// POST /api/users/auth
{
  "email": "john@example.com",
  "password": "password123"
}
```

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License.

## 👨‍💻 Author

**Nithin Kumar Kondabattini**
- GitHub: [@NithinKumarKondabattini](https://github.com/NithinKumarKondabattini)
- Student at SR University

## 🙏 Acknowledgments

- Original template by [Brad Traversy](https://github.com/bradtraversy/mern-auth)
- MERN Stack community
- MongoDB, Express, React, and Node.js teams

## 📞 Support

For support, email your-email@example.com or create an issue in this repository.

---

⭐ **If you find this project helpful, please give it a star!** ⭐
