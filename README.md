# 🗳 VoteVerse

![React](https://img.shields.io/badge/Frontend-React-blue?logo=react)
![TailwindCSS](https://img.shields.io/badge/Styling-TailwindCSS-38B2AC?logo=tailwindcss)
![Node.js](https://img.shields.io/badge/Backend-Node.js-green?logo=node.js)
![Express](https://img.shields.io/badge/Framework-Express-black?logo=express)
![MongoDB](https://img.shields.io/badge/Database-MongoDB-4EA94B?logo=mongodb)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Vercel](https://img.shields.io/badge/Deployed%20on-Vercel-black?logo=vercel)
![Render](https://img.shields.io/badge/Backend%20on-Render-purple?logo=render)

> **VoteVerse** is a secure and modern voting platform that allows users to register, verify via OTP, participate in elections, and cast their votes — all with a responsive and professional UI.

---

## 🌐 Live Demo

- **Frontend:** [VoteVerse Client](https://voteverse-client.vercel.app/)  
- **Backend API:** [VoteVerse Server](https://your-render-backend-url.onrender.com)

---

## ✨ Features

✅ User Registration & Login with OTP verification  
✅ Secure Backend API with authentication & validation  
✅ Responsive design for mobile, tablet, and desktop  
✅ Instant Toast Notifications for user feedback  
✅ Shareable Election Links (Copy to clipboard)  
✅ Professional UI with smooth animations  
✅ Custom 404 Not Found page with animations  

---

## 🛠 Tech Stack

**Frontend**
- ⚛️ React.js  
- 🎨 Tailwind CSS  
- 🔗 React Router DOM  
- 🔔 React Toastify  
- 🖼 React Icons  
- 📡 Axios  

**Backend**
- 🟢 Node.js  
- 🚀 Express.js  
- 🍃 MongoDB + Mongoose  
- ✉️ Nodemailer (for OTP)  
- 🔑 JWT Authentication  
- 🔒 bcrypt (password hashing)  
- 🌿 dotenv  

---

## ⚙️ Installation

### 1️⃣ Clone the repository

```bash
git clone https://github.com/Arbab-ofc/voteverse-client.git
git clone https://github.com/Arbab-ofc/voteverse-server.git
```

## 2️⃣ Frontend Setup

```
cd voteverse-client
npm install
npm run dev

```

## 3️⃣ Backend Setup

```
cd voteverse-server
npm install

```

### Create .env in voteverse-server:
```
PORT=5000
MONGO_URI=your_mongo_connection_string
JWT_SECRET=your_jwt_secret
EMAIL_USER=your_email@example.com
EMAIL_PASS=your_email_password
```

### Run backend locally:
```
npm run dev

```
## 🚀 Deployment

### Frontend (Vercel)
- Add vercel.json to fix refresh issues in React Router:

```
{
  "rewrites": [
    {
      "source": "/(.*)",
      "destination": "/index.html"
    }
  ]
}
```
### Backend (Render)
-- Create a new web service on Render
-- Connect to your GitHub repository
-- Set the build command to `npm install` and the start command to `npm run dev`
-- Add environment variables in Render:
  - `PORT` (default: 5000)
  - `MONGO_URI`
  - `JWT_SECRET`
  - `EMAIL_USER`
  - `EMAIL_PASS`
- Deploy the service

## 🖼 Screenshots
![Home Page](client/src/assets/homePage.png)
![Login Page](client/src/assets/loginPage.png)
![Register Page](client/src/assets/registerPage.png)
![Election Page](client/src/assets/electionPage.png)
![Vote Page](client/src/assets/votePage.png)
![Not Found Page](client/src/assets/notFound.png)

## 🤝 Contributing
-- Fork the repository

-- Create a branch (feature/new-feature)

-- Commit changes

-- Push to branch

-- Create a Pull Request

## 📄 License
-- This project is licensed under the MIT License.

## 📬 Contact Me
-- 📧 Email: arbab.2201156ec@iiitbh.ac.in
-- 💼 LinkedIn: https://www.linkedin.com/in/arbab-arshad-0b2961326/
-- 💻 GitHub: https://github.com/Arbab-ofc/

### 💡 I’m always open to collaborating on exciting projects, discussing tech, or helping out with open-source contributions.

