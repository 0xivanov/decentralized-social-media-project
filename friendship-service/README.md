# Friendship Service

The Friendship Service is a microservice within the social media application responsible for managing user connections, friendships, and follower/following relationships. It facilitates functionalities such as sending and accepting friend requests.

## Table of Contents

1. [Overview](#overview)
2. [Endpoints](#endpoints)
3. [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
4. [Usage](#usage)
    - [Send Friend Request](#send-friend-request)
    - [Accept Friend Request](#accept-friend-request)
    - [Get User Friends](#get-user-friends)
5. [License](#license)

## Overview

The Friendship Service plays a crucial role in the social media application, allowing users to connect with each other, send and accept friend requests, and view their list of friends.

## Endpoints

The Friendship Service exposes the following RESTful endpoints:

- **POST /api/friendships/send-request:** Send a friend request.
- **POST /api/friendships/accept-request:** Accept a friend request.
- **GET /api/friendships/{userID}/friends:** Get the list of friends for a user.

## Getting Started

### Prerequisites

Before running the Friendship Service, ensure you have the following dependencies installed:

- Go (version ^1.20)
- Oracle Database

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/0xivanov/decentralized-social-media-project.git
    cd decentralized-social-media-project/friendship-service
    ```

2. Install dependencies:

    ```bash
    go mod download
    ```

3. Set up the Oracle Database:

    - Provide necessary configuration in the `.env` file based on the provided `.env.example`.

4. Run the Friendship Service:

    ```bash
    go run main.go
    ```

## Usage

### Send Friend Request

**Endpoint:** `POST /api/friendships/send-request`

**Request:**
```json
{
    "sender_id": "123",
    "receiver_id": "456"
}
```

**Response:**
```json
{
    "request_id": "789",
    "status": "pending"
}
```

### Accept Friend Request

**Endpoint:** `POST /api/friendships/accept-request`

**Request:**
```json
{
    "request_id": "789"
}
```

**Response:**
```json
{
    "status": "accepted"
}
```

### Get User Friends

**Endpoint:** `GET /api/friendships/{userID}/friends`

**Response:**
```json
{
    "friends": [
        {
            "user_id": "456",
            "username": "friend1"
        },
        {
            "user_id": "789",
            "username": "friend2"
        }
    ]
}
```

## License

This project is licensed under the [MIT License](LICENSE).