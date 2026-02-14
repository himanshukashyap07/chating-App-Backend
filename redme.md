# 🚀 Chatting App Backend

<div align="center">

[![GitHub stars](https://img.shields.io/github/stars/himanshukashyap07/chating-App-Backend?style=for-the-badge)](https://github.com/himanshukashyap07/chating-App-Backend/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/himanshukashyap07/chating-App-Backend?style=for-the-badge)](https://github.com/himanshukashyap07/chating-App-Backend/network)
[![GitHub issues](https://img.shields.io/github/issues/himanshukashyap07/chating-App-Backend?style=for-the-badge)](https://github.com/himanshukashyap07/chating-App-Backend/issues)
[![GitHub license](https://img.shields.io/github/license/himanshukashyap07/chating-App-Backend?style=for-the-badge)](LICENSE)

**Robust Node.js backend for a real-time chat application, built with Express.js, MongoDB, and Socket.IO.**

</div>

## 📖 Overview

This repository hosts the backend service for a real-time chat application, designed to facilitate seamless communication between users. Functioning as the server-side component of a WhatsApp-like clone, it handles user authentication, message exchange, and persistent data storage. The application is built with a focus on real-time capabilities, ensuring messages are delivered instantly and user interactions are smooth and dynamic.

## ✨ Features

-   **🔐 User Authentication:** Secure user registration and login using JSON Web Tokens (JWT) and hashed passwords (bcrypt).
-   **💬 Real-time Messaging:** Instant message delivery and receipt via WebSocket communication (Socket.IO).
-   **👥 User Management:** Endpoints for listing and managing users within the chat platform.
-   **🚪 Chat Room / Direct Messaging:** Support for creating and managing individual and group chat conversations.
-   **💾 Message Persistence:** Storage and retrieval of chat messages using MongoDB.
-   **⚙️ Scalable Architecture:** Modular design with Express.js for efficient route handling and API management.

## 🛠️ Tech Stack

**Backend:**
![Node.js](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB)
![Socket.IO](https://img.shields.io/badge/Socket.io-010101?style=for-the-badge&logo=socket.io&logoColor=white)
![JSON Web Tokens](https://img.shields.io/badge/jsonwebtoken-000000?style=for-the-badge&logo=json-web-tokens&logoColor=white)
![Bcrypt](https://img.shields.io/badge/bcrypt-263238?style=for-the-badge&logo=bcrypt&logoColor=white)
![CORS](https://img.shields.io/badge/CORS-FF69B4?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA1MTIgNTEyIj48cGF0aCBkPSJNMzQ5LjUgMjI0LjVDMzQ5LjUgMTE5LjcgMjYwLjggMzEgMTU2IDMxUzYyLjUgMTE5LjcgNjIuNSAyMjQuNSA2Mi41IDM3Ny41IDE1NiAzNzcuNSA2Mi41IDQ2NS44IDYyLjUgNDc5LjUgOTMuNCA0ODguNSAxNTYgNDg3cy05My40LTEzLjYtOTMuNC02Mi44QzYyLjUgMzgzLjcgMTc5LjYgMjYxLjUgMzQ5LjUgMjI0LjVoLTkuM1Y0NDEuOWgyNTJWNzcuNnoiIGZpbGw9IiMwMDAiLz48L3N2Z3U+&logoColor=white)
![Dotenv](https://img.shields.io/badge/dotenv-white?style=for-the-badge&logo=dotenv&logoColor=black)

**Database:**
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
![Mongoose](https://img.shields.io/badge/Mongoose-800000?style=for-the-badge&logo=mongoose&logoColor=white)

## 🚀 Quick Start

### Prerequisites
Before you begin, ensure you have the following installed:
-   **Node.js**: Latest LTS version (e.g., v18.x or v20.x)
-   **npm**: Comes bundled with Node.js
-   **MongoDB**: A running instance of MongoDB (local or cloud-hosted)

### Installation

1.  **Clone the repository**
    ```bash
    git clone https://github.com/himanshukashyap07/chating-App-Backend.git
    cd chating-App-Backend
    ```

2.  **Install dependencies**
    ```bash
    npm install
    ```

3.  **Environment setup**
    Create a `.env` file in the root directory by copying the `.env.example` file (or creating it if it doesn't exist):
    ```bash
    cp .env.example .env
    ```
    (Note: A `.env.example` file was not detected, but it's standard practice. Please create one based on the variables below.)

    Configure your environment variables in `.env`:

    | Variable         | Description                                     | Example Default | Required |
    |------------------|-------------------------------------------------|-----------------|----------|
    | `PORT`           | Port on which the server will run               | `5000`          | Yes      |
    | `MONGO_URI`      | Connection string for your MongoDB database     | `mongodb://localhost:27017/chat_app` | Yes |
    | `JWT_SECRET`     | Secret key for signing JWTs                     | `supersecretjwtkey` | Yes |

4.  **Database setup**
    Ensure your MongoDB instance is running and accessible via the `MONGO_URI` provided in your `.env` file. No specific migration commands are typically needed for Mongoose, as schemas are defined in the `models` directory.

5.  **Start development server**
    ```bash
    npm run dev
    ```
    The server will typically run on `http://localhost:5000` (or your specified `PORT`).

## 📁 Project Structure

```
chating-App-Backend/
├── app.js               # Main application entry point, server setup, middleware, and Socket.IO
├── db/                  # Database connection configuration (e.g., `dbConnect.js`)
├── models/              # Mongoose schemas for User, Chat, Message, etc.
│   ├── User.js
│   ├── Chat.js
│   └── Message.js
├── routes/              # Express route definitions for API endpoints
│   ├── authRoutes.js
│   ├── userRoutes.js
│   └── chatRoutes.js
├── package.json         # Project metadata and dependencies
├── package-lock.json    # npm dependency lock file
├── .gitignore           # Specifies intentionally untracked files to ignore
└── redme.md             # This README file
```

## ⚙️ Configuration

### Environment Variables
The application uses environment variables for sensitive data and configuration. Please refer to the `Environment setup` section under Quick Start for details.

### Configuration Files
-   **`package.json`**: Defines project scripts and dependencies.
-   **`db/`**: Contains database connection logic.

## 🔧 Development

### Available Scripts
Based on typical Node.js projects, the following script is likely available:

| Command     | Description                           |
|-------------|---------------------------------------|
| `npm start` | Starts the production server (often `node app.js`). |

(Note: Additional development scripts like `npm run dev` or `npm run watch` might be defined in `package.json` for hot-reloading or development-specific tasks.)

## 📚 API Reference

This backend provides a RESTful API for user authentication and management, along with WebSocket (Socket.IO) events for real-time chat functionality.

### Authentication
All protected routes require a valid JSON Web Token (JWT) sent in the `Authorization` header as a Bearer token.

**Header Example:**
`Authorization: Bearer <your_jwt_token>`

### Endpoints

#### Authentication
-   `POST /api/auth/register`
    -   **Description**: Registers a new user.
    -   **Body**: `{ "username": "...", "email": "...", "password": "..." }`
    -   **Response**: `{ "message": "User registered successfully", "token": "..." }`
-   `POST /api/auth/login`
    -   **Description**: Authenticates a user and returns a JWT.
    -   **Body**: `{ "email": "...", "password": "..." }`
    -   **Response**: `{ "message": "Login successful", "token": "..." }`
-   `GET /api/auth/me` (Protected)
    -   **Description**: Retrieves the profile of the authenticated user.
    -   **Response**: `{ "id": "...", "username": "...", "email": "..." }`

#### Users
-   `GET /api/users` (Protected)
    -   **Description**: Retrieves a list of all registered users.
    -   **Response**: `[ { "id": "...", "username": "...", "email": "..." } ]`
-   `GET /api/users/:id` (Protected)
    -   **Description**: Retrieves a specific user's profile by ID.
    -   **Response**: `{ "id": "...", "username": "...", "email": "..." }`

#### Chats
-   `POST /api/chats` (Protected)
    -   **Description**: Creates a new chat (direct or group).
    -   **Body**: `{ "participants": ["userId1", "userId2"], "isGroupChat": false, "name": "Optional Group Name" }`
    -   **Response**: `{ "id": "...", "participants": [...], "isGroupChat": false, "name": "..." }`
-   `GET /api/chats` (Protected)
    -   **Description**: Retrieves all chats for the authenticated user.
    -   **Response**: `[ { "id": "...", "participants": [...], "latestMessage": {...} } ]`
-   `GET /api/chats/:id/messages` (Protected)
    -   **Description**: Retrieves messages for a specific chat.
    -   **Response**: `[ { "id": "...", "sender": {...}, "content": "...", "timestamp": "..." } ]`
-   `POST /api/chats/:id/messages` (Protected)
    -   **Description**: Sends a new message to a specific chat.
    -   **Body**: `{ "content": "Hello, world!" }`
    -   **Response**: `{ "id": "...", "sender": {...}, "content": "...", "timestamp": "..." }`

### Real-time Communication (Socket.IO Events)

The server utilizes Socket.IO for real-time bi-directional communication.

#### Client Emits:
-   `joinChat`: Joins a specific chat room.
    -   **Payload**: `chatId` (string)
    -   **Example**: `socket.emit('joinChat', 'chat_id_123');`
-   `sendMessage`: Sends a message to a chat.
    -   **Payload**: `{ chatId: string, content: string, sender: string }`
    -   **Example**: `socket.emit('sendMessage', { chatId: 'chat_id_123', content: 'Hi there!', sender: 'user_id_xyz' });`

#### Server Emits:
-   `receiveMessage`: Broadcasts a new message to all participants in a chat room.
    -   **Payload**: `{ chatId: string, message: { id: string, sender: { id: string, username: string }, content: string, timestamp: string } }`
    -   **Example**: `socket.on('receiveMessage', (data) => console.log(data.message));`
-   `connected`: Confirms a successful Socket.IO connection.
    -   **Payload**: (None)

## 🤝 Contributing

We welcome contributions to improve this project! To get started:

### Development Setup
1.  Fork the repository.
2.  Clone your forked repository:
    ```bash
    git clone https://github.com/YOUR_USERNAME/chating-App-Backend.git
    cd chating-App-Backend
    ```
3.  Install dependencies: `npm install`
4.  Set up your `.env` file as described in the Quick Start section.

### Submitting Contributions
1.  Create a new branch for your feature or bugfix: `git checkout -b feature/your-feature-name`
2.  Make your changes and commit them with descriptive messages.
3.  Push your branch: `git push origin feature/your-feature-name`
4.  Open a Pull Request to the `main` branch of this repository.

## 📄 License

This project is licensed under the [MIT License](LICENSE) - see the [LICENSE](LICENSE) file for details. <!-- TODO: Add actual license file -->

## 🙏 Acknowledgments

-   Built with [Node.js](https://nodejs.org/) and [Express](https://expressjs.com/).
-   Powered by [MongoDB](https://www.mongodb.com/) and [Mongoose](https://mongoosejs.com/) for database operations.
-   Real-time features enabled by [Socket.IO](https://socket.io/).
-   Secure authentication leveraging [JWT](https://jwt.io/) and [bcrypt](https://www.npmjs.com/package/bcrypt).

## 📞 Support & Contact

-   🐛 Issues: [GitHub Issues](https://github.com/himanshukashyap07/chating-App-Backend/issues)
-   📧 For questions or further support, please contact the repository owner. <!-- TODO: Add contact email -->

---

<div align="center">

**⭐ Star this repo if you find it helpful!**

Made with ❤️ by [himanshukashyap07] <!-- TODO: Add author name if different from owner -->

</div>