# 🎬 Movie Script RAG Chatbot

A Retrieval-Augmented Generation (RAG) chatbot that answers questions from a movie script PDF using OpenAI's GPT-3.5, ChromaDB, and SentenceTransformers.

---

## 📖 Overview

This project demonstrates how to combine document parsing, vector embeddings, vector databases, and a large language model to enable intelligent Q&A over a movie script. The chatbot can understand user questions and respond contextually using actual scenes from the uploaded script.

---

## 📌 Features

- Parses movie script PDFs and extracts scene-based content
- Splits the text into chunks using scene markers
- Generates semantic embeddings using a pretrained model (`all-MiniLM-L6-v2`)
- Stores embeddings in a local vector database (`ChromaDB`)
- Retrieves the most relevant scene for a given question
- Constructs a prompt using the retrieved scene and user's question
- Sends the prompt to OpenAI's GPT model to generate a response
- Can be extended with a frontend using Streamlit

---

## 🎯 Objective

To create an intelligent, domain-specific chatbot that can answer questions about a movie script without retraining the LLM. Instead, it augments the model with custom knowledge using the RAG technique.

---

## 🧠 How It Works

### Step 1: PDF Parsing  
Extracts text from a movie script using a PDF processing library.

### Step 2: Scene-Based Chunking  
Splits the extracted text based on the word “Scene” to organize it into smaller, meaningful units.

### Step 3: Embedding Generation  
Each scene is converted into a numerical vector using a sentence embedding model.

### Step 4: Vector Database Storage  
These embeddings are stored in ChromaDB, which allows for similarity-based retrieval.

### Step 5: User Input  
The user asks a question related to the script.

### Step 6: Retrieval  
The system finds the most similar scene chunk to the question based on vector similarity.

### Step 7: Prompt Construction  
The retrieved scene and the question are merged to create a final prompt.

### Step 8: GPT Response  
This prompt is sent to GPT-3.5, which returns an answer based on both its training and the retrieved context.

---

## 🛠️ Technologies Used

- **Python** – Core programming language  
- **pdfplumber** – For extracting text from PDF  
- **SentenceTransformers** – For generating vector embeddings  
- **ChromaDB** – For storing and retrieving embeddings  
- **OpenAI GPT-3.5** – For generating answers using the retrieved context  
- **Streamlit (optional)** – For building a user-friendly interface

---

## 💡 Concepts Covered

- Large Language Models (LLMs)
- Tokenization & Embeddings
- Retrieval-Augmented Generation (RAG)
- Vector Databases & Semantic Search
- Prompt Engineering
- End-to-End AI Pipeline Integration
