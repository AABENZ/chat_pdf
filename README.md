# Ask Multiple PDFs: Conversational PDF Query App

This project is a Streamlit application that allows users to upload multiple PDF files and chat with the content extracted from these documents. Leveraging the power of language models and vector search, it enables users to ask questions about their documents and receive relevant answers from the embedded text.

## Project Structure

- **app.py**: Main Streamlit application script.
- **htmlTemplates.py**: Contains HTML templates for displaying user and bot messages.
- **.env**: File for storing environment variables (e.g, **OPENAI_API_KEY**).
- **requirements.txt**: List of dependencies required for the project.


## Features

- **PDF Upload and Text Extraction**: Upload one or more PDFs and extract the text from each page.
- **Text Chunking and Vector Storage**: Split extracted text into chunks for more effective search and store them in a FAISS vector store for fast retrieval.
- **Conversational Interaction**: Engage in a question-answer format with the content of the PDFs using OpenAI or HuggingFace models.
- **Session Memory**: Maintains conversation history for smooth and coherent interaction.

## Tech Stack

- **Python**
- **Streamlit**: For building the web application interface.
- **PyPDF2**: For PDF text extraction.
- **LangChain**: For language model-based retrieval and conversation.
- **FAISS**: Vector storage for fast similarity search.
- **OpenAI / HuggingFace Models**: For embeddings and conversational AI.

## How it works

- **PDF Upload**: Users upload one or more PDF files through the Streamlit interface.
- **Text Extraction**: Text is extracted from the uploaded PDFs.
- **Text Chunking and Vectorization**: The text is split into chunks, embedded into vectors, and stored in a FAISS vector store.
- **Conversational Retrieval**: Users can ask questions, and the app will retrieve relevant chunks from the vector store to provide answers.


## Getting Started

### Prerequisites

Make sure you have Python 3.7 or later installed on your system.

### Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/yourusername/ask_multiple_pdfs.git
   cd ask_multiple_pdfs

2. **Create a Virtual Environment**:

   ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`

3. **Install Dependencies**:

   ```bash
    pip install -r requirements.txt

2. **Set Up API Keys**:

   ```bash
    OPENAI_API_KEY=your_openai_api_key_here

### Running the Application

**To start the Streamlit app, run**:

```bash
streamlit run app.py