# DeepSeek RAG Application

![image](https://github.com/user-attachments/assets/902c1a05-f00e-4f07-b584-6f5311713e71)

With the emergence of DeepSeek R1, an efficient and cost-effective open-source model, building an optimized RAG system has become more accessible than ever. 
Retrieval-Augmented Generation (RAG) and Graph RAG have transformed the way AI systems interact with data. By combining powerful retrieval mechanisms with generative AI, RAG models deliver more accurate and contextually aware responses.

DeepSeek RAG is an innovative Retrieval-Augmented Generation (RAG) system that extracts information from PDF documents and provides precise answers to user queries by leveraging advanced language models. This project integrates powerful tools such as pdfplumber, FAISS, and Sentence Transformers with the state-of-the-art Groq API, which calls upon the DeepSeek R1 70B Distill model—one of the most advanced LLMs available today.

---

## Table of Contents

- [Overview](#overview)
- [Why DeepSeek RAG?](#why-deepseek-rag)
- [Features](#features)
- [Architecture](#architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Contributing](#contributing)

---

## Overview

DeepSeek RAG is designed to handle complex queries by:
- **Extracting Text from PDFs:** Using [pdfplumber](https://github.com/jsvine/pdfplumber) to extract textual data.
- **Chunking and Indexing:** Dividing the text into manageable chunks and indexing them using [FAISS](https://github.com/facebookresearch/faiss) for efficient similarity search.
- **Retrieving Contextual Information:** Utilizing [Sentence Transformers](https://www.sbert.net/) to create embeddings and retrieve the most relevant chunks based on user queries.
- **Answer Generation:** Leveraging the Groq API to call upon the **DeepSeek R1 Distill** model for generating high-quality answers.

---

## Why DeepSeek RAG?

### Superior Model Performance
- **State-of-the-Art LLM:** DeepSeek R1 Distill is a top-notch open source model known for its robust performance in understanding and generating human-like text.
- **Optimized for Accuracy:** With its advanced architecture, DeepSeek R1 Distill outperforms many other models in delivering precise and contextually relevant responses.

### Enhanced Retrieval Capabilities
- **Contextual Awareness:** By combining retrieval methods with generation capabilities, DeepSeek RAG ensures that responses are grounded in the actual content of the source documents.
- **Efficient Query Handling:** The integration of FAISS and Sentence Transformers ensures that even large PDF documents can be processed quickly and accurately.

### Groq API Integration
- **Cutting-Edge Technology:** The Groq API provides a robust and scalable interface for accessing deep learning models, making it easier to integrate and deploy advanced LLMs in production.
- **Flexibility and Scalability:** With the Groq API, this project can easily scale to handle larger datasets and more complex queries, ensuring a seamless user experience.

---

## Features

- **PDF Text Extraction:** Accurately extracts text from PDF documents using pdfplumber.
- **Intelligent Chunking:** Splits long texts into manageable chunks for better context retrieval.
- **Semantic Search:** Employs FAISS and Sentence Transformers to find the most relevant content based on the query.
- **High-Quality Answer Generation:** Uses the DeepSeek R1 Distill model via the Groq API for generating insightful answers.
- **Interactive Web UI:** A user-friendly Gradio interface allows users to upload PDFs, ask questions, and view answers interactively.
- **Customizable UI:** With integrated custom CSS and layout enhancements, the UI is both visually appealing and easy to use.

---

## Architecture

1. **PDF Extraction:**  
   The system uses `pdfplumber` to read and extract text from PDF files.

2. **Text Processing and Chunking:**  
   Extracted text is divided into smaller, manageable chunks to preserve context and improve retrieval accuracy.

3. **Embedding and Indexing:**  
   Chunks are encoded using the Sentence Transformers model and indexed with FAISS for fast similarity search.

4. **Retrieval:**  
   User queries are encoded and matched against the indexed chunks to retrieve the most relevant pieces of text.

5. **Answer Generation:**  
   The retrieved context is fed into the Groq API, which calls the DeepSeek R1 Distill model to generate a high-quality answer.

6. **User Interface:**  
   An interactive Gradio UI provides an easy way for users to interact with the system—uploading PDFs and asking queries directly through the web interface.

---

![image](https://github.com/user-attachments/assets/52abe65b-16ca-4994-b527-ec8282e6ef5d)


---

## Installation

### Prerequisites

- Python 3.7+
- pip

### Required Packages

Install the necessary Python packages with:

```bash
pip install pdfplumber faiss-cpu sentence-transformers groq gradio
```

---

## Usage

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/deepseek-rag.git
   cd deepseek-rag
   ```

2. **Configure the Groq API Key:**

   In your code, replace the placeholder API key with your actual Groq API key:

   ```python
   client = Groq(api_key='YOUR_GROQ_API_KEY')
   ```

3. **Run the Application:**

   Execute the script to start the Gradio web UI:

   ```bash
   python your_script.py
   ```

4. **Interact via Web UI:**

   - Upload your PDF using the provided file uploader.
   - Enter your query in the text box.
   - Click "Get Answer" to retrieve the response generated by the DeepSeek R1 Distill model.

---

## Project Structure

```
deepseek-rag/
│
├── README.md             # Project documentation
├── requirements.txt      # Python dependencies
├── your_script.py        # Main application script (Gradio UI, PDF processing, etc.)
└── assets/
    └── header_image.png  # (Optional) Custom header image for the UI
```

---

## Contributing

Contributions are welcome! If you'd like to improve DeepSeek RAG, please fork the repository and create a pull request with your proposed changes. For major changes, please open an issue first to discuss what you would like to change.

---

*DeepSeek RAG leverages state-of-the-art technology to deliver accurate, contextually rich answers by combining efficient retrieval mechanisms with the advanced DeepSeek R1 Distill model. Experience the power of DeepSeek and transform the way you interact with complex documents!*

---
