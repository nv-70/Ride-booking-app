# 🚖 Ride Booking App (Uber Clone) - MERN Stack

A **complete ride-booking application** (similar to Uber) built using the **MERN stack**:  
**MongoDB, Express.js, React.js, Node.js**.  

This project demonstrates how to build a **production-grade full-stack app** with authentication, Google Maps integration, ride booking system, and real-time features.  

It’s an ideal project for understanding **end-to-end web application development** and showcases clean architecture, modular code, and industry-standard practices.  

---

## ✨ Features

### 👤 User
- Register & Login with authentication  
- Search locations via Google Maps  
- Request and book rides  
- View ride details, distance, and estimated time  
- Logout functionality  

### 🚗 Captain
- Register & Login with authentication  
- Accept and manage ride requests  
- Dedicated dashboard with ride history  
- Google Maps integration for live location  

### 🌍 Common
- JWT Authentication & Middleware  
- Separate dashboards for **Users** and **Captains**  
- Responsive, modern UI (React + Tailwind)  
- REST APIs with Node.js & Express  
- MongoDB for database storage  

---

## 🛠️ Tech Stack

- **Frontend:** React.js, Tailwind CSS  
- **Backend:** Node.js, Express.js  
- **Database:** MongoDB  
- **APIs & Libraries:** Google Maps API, JWT Authentication  
- **Tools:** Postman (API Testing), Git & GitHub  

---

## 📂 Project Structure

Ride-booking-app/
│── backend/ # Node.js + Express (API & Authentication)
│ │── routes/ # API routes (User, Captain, Ride)
│ │── models/ # MongoDB models
│ │── controllers/# Business logic
│ │── server.js # Entry point
│
│── frontend/ # React.js (User & Captain UI)
│ │── src/
│ │ ├── components/
│ │ ├── pages/
│ │ ├── App.js
│ │ └── index.js
│
│── README.md # Documentation
│── .gitignore