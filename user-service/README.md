# User Service

The User Service is a microservice within the social media application responsible for managing user-related operations, including user registration, authentication, and profile management.

## Table of Contents

1. [Overview](#overview)
2. [Endpoints](#endpoints)
3. [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
4. [Usage](#usage)
    - [User Registration](#user-registration)
    - [User Authentication](#user-authentication)
    - [Get User Profile](#get-user-profile)
    - [Update User Profile](#update-user-profile)
5. [License](#license)

## Overview

The User Service is a critical component of the social media application, providing functionality for user-related operations. It communicates with other microservices to ensure a seamless user experience.

## Endpoints

The User Service exposes the following RESTful endpoints:

- **POST /api/users:** Create a new user (User Registration).
- **POST /api/users/login:** Authenticate a user and generate an access token.
- **GET /api/users/{userID}:** Retrieve user profile information.
- **PUT /api/users/{userID}:** Update user profile information.

## Getting Started

### Prerequisites

Before running the User Service, ensure you have the following dependencies installed:

- Go (version ^1.20)
- Postgres Database

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/0xivanov/decentralized-social-media-project.git
    cd decentralized-social-media-project/user-service
    ```

2. Install dependencies:

    ```bash
    go mod download
    ```

3. Set up the Postgres Database:

    - Provide necessary configuration in the `.env` file based on the provided `.env.example`.

4. Configure the User Service:

    - Create a `.env` file based on the provided `.env.example` and configure the necessary environment variables.

5. Run the User Service:

    ```bash
    go run main.go
    ```

## Usage

### User Registration

**Endpoint:** `POST /api/users`

**Request:**
```json
{
    "username": "john_doe",
    "email": "john.doe@example.com",
    "password": "password123"
}
```

**Response:**
```json
{
    "userID": "12345",
    "username": "john_doe",
    "email": "john.doe@example.com"
}
```

### User Authentication

**Endpoint:** `POST /api/users/login`

**Request:**
```json
{
    "email": "john.doe@example.com",
    "password": "password123"
}
```

**Response:**
```json
{
    "userID": "12345",
    "username": "john_doe",
    "token": "your_access_token"
}
```

### Get User Profile

**Endpoint:** `GET /api/users/{userID}`

**Response:**
```json
{
    "userID": "12345",
    "username": "john_doe",
    "email": "john.doe@example.com",
    "profilePicture": "https://example.com/profile-picture.jpg"
}
```

### Update User Profile

**Endpoint:** `PUT /api/users/{userID}`

**Request:**
```json
{
    "username": "john_doe_updated",
    "profilePicture": "https://example.com/new-profile-picture.jpg"
}
```

**Response:**
```json
{
    "userID": "12345",
    "username": "john_doe_updated",
    "email": "john.doe@example.com",
    "profilePicture": "https://example.com/new-profile-picture.jpg"
}
```

## License

This project is licensed under the [MIT License](LICENSE).