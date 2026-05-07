# Advanced LangChain RAG & Agentic Workflows

This repository contains two primary modules showcasing advanced Large Language Model (LLM) implementations using **LangChain** and **Ollama**. Both modules leverage local model capabilities while maintaining professional-grade toolsets and retrieval mechanisms.

---

## 📂 Project Overview

This repository is divided into two main components:

1.  **[Research Assistant Agent](./agents/agents.ipynb)**: An intelligent agent that uses the **ReAct** logic framework to search across Wikipedia, arXiv, and custom documentation.
2.  **[Document-Centric RAG Pipeline](./chain/retriever.ipynb)**: A high-performance Retrieval-Augmented Generation (RAG) system for querying structured documents (like PDFs) using FAISS and local embeddings.

---

## 🤖 1. Research Assistant Agent
Located in `/agents/agents.ipynb`

This module implements a versatile research agent capable of deciding which tools to use based on the user's query.

### 🌟 Key Features
*   **Multi-Tool Integration**:
    *   **Wikipedia**: For general facts and historical data.
    *   **arXiv**: For scientific research papers and pre-prints.
    *   **Custom Retriever Tool**: Specifically trained to search through LangSmith documentation.
*   **ReAct Logic**: Uses the `create_react_agent` logic to think, act, and observe until a final answer is found.
*   **Local Model Support**: Powered by `Ollama` (model: `glm-4.6:cloud`) with robust error handling for parsing local outputs.

### 🛠 Tech Stack
*   **Framework**: LangChain
*   **Tools**: Wikipedia API, Arxiv API
*   **LLM**: Ollama (GLM-4.6)
*   **Logic**: ReAct Framework

---

## 📄 2. Document-Centric RAG Pipeline
Located in `/chain/retriever.ipynb`

A focused implementation of a RAG pipeline designed to provide highly accurate answers based on specific document contexts.

### 🌟 Key Features
*   **Advanced PDF Processing**: Uses `PyPDFLoader` and `RecursiveCharacterTextSplitter` for optimal context chunking.
*   **Vector Search**: Utilizes **FAISS** (Facebook AI Similarity Search) for blazing-fast similarity searches.
*   **High-Quality Embeddings**: Implements `nomic-embed-text` via Ollama for superior semantic understanding.
*   **Step-by-step Thinking**: Uses custom prompts to force the model to think through the context before answering.

### 🛠 Tech Stack
*   **Vector Store**: FAISS
*   **Embeddings**: Nomic (via Ollama)
*   **LLM**: Ollama (GLM-4.6)
*   **Processing**: PyPDF, BeautifulSoup4

---

## 🚀 Getting Started

### Prerequisites
1.  **Ollama**: Ensure Ollama is installed and running on your local machine.
2.  **Models**: Pull the necessary models:
    ```bash
    ollama pull glm-4.6:cloud
    ollama pull nomic-embed-text
    ```

### Installation
1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   ```
2. Install dependencies (recommended to use a virtual environment):
   ```bash
   pip install -r requirements.txt
   ```
   *Note: If you use `uv`, you can run `uv pip install -r requirements.txt`.*

### Usage
Open the respective `.ipynb` files in Jupyter Notebook or VS Code to explore the implementations:
*   Run `agents/agents.ipynb` for the multi-tool research agent.
*   Run `chain/retriever.ipynb` for the PDF-based Q&A system.

---

## 🤝 Contributing
Feel free to fork this project, submit issues, or create pull requests. Contributions to improve retrieval accuracy or add more agent tools are welcome!

