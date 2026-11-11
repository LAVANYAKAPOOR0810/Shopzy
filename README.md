# Shopzy — E-Commerce Web Application

Shopzy is a full-stack e-commerce platform built using the MERN stack (MongoDB, Express.js, React, Node.js). The application provides an intuitive user interface for browsing products, managing shopping carts, and placing orders, supported by a secure RESTful API backend.

## 🚀 Features

- **User Authentication & Authorization**: Secure sign-up, login, and protected routes using JSON Web Tokens (JWT).
- **Product Catalog Management**: Browse, search, and filter products efficiently with dynamic server-side data fetching.
- **Shopping Cart & Checkout**: Interactive client-side shopping cart with real-time state updates and item management.
- **Responsive UI**: Component-driven layout built with React and styled using Tailwind CSS for cross-device compatibility.
- **RESTful API Backend**: Modular backend design following controller-route architecture for clean data operations.

---

## 🛠️ Tech Stack

- **Frontend**: React.js, Tailwind CSS, JavaScript (ES6+), Vite
- **Backend**: Node.js, Express.js
- **Database**: MongoDB (Mongoose ODM)
- **Authentication**: JSON Web Tokens (JWT), Bcrypt.js
- **API Testing & Tools**: Postman, Git

---

## 📂 Project Structure

```text
Shopzy/
├── backend/
│   ├── config/          # Database connection configuration
│   ├── controllers/     # Route request handlers
│   ├── middleware/      # Auth and error-handling middleware
│   ├── models/          # MongoDB schemas (User, Product, Order)
│   ├── routes/          # Express route definitions
│   └── server.js        # Server entry point
└── frontend/
    ├── public/          # Static assets
    ├── src/
    │   ├── components/  # Reusable UI components
    │   ├── context/     # React state management / context providers
    │   ├── pages/       # Page views (Home, Cart, Checkout, Auth)
    │   └── App.jsx      # Main application router
    └── package.json
```



⚙️ Installation and Setup
Prerequisites<br>
Node.js (v16.x or higher)<br>
MongoDB instance (Local or MongoDB Atlas)<br>
Git<br>
1. Clone the Repository

git clone [https://github.com/LAVANYAKAPOOR0810/Shopzy.git](https://github.com/LAVANYAKAPOOR0810/Shopzy.git)<br>
cd Shopzy

2. Backend Setup

cd backend<br>
npm install<br>
Create a .env file in the backend directory and add your environment variables:<br>
Code snippet<br>
PORT=5000<br>
MONGO_URI=your_mongodb_connection_string<br>
JWT_SECRET=your_jwt_secret_key<br>
Start the backend server:<br>
npm start

3. Frontend Setup

cd ../frontend<br>
npm install<br>
npm run dev<br>

## 🔑 Key API Endpoints

| Method | Endpoint | Description | Access |
| :--- | :--- | :--- | :--- |
| `POST` | `/api/auth/register` | Register a new user | Public |
| `POST` | `/api/auth/login` | User authentication & token issuance | Public |
| `GET` | `/api/products` | Fetch all products | Public |
| `GET` | `/api/products/:id` | Fetch product details by ID | Public |
| `POST` | `/api/cart` | Add item to user shopping cart | Protected |
| `POST` | `/api/orders` | Create a new order | Protected |
