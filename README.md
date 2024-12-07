---

## Project Description: Role Based Access Control Online Examination System

The **Role Based Access Control Online Examination System** is a backend application designed to manage online examinations while ensuring security through authentication and role-based access control. It allows administrators, instructors, and students to perform specific actions based on their roles, ensuring a structured and efficient examination management process.

### Key Features

- **Authentication & Security**: The application uses JSON Web Tokens (JWT) for user authentication, ensuring secure access to protected resources. It also handles token expiry with proper error messaging to enhance user experience.
  
- **Role-Based Access Control (RBAC)**: Users are assigned roles (Admin, Instructor, or Student), and their actions are restricted based on permissions defined for each role:
  - **Admin**: Monitors and manages all exams.
  - **Instructor**: Creates, updates, and deletes exams.
  - **Student**: Views exams, attempts exams, and submits answers.
  
- **CRUD Operations**: Includes robust APIs for creating, reading, updating, and deleting user and exam data.

- **Scalable Design**: A clean and organized folder structure ensures scalability and maintainability of the codebase.

### Technologies Used
- **Backend**: Built with Node.js and Express.js for fast and scalable server-side development.
- **Database**: MongoDB is used to store and manage user and exam data.
- **Authentication**: JWT ensures secure user sessions with customizable token expiry.

This project showcases a functional and practical backend for handling online examination systems with proper user management and security. It is designed to be a modular, extensible, and production-ready solution.

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Folder Structure](#folder-structure)
- [Setup Instructions](#setup-instructions)
- [API Documentation](#api-documentation)

## Folder Structure

```plaintext
root-dir/
├── config/
│   └── DB.Connect.js               # Database connection
├── controllers/
│   ├── exam.controller.js          # Business logic for exam routes
│   └── user.controller.js          # Business logic for user routes
├── middlewares/
│   ├── Auth.middleware.js          # Authentication middleware (JWT verification)
│   └── Role.middleware.js          # Authorization middleware (RBAC)
├── models/
│   ├── exam.model.js               # Schema for exams
│   └── user.model.js               # Schema for users
├── routes/
│   ├── exam.routes.js              # Routes for exam-related APIs
│   └── user.routes.js              # Routes for user-related APIs
├── .env                            # Environment variables
├── .gitignore                      # Files/folders to ignore in Git
├── app.js                          # Main Express app setup
├── package.json                    # Node.js dependencies and scripts
├── package-lock.json               # Dependency lock file
└── README.md                       # Project documentation
```

---

## Setup Instructions

1. **Clone the Repository**

   ```bash
   git clone https://github.com/brijendra04/Brijendra_Pratap_VRV
   
   ```

2. **Install Dependencies**

   ```bash
   npm install
   ```

3. **Set Up Environment Variables**

   - Create a `.env` file in the root directory.
   - Add the following variables:
     ```env
     PORT=<your-port-number>
     MONGO_URL=<your-mongodb-connection-string>
     JWT_SECRET=<your-jwt-secret-key>
     JWT_EXPIRY=<yout-jwt-expiry>
     ```

4. **Start the Application**
   ```bash
   npm start
   ```

---


---
