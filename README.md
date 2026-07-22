# Shop-Circuit

Shop-Circuit is a full-stack MERN (MongoDB, Express, React, Node.js) application designed to facilitate selling and renting products. It features real-time chat, user authentication, profile management, an admin dashboard, and seamless product listings.

## 🚀 Features

- **User Authentication**: Secure signup, login, and password reset functionalities using JWT and bcryptjs.
- **Product Management**: Users can post products for selling or renting.
- **Real-time Chat**: Integrated messaging system using Socket.io for buyers and sellers to communicate seamlessly.
- **Admin Dashboard**: Dedicated portal for administrators to manage products, users, and contact queries.
- **Profile Settings**: Users can manage their personal information and account settings.
- **Cloud Image Storage**: Secure image uploads and management using Cloudinary.
- **Responsive UI**: A modern, responsive frontend built with React, Vite, and Tailwind CSS.

## 🛠️ Tech Stack

### Frontend
- **Framework**: React 19 (via Vite)
- **Styling**: Tailwind CSS
- **Routing**: React Router DOM
- **State Management**: React Context (Custom Hooks)
- **Real-time**: Socket.io-client
- **Icons & Animations**: FontAwesome, Lucide React, Framer Motion, Lottie React
- **HTTP Client**: Axios

### Backend
- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: MongoDB (Mongoose)
- **Real-time**: Socket.io
- **Authentication**: JSON Web Tokens (JWT)
- **File Uploads**: Cloudinary & Multer
- **Emails**: Nodemailer

## 📦 Prerequisites

Before running this project, ensure you have the following installed:
- [Node.js](https://nodejs.org/) (v16 or higher)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)
- [MongoDB](https://www.mongodb.com/) (Local or Atlas)
- A [Cloudinary](https://cloudinary.com/) account for image uploads

## ⚙️ Environment Variables

Create a `config.env` file in the `backend` directory and add the following variables:

```env
NODE_ENV=development
PORT=3000

# Database
DATABASE=your_mongodb_connection_string
DATABASE_USERNAME=your_db_username
DATABASE_PASSWORD=your_db_password

# JWT Authentication
JWT_SECRET=your_jwt_secret_key
JWT_EXPIRES_IN=7776000
JWT_COOKIE_EXPIRES_IN=90

# Cloudinary
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# Client URL (for CORS)
CLIENT_URL=http://localhost:5173
```

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/shop-circuit.git
cd shop-circuit
```

### 2. Backend Setup
```bash
cd backend
npm install
# Start the backend server
node server.js
```

### 3. Frontend Setup
Open a new terminal window:
```bash
cd frontend
npm install
# Start the development server
npm run dev
```
The frontend will run at `http://localhost:5173` and proxy API requests to the backend server.

## 📂 Project Structure

```text
shop-circuit/
├── backend/
│   ├── controllers/      # Route logic
│   ├── middlewares/      # Custom express middlewares
│   ├── models/           # Mongoose schemas (User, Product, Chat, etc.)
│   ├── routes/           # Express routes
│   ├── utils/            # Helper functions and utilities
│   ├── app.js            # Express app configuration
│   ├── server.js         # Entry point for backend server
│   └── socket.js         # Socket.io configuration
│
└── frontend/
    ├── public/           # Static assets
    ├── src/
    │   ├── assets/       # Images, icons, etc.
    │   ├── components/   # Reusable UI components
    │   ├── pages/        # Application views/pages
    │   ├── store/        # Context providers for global state
    │   ├── App.jsx       # Main routing component
    │   └── main.jsx      # React entry point
    ├── vite.config.js    # Vite configuration
    └── package.json      # Frontend dependencies
```
