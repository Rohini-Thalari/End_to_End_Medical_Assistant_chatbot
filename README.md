# 🏥 End-to-End Medical Assistant Chatbot

An AI-powered medical Q&A chatbot with conversational memory and document retrieval.

**Tech Stack:** Python | LangChain | FAISS | Streamlit | HuggingFace

---

## 📖 Project Overview

The **End-to-End Medical Assistant Chatbot** is an intelligent, document-grounded conversational AI system designed to answer medical queries using curated medical knowledge sources.

The chatbot leverages **Retrieval-Augmented Generation (RAG)** to provide accurate, context-aware responses drawn from authoritative medical documents, while maintaining conversational memory across sessions.

The system ingests large medical reference PDFs — including the *Gale Encyclopedia of Medicine* and a Medical Q&A dataset — and makes this knowledge searchable and conversational through a clean web interface.

---

## ✨ Key Features

* ✅ RAG-based medical Q&A using real PDF medical references
* ✅ Conversational memory for multi-turn dialogue
* ✅ FAISS vector store for fast semantic retrieval
* ✅ HuggingFace embeddings for high-quality text representation
* ✅ Interactive Streamlit web UI
* ✅ Modular architecture (app, chatbot logic, memory)
* ✅ Secure API key handling using environment variables

---

## 📁 Project Structure

```
├── app.py
├── medibot.py
├── memory.py
├── requirements.txt
├── .env
├── Medical_QA_Combined_50Qs.pdf
├── The_GALE_ENCYCLOPEDIA_of_MEDICINE_SECOND.pdf
├── output Image.jpg
└── README.md
```

| File / Folder                                  | Description                                       |
| ---------------------------------------------- | ------------------------------------------------- |
| `app.py`                                       | Main Streamlit application (UI entry point)       |
| `medibot.py`                                   | Core chatbot logic (RAG pipeline, LLM, retrieval) |
| `memory.py`                                    | Handles conversational memory                     |
| `requirements.txt`                             | Project dependencies                              |
| `.env`                                         | API keys and config (ignored in git)              |
| `Medical_QA_Combined_50Qs.pdf`                 | Curated medical Q&A dataset                       |
| `The_GALE_ENCYCLOPEDIA_of_MEDICINE_SECOND.pdf` | Primary medical reference                         |
| `output Image.jpg`                             | Sample UI screenshot                              |

---

## 🛠️ Tech Stack

| Category        | Technology                         | Purpose                      |
| --------------- | ---------------------------------- | ---------------------------- |
| Frontend        | Streamlit                          | Web-based chat UI            |
| LLM Framework   | LangChain                          | RAG pipeline & orchestration |
| Embeddings      | HuggingFace Transformers           | Text vectorization           |
| Vector Store    | FAISS                              | Semantic similarity search   |
| Memory          | LangChain ConversationBufferMemory | Context retention            |
| Document Loader | LangChain PDF Loader               | PDF ingestion                |
| Language        | Python 3.x                         | Core development             |

---

## 🚀 Getting Started

### 🔧 Prerequisites

* Python 3.8+
* pip (Python package manager)
* HuggingFace API Token (or OpenAI API Key)

---

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/Rohini-Thalari/End_to_End_Medical_Assistant_chatbot.git
cd End_to_End_Medical_Assistant_chatbot
```

---

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 3️⃣ Configure Environment Variables

Create a `.env` file in the root directory:

```env
HUGGINGFACEHUB_API_TOKEN=your_huggingface_token_here
```

⚠️ **Important:** Never commit `.env` files to version control.

---

### 4️⃣ Run the Application

```bash
streamlit run app.py
```

Open in browser:

```
http://localhost:8501
```

---

## 🔍 How It Works (RAG Pipeline)

| Step | Component | Description                                   |
| ---- | --------- | --------------------------------------------- |
| 1    | Ingest    | PDFs are loaded and split into chunks         |
| 2    | Embed     | Text converted to vectors using HuggingFace   |
| 3    | Index     | Stored in FAISS vector database               |
| 4    | Query     | User inputs a medical question                |
| 5    | Retrieve  | Relevant chunks fetched via similarity search |
| 6    | Generate  | LLM produces answer using retrieved context   |
| 7    | Memory    | Chat history preserved for context            |

---

## 📚 Knowledge Sources

The chatbot uses:

* 📘 *The Gale Encyclopedia of Medicine (2nd Edition)*
* 📄 *Medical_QA_Combined_50Qs.pdf*

These documents are chunked and embedded to form the knowledge base.

---

## 📦 Dependencies

Key libraries used:

* `langchain` – RAG pipelines and chains
* `streamlit` – UI framework
* `faiss-cpu` – Vector similarity search
* `sentence-transformers` – Embedding models
* `pypdf / pdfplumber` – PDF parsing
* `python-dotenv` – Environment management
* `huggingface-hub` – Model access

---

## ⚠️ Disclaimer

This chatbot is intended for **educational and informational purposes only**.

🚫 It is **NOT** a substitute for professional medical advice, diagnosis, or treatment.
✅ Always consult a qualified healthcare provider for medical concerns.

---

## 📸 Demo

*Add your screenshot here (`output Image.jpg`)*

---

## 🤝 Contributing

Contributions are welcome! Feel free to fork the repo and submit a pull request.

---

## ⭐ Acknowledgements

* LangChain
* HuggingFace
* FAISS
* Streamlit


