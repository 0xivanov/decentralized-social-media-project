# Social Media Project

The Social Media Project is a comprehensive social networking platform built to connect users, share content, and foster online communities. The project consists of multiple microservices, each responsible for specific functionalities.

## Table of Contents

1. [Overview](#overview)
2. [Microservices](#microservices)
    - [User Service](#user-service)
    - [Post Service](#post-service)
    - [Friendship Service](#friendship-service)
    - [Chat Service](#chat-service)
3. [Features](#features)
4. [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
5. [License](#license)

## Overview

The Social Media Project aims to provide users with a versatile and interactive platform for connecting with friends, sharing posts, and engaging in real-time conversations. The project is designed using a microservices architecture to ensure modularity, scalability, and maintainability.

## Microservices

### User Service

The User Service manages user-related operations, including user registration, authentication, and profile management. It handles user data and authentication mechanisms to ensure a secure and personalized user experience.

### Post Service

The Post Service facilitates the creation and retrieval of user posts. Users can share content, and the service manages the storage and retrieval of posts, including comments and interactions.

### Friendship Service

The Friendship Service handles user connections, friendships, and follower/following relationships. It allows users to send and accept friend requests, view their list of friends, and manage social connections.

### Chat Service

The Chat Service enables real-time communication between users through WebSocket technology. It provides a secure and efficient messaging platform, ensuring end-to-end encryption for message transmission.

## Features

- User registration and authentication.
- Post creation, retrieval, and commenting.
- Social connections through friend requests and friendships.
- Real-time chat and messaging with end-to-end encryption.
- Modular microservices architecture for scalability and maintainability.

## Getting Started

### Prerequisites

Before running the Social Media Project, ensure you have the necessary dependencies installed for each microservice. Refer to the README files in each microservice directory for specific instructions.

## License

This project is licensed under the [MIT License](LICENSE).