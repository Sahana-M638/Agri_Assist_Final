# 🌱 AgriAssist AI

AgriAssist AI is a web-based agriculture assistance application designed to provide farmers with a simple platform for managing farm information and accessing different agricultural assistance modules.

The application provides farmer registration and login, farm management, profile management, crop disease and pest detection interfaces, fertilizer information, weather information, and an administrative interface.
The project uses a Node.js and Express.js backend with MongoDB for persistent storage. Mongoose is used to communicate with MongoDB.

## 📌 Project Overview

Agriculture requires farmers to manage different types of information such as farm details, crops, locations, and agricultural guidance.

AgriAssist AI provides a centralized web interface where farmers can:

- Register and log in
- Manage their profile
- Add farm details
- View their farms
- Edit farm information
- Delete farm information
- Access crop disease detection
- Access pest detection
- Access fertilizer information
- Access weather information

The backend provides REST APIs for authentication and farm management, while MongoDB is used for storing user and farm data.

## 🎯 Objectives

The main objectives of AgriAssist AI are:

- To provide a user-friendly agriculture assistance interface.
- To allow farmers to manage their farm information digitally.
- To provide persistent storage for farmer and farm data.
- To implement secure password storage using password hashing.
- To provide REST APIs for farm management.
- To implement CRUD operations using MongoDB.
- To organize different agricultural assistance modules in a single platform.

## ✨ Features

### 👨‍🌾 Farmer Registration

Farmers can create an account by providing:

- Full name
- Email
- Username
- Password

Passwords are hashed before being stored in the database.

### 🔐 Farmer Login

Registered farmers can log in using their username and password.

After successful login, the application stores the required user information in browser local storage for the current session.

### 🚜 Farm Management

Farmers can manage their farm information through:

- Add Farm
- View Farms
- Edit Farm
- Delete Farm

Farm information includes:

- Farm name
- Crop
- Area
- Location
- Description
- Status

### 🗄️ MongoDB Database

MongoDB is used as the persistent database.

Mongoose provides the connection between the Node.js application and MongoDB.

### 🔄 CRUD Operations

The application implements:

 Create Farm - POST - `/api/farms` 
 Read Farms - GET - `/api/farms?userId=USER_ID` 
 Update Farm - PUT - `/api/farms/:id` 
 Delete Farm - DELETE - `/api/farms/:id?userId=USER_ID` 

### 🌿 Agricultural Modules

The application contains interfaces for:

- Crop Disease Detection
- Pest Detection
- Fertilizer Information
- Weather Information
- Farmer Profile
- Dashboard

### 👨‍💼 Admin Interface

An administrative interface is included for the application.

## 🛠️ Technologies Used

### Frontend

- HTML5
- CSS3
- JavaScript
- AngularJS

### Backend

- Node.js
- Express.js

### Database

- MongoDB
- Mongoose

### Authentication & Security

- bcryptjs
- Browser local storage for session-related user information

### Development Tools

- Visual Studio Code
- Git
- GitHub
- MongoDB Atlas / MongoDB

## 🏗️ System Architecture

                ┌──────────────────────┐
                │      Frontend        │
                │ HTML / CSS / JS      │
                │     AngularJS        │
                └──────────┬───────────┘
                           │
                           │ HTTP Requests
                           ▼
                ┌──────────────────────┐
                │    Node.js Server    │
                │      Express.js      │
                └──────────┬───────────┘
                           │
                           │ Mongoose
                           ▼
                ┌──────────────────────┐
                │       MongoDB        │
                │                      │
                │ Users + Farms        │
                └──────────────────────┘
