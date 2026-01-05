<div align="center">

# 🎓 SkillSharing Web

### A Modern Full-Stack Platform for Showcasing and Discovering Skills

[![React](https://img.shields.io/badge/React-19.1.1-61DAFB?style=for-the-badge&logo=react&logoColor=white)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-20.x-339933?style=for-the-badge&logo=node. js&logoColor=white)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-Database-47A248?style=for-the-badge&logo=mongodb&logoColor=white)](https://www.mongodb.com/)
[![Express](https://img.shields.io/badge/Express-4.19-000000?style=for-the-badge&logo=express&logoColor=white)](https://expressjs.com/)
[![TailwindCSS](https://img.shields.io/badge/Tailwind-4.1-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)

[Features](#-features) • [Tech Stack](#-tech-stack) • [Getting Started](#-getting-started) • [API Documentation](#-api-documentation) • [Contributing](#-contributing)

</div>

---

## 📖 About

**SkillSharing Web** is a comprehensive MERN stack platform that empowers users to showcase their professional skills, connect with others, and discover talent within a collaborative community. Similar to LinkedIn's skill endorsement system, this platform provides a seamless experience for building professional networks based on expertise and capabilities.

### ✨ Why SkillSharing Web?

- 🎯 **Focused Networking**: Connect with professionals based on specific skills
- 🔒 **Secure Authentication**: JWT-based authentication system
- 🎨 **Modern UI/UX**: Beautiful, responsive design with dark mode support
- ⚡ **Real-time Updates**: Fast and responsive user experience
- 📱 **Mobile-First**: Fully responsive across all devices

---

## 🚀 Features

### Core Functionality

- ✅ **User Authentication & Authorization**
  - Secure registration and login system
  - JWT token-based authentication
  - Protected routes and middleware
  - Cookie-based session management

- 👤 **Profile Management**
  - Create and customize user profiles
  - Add personal information and bio
  - Upload and manage avatars
  - Unique username generation

- 🎯 **Skill Management**
  - Add multiple skills to your profile
  - Edit and update skill information
  - Delete skills you no longer want to showcase
  - Categorize skills by proficiency level

- 🔍 **Discovery & Networking**
  - Browse skills shared by other users
  - Search and filter by specific skills
  - View detailed user profiles
  - Connect with skill-matched professionals

- 🎨 **UI/UX Features**
  - Dark/Light theme toggle
  - Smooth animations and transitions
  - Loading states and alerts
  - Responsive navigation
  - Background patterns and overlays

---

## 🛠️ Tech Stack

### Frontend
```json
{
  "framework": "React 19.1.1",
  "bundler": "Vite 7.1.7",
  "routing": "React Router DOM 7.9.1",
  "styling": "TailwindCSS 4.1.12",
  "http-client": "Axios 1.12.2",
  "auth": "JWT Decode 4.0.0",
  "animations": "ldrs 1.1.7"
}
```

**Key Libraries:**
- React 19 with modern hooks
- Vite for lightning-fast development
- TailwindCSS for utility-first styling
- React Router for client-side routing
- Context API for state management

### Backend
```json
{
  "runtime": "Node.js 20.x",
  "framework": "Express 4.19.2",
  "database": "MongoDB (Mongoose 8.3.3)",
  "authentication": "JWT + bcrypt",
  "security": "CORS, Cookie-Parser"
}
```

**Key Libraries:**
- Express. js for RESTful API
- Mongoose for MongoDB ODM
- bcrypt for password hashing
- jsonwebtoken for JWT authentication
- cors for cross-origin requests
- unique-username-generator for unique usernames

---

## 📂 Project Structure

```
skillssharingweb/
│
├── frontend/                # React frontend application
│   ├── src/
│   │   ├── components/      # Reusable React components
│   │   │   └── utils/       # Utility components (Navbar, Footer, etc.)
│   │   ├── assets/          # Images, icons, backgrounds
│   │   ├── App.jsx          # Root component
│   │   ├── main.jsx         # Application entry point
│   │   └── index. css        # Global styles
│   ├── package.json
│   └── vite.config.js       # Vite configuration
│
├── backend/                 # Node.js/Express backend
│   ├── config/              # Database and configuration files
│   │   └── db.js            # MongoDB connection
│   ├── controllers/         # Route controllers
│   ├── models/              # Mongoose schemas
│   ├── routes/              # API routes
│   ├── middleware/          # Custom middleware (auth, etc.)
│   ├── app.jsx              # Express app configuration
│   ├── package.json
│   └── vercel.json          # Vercel deployment config
│
└── README. md                # You are here! 
```

---

## 🚦 Getting Started

### Prerequisites

Before you begin, ensure you have the following installed: 
- **Node.js** (v20.x or higher)
- **npm** or **yarn**
- **MongoDB** (local or Atlas)
- **Git**

### Installation

1️⃣ **Clone the repository**
```bash
git clone https://github.com/Gouravlamba/skillssharingweb. git
cd skillssharingweb
```

2️⃣ **Backend Setup**

```bash
# Navigate to backend directory
cd backend

# Install dependencies
npm install

# Create .env file
touch .env
```

Add the following environment variables to `.env`:
```env
# Server Configuration
PORT=5000
NODE_ENV=development

# Database
MONGODB_URI=your_mongodb_connection_string

# JWT Secret
JWT_SECRET=your_super_secret_jwt_key_here

# Cookie Settings
COOKIE_SECRET=your_cookie_secret_here

# CORS Origin (Frontend URL)
CORS_ORIGIN=http://localhost:5173
```

```bash
# Start backend server
npm run dev
```

Backend will run on:  **http://localhost:5000**

3️⃣ **Frontend Setup**

```bash
# Navigate to frontend directory (from root)
cd ../frontend

# Install dependencies
npm install

# Create .env file (optional)
touch .env
```

Add the following environment variables to `.env`:
```env
VITE_API_URL=http://localhost:5000/api
```

```bash
# Start frontend development server
npm run dev
```

Frontend will run on: **http://localhost:5173**

---

## 🔌 API Documentation

### Authentication Endpoints

#### Register User
```http
POST /api/auth/register
Content-Type: application/json

{
  "name": "John Doe",
  "email": "john@example. com",
  "password": "securePassword123"
}
```

#### Login User
```http
POST /api/auth/login
Content-Type:  application/json

{
  "email": "john@example.com",
  "password": "securePassword123"
}
```

#### Logout User
```http
POST /api/auth/logout
Authorization: Bearer <token>
```

### User Endpoints

#### Get User Profile
```http
GET /api/users/profile
Authorization: Bearer <token>
```

#### Update User Profile
```http
PUT /api/users/profile
Authorization: Bearer <token>
Content-Type: application/json

{
  "name": "John Doe Updated",
  "bio":  "Software Developer",
  "avatar": "avatar-url"
}
```

### Skills Endpoints

#### Get All Skills
```http
GET /api/skills
```

#### Add Skill
```http
POST /api/skills
Authorization: Bearer <token>
Content-Type: application/json

{
  "name":  "React",
  "proficiency": "Advanced",
  "description": "Frontend development"
}
```

#### Update Skill
```http
PUT /api/skills/:id
Authorization:  Bearer <token>
Content-Type: application/json

{
  "proficiency": "Expert"
}
```

#### Delete Skill
```http
DELETE /api/skills/:id
Authorization: Bearer <token>
```

---

## 🎨 Features Showcase

### Context Providers
The application uses React Context API for state management: 

- **UserProvider**: Manages user authentication state
- **AlertProvider**: Handles global alert notifications
- **LoadingProvider**: Controls loading states across the app

### Theme Support
- **Dark Mode**: Sleek dark theme with optimized contrast
- **Light Mode**:  Clean and bright interface
- **Toggle**:  Easy theme switching with persistent preferences

### Responsive Design
- Mobile-first approach
- Breakpoint optimization
- Touch-friendly interface
- Adaptive layouts

---

## 🚢 Deployment

### Frontend (Vercel/Netlify)

**Vercel:**
```bash
cd frontend
npm run build
vercel --prod
```

**Environment Variables:**
- `VITE_API_URL`: Your backend API URL

### Backend (Vercel/Render/Railway)

**Vercel:**
- The project includes `vercel.json` configuration
- Deploy directly from GitHub

**Environment Variables:**
- Set all environment variables from `.env` in your hosting platform

---

## 🧪 Development Scripts

### Frontend
```bash
npm run dev      # Start development server
npm run build    # Build for production
npm run preview  # Preview production build
npm run lint     # Run ESLint
```

### Backend
```bash
npm run dev      # Start with nodemon (auto-reload)
npm start        # Start production server
npm test         # Run tests
```

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Contribution Guidelines
- Follow the existing code style
- Write clear commit messages
- Add tests for new features
- Update documentation as needed

---

## 📝 License

This project is licensed under the **ISC License**. 

---

## 👨‍💻 Author

**Gourav Lamba**

- GitHub: [@Gouravlamba](https://github.com/Gouravlamba)
- Repository: [skillssharingweb](https://github.com/Gouravlamba/skillssharingweb)

---

## 🙏 Acknowledgments

- React Team for the amazing framework
- MongoDB for the flexible database
- TailwindCSS for the utility-first CSS framework
- Vite for the blazing-fast build tool
- The open-source community

---

## 📞 Support

If you encounter any issues or have questions: 

1. Check existing [Issues](https://github.com/Gouravlamba/skillssharingweb/issues)
2. Create a new issue with detailed information
3. Reach out via GitHub Discussions

---

<div align="center">

### ⭐ Star this repository if you find it helpful!

**Made with ❤️ and React**

[Back to Top](#-skillsharing-web)

</div>
