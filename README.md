

## RAG-Powered Document Analysis Tool

This project is a powerful, conversational Q\&A system that leverages a Retrieval-Augmented Generation (RAG) pipeline to answer questions based on the content of a private PDF document. It uses Google's Gemini model, orchestrated by the LangChain framework, to provide accurate and context-aware answers, preventing model hallucinations by grounding responses in the provided source material.

-----

## 🚀 Key Features

  - **Dynamic Document Loading:** Ingests and processes any PDF document as a custom knowledge base.
  - **Intelligent Text Chunking:** Employs a recursive character text splitter to break down the document into optimal, context-aware chunks.
  - **Efficient Vector Storage:** Utilizes ChromaDB to create a fast and efficient vector store for semantic searching.
  - **Accurate Information Retrieval:** Implements Google's state-of-the-art embedding models to find the most relevant document chunks for any given query.
  - **Context-Aware Generation:** Uses Google's Gemini model to generate human-like answers based on the retrieved context.

-----

## 🛠️ Tech Stack

  - **Core Logic:** Python
  - **LLM Framework:** LangChain
  - **LLM & Embeddings:** Google Gemini (`gemini-2.0-flash`, `models/embedding-001`)
  - **Vector Database:** ChromaDB
  - **Document Loading:** PyPDF

-----

 How It Works

The application follows a complete RAG pipeline:

1.  Load: A PDF document is loaded into the system.
2.  Split: The document is split into smaller, overlapping text chunks to ensure context is preserved.
3.  Embed & Store: Each chunk is converted into a numerical vector using Google's embedding model and stored in a ChromaDB vector store.
4.  Retrieve: When a user asks a question, their query is also embedded, and the system performs a similarity search in ChromaDB to find the most relevant text chunks.
5.  Generate: The user's original question and the retrieved text chunks are passed to the Gemini model, which then generates a final, source-grounded answer.


