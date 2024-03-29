# FastAPI Todo App with JWT Authentication

## Overview

This repository contains a FastAPI-based Todo application with JWT (JSON Web Token) authentication. The application emphasizes security by using hashed passwords and follows best practices for user authentication.

## Features

- JWT Authentication
- Hashed Passwords
- User Registration
- User Login
- Todo CRUD Operations

## Installation

To set up the project locally, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/sulemanpervez/Todo-App-FastAPI-With-JWT.git
   cd Todo-App-FastAPI-With-JWT
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Set up environment variables:

   Create a `.env` file in the project root with the following content:

   ```env
   JWT_SECRET_KEY = "your_secret_key"
   ALGORITHM_JWT = "your_algorithm"
   DatabaseConnectionString = "your_database_connection_string"
   ```

   Replace `your_secret_key`, `your_algorithm`, and `your_database_connection_string` with your own values.
   You have the flexibility to insert any distinct value for SECERT_KEY_JWT, and for ALGORITH_JWT, you can opt for 'HS256' as per your preference.

4. Run the application:

   ```bash
   uvicorn main:app --reload
   ```

Visit [http://localhost:8000/docs](http://localhost:8000/docs) to explore the Swagger UI and test the API endpoints.

## Project Structure

- **auth.py**: Handles authentication-related tasks, including user registration, login, and token generation.
- **models.py**: Defines database models, including the User model with hashed passwords.
- **database.py**: Manages database setup, including connection and session handling.
- **main.py**: Core application logic, including CRUD operations for Todos and user authentication flow.

## Testing

This project includes comprehensive testing for each module:

- **auth.py**: Ensures secure user authentication through user creation, token generation, and authentication checks.
- **models.py**: Rigorous tests for the User model, validating data storage and retrieval.
- **database.py**: Tests for database operations, verifying the correctness of Todo model behavior.
- **main.py**: Full application flow testing, covering user authentication, Todo creation, retrieval, and modification.

## Contribution

Feel free to contribute by opening issues or submitting pull requests

## License

This project is licensed under the [MIT License](LICENSE).
