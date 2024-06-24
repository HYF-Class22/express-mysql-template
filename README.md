# Projects Template

These projects are designed for students to build a web application using Express and MySQL2. The project will involve creating routes and controllers for users and  implementing user authentication using cookies, and utilizing middleware utility functions.

## Introduction

These projects aim to provide a platform where users can register, log in, and manage their favorite recipes. The backend is built with Express and MySQL2, with authentication handled via cookies.

## Project Structure

```md
Project/
├── controllers/
│   ├── userController.js
│   ├── ---------------.js
├── middleware/
│   ├── verifyToken.js
├── routes/
│   ├── userRoutes.js
│   ├── ----------.js
├── utils/
│   ├── hashPassword.js
|   |── matchPasswords.js
|   |── validateEmail.js
|   |── validatePasswords.js
├── .env
├── index.js
├── package.json
└── README.md
```

## Setup Instructions

1. **Use this Template reo:**
[use this template to create your repo](https://github.com/samirm00/express-mysql-template)

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
     ```

5. **Run the application:**

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

### Other Routes depending on your project ex: recipes

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

### Recipe Controller (`controllers/recipeController.js`)

- Manages CRUD operations for recipes.

## Middleware Functions

### Verify Token (`helpers/verifyToken.js`)

- A middleware function to verify user tokens for authentication purposes.

## Utility Functions

### hashPassword.js (`utils/hashPassword.js`)

### matchPasswords.js (`utils/matchPasswords.js.`)

### validateEmail.js (`utils/validateEmail.js`)

### validatePasswords.js (`utils/validatePasswords.js`)

## Authentication

- Users must register and log in to perform certain actions.
- Authentication is handled using cookies.
- The `verifyToken` helper function ensures that only authenticated users can access certain routes.

## Resources

- [Express Documentation](https://expressjs.com/)
- [MySQL2 Documentation](https://www.npmjs.com/package/mysql2)
- [Node.js Documentation](https://nodejs.org/en/docs/)
- [Cookie Parser Middleware](https://www.npmjs.com/package/cookie-parser)
