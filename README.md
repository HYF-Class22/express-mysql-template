# Projects Template

These projects are designed for students to build a web application using Express and MySQL2. The project will involve creating routes and controllers for users and implementing user authentication using cookies, and utilizing middleware utility functions.

## Introduction

These projects aim to provide a platform where users can register, log in, and manage their favorite recipes or flights. The backend is built with Express and MySQL2, with authentication handled via cookies.

## Description

- You need to build different APIs using express ex: Recipes.
- you need to able to login existing user.
- You need to be able to add a new user.
- non-authenticate user can only see all recipes, BUT he is not able to delete, update or add Recipe.
- You need to be able to add, get all, getById, update and delete Recipes.

## Project Structure

```md
Project/
├── controllers/
│   ├── userController.js
│   ├── recipeController.js <!-- depending on the project -->
├── middleware/
│   ├── verifyToken.js
├── routes/
│   ├── userRoutes.js
│   ├── recipeRoutes.js <!-- depending on the project -->
├── utils/
│   ├── hashPassword.js
│   ├── matchPasswords.js
│   ├── validateEmail.js
│   ├── validatePasswords.js
├── .env
├── index.js
├── package.json
└── README.md
```

## Setup Instructions

1. **Use this Template Repo:**
   [Use this template to create your repo](https://github.com/samirm00/express-mysql-template)

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Configure environment variables:**

   - Create a `.env` file in the root directory and add the following:

     ```env
     DB_HOST=your_database_host
     DB_USER=your_database_user
     DB_PASSWORD=your_database_password
     DB_NAME=your_database_name
     SECRET_KEY=your_secret_key
     ```

4. **Run the application:**

   ```bash
   npm run dev
   ```

## Environment Variables

Ensure you have the following environment variables set up in your `.env` file:

```env
DB_HOST=your_database_host
DB_USER=your_database_user
DB_PASSWORD=your_database_password
DB_NAME=your_database_name
SECRET_KEY=your_secret_key
```

## Routes

### User Routes

- **POST /register**
  - Registers a new user.

- **POST /login**
  - Logs in an existing user.

### Recipe Routes  <!-- Depending on the project-->

- **GET /recipes**
  - Retrieves all recipes.

- **POST /recipes**
  - Creates a new recipe (authenticated users only).

- **GET /recipes/:id**
  - Retrieves a single recipe by ID.

- **PUT /recipes/:id**
  - Updates a recipe by ID (authenticated users only).

- **DELETE /recipes/:id**
  - Deletes a recipe by ID (authenticated users only).

## Controllers

### User Controller (`controllers/userController.js`)

- Handles user registration, login, and other user-related actions.

### Recipe Controller (`controllers/recipeController.js`) <!-- Depending on the project-->

- Manages CRUD operations for recipes.

## Middleware Functions

### Verify Token (`middleware/verifyToken.js`)

- A middleware function to verify user tokens for authentication purposes.

## Utility Functions

### hashPassword.js (`utils/hashPassword.js`)

- Hashes user passwords for secure storage.

### matchPasswords.js (`utils/matchPasswords.js`)

- Compares plain and hashed passwords for login verification.

### validateEmail.js (`utils/validateEmail.js`)

- Validates email format.

### validatePasswords.js (`utils/validatePasswords.js`)

- Ensures passwords meet required complexity criteria.

## Authentication

- Users must register and log in to perform certain actions.
- Authentication is handled using cookies.
- The `verifyToken` middleware function ensures that only authenticated users can access certain routes.

## Resources

- [Express Documentation](https://expressjs.com/)
- [MySQL2 Documentation](https://www.npmjs.com/package/mysql2)
- [Node.js Documentation](https://nodejs.org/en/docs/)
- [Cookie Parser Middleware](https://www.npmjs.com/package/cookie-parser)
