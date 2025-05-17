Real-Time Chat Room

Introduction

The Real-Time Chat Room is a modern, responsive, and minimal chat application that allows users to communicate in real-time using WebSockets. It enables multiple users to join a room via a unique ID and exchange messages instantly. This project is suitable for learning or demonstrating real-time communication concepts using Socket.IO and React.

Objectives

To demonstrate real-time bidirectional communication.

To create a user-friendly chat interface using modern frontend technologies.

To implement a basic client-server architecture for chat rooms.

Technologies Used

Frontend: React, TypeScript, Tailwind CSS, Vite

Backend: Node.js, Express.js

WebSocket: Socket.IO

Features

Join chat rooms with a unique Room ID

Real-time messaging

Responsive UI design

Message timestamps

Auto-scrolling chat window

Folder Structure

react-chat-websocket-main/
├── client/        # React frontend
│   ├── src/
│   │   ├── components/
│   │   ├── App.tsx
│   │   └── main.tsx
│   ├── index.html
│   └── vite.config.ts
├── server/        # Node.js + Express backend
│   └── index.js

How It Works

The server is created using Express and upgraded with Socket.IO for real-time communication.

When a user joins a room, a join_room event is emitted and the server adds the socket to the room.

When a user sends a message, it is emitted with send_message and broadcast to others in the same room using socket.to(room).emit(...).

The frontend listens for the receive_message event and updates the message list in real-time.

Installation and Setup

Backend (Server)

Navigate to the server directory:

cd server

Install dependencies:

npm install

Start the server:

npm start

Runs on http://localhost:3001

Frontend (Client)

Open a new terminal and navigate to the client directory:

cd client

Install dependencies:

npm install

Start the frontend server:

npm run dev

Opens on http://localhost:5173

Usage Instructions

Open http://localhost:5173 in multiple tabs or browsers.

Enter different usernames.

Use the same room ID to join the same chat room.

Start chatting in real-time.

Environment Configuration

In the /client directory, configure .env.local if needed:

VITE_SERVER_URL=http://localhost:3001

Future Enhancements

User authentication

Database integration for chat history

Typing indicators

User avatars and status

Conclusion

This project showcases the fundamental implementation of real-time communication using Socket.IO and a clean frontend experience with React and Tailwind. It is a great foundation for more complex chat systems or collaborative apps.
