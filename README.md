# 📚 StudyMate RAG

### Personalized Academic Support Tool using Retrieval-Augmented Generation

StudyMate RAG is an AI-powered academic assistant that helps students prepare for examinations using their own study materials.

Students can upload study materials such as **PDF, DOCX, PPTX, TXT, CSV, and XLSX files**. The system extracts the content, converts it into embeddings, stores it in a vector database, and uses a local Large Language Model (LLM) to generate exam-oriented study content.

---

## 🎯 Objective

The main objective of StudyMate RAG is to provide students with a personalized study assistant that works directly with their own academic materials.

The system generates:

- 📖 Complete Summary
- 📌 Topic-wise Important Points
- ❓ Topic-wise Important Questions
- 💬 Question Answering from uploaded materials

---

## ✨ Features

### 📂 Multiple File Support

Users can upload:

- PDF
- DOCX
- PPTX
- TXT
- CSV
- XLSX

### 📖 Complete Summary

The system analyzes the uploaded material and generates a simplified summary containing the important concepts.

### 📌 Topic-wise Important Points

Important concepts are organized topic by topic to make revision easier.

### ❓ Topic-wise Important Questions

The system generates exam-oriented questions such as:

- Short-answer questions
- 5-mark questions
- 10-mark questions

### 💬 RAG-based Question Answering

Students can ask questions about their uploaded material.

The system retrieves the most relevant content from the uploaded document before generating the answer.

### 🔒 Local AI Processing

StudyMate uses **Ollama with Llama 3.2** locally, so the project does not require a Gemini API key for AI generation.

---

## 🧠 How StudyMate RAG Works

```text
              STUDENT
                 │
                 ▼
        Upload Study Material
                 │
                 ▼
          Text Extraction
                 │
                 ▼
             Chunking
                 │
                 ▼
      Sentence Transformer
       (Embeddings Model)
                 │
                 ▼
           ChromaDB
        Vector Database
                 │
                 ▼
        Relevant Chunks
          Retrieved
                 │
                 ▼
          Ollama Llama 3.2
                 │
                 ▼
        AI Generated Output
                 │
        ┌────────┼─────────┐
        ▼        ▼         ▼
     Summary  Important  Questions
                Points
