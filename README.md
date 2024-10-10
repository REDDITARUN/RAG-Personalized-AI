# RAG-Personalized-AI

# RAG Personalized AI Assistant

This repository demonstrates how to build an AI assistant using Retrieval-Augmented Generation (RAG) models. The assistant can retrieve and answer questions based on personal documents (like PDFs). It’s a practical implementation that leverages the power of LangChain, FAISS vector stores, and Ollama models.

## Features
- Use of **RAG models** to efficiently retrieve and generate answers from large documents.
- **Embeddings** with Ollama for document chunking and comparison.
- **FAISS vector store** for fast retrieval of document data.
- Customizable with your own PDFs to personalize the assistant’s knowledge.

## Setup and Installation

### Requirements

To run this project, you'll need to install the required dependencies listed in the `requirements.txt` file. You can install them with:

```bash
pip install -r requirements.txt
```

### Step-by-Step Guide

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your-username/RAG-Personalized-AI-Assistant.git
   cd RAG-Personalized-AI-Assistant
   ```

2. **Install dependencies:**

   Make sure you have all required libraries installed by running:

   ```bash
   pip install -r requirements.txt
   ```

3. **Replace the PDF file:**

   The assistant is pre-configured to use a sample PDF (`PEFT_LORA.pdf`). To personalize it with your own content, replace the `PEFT_LORA.pdf` with your own PDF file and rename it accordingly in the code. This file will be used for question answering.

   ```bash
   # Replace with your own PDF in the same directory
   PDF_FILE = "your_own_pdf_file.pdf"
   ```

4. **Run the code:**

   After replacing the PDF, you can run the script to test the AI assistant's capabilities:

   ```bash
   python your_script.py
   ```

   The assistant will now answer questions based on the content of your own document.

## Usage Example

```python
# Load your own PDF and start querying the assistant
loader = PyPDFLoader(PDF_FILE)
pages = loader.load()

# Example query
retriever.invoke("What is LoRA?")
```

### Customization
- Modify the **chunk size** and **chunk overlap** for better control over document splitting.
- Customize the **embedding model** or use a different vector store if needed.

## Suggested Improvements
- Experiment with different models or vector stores to optimize retrieval performance.
- Add support for handling multiple documents.
- Explore integrating this assistant with external APIs or UIs for wider use cases.



## Acknowledgments
Thanks to the creators of **Underfitted** for his tutorial. - https://www.youtube.com/watch?v=q9MD_hU2Yd8
```
