# 0x01-Basic_authentication

## Table of Contents

1. [Introduction](#introduction)
2. [Project Structure](#project-structure)
3. [Getting Started](#getting-started)
4. [Usage](#usage)
5. [Endpoints](#endpoints)
6. [Testing](#testing)
7. [License](#license)

## Introduction

The `0x01-Basic_authentication` project focuses on implementing basic authentication for a web application. Basic authentication is a method for an HTTP user agent (e.g., a web browser) to provide a username and password when making a request. This project will teach you how to implement and handle basic authentication in a backend system.

## Project Structure

The project directory contains the following files and folders:

```
0x01-Basic_authentication/
├── api/
│   ├── v1/
│   │   ├── app.py
│   │   ├── auth/
│   │   │   ├── __init__.py
│   │   │   ├── auth.py
│   │   │   ├── basic_auth.py
│   │   ├── views/
│   │   │   ├── __init__.py
│   │   │   ├── index.py
│   │   │   ├── users.py
├── models/
│   ├── __init__.py
│   ├── user.py
├── main.py
├── README.md
├── requirements.txt
└── tests/
    ├── test_auth.py
    ├── test_basic_auth.py
```

## Getting Started

### Prerequisites

- Python 3.8 or higher
- pip (Python package installer)

### Installation

1. Clone the repository:

```bash
git clone https://github.com/your_username/0x01-Basic_authentication.git
```

2. Navigate to the project directory:

```bash
cd 0x01-Basic_authentication
```

3. Install the required packages:

```bash
pip install -r requirements.txt
```

## Usage

To run the application, execute the following command:

```bash
python main.py
```

The server will start and listen on `http://127.0.0.1:5000`.

## Endpoints

### Authentication Endpoints

- **POST /auth/login**: Logs in a user using basic authentication.

### User Endpoints

- **GET /api/v1/users**: Retrieves a list of all users.
- **GET /api/v1/users/<user_id>**: Retrieves a specific user by ID.
- **POST /api/v1/users**: Creates a new user.
- **PUT /api/v1/users/<user_id>**: Updates a specific user by ID.
- **DELETE /api/v1/users/<user_id>**: Deletes a specific user by ID.

### Index Endpoint

- **GET /api/v1/status**: Returns the status of the API.

## Testing

To run the tests, execute the following command:

```bash
python -m unittest discover tests/
```

This will run all tests in the `tests` directory.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
