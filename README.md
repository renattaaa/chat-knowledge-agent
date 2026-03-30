# 🧠 Chat Knowledge Agent (AI Document Q&A)

An AI-powered application that allows users to upload documents (PDF, DOCX, CSV) and ask questions based on their content.

This project implements a Retrieval-Augmented Generation (RAG) pipeline:
Upload → Extraction → Embedding → Vector Search → AI-generated Answer.

---

## 🚀 Features

- 📄 Upload documents (PDF, DOCX, CSV)
- 🔍 Automatic text extraction & chunking
- 🧠 Embedding generation (1024-dimension vectors)
- 📦 Vector similarity search using FAISS / Chroma
- 💬 Context-aware Q&A using LLM
- ⚡ FastAPI backend with REST API
- 🗂️ Metadata storage (PostgreSQL)
- ⚡ Chat caching (Redis)

---

## 🏗️ Tech Stack

- **Backend**: FastAPI (Python)
- **Frontend**: React / Next.js (optional)
- **LLM**: gpt-oss-20b
- **Embedding Model**: ebbge-m3
- **Vector Database**: FAISS / Chroma
- **Database**: PostgreSQL
- **Cache**: Redis

---

## 🧠 How It Works

1. User uploads a document
2. System extracts text from file (PDF/DOCX/CSV)
3. Text is split into chunks (500–1000 characters)
4. Each chunk is converted into embeddings
5. Embeddings are stored in a vector database
6. User submits a question
7. System retrieves the most relevant chunks
8. LLM generates a contextual answer based on retrieved data

---

## 📡 API Endpoints

| Method | Endpoint       | Description                      |
|--------|--------------|----------------------------------|
| POST   | /upload      | Upload and process document      |
| POST   | /index       | Generate embeddings & store data |
| POST   | /chat        | Ask question based on document   |
| GET    | /docs/{id}   | Retrieve document metadata       |

---

## ▶️ Run Locally

### 1. Clone repository
```bash
git clone https://github.com/your-username/chat-knowledge-agent.git
cd chat-knowledge-agent/backend