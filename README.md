# 🚗 Rental Car Management System

A **Rental Car Management System** developed using **Node.js**, **Express.js**, and **MongoDB**.  
This application streamlines the process of managing car rentals by enabling users to browse and book vehicles, while administrators can manage cars, users, and rental transactions efficiently.

---

## 📖 Overview

The system provides a RESTful backend for a car rental platform.  
It supports secure authentication, role-based access (user and admin), booking management, and car availability tracking.

---

## ✨ Features

### 👤 User Features
- User registration and authentication (JWT-based)
- Browse available cars
- Search and filter cars by type, price, and availability
- Book cars for a selected time period
- View personal booking history

### 🛠 Administrator Features
- Add, update, and delete car records
- Manage registered users
- View all bookings
- Update booking status (active, completed, canceled)

---

## 🧰 Tech Stack

- **Backend:** Node.js, Express.js  
- **Database:** MongoDB with Mongoose  
- **Authentication:** JSON Web Tokens (JWT)  
- **API Architecture:** RESTful APIs  
- **Configuration:** dotenv for environment variables  

---

## 📂 Project Structure

```bash
rental-car-management-system/
│
├── controllers/        # Business logic
├── models/             # Mongoose schemas
├── routes/             # API route definitions
├── middleware/         # Authentication & authorization logic
├── config/             # Database and app configuration
├── utils/              # Utility and helper functions
│
├── .env                # Environment variables
├── server.js           # Application entry point
├── package.json
└── README.md
```
## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/rental-car-management-system.git
cd rental-car-management-system
```
### 2️⃣ Install Dependencies
```bash
npm install
```
### 3️⃣ Configure Environment Variables
Create a .env file in the root directory and add the following:
```bash
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
```
### 4️⃣ Run the Application
```bash
npm start
```
The server will start on the port defined in your .env file.

---

## ⚙️ Installation & Setup
### 🔐 Authentication
```http
POST /api/auth/register   # Register a new user
POST /api/auth/login      # Authenticate user and return JWT
```
### 🚘 Cars
```http
GET    /api/cars           # Get all available cars
POST   /api/cars           # Add a new car (Admin only)
PUT    /api/cars/:id       # Update car details (Admin only)
DELETE /api/cars/:id       # Delete a car (Admin only)
```
### 📅 Bookings
```http
POST /api/bookings        # Create a new booking
GET  /api/bookings/user   # View logged-in user’s bookings
GET  /api/bookings        # View all bookings (Admin only)
```
### 🧪 Testing
```text
API endpoints can be tested using:
- Postman
- Thunder Client
- Insomnia
```
### 📄 License
```text
This project is licensed under the MIT License.
You are free to use, modify, and distribute this project.
```
