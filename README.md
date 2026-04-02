# RAG_Project2.ipynb

## Overview

This Jupyter notebook demonstrates the implementation of a Retrieval-Augmented Generation (RAG) system for processing and querying a Curriculum Vitae (CV) PDF document. The project uses LangChain for orchestration, Cohere for language model interactions, HuggingFace embeddings for text vectorization, and Qdrant as the vector database for efficient document retrieval.

## Features

- **PDF Loading and Processing**: Loads and parses a CV PDF using PyPDFLoader.
- **Text Chunking**: Splits the document into manageable chunks using RecursiveCharacterTextSplitter.
- **Embeddings**: Generates vector embeddings using HuggingFace's sentence-transformers model.
- **Vector Storage**: Stores embeddings in a Qdrant vector database for fast similarity search.
- **Language Model Integration**: Uses Cohere's ChatCohere model for generating responses based on retrieved context.

## Prerequisites

- Python 3.8 or higher
- Jupyter Notebook or JupyterLab
- API key for Cohere (set as environment variable `api_key`)
- Required Python packages (installed via pip in the notebook):
  - langchain
  - langchain-cohere
  - langchain-community
  - pypdf
  - langchain-huggingface
  - sentence-transformers
  - langchain-qdrant
  - qdrant-client

## Setup

1. Clone or download the repository.
2. Ensure you have a Cohere API key. Set it as an environment variable:
   ```
   export api_key="your-cohere-api-key"
   ```
   Or create a `.env` file in the project directory with:
   ```
   api_key=your-cohere-api-key
   ```
3. Place your CV PDF file at the specified path: `E:\CV_RAG_Project\Updated CV.pdf` (or update the path in the notebook).

## Usage

1. Open the notebook in Jupyter Notebook or VS Code.
2. Run the cells sequentially from top to bottom.
3. The notebook will install required packages, load the PDF, process the text, create embeddings, and set up the vector store.
4. After setup, you can query the system (additional cells may be added for querying).

## Project Structure

- `RAG_Project2.ipynb`: Main notebook containing the RAG implementation.
- `Updated CV.pdf`: Sample CV PDF for processing (not included; user must provide).

## Notes

- The PDF path is currently hardcoded. Modify the `path` variable in the notebook to point to your CV file.
- Ensure the vector store path `../tmp/langchain_qdrant3` is writable or adjust as needed.
- Some cells may require execution in order, especially package installations.

## License

[Add license information if applicable]
