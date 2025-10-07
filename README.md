# 🌐 English ↔ Hindi Cross-Lingual Information Retrieval (CLIR) System

![Python](https://img.shields.io/badge/Python-3.10-green?style=for-the-badge&logo=python)
![Hugging Face](https://img.shields.io/badge/Transformer-LaBSE-orange?style=for-the-badge&logo=huggingface)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

---

## ✨ Overview

With the exponential growth of multilingual content online, accessing relevant information across languages is critical. This project implements a **bidirectional English ↔ Hindi CLIR system**, enabling:

- **English → Hindi** queries  
- **Hindi → English** queries  

The system combines **semantic embeddings** using **LaBSE** and **lexical retrieval** through **BM25**, providing **highly accurate, context-aware results**.

---

## 🚀 Key Features

- 🔄 **Bidirectional Retrieval** – English ↔ Hindi  
- 🧠 **Hybrid Semantic + Lexical Retrieval** – Semantic embeddings + BM25 keyword matching  
- 🌍 **Automatic Language Detection** – Query language auto-detected  
- ⚡ **Fast & Scalable** – Precomputed embeddings for real-time results  
- 🖥️ **User-Friendly Interface** – Clean, intuitive web interface

---

## 🏗 Architecture

The system consists of the following modules:

```mermaid
flowchart TD
    A[User Query Input] --> B[Language Detection]
    B --> C{Query Language?}
    C -->|English| D[Semantic Retrieval - Hindi]
    C -->|Hindi| E[Semantic Retrieval - English]
    D --> F[Lexical BM25 Scoring]
    E --> F
    F --> G[Hybrid Ranking & Top-K Results]
    G --> H[Display Results in Web Interface]
