# 🩺 Medical AI Chatbot & Cardiovascular Disease Prediction

An intelligent, local-first healthcare assistant combining conversational AI with document understanding and disease risk prediction.

## 🚀 Overview

This project is a **privacy-preserving, offline-capable** medical assistant built with:

- Natural language understanding via **LLaMA**
- Smart document analysis with **LangChain** & **FAISS**
- Predictive modeling using **XGBoost** for **cardiovascular disease risk assessment**

---

## 🧠 Key Features

- 💬 **Conversational Q&A**  
  Chat with an AI trained on your medical PDFs and CSVs.

- 📁 **Smart Document Retrieval**  
  Retrieves context-aware answers from uploaded health documents.

- 🧠 **Local LLM Intelligence**  
  Uses LLaMA with sentence transformers for local, accurate responses.

- 🩺 **Cardiovascular Risk Prediction**  
  Predicts CVD risk based on structured input (CSV or manual form).

- ⚡ **Real-Time Interface**  
  Communicate with the assistant via an elegant Chainlit UI.

---

## 🧰 Tech Stack

| Component         | Tool/Library                             |
|------------------|------------------------------------------|
| LLM              | LLaMA via CTransformers                  |
| NLP Pipeline     | LangChain + Sentence Transformers        |
| Vector Store     | FAISS                                     |
| Embeddings       | HuggingFace (all-MiniLM-L6-v2)            |
| Document Loader  | PyPDFLoader, DirectoryLoader              |
| Prediction Model | XGBoost (for CVD prediction)              |
| Interface        | Chainlit                                  |
| Backend Language | Python                                    |
| Data Handling    | Pandas                                    |

---

## ⚙️ How It Works

### 1. Preprocessing
- PDFs and CSVs are loaded from `C:/MEDIBOT/dataset/`
- Text is chunked using recursive splitting

### 2. Embedding & Indexing
- Chunks are embedded with `sentence-transformers`
- Stored in FAISS for efficient similarity search

### 3. Conversational Flow
- User query triggers vector search for relevant chunks
- LLaMA generates an answer using retrieved context
- Response is shown via Chainlit

### 4. Health Risk Prediction
- CSV data is preprocessed using Pandas
- XGBoost model predicts cardiovascular disease risk

---

## 🚀 Getting Started

### 📦 Requirements

```bash
pip install -r requirements.txt
