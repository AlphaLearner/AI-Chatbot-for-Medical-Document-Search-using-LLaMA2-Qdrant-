# 🧠 MediContextLLM

> A context-aware, intelligent LLM-powered agent for extracting, retrieving, and reasoning over medical data.

MediContextLLM is an agentic AI system that uses **Large Language Models (LLMs)**, **context-aware task routing**, and **Retrieval-Augmented Generation (RAG)** to provide insightful answers and summaries based on unstructured medical documents, electronic health records (EHRs), research papers, and more.

---

## 🚀 Features

- 🔍 **RAG-Powered Search**: Combines LLMs with vector search to answer domain-specific queries with high accuracy.
- 🧩 **Model Context Protocol (MCP)**: Modular context handling for task-specific agents (e.g., summarization, diagnosis, document classification).
- 🤖 **Multi-Agent Framework**: Specialized agents collaborate to complete complex medical information tasks.
- 📚 **Document Ingestion Pipeline**: PDF/CSV/EMR ingestion, chunking, and embedding using LangChain.
- 🧠 **LLMs Supported**: GPT-4, Claude, Gemini, Mistral, or custom open-source LLMs.
- 🧵 **Conversation Memory**: Maintains context throughout user sessions using LangChain memory modules.
- 🛠️ **Modular and Extensible**: Easily pluggable components for embeddings, databases, and UI.

---

## 🏗️ Architecture

```mermaid
graph TD
    A[User Query] --> B[LangChain Router]
    B --> C{Agent Type?}
    C -->|Query| D[QA Agent w/ RAG]
    C -->|Summarize| E[Summarization Agent]
    C -->|Classify| F[Document Classifier Agent]
    D --> G[Vector DB]
    G --> H[Top-k Chunks]
    H --> I[LLM Response]
    I --> J[Output to User]
