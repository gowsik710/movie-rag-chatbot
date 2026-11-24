# 🎬 Movie Script RAG Chatbot

A Retrieval-Augmented Generation (RAG) chatbot that answers questions from a movie script PDF using OpenAI's GPT models, ChromaDB, and SentenceTransformers.

---

## 📖 Overview

This project demonstrates how to combine document parsing, vector embeddings, vector databases, and a large language model to enable intelligent Q&A over a movie script.

The chatbot retrieves relevant scenes from the uploaded script and uses OpenAI's language models to generate contextual responses based on the retrieved content.

---

## 📌 Features

- Parses movie script PDFs and extracts scene-based content.
- Splits text into chunks using scene markers.
- Generates semantic embeddings using a pretrained model (`all-MiniLM-L6-v2`).
- Stores embeddings in a local vector database using ChromaDB.
- Retrieves the most relevant scene for a given question.
- Constructs prompts using retrieved scene content and the user's question.
- Generates contextual responses using OpenAI's GPT models.
- Provides a chatbot interface using Streamlit.

---

## 🎯 Objective

To create an intelligent, domain-specific chatbot that can answer questions about a movie script without retraining the LLM. Instead, it augments the model with custom knowledge using the Retrieval-Augmented Generation (RAG) technique.

---

## 🧠 How It Works

### Step 1: PDF Parsing

Extracts text from a movie script using a PDF processing library.

### Step 2: Scene-Based Chunking

Splits the extracted text based on scene markers to organize it into smaller, meaningful units.

### Step 3: Embedding Generation

Each scene is converted into a numerical vector using a SentenceTransformer pretrained model.

### Step 4: Vector Database Storage

These embeddings are stored in ChromaDB, which allows for similarity-based retrieval.

### Step 5: User Input

The user asks a question related to the movie script through the chatbot interface.

### Step 6: Retrieval

The system finds the most relevant scene chunks based on semantic similarity.

### Step 7: Prompt Construction

The retrieved scene content and the user's question are combined to create a contextual prompt.

### Step 8: GPT Response

The prompt is sent to an OpenAI GPT model through the OpenAI Python client using the client-style API. The model generates a contextual response using the retrieved information.

---

## 🛠️ Technologies Used

- **Python** – Core programming language.
- **OS** – Environment configuration for package compatibility.
- **pdfplumber** – Extracting text from PDF documents.
- **SentenceTransformers** – Generating semantic embeddings.
- **ChromaDB** – Storing and retrieving vector embeddings.
- **OpenAI API** – Generating contextual responses using GPT models.
- **Streamlit** – Building the chatbot interface.
- **Pandas** – Data handling and processing.
- **TensorFlow/Keras compatibility configuration** – Using `TF_USE_LEGACY_KERAS` to address package compatibility requirements.

---

## 💡 Concepts Covered

- Large Language Models (LLMs)
- Tokenization and Embeddings
- Retrieval-Augmented Generation (RAG)
- Vector Databases and Semantic Search
- Prompt Engineering
- OpenAI API Integration
- Package and Environment Compatibility
- End-to-End AI Pipeline Integration
