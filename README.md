# 🧠 Document-Intelligence-System

> **OmniMind AI** is a production-grade **Multi-Source Knowledge Intelligence Platform** that ingests documents, resumes, and YouTube videos, builds a unified knowledge base, and enables **retrieval-augmented generation (RAG)**, **structured information extraction**, and **multi-LLM reasoning** through an interactive **Streamlit GUI**.

This project is designed as a **flagship LLM engineering capstone**, showcasing real-world system design, modular architecture, and practical AI engineering practices.

---

## 🚀 Why Document-Intelligence-System?

Modern knowledge is fragmented across PDFs, videos, resumes, and notes. Traditional chatbots lack:

* Persistent memory over private data
* Source grounding and traceability
* Structured outputs for downstream systems
* Flexibility to use different LLM providers

**OmniMind AI solves this** by acting as a unified AI layer over heterogeneous knowledge sources.

---

## 🎯 Key Features

### 🔹 Multi-Source Ingestion

* 📄 **PDFs** (research papers, reports, resumes)
* ▶️ **YouTube videos** (via transcript extraction)
* 🧾 **Text / Resume snippets**

### 🔹 Retrieval-Augmented Generation (RAG)

* Semantic chunking & embeddings
* Vector database–backed retrieval
* Context-aware, grounded answers
* Source attribution (document & timestamp aware)

### 🔹 Structured Information Extraction

* Resume → clean **JSON output**
* Controlled generation using **LangChain Output Parsers**

### 🔹 Multi-LLM Routing

* 🔵 OpenAI
* 🟢 DeepSeek
* 🤖 Auto-routing based on task type (summarization, Q&A, structured extraction)

### 🔹 Interactive Streamlit UI

* Multi-tab interface
* Chat-based querying
* File upload & management
* LLM selection & configuration

---

## 🧠 System Architecture (High-Level)

```
User Input (PDF / YouTube / Text)
        ↓
Data Ingestion & Parsing
        ↓
Text Chunking + Embeddings
        ↓
Vector Store (FAISS / Chroma)
        ↓
Retriever
        ↓
Prompt Templates + Output Parsers
        ↓
LLM Router (OpenAI / DeepSeek)
        ↓
Structured or Natural Language Output
```

---

## 🛠️ Tech Stack

### Core

* **Python 3.10+**
* **Streamlit** – interactive GUI
* **LangChain** – LLM orchestration

### LLM Providers

* **OpenAI API**
* **DeepSeek API**

### Retrieval & Storage

* **FAISS** or **Chroma** (Vector Database)
* Embedding models (provider-agnostic)

### Data Processing

* PDF loaders
* YouTube transcript loaders
* Text splitters

### Engineering Best Practices

* Modular project structure
* Environment-based configuration (`.env`)
* Error handling & logging
* Type hints & docstrings

---

## 📂 Project Structure

```
omnimind-ai/
│
├── app.py                     # Streamlit entry point
├── requirements.txt
├── .env.example
├── README.md
│
├── core/
│   ├── llm_router.py          # OpenAI / DeepSeek routing logic
│   ├── prompts.py             # Prompt templates
│   ├── output_parsers.py      # StructuredOutputParser definitions
│
├── ingestion/
│   ├── pdf_loader.py
│   ├── youtube_loader.py
│   ├── resume_parser.py
│
├── rag/
│   ├── chunking.py
│   ├── embeddings.py
│   ├── vector_store.py
│   ├── retriever.py
│
├── ui/
│   ├── sidebar.py
│   ├── tabs.py
│
└── utils/
    ├── config.py
    ├── logger.py
    └── helpers.py
```

---

## ⚙️ Setup & Installation

```bash
# Clone the repository
git clone https://github.com/your-username/omnimind-ai.git
cd omnimind-ai

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### 🔐 Environment Variables

Create a `.env` file:

```env
OPENAI_API_KEY=your_openai_key
DEEPSEEK_API_KEY=your_deepseek_key
```

---

## ▶️ Run the Application

```bash
streamlit run app.py
```

---

## 📌 Use Cases

* Chat with private documents
* Summarize long PDFs or videos
* Extract structured data from resumes
* Compare LLM reasoning quality
* Build a personal or enterprise knowledge base

---

## 🧪 Future Enhancements

* User authentication
* Persistent vector storage
* Token usage & cost dashboard
* Document-level access control
* API version (FastAPI backend)

---

## 👤 Author

**Basel Amr Barakat**
Electrical & Computer Engineer | AI & LLM Engineer
📧 [baselamr52@gmail.com](mailto:baselamr52@gmail.com)

---

## ⭐ If you like this project

Give it a star ⭐ and feel free to fork or contribute!
