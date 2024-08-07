### README.md

# Task App

## Overview

Task App is a comprehensive task management application designed to help users efficiently manage their daily tasks. This project leverages modern web development technologies to provide a robust and scalable solution.

## Technologies Used

- *Node.js*: JavaScript runtime built on Chrome's V8 JavaScript engine.
- *Express.js*: Fast, unopinionated, minimalist web framework for Node.js.
- *MongoDB*: NoSQL database program, using JSON-like documents with optional schemas.
- *Mongoose*: Elegant MongoDB object modeling for Node.js.
- *JWT (JSON Web Tokens)*: For securely transmitting information between parties as a JSON object.
- *Bcrypt*: For hashing passwords.

## Project Structure

plaintext
Task-App-main/
├── .gitignore
├── package-lock.json
├── package.json
└── src/
    ├── db/
    │   └── mongoose.js
    ├── index.js
    ├── middleware/
    │   ├── auth.js
    │   └── errorHandler.js
    ├── models/
    │   ├── Task.js
    │   └── User.js
    └── routers/
        ├── taskRouter.js
        └── userRouter.js


### Directories and Files

- **src/db/mongoose.js**: Database connection setup using Mongoose.
- **src/index.js**: Main entry point for the application. Sets up the Express server and middleware.
- **src/middleware/auth.js**: Middleware for authentication using JWT.
- **src/middleware/errorHandler.js**: Middleware for handling errors globally.
- **src/models/Task.js**: Task model schema definition.
- **src/models/User.js**: User model schema definition.
- **src/routers/taskRouter.js**: Router for task-related API endpoints.
- **src/routers/userRouter.js**: Router for user-related API endpoints.

## Getting Started

### Prerequisites

- Node.js
- MongoDB

### Installation

1. Clone the repository:
   sh
   git clone <repository-url>
   
2. Navigate to the project directory:
   sh
   cd Task-App-main
   
3. Install dependencies:
   sh
   npm install
   

### Running the Application

1. Start the MongoDB server if it is not already running.
2. Start the application:
   sh
   npm start
   
3. The server will be running at http://localhost:3000.

### API Endpoints

#### User Endpoints

- *POST /users*: Create a new user.
- *POST /users/login*: Login a user.
- *POST /users/logout*: Logout the current user.
- *POST /users/logoutAll*: Logout the current user from all devices.
- *GET /users/me*: Get the profile of the logged-in user.
- *PATCH /users/me*: Update the profile of the logged-in user.
- *DELETE /users/me*: Delete the logged-in user's profile.

#### Task Endpoints

- *POST /tasks*: Create a new task.
- *GET /tasks*: Get all tasks of the logged-in user.
- *GET /tasks/:id*: Get a task by its ID.
- *PATCH /tasks/:id*: Update a task by its ID.
- *DELETE /tasks/:id*: Delete a task by its ID.

## Authentication

The application uses JWT for authentication. Tokens are issued when a user logs in and are required for accessing protected routes.

## Error Handling

The application uses centralized error handling through the errorHandler.js middleware. This ensures consistent and informative error responses across the application.

## Contribution

Contributions are welcome! Please fork the repository and submit a pull request for review.

## License

This project is licensed under the MIT License.

---

This detailed README.md provides an overview of the project, technologies used, installation instructions, API endpoints, and other relevant information to help developers understand and contribute to the project.
