# PDFSense AI

AI-powered PDF reader with semantic search, RAG-based chat, and contextual explanations.

---

## Overview

PDFSense AI allows you to read, explore, and interact with documents intelligently.  
It combines fast PDF rendering with retrieval-augmented generation to provide precise, context-aware answers.

---

## Features

**Core**
- Fast in-browser PDF rendering using PDF.js
- Text selection and highlighting
- Clean and responsive interface

**AI Capabilities**
- Chat with PDF (RAG pipeline via LlamaIndex)
- Context-aware explanations for selected text
- Semantic search across the document
- Gemini-powered summaries and insights

**Search & Retrieval**
- Vector search using PostgreSQL + pgvector
- Accurate retrieval from large documents

---

## Tech Stack

**Backend**
- FastAPI
- LlamaIndex
- PostgreSQL with pgvector
- Gemini API

**Frontend**
- React (Vite)
- PDF.js

**Infrastructure**
- Docker Compose

---

## Installation

### Clone repository

```bash
git clone https://github.com/darshil-sisodiya/pdfviewer.git
cd pdfviewer
```

### Configure environment

```bash
cp backend/.env.example backend/.env
cp frontend/.env.example frontend/.env
```

Update environment variables:
- Database credentials
- Gemini API key

---

## Running the Application

### Using Docker (recommended)

```bash
docker compose -f infra/docker-compose.yml up -d
```

---

### Local Development

**Backend**

```bash
cd backend
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt
uvicorn app:app --reload
```

**Frontend**

```bash
cd frontend
npm install
npm run dev
```

---

## Project Structure

```
.
├── backend/        FastAPI backend, RAG pipeline, database logic
├── frontend/       React + PDF.js interface
├── infra/          Docker configuration
├── docs/           Architecture and API documentation
└── README.md
```

---

## System Flow

1. PDF is parsed and chunked using LlamaIndex  
2. Embeddings are stored in PostgreSQL (pgvector)  
3. Queries trigger semantic retrieval  
4. Gemini generates final responses  

---

## Future Work

- Document annotations
- Multi-document chat
- User authentication
- Exportable insights

---

## License

MIT License

---

Built by Darshil
