# English ↔ Hindi Cross-Lingual Information Retrieval (CLIR) System

![CLIR Badge](https://img.shields.io/badge/Language-Multilingual-blue)
![Python](https://img.shields.io/badge/Python-3.10-green)
![Transformer](https://img.shields.io/badge/Model-LaBSE-orange)

---

## Overview

With the exponential growth of multilingual content on the web, accessing relevant information across languages has become increasingly important. This project implements a **bidirectional English ↔ Hindi Cross-Lingual Information Retrieval (CLIR) system**, enabling users to:

- Enter queries in **English** and retrieve **Hindi documents**  
- Enter queries in **Hindi** and retrieve **English documents**

The system combines **semantic embeddings** using **LaBSE** with **lexical retrieval** through **BM25**, providing high-accuracy and context-aware retrieval.

---

## Key Features

- **Bidirectional Retrieval**: Supports both English → Hindi and Hindi → English queries.  
- **Hybrid Retrieval**: Combines **semantic similarity** (transformer embeddings) and **lexical matching** (BM25).  
- **Automatic Language Detection**: Queries are automatically routed to the correct retrieval direction.  
- **Fast and Scalable**: Precomputed embeddings allow real-time query response.  
- **User-Friendly Interface**: Web-based interface for easy interaction.

---

## Architecture

The system is divided into the following modules:

1. **User Query Interface**: Accepts queries in English or Hindi.  
2. **Language Detection**: Automatically detects query language.  
3. **Semantic Retrieval**: Uses **LaBSE embeddings** to retrieve semantically similar documents.  
4. **Lexical Retrieval**: BM25 indexes ensure exact keyword matching.  
5. **Hybrid Ranking**: Combines semantic and lexical scores to rank top results.  
6. **Result Display**: Shows top-k relevant documents in the target language.

![Architecture Diagram](path_to_your_flowchart_image_or_mermaid_diagram.png)

---

## Dataset

- **IIT Bombay English-Hindi Parallel Corpus**  
- **Subset Used**: 50,000 sentence pairs for efficient training and testing.  
- Sentences were **preprocessed** for alignment, normalization, and tokenization.

---

## Installation

1. Clone the repository:  
```bash
git clone https://github.com/yourusername/clir-english-hindi.git
cd clir-english-hindi
