# 💬 MERN Real-Time Chat Application

A modern, full-stack real-time messaging web application built with the **MERN** stack (MongoDB, Express, React, Node.js), powered by **Socket.io** for instant two-way communication, styled with **TailwindCSS** and **DaisyUI**, and state-managed using **Zustand**.

![Chat Application Preview](https://i.ibb.co/XxNhSRzG/Gemini-Generated-Image-edd8wledd8wledd8.png)

---

## ✨ Features

- 🔐 **Authentication & Authorization**: Secure user registration and login with bcrypt password hashing and JWT stored in HTTP-only cookies.
- ⚡ **Real-Time Messaging**: Instant bi-directional messaging with Socket.io.
- 🟢 **Online / Offline Status**: Live tracking of connected users in real time.
- 🎨 **Modern & Responsive UI**: Sleek glassmorphism-inspired dark theme powered by TailwindCSS and DaisyUI.
- 🗂️ **Global State Management**: Fast, lightweight state handling via Zustand.
- 🔔 **Instant Sound Alerts & Notifications**: Sound notifications for incoming real-time messages.
- 🛡️ **Robust Error Handling**: Comprehensive client-side and server-side validation and toast notifications.
- 📦 **Monolithic Production Build**: Client and server bundled and served from a single Express instance.

---

## 🛠️ Tech Stack

### Frontend
- **React.js (Vite)**
- **TailwindCSS & DaisyUI**
- **Socket.io Client**
- **Zustand** (Global State)
- **React Router DOM**
- **React Hot Toast** & **React Icons**

### Backend
- **Node.js** & **Express.js**
- **MongoDB** & **Mongoose**
- **Socket.io**
- **JSON Web Tokens (JWT)**
- **Bcrypt.js** & **Cookie-Parser**

---

## 🚀 Getting Started

### Prerequisites

Ensure you have the following installed:
- [Node.js](https://nodejs.org/) (v16.x or higher)
- [MongoDB](https://www.mongodb.com/) (Local instance or MongoDB Atlas cluster)
- [Git](https://git-scm.com/)

---

### Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/differentiatorX/mern-chat.git
   cd mern-chat
   ```

2. **Install root & backend dependencies:**
   ```bash
   npm install
   ```

3. **Install frontend dependencies:**
   ```bash
   cd frontend
   npm install
   cd ..
   ```

4. **Environment Variables:**
   Create a `.env` file in the root directory and configure the following:
   ```env
   PORT=5000
   MONGO_DB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   NODE_ENV=development
   ```

---

### Running the Application

#### 1. Development Mode (Concurrent Backend & Frontend)
- **Run Backend:**
  ```bash
  npm run server
  ```
- **Run Frontend (in another terminal):**
  ```bash
  cd frontend
  npm run dev
  ```
The frontend will start at `http://localhost:3000` and proxy API calls to backend at `http://localhost:5000`.

#### 2. Production Build
```bash
# Build frontend and install dependencies
npm run build

# Start production server
npm start
```
The app will be accessible at `http://localhost:5000`.

---

## 📁 Project Structure

```
mern-chat/
├── backend/
│   ├── controllers/      # Route controllers (auth, message, user)
│   ├── db/               # MongoDB connection helper
│   ├── middleware/       # JWT route protection middleware
│   ├── models/           # Mongoose schemas (User, Message, Conversation)
│   ├── routes/           # Express API endpoints
│   ├── socket/           # Socket.io server configuration & event handlers
│   ├── utils/            # JWT token generator
│   └── server.js         # Express app entry point
├── frontend/
│   ├── public/           # Static assets & sounds
│   ├── src/
│   │   ├── components/   # UI components (messages, sidebar, etc.)
│   │   ├── context/      # React contexts (AuthContext, SocketContext)
│   │   ├── hooks/        # Custom React hooks
│   │   ├── pages/        # Route pages (Home, Login, SignUp)
│   │   ├── zustand/      # Zustand store slices
│   │   ├── App.jsx       # Root React component
│   │   └── main.jsx      # Vite entry point
│   └── package.json
├── .gitignore
├── LICENSE
├── package.json
└── README.md
```

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**differentiatorX**
- GitHub: [@differentiatorX](https://github.com/differentiatorX)
