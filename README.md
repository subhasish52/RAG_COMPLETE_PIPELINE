# RAG Pipeline From Scratch 

A complete **Retrieval-Augmented Generation (RAG)** pipeline built entirely from scratch **without using frameworks like LangChain or LangGraph**.

This project demonstrates how to design and implement a production-style RAG architecture by manually handling every stage of the pipeline from **data ingestion** to **retrieval** and **response generation**.

## Features 

* **Custom Data Ingestion Pipeline**

  * PDF parsing using **PyMuPDF**
  * OCR for scanned documents/images using **TesseractOCR**
  * Structured document parsing using **Docling**
  * Supports **text, image, and tabular data**

* **Data Preprocessing**

  * Cleaning and normalization
  * Metadata extraction
  * Intelligent chunking strategies
  * Overlap-based chunk generation

* **Embedding Generation**

  * Converts chunks into vector embeddings using transformer-based embedding models

* **Vector Storage & Retrieval**

  * Efficient similarity search using vector databases / FAISS
  * Top-k retrieval for relevant context

* **Advanced Retrieval Techniques**

  * Semantic search
  * Hybrid retrieval (optional)
  * Re-ranking support

* **LLM-based Answer Generation**

  * Retrieved chunks are injected into prompts
  * Generates grounded responses with minimal hallucination

* **Framework-Free Architecture**

  * No LangChain
  * No LangGraph
  * Full control over the pipeline and orchestration

## Tech Stack 🛠️

* Python
* PyMuPDF
* TesseractOCR
* Docling
* FAISS / ChromaDB
* Hugging Face Transformers
* Sentence Transformers
* PyTorch

## Workflow 

1. Ingest raw documents (PDF, images, tables)
2. Extract text and metadata
3. Chunk documents intelligently
4. Generate embeddings
5. Store embeddings in vector DB
6. Retrieve top relevant chunks
7. Inject context into prompt
8. Generate final response using LLM

## Goal 

To understand and implement the **core internals of RAG systems** without relying on abstraction-heavy frameworks, making the architecture transparent, customizable, and production-ready.
