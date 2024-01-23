# Post Service

The Post Service is a microservice within the social media application responsible for managing user posts, comments, and interactions. It facilitates the creation and retrieval of posts, along with the ability to add comments.

## Table of Contents

1. [Overview](#overview)
2. [Endpoints](#endpoints)
3. [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
4. [Usage](#usage)
    - [Create Post](#create-post)
    - [Get Post](#get-post)
    - [Add Comment](#add-comment)
5. [License](#license)

## Overview

The Post Service is a vital component of the social media application, enabling users to share posts, engage in discussions through comments, and interact with each other's content.

## Endpoints

The Post Service exposes the following gRPC endpoints:

- **CreatePost:** Create a new post.
- **GetPost:** Retrieve post information.
- **AddComment:** Add a comment to a post.

## Getting Started

### Prerequisites

Before running the Post Service, ensure you have the following dependencies installed:

- Go (version ^1.20)
- Oracle Database

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

3. Set up the Oracle Database:

    - Provide necessary configuration in the `.env` file based on the provided `.env.example`.

4. Configure the Post Service:

    - Create a `.env` file based on the provided `.env.example` and configure the necessary environment variables.

5. Run the Post Service:

    ```bash
    go run main.go
    ```

## Usage

### Create Post

**Endpoint:** `CreatePost`

**Request:**
```protobuf
syntax = "proto3";

message PostRequest {
  string user_id = 1;
  string content = 2;
}
```

**Response:**
```protobuf
syntax = "proto3";

message PostResponse {
  string post_id = 1;
  string user_id = 2;
  string content = 3;
}
```

### Get Post

**Endpoint:** `GetPost`

**Request:**
```protobuf
syntax = "proto3";

message PostIDRequest {
  string post_id = 1;
}
```

**Response:**
```protobuf
syntax = "proto3";

message PostResponse {
  string post_id = 1;
  string user_id = 2;
  string content = 3;
  repeated Comment comments = 4;
}
```

### Add Comment

**Endpoint:** `AddComment`

**Request:**
```protobuf
syntax = "proto3";

message CommentRequest {
  string post_id = 1;
  string user_id = 2;
  string content = 3;
}
```

**Response:**
```protobuf
syntax = "proto3";

message CommentResponse {
  string comment_id = 1;
  string user_id = 2;
  string content = 3;
}
```

## License

This project is licensed under the [MIT License](LICENSE).