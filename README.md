# 🚀 AI-Powered Social Media Automation & Scheduler

An AI-powered full-stack web application that helps users **generate, manage, schedule, and publish social media content** from a centralized dashboard.

The platform combines AI content generation, AI image generation, cloud media storage, social account management, and automated post scheduling into a single application.

---

## ✨ Features

- 🤖 **AI Content Generation** using Google Gemini
- 🖼️ **AI Image Generation** using Leonardo AI
- 📅 **Post Scheduling** with automated background jobs
- 📱 **Social Media Account Management**
- 🚀 **Automated Social Media Publishing** using Zernio API
- 🔐 **JWT-based Authentication**
- ☁️ **Cloud Media Storage** using Cloudinary
- 📊 **Dashboard** for managing posts, accounts, and activities
- 📝 **Post Management** for creating and tracking content
- 📋 **Activity Logging**
- 🎨 Responsive UI built with React and Tailwind CSS

---

## 🛠️ Tech Stack

### Frontend
- React.js
- TypeScript
- Vite
- Tailwind CSS
- React Router
- Axios
- Lucide React
- React Hot Toast

### Backend
- Node.js
- Express.js
- TypeScript
- MongoDB
- Mongoose
- JWT
- bcrypt
- Multer
- Node-Cron

### APIs & Services
- **Google Gemini API** – AI content generation
- **Leonardo AI** – AI image generation
- **Cloudinary** – image/media storage
- **Zernio API** – social media publishing and account integration

---

## 🖥️ Application Screenshots

### 1. Dashboard

The dashboard provides an overview of scheduled posts, published posts, connected social accounts, and recent activity.

![Dashboard](screenshots/dashboard.png)

---

### 2. Social Media Accounts

Users can connect and manage their social media accounts from one place.

![Social Media Accounts](screenshots/social-accounts.png)

---

### 3. Post Scheduler

Users can select social platforms, write content, upload media, and schedule posts for a specific date and time.

![Post Scheduler](screenshots/post-scheduler.png)

---

### 4. AI Composer

The AI Composer generates social media content based on the user's idea and selected writing style. It can also generate AI images.

![AI Composer](screenshots/ai-composer.png)

---

### 5. MongoDB Database

The application uses MongoDB for storing application data such as users, posts, connected accounts, and activities.

![MongoDB Database](screenshots/mongodb-database.png)

> **Security note:** The screenshot is included for project documentation only. Never expose your MongoDB credentials, connection strings, or API keys in the repository.

---

## 🔄 How It Works

```text
User
  │
  ▼
React Dashboard
  │
  ├── Generate Content ──► Gemini API
  │
  ├── Generate Image ────► Leonardo AI
  │                           │
  │                           ▼
  │                       Cloudinary
  │
  ├── Schedule Post ─────► Node-Cron
  │                           │
  │                           ▼
  │                       Zernio API
  │                           │
  │                           ▼
  │                    Social Platforms
  │
  ▼
Node.js / Express API
  │
  ▼
MongoDB
```

---

## 📌 Main Modules

### 🤖 AI Composer
Allows users to enter an idea and generate social media content using AI. Different content styles such as Professional, Creative, Funny, Minimalist, and Excited can be selected.

### 🖼️ AI Image Generation
Generates visual content from prompts using an AI image-generation service and stores media using Cloudinary.

### 📅 Scheduler
Users can choose a platform, write content, attach media, and select a date/time. Scheduled jobs are handled by the backend.

### 📱 Social Accounts
Provides a centralized interface for managing connected social media accounts such as Instagram and LinkedIn.

### 📊 Dashboard
Displays:
- Scheduled posts
- Published posts
- Connected accounts
- Recent activity

### 🔐 Authentication
The application uses JWT-based authentication, password hashing, and protected backend routes.

---

## 🏗️ Project Structure

```text
social-scheduler/
│
├── client/
│   ├── public/
│   └── src/
│       ├── api/
│       ├── assets/
│       ├── components/
│       ├── context/
│       └── pages/
│           ├── Accounts.tsx
│           ├── AIComposer.tsx
│           ├── Dashboard.tsx
│           ├── Home.tsx
│           ├── Login.tsx
│           └── Scheduler.tsx
│
├── server/
│   ├── config/
│   ├── controllers/
│   ├── middlewares/
│   ├── models/
│   ├── routes/
│   ├── services/
│   └── server.ts
│
├── screenshots/
│   ├── dashboard.png
│   ├── social-accounts.png
│   ├── post-scheduler.png
│   ├── ai-composer.png
│   └── mongodb-database.png
│
├── .gitignore
└── README.md
```

---

## ⚙️ Installation & Setup

### Prerequisites

- Node.js
- npm
- MongoDB
- Git

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/social-scheduler.git
cd social-scheduler
```

### 2. Install Frontend Dependencies

```bash
cd client
npm install
```

### 3. Install Backend Dependencies

Open another terminal:

```bash
cd server
npm install
```

---

## 🔑 Environment Variables

Create a `.env` file inside the `server` directory.

```env
PORT=4000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
GEMINI_API_KEY=your_gemini_api_key
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
ZERNIO_API_KEY=your_zernio_api_key
```

If the frontend requires a backend URL, create:

```text
client/.env
```

and configure the required frontend environment variable.

> ⚠️ **Never commit `.env` files, API keys, passwords, or MongoDB connection strings to GitHub.**

---

## ▶️ Run the Project

### Start Backend

```bash
cd server
npm run server
```

### Start Frontend

Open another terminal:

```bash
cd client
npm run dev
```

Then open the local URL displayed by Vite.

---

## 🧪 Production Build

### Frontend

```bash
cd client
npm run build
```

### Backend

```bash
cd server
npm run build
```

---

## 🔐 Security

The application includes:

- JWT authentication
- Password hashing using bcrypt
- Protected API routes
- Environment variables for sensitive credentials
- CORS configuration
- Server-side third-party API integration

---

## 🚀 Future Improvements

- Add analytics for post performance
- Support additional social media platforms
- Add a visual content calendar
- Add hashtag recommendations
- Add AI-based posting-time recommendations
- Add engagement analytics
- Add role-based access control
- Add Docker support
- Add CI/CD deployment

---

## 🎯 Learning Outcomes

This project demonstrates practical experience with:

- Full-stack web development
- React and TypeScript
- REST API development
- Authentication and authorization
- MongoDB and Mongoose
- Third-party API integration
- AI API integration
- Cloud media storage
- Background job scheduling
- Social media automation
- Responsive UI development

---

## 👨‍💻 Author

**Anurag Trivedi**

B.Tech Computer Science & Engineering

---

## ⭐ Acknowledgements

This project uses technologies and services including React, TypeScript, Node.js, Express.js, MongoDB, Google Gemini, Leonardo AI, Cloudinary, and Zernio.
