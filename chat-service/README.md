# Chat Service 

The Chat Service is a microservice within the social media application responsible for enabling real-time chat and messaging functionality between users. It utilizes WebSocket communication for efficient and low-latency interactions and ensures end-to-end encryption for secure message transmission.

## Table of Contents

1. [Overview](#overview)
2. [Features](#features)
3. [Endpoints](#endpoints)
4. [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
5. [Usage](#usage)
    - [WebSocket Connection](#websocket-connection)
    - [Sending Messages](#sending-messages)
    - [Receiving Messages](#receiving-messages)
6. [Security Considerations](#security-considerations)
    - [End-to-End Encryption](#end-to-end-encryption)
7. [Database Integration](#database-integration)
8. [License](#license)

## Overview

The Chat Service facilitates real-time communication between users through WebSocket technology. It powers the chat functionality in the social media application, providing a seamless and responsive user experience. All messages are end-to-end encrypted for enhanced security.

## Features

- Real-time bi-directional communication.
- Instant message delivery.
- Support for multiple chat rooms or channels.
- Secure WebSocket connections.
- End-to-End Encryption for message security.
- Messages are saved to the database for persistence.

## Endpoints

The Chat Service uses WebSocket communication and does not expose traditional RESTful endpoints. WebSocket connections are established at the `/ws` endpoint.

## Getting Started

### Prerequisites

Before running the Chat Service, ensure you have the following dependencies installed:

- Go (version ^1.20)

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

3. Configure the Chat Service:

    - Create a `.env` file based on the provided `.env.example` and configure the necessary environment variables.

4. Run the Chat Service:

    ```bash
    go run main.go
    ```

## Usage

### WebSocket Connection

Users can establish WebSocket connections to the `/ws` endpoint. The WebSocket URL will typically look like `/ws`.

### Sending Messages

Users can send messages by sending WebSocket messages to the server. The server will broadcast these messages to other connected users in the same chat room or channel. All messages are end-to-end encrypted for security.

### Receiving Messages

Connected users will receive incoming messages in real-time through their WebSocket connections. The client application should handle incoming messages and update the user interface accordingly.

## Security Considerations

### End-to-End Encryption

The Chat Service implements end-to-end encryption to secure message transmission. Messages are encrypted on the sender's side and decrypted on the recipient's side, ensuring that only the intended recipient can read the message content.

## Database Integration

All messages sent through the Chat Service are persisted to the database for future reference and retrieval. This ensures that chat history is maintained even if users disconnect and reconnect.

## License

This project is licensed under the [MIT License](LICENSE).