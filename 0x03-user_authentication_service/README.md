# 0x03-user_authentication_service

## Table of Contents

1. [Introduction](#introduction)
2. [Project Structure](#project-structure)
3. [Getting Started](#getting-started)
4. [Usage](#usage)
5. [Endpoints](#endpoints)
6. [Environment Variables](#environment-variables)
7. [Testing](#testing)
8. [License](#license)

## Introduction

The `0x03-user_authentication_service` project focuses on creating a user authentication service. This service includes user registration, login, session management, password reset, and more. It is designed to help you understand and implement common authentication mechanisms used in web applications.

## Project Structure

The project directory contains the following files and folders:

```
0x03-user_authentication_service/
├── app/
│   ├── __init__.py
│   ├── auth/
│   │   ├── __init__.py
│   │   ├── auth.py
│   │   ├── session.py
│   ├── models/
│   │   ├── __init__.py
│   │   ├── user.py
│   ├── routes/
│   │   ├── __init__.py
│   │   ├── auth.py
│   │   ├── users.py
│   ├── utils/
│   │   ├── __init__.py
│   │   ├── email.py
│   │   ├── hashing.py
│   │   ├── token.py
├── migrations/
│   ├── versions/
│   │   ├── <migration_files>.py
│   ├── __init__.py
│   ├── env.py
│   ├── script.py.mako
├── tests/
│   ├── __init__.py
│   ├── test_auth.py
│   ├── test_models.py
│   ├── test_routes.py
│   ├── test_utils.py
├── .env
├── .gitignore
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
├── run.py
└── README.md
```

## Getting Started

### Prerequisites

- Python 3.8 or higher
- pip (Python package installer)
- Docker (optional, for containerization)

### Installation

1. Clone the repository:

```bash
git clone https://github.com/your_username/0x03-user_authentication_service.git
```

2. Navigate to the project directory:

```bash
cd 0x03-user_authentication_service
```

3. Install the required packages:

```bash
pip install -r requirements.txt
```

4. Set up the environment variables by creating a `.env` file based on the `.env.example` provided.

5. Apply database migrations:

```bash
flask db upgrade
```

### Using Docker (optional)

1. Build the Docker image:

```bash
docker-compose build
```

2. Run the Docker container:

```bash
docker-compose up
```

## Usage

To run the application, execute the following command:

```bash
python run.py
```

The server will start and listen on `http://127.0.0.1:5000`.

## Endpoints

### Authentication Endpoints

- **POST /auth/register**: Registers a new user.
- **POST /auth/login**: Logs in a user and creates a session.
- **POST /auth/logout**: Logs out the current user and destroys the session.
- **POST /auth/reset_password_request**: Requests a password reset.
- **POST /auth/reset_password**: Resets the user's password.

### User Endpoints

- **GET /users**: Retrieves a list of all users.
- **GET /users/<user_id>**: Retrieves a specific user by ID.
- **PUT /users/<user_id>**: Updates a specific user by ID.
- **DELETE /users/<user_id>**: Deletes a specific user by ID.

## Environment Variables

The project uses the following environment variables for configuration:

- `SECRET_KEY`: A secret key used for session management and encryption.
- `DATABASE_URL`: The URL of the database used for storing user data.
- `MAIL_SERVER`: The mail server used for sending emails.
- `MAIL_PORT`: The port used by the mail server.
- `MAIL_USERNAME`: The username for the mail server.
- `MAIL_PASSWORD`: The password for the mail server.
- `MAIL_DEFAULT_SENDER`: The default sender email address.

## Testing

To run the tests, execute the following command:

```bash
python -m unittest discover tests/
```

This will run all tests in the `tests` directory.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
