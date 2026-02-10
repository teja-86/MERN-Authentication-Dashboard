# Dashboard & Authentication System using MERN Stack

## Introduction:
This project is an Dashboard & authentication system built using the MERN stack, which stands for MongoDB, Express, React, and Node.js. The system allows users to register, log in and log out. The frontend of the system is built using React and the backend is built using Node.js and Express. The database used is MongoDB.

## Architecture:
The frontend is the view and is responsible for displaying the user interface. The backend is the controller and is responsible for handling requests from the frontend and communicating with the database. The database is the model and is responsible for storing the user data.

## Tech Stack

### Frontend
- React.js
- Tailwind CSS
- Fetch API

### Backend
- Node.js
- Express.js
- MongoDB
- JWT Authentication
- bcrypt

## Features

- User registration and login with JWT authentication
- Protected dashboard routes
- User profile fetching
- Task CRUD operations (Create, Read, Update, Delete)
- Search and filter functionality
- Secure password hashing
- Error handling and validation

## Functionality:
The system has the following functionality:

- **Register:** Users can register by providing their email address and a password. The email address must be unique and a password must meet the password strength requirements. Once the user is registered, their information is stored in the database and they are redirected to the login page.
- **Login:** Users can log in by providing their email address and password. If the email address and password match the user's information in the database, the user is redirected to the dashboard.
- **Logout:** Users can log out by clicking on the logout button on the dashboard. Once logged out, the user is redirected to the login page.
- **Authentication:** The system uses JSON Web Tokens (JWT) for authentication. Once a user logs in, a JWT is created and stored in local storage. This JWT is then sent with every request to the backend to authenticate the user.

## Authentication Flow

1. User registers or logs in
2. Backend validates credentials
3. JWT token is generated and returned
4. Token is stored on the frontend
5. Protected APIs require token in Authorization header

## API Endpoints

### Auth
- POST /register – Register a new user
- POST /login – Login user
- POST /logout – Logout user

### Tasks
- GET /validuser – Get user details

## How to Run Locally

### Backend
1. npm install
2. npm start

## Environment Variables for backend

Create a `.env` file in root directory and add the following variables:
SECRET_KEY=your_jwt_secret_key
DB=your_mongodb_connection_string

### Frontend
1. cd client
2. npm install
3. npm start

## Scalability & Production Considerations

- Frontend can be deployed on Vercel or Netlify
- Backend can be containerized using Docker
- JWT authentication can be extended using refresh tokens
- Redis can be used for caching and rate limiting
- Database indexing can improve performance
- Modular folder structure allows easy feature expansion

## Security:
The system has the following security measures:

- **Password strength requirements:** Passwords must be at least 8 characters long and contain at least one uppercase letter, one lowercase letter, one number, and one special character.
- **Hashing and salting:** Passwords are hashed and salted before being stored in the database. This ensures that even if the database is compromised, the passwords cannot be easily decrypted.
- **JWT:** JWTs are used for authentication and are signed with a secret key. This ensures that only the server can create and verify JWTs.

## Conclusion:
This authentication system using the MERN stack provides a secure and scalable solution for user authentication and authorization. The system can be easily extended to include additional functionality such as password reset, email verification, and two-factor authentication.
