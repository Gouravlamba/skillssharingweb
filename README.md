📚 SkillSharing Web

A full-stack MERN platform that allows users to share the skills they have—similar to LinkedIn skill showcasing.
Users can create profiles, add skills, view other users’ skills, and connect with people who have the expertise they need.

🚀 Features

👤 User Authentication (Register / Login / JWT)

📝 Create & Edit User Profile

🧠 Add, Edit & Delete Skills

🔍 Browse Skills Shared by Other Users

⭐ View Detailed Skill Profiles

🖼️ Image / Avatar Upload (optional)

📱 Fully Responsive UI

🌐 RESTful API built using Node.js + Express

🛠️ Tech Stack (MERN)
Frontend

React.js

React Router

Axios

TailwindCSS / Bootstrap (choose the one you used)

Backend

Node.js

Express.js

MongoDB / Mongoose

JSON Web Token (JWT)

📂 Project Folder Structure
SkillSharing-Web/
│
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── context/
│   │   ├── hooks/
│   │   └── App.js
│   └── package.json
│
├── backend/
│   ├── config/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── server.js
│   └── package.json
│
└── README.md

🔧 Installation & Setup
1. Clone the repository
git clone https://github.com/your-username/SkillSharing-Web.git
cd SkillSharing-Web

⚙️ Backend Setup
cd backend
npm install

Create .env file in /backend
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key

Run backend server
npm start


Backend runs on: http://localhost:5000

🎨 Frontend Setup
cd frontend
npm install

Run frontend
npm start
