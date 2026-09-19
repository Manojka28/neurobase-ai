
# NeuroBase AI

NeuroBase AI is a full-stack AI-powered learning platform built for students, teachers, and lifelong learners. It brings together document intelligence, personalized tutoring, learning analytics, and live classroom collaboration in one modern application.

## Overview

NeuroBase AI acts as a digital learning workspace where users can:
- upload documents and study materials
- ask AI-powered questions based on their own content
- organize notes and topics
- generate flashcards for revision
- track learning progress and gaps
- participate in live classroom activities
- review lectures and classroom performance

The project combines a React frontend with a Node.js/Express backend and MongoDB storage, along with Google Gemini integration for AI-powered responses.

---

## Features

- User authentication with JWT
- Sign up and login flows
- AI tutor powered by Google Gemini
- PDF and text document upload
- Document text extraction and chunking
- Retrieval-based AI answers from uploaded content
- Topic-based learning organization
- Notes management
- Flashcards support
- Quiz and progress-oriented learning workflows
- Search across uploaded materials and knowledge
- Analytics dashboard
- Live classroom sessions with real-time updates
- Lecture review and class analytics
- Theme customization and settings

---

## Tech Stack

### Frontend
- React
- Vite
- Tailwind CSS
- React Router
- Axios
- Socket.IO Client
- Lucide React

### Backend
- Node.js
- Express
- MongoDB with Mongoose
- JWT
- bcryptjs
- CORS
- Multer
- pdf-parse
- Socket.IO

### AI / Intelligence
- Google Gemini API
- Retrieval-Augmented Generation (RAG)
- Text chunking and keyword-based relevance matching

---

## Project Structure

```text
neurobase-ai/
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── api/
│   │   ├── assets/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   ├── index.css
│   │   └── ...
│   ├── index.html
│   ├── package.json
│   ├── vite.config.js
│   ├── tailwind.config.js
│   ├── postcss.config.js
│   └── eslint.config.js
├── server/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── services/
│   ├── socket/
│   ├── server.js
│   └── package.json
├── render.yaml
├── .gitignore
└── README.md
```

---

## Frontend

The frontend is built with React and Vite. It includes:
- authentication flow
- dashboard and home screen
- chat interface
- notes and documents management
- search and analytics pages
- classroom pages
- flashcards and quiz pages
- settings and personalization

The main app routing is managed in the React app shell and the layout is shared across pages.

---

## Backend

The backend is powered by Express and runs the core API and business logic. It includes:
- user authentication and authorization
- document upload and retrieval
- AI chat integration
- quiz and study module APIs
- analytics endpoints
- classroom route handling
- Socket.IO real-time services

The server also connects to MongoDB and falls back to an in-memory database if a MongoDB URI is not provided.

---

## Database

MongoDB is used for persistent storage via Mongoose models. Core data models include:
- User
- Document
- Topic
- Learning items like chat history, notes, and flashcards

If `MONGO_URI` is missing, the application uses an in-memory MongoDB instance for local development and testing.

---

## AI Integration

The AI engine is built around Google Gemini. The flow works as follows:
1. User uploads or pastes study content.
2. Content is split into chunks.
3. The app retrieves the most relevant chunks based on the user query.
4. A contextual prompt is generated.
5. Gemini returns a helpful answer grounded in the user's uploaded knowledge.

This behavior is implemented in the backend AI service and is used in the chat system.

---

## Real-Time Classroom Features

The project includes live learning interactions through Socket.IO, including:
- joining lecture rooms
- participant count updates
- live transcript updates
- classroom chat
- raise-hand functionality
- current topic tracking
- lecture end notifications

This real-time layer is handled in the classroom socket service.

---

## Environment Variables

Create a `.env` file in the `server` directory with the following variables:

```env
PORT=8000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
GEMINI_API_KEY=your_gemini_api_key
NODE_ENV=development
```

### Notes
- `PORT` sets the backend port.
- `MONGO_URI` is the MongoDB connection string.
- `JWT_SECRET` is used to sign authentication tokens.
- `GEMINI_API_KEY` is required for AI features.
- If `MONGO_URI` is not configured, the app falls back to an in-memory MongoDB instance.

---

## Installation

### 1. Clone the repository

```bash
git clone <repository-url>
cd neurobase-ai
```

### 2. Install frontend dependencies

```bash
cd frontend
npm install
```

### 3. Install backend dependencies

```bash
cd ../server
npm install
```

---

## Run the Project

### Start the backend

```bash
cd server
npm run dev
```

### Start the frontend

```bash
cd frontend
npm run dev
```

### Production mode

```bash
cd server
npm start
```

---

## Deployment

The project includes a Render deployment configuration in `render.yaml`, which is set up for the Node.js backend service.

---

## Usage

After starting both frontend and backend:

1. Create an account or log in.
2. Upload study documents or add text content.
3. Ask questions in the AI chat assistant.
4. Browse topics, notes, and flashcards.
5. Review analytics and learning gaps.
6. Join or manage live classroom sessions.

---

## Project Goals

NeuroBase AI is designed to make learning more personalized, efficient, and collaborative by combining:
- AI tutoring
- document intelligence
- structured knowledge management
- real-time communication
- student learning analytics

---

## License

ISC

---

## Summary

NeuroBase AI is a modern AI learning platform built with React and Node.js. It demonstrates a practical implementation of a document-aware AI tutor, classroom collaboration system, and educational productivity tool in a single application.

```





