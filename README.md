# AI-Powered PDF Reader (FastAPI + React)

An AI-powered PDF Reader that lets you open PDFs, highlight text, and instantly get explanations. Includes chat-with-PDF using RAG, semantic search, and Gemini-powered insights over the entire document.

Tech stack: FastAPI, LlamaIndex, PostgreSQL + pgvector, React, PDF.js, Gemini API.

## Quick Start

1) Copy env templates and fill values

```
cp backend/.env.example backend/.env
cp frontend/.env.example frontend/.env
```

2) Start services via Docker Compose (optional)

```
docker compose -f infra/docker-compose.yml up -d
```

3) Local dev (alternative)

- Backend: create venv, install `backend/requirements.txt`, then run uvicorn.
- Frontend: `cd frontend; npm install; npm run dev`.

## Structure

```
backend/        # FastAPI, LlamaIndex, DB models, services
frontend/       # React + Vite + PDF.js UI
infra/          # Docker Compose and DB init scripts
docs/           # Architecture and API notes
```

See `docs/architecture.md` and `docs/api.md` for details.