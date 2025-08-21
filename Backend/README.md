# 🚀 Ride Booking App - Backend API Documentation

This document provides an overview of the backend APIs for the **Ride Booking App**.  
The system supports **user authentication**, **captain registration**, **ride booking**, and **ride management**.

---

## 🔑 Authentication & User APIs

### 1. Register User
**POST** `/users/register`  
Creates a new passenger account and returns a JWT for authentication.

**Request Body**
```json
{
  "email": "user@example.com",
  "password": "securepassword",
  "name": "John Doe"
}
```

**Response**
```json
{
  "message": "User registered successfully",
  "token": "jwt-token"
}
```

---

### 2. Login User
**POST** `/users/login`  
Authenticates a registered user and issues a JWT.

**Request Body**
```json
{
  "email": "user@example.com",
  "password": "securepassword"
}
```

**Response**
```json
{
  "message": "Login successful",
  "token": "jwt-token"
}
```

---

## 👨‍✈️ Captain APIs

### 3. Register Captain
**POST** `/captains/register`  
Registers a new captain (driver) and returns a JWT.

**Request Body**
```json
{
  "email": "captain@example.com",
  "password": "securepassword",
  "name": "Jane Smith",
  "vehicle": {
    "plate": "AB-1234",
    "model": "Toyota Prius"
  }
}
```

**Response**
```json
{
  "message": "Captain registered successfully",
  "token": "jwt-token"
}
```

---

### 4. Login Captain
**POST** `/captains/login`  
Authenticates a captain and issues a JWT.

**Request Body**
```json
{
  "email": "captain@example.com",
  "password": "securepassword"
}
```

**Response**
```json
{
  "message": "Login successful",
  "token": "jwt-token"
}
```

---

## 🚖 Ride APIs

### 5. Create Ride
**POST** `/rides/create`  
Creates a new ride request.

**Request Body**
```json
{
  "pickup": "Downtown Station",
  "destination": "Airport",
  "userId": "user-id"
}
```

**Response**
```json
{
  "message": "Ride created successfully",
  "rideId": "ride-id"
}
```

---

### 6. Accept Ride
**POST** `/rides/accept`  
Allows a captain to accept a ride request.

**Request Body**
```json
{
  "rideId": "ride-id",
  "captainId": "captain-id"
}
```

**Response**
```json
{
  "message": "Ride accepted successfully",
  "rideId": "ride-id"
}
```

---

### 7. Complete Ride
**POST** `/rides/complete`  
Marks a ride as completed by the captain.

**Request Body**
```json
{
  "rideId": "ride-id"
}
```

**Response**
```json
{
  "message": "Ride completed successfully",
  "rideId": "ride-id"
}
```

---

## 📌 Notes
- All APIs are **JWT-secured**.  
- The system enforces **role-based access** for **Passengers** and **Captains**.  
- Planned features include **real-time ride tracking (Socket.io)** and **payment gateway integration**.  
