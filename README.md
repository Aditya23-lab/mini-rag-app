# Mini-RAG App — AI Engineer Assessment

## Project
A minimal Retrieval-Augmented Generation (RAG) demo:
- Upload/paste documents → chunk → embed → store in Pinecone.
- Ask query → retrieve → rerank → LLM answers with inline citations.

## Live
- Frontend: (add Vercel URL)
- Backend: (add deployed backend URL)

## Quickstart (local)
1. Clone repo
2. Create `.env` from `.env.example` and fill API keys
3. Backend:
   - cd backend
   - (instructions added later)
4. Frontend:
   - cd frontend
   - (instructions added later)

## Architecture
```mermaid
flowchart LR
  Frontend --> Backend
  Backend -->|embeddings| Pinecone[(Pinecone)]
  Backend -->|LLM calls| OpenAI[(OpenAI)]
  Backend -->|rerank (optional)| Cohere[(Cohere)]
