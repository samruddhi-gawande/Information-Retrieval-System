# Information Retrieval System

This repository hosts an Information Retrieval System that allows users to upload multiple PDF files and ask questions about their content. The system leverages PaLM2, LangChain, FAISS, and Streamlit to provide an interactive and efficient interface for information retrieval.

## Overview

This project is designed to help users quickly retrieve relevant information from a large collection of PDF documents. By utilizing vector-based search and conversational retrieval, the system provides accurate and contextual answers to user queries.

## Features

- **Multi-PDF Input**: Upload multiple PDF files simultaneously.
- **Conversational Q&A**: Interact with the content of the PDFs by asking questions.
- **Vectorized Storage**: FAISS-powered vector storage for efficient text search.
- **Persistent Memory**: Tracks conversation history for a seamless user experience.

## Tech Stack

- **Python**
- **Streamlit**: Frontend interface for user interaction.
- **PaLM2 & LangChain**: Language processing and question-answering.
- **FAISS**: Vector search library for fast similarity search.
- **Google Palm Embeddings**: Embeddings to convert text into vector representations.

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables**
- Add your Google API key to a .env file in the root directory:
   ```bash
   GOOGLE_API_KEY=your_google_api_key
   ```

## Usage

1. **Run the application**:
   ```bash
   streamlit run app.py
   cd your-repo-name
   ```
2. **Upload PDFs**
- Use the sidebar to upload one or more PDF files.
- Click on the "Submit & Process" button to process the files.

3. **Ask Questions:**
- Enter a question in the text input box to query the content of the uploaded PDFs.
- The system will retrieve relevant information and display the response.

## Code Structure

**app.py**
The main script to run the Streamlit application. It handles:
- User interface with Streamlit.
- User input processing and conversation state management.
- PDF upload and processing initiation.

**src/helper.py**
Contains utility functions for core operations:
- **get_pdf_text(pdf_docs):** Extracts text from uploaded PDF documents.
- **get_text_chunks(text):** Splits text into chunks using RecursiveCharacterTextSplitter.
- **get_vector_store(text_chunks):** Creates a FAISS vector store using Google Palm embeddings for text search.
- **get_conversational_chain(vector_store):** Sets up a conversational chain with memory to handle user queries.

## Future Enhancements

- **Support for Additional File Formats**
- **Enhanced Error Handling**
- **Broader Language Model Compatibility**
