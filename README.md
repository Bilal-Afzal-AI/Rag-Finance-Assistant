# 📊 Financial Filings RAG Copilot

A production-style Retrieval-Augmented Generation (RAG) system that answers questions from SEC financial filings (10-K, 10-Q) with grounded responses and citations.

---

## 🚀 Overview

Financial Filings RAG Copilot is an end-to-end AI system designed to:

* Ingest public SEC filings
* Index and retrieve relevant financial data
* Generate accurate, citation-backed answers
* Provide a chat-based interface for querying filings

This project is built as a **portfolio-grade system** demonstrating real-world AI engineering skills, including data pipelines, retrieval systems, LLM integration, and deployment readiness.

---

## 🎯 Features

* 🔍 Semantic search over financial filings
* 📑 Citation-based answers with evidence snippets
* 🏢 Filtering by company, filing type, and year
* 🔄 Incremental data ingestion (new filings)
* 💬 Chat interface with session persistence
* 📊 Evaluation pipeline for quality testing
* 🧾 Logging and audit tracking

---

## 🏗️ Architecture

```
User Query → API (FastAPI)
           → Retriever (Qdrant)
           → Relevant Chunks
           → LLM (Gemini)
           → Grounded Answer + Citations
```

---

## 🧰 Tech Stack

| Layer             | Technology     |
| ----------------- | -------------- |
| Backend API       | FastAPI        |
| RAG Orchestration | LangChain      |
| LLM               | Gemini API     |
| Vector DB         | Qdrant         |
| Database          | MongoDB        |
| Parsing           | Docling        |
| UI                | Streamlit      |
| DevOps            | Docker, GitHub |

---

## 📂 Repository Structure

```
financial-rag-copilot/
├── app/
│   ├── api/
│   ├── core/
│   ├── services/
│   ├── models/
│   └── db/
├── ingestion/
├── indexing/
├── evaluation/
├── ui/
├── scripts/
├── tests/
├── docs/
├── docker/
├── .env.example
├── requirements.txt
└── README.md
```

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/financial-rag-copilot.git
cd financial-rag-copilot
```

### 2. Create Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables

Create a `.env` file based on `.env.example`:

```
GEMINI_API_KEY=your_api_key
MONGODB_URI=your_mongodb_uri
QDRANT_URL=your_qdrant_url
```

### 5. Run Services

```bash
# Start API
uvicorn app.api.main:app --reload

# Start UI
streamlit run ui/app.py
```

---

## 🔄 Workflow

1. **Ingestion** → Fetch SEC filings
2. **Parsing** → Extract clean text + metadata
3. **Indexing** → Chunk + embed + store in Qdrant
4. **Retrieval** → Search relevant chunks
5. **Generation** → LLM produces answer with citations
6. **Evaluation** → Test accuracy and quality

---

## 📊 Evaluation

The system includes:

* Benchmark question set
* Retrieval relevance checks
* Answer quality evaluation

---

## 🚧 Roadmap

* [ ] Multi-company comparison optimization
* [ ] Improved parsing accuracy
* [ ] Advanced ranking (rerankers)
* [ ] UI enhancements
* [ ] Deployment (Docker + cloud)

---

## ⚠️ Limitations

* No financial or investment advice
* Dependent on parsing quality
* Free-tier limitations on APIs

---

## 📜 License

This project is for educational and portfolio purposes.

---

## 👨‍💻 Author

Bilal Mohammad Afzal
Machine Learning Engineer (Self-Taught)

---

## ⭐ Acknowledgements

* SEC EDGAR for public financial data
* Open-source AI ecosystem

---

## 💡 Final Note

This project demonstrates a **production-ready RAG system** with real-world constraints, making it a strong portfolio piece for AI/ML and backend engineering roles.
