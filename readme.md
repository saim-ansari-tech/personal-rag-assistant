# Personal RAG Assistant

A Retrieval-Augmented Generation (RAG) system built using LangChain, Qdrant, Hugging Face embeddings, and a local Qwen 2.5 model through Ollama.

## Overview

This project allows users to ask questions about a custom knowledge base. The system retrieves relevant information from stored documents and uses a Large Language Model (LLM) to generate grounded responses.

## Technologies Used

- Python
- LangChain
- Qdrant Vector Database
- Hugging Face Embeddings
  - all-MiniLM-L6-v2
- Ollama
- Qwen 2.5:7B

## Project Workflow

```text
Knowledge Base Files
        ↓
Document Loading
        ↓
Chunking
        ↓
Embeddings
        ↓
Qdrant Vector Store
        ↓
Retriever
        ↓
Context Formatting
        ↓
Prompt Template
        ↓
Qwen 2.5:7B
        ↓
Response
```

## Knowledge Base

The system currently uses the following files:

- bio.txt
- skills_and_projects.txt
- career_goals.txt

## Features

- Document loading using LangChain
- Recursive text chunking
- Semantic embeddings generation
- Vector storage with Qdrant
- Similarity-based retrieval
- Local LLM inference using Ollama
- Grounded responses based on retrieved context
- Refuses to answer questions not present in the knowledge base

## Example Questions

### In-domain Questions

- What are Saim's career goals?
- What projects has Saim built?
- What technical skills does Saim have?

### Out-of-domain Questions

- What is the capital of Japan?

Expected response:

```
I don't have enough information to answer that.
```

## Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/personal-rag-assistant.git
cd personal-rag-assistant
```

Install dependencies:

```bash
pip install -r requirements.txt
```

## Run Qdrant

Make sure Qdrant is running locally:

```bash
docker run -p 6333:6333 qdrant/qdrant
```

Or use an existing local Qdrant installation.

## Run Ollama

Make sure Ollama is installed and the model is available:

```bash
ollama pull qwen2.5:7b
```

Verify:

```bash
ollama list
```

## Run the Project

```bash
python rag.py
```

## Learning Outcomes

Through this project, I learned:

- Document ingestion
- Text chunking strategies
- Vector embeddings
- Vector databases
- Semantic retrieval
- Prompt engineering
- Retrieval-Augmented Generation (RAG)
- Local LLM deployment with Ollama

## Future Improvements

- Streamlit web interface
- Chat history and memory
- Source citations
- Multiple document formats (PDF, DOCX)
- Hybrid search
- Re-ranking

## Author

Saim

Robotics Student | AI & Robotics Enthusiast
