# Femora AI – Design Document

## 1. System Architecture Overview

Femora AI follows a client-server architecture integrated with an AI model.

User (Frontend Web App)
        ↓
Backend API Server
        ↓
AI Model (AWS Bedrock)
        ↓
Database
        ↓
Response to User

---

## 2. High-Level Components

### 2.1 Frontend

- Built using React.js
- Provides user interface
- Accepts questions and file uploads
- Displays structured AI responses

### 2.2 Backend

- Built using Node.js and Express
- Handles API requests
- Sends user queries to AI model
- Manages response formatting
- Handles authentication (future scope)

### 2.3 AI Integration

- AWS Bedrock for:
  - Concept simplification
  - Code explanation
  - Summarization
  - Debug suggestions

### 2.4 Database

- MongoDB
- Stores user queries and summaries (optional for MVP)

---

## 3. Workflow Design

1. User enters a question or uploads notes.
2. Frontend sends request to backend API.
3. Backend processes and forwards to AI model.
4. AI generates structured response.
5. Backend formats output.
6. Frontend displays explanation and summary.

---

## 4. Key Design Principles

- Simplicity: Clean and distraction-free UI.
- Clarity: Structured AI responses.
- Productivity: Quick summaries and debugging help.
- Scalability: Cloud-based deployment.

---

## 5. Security Considerations

- Secure API key management.
- Input validation.
- HTTPS-based communication.
- Limited storage of sensitive data.

---

## 6. Deployment Plan

- Frontend hosted on AWS.
- Backend deployed on AWS EC2 / serverless.
- Database hosted on MongoDB Atlas.
- AI accessed via AWS Bedrock APIs.
