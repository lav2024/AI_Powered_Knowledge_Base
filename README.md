# 📚 AI-Powered Knowledge Base

An AI-powered knowledge base that allows users to upload PDF documents, ask questions about their content, and receive context-grounded answers with source citations.

Built using **LangChain, ChromaDB, HuggingFace, Google Gemini, and Gradio**, this project implements a Retrieval-Augmented Generation (RAG) pipeline to make document search and information retrieval easier.

## 🚀 Features

- **PDF Ingestion:** Upload and process multiple PDF documents.
- **Text Extraction:** Extract text from PDF documents while preserving page numbers and source filenames.
- **Text Chunking:** Split extracted content into smaller, overlapping chunks using LangChain.
- **Semantic Embeddings:** Generate text embeddings using HuggingFace Sentence Transformers.
- **Vector Database:** Store and retrieve document embeddings using ChromaDB.
- **AI-Powered Question Answering:** Use Google Gemini to generate answers based on retrieved document content.
- **Source Citations:** Display source PDF filenames and page numbers alongside generated answers.
- **Interactive Chatbot:** Ask questions and interact with your documents through a Gradio interface.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Google Colab | Development environment |
| LangChain | RAG pipeline and document processing |
| PyPDF | PDF text extraction |
| HuggingFace | Text embedding generation |
| ChromaDB | Vector database |
| Google Gemini | AI-powered answer generation |
| Gradio | Interactive chatbot interface |

## 🏗️ Project Architecture

```text
             PDF Documents
                   |
                   v
             PDF Extraction
                   |
                   v
              Text Chunking
                   |
                   v
          HuggingFace Embeddings
                   |
                   v
               ChromaDB
                   |
                   v
             User Question
                   |
                   v
          Semantic Retrieval
                   |
                   v
           Relevant Context
                   |
                   v
              Gemini LLM
                   |
                   v
          Grounded AI Answer
                   |
                   v
         Source Citations
                   |
                   v
           Gradio Chatbot
```

## ⚙️ How It Works

1. Users upload one or more PDF documents.
2. PyPDF extracts text from each document while retaining page information.
3. LangChain's text splitter divides the extracted text into manageable chunks.
4. HuggingFace converts the chunks into numerical embeddings.
5. ChromaDB stores the embeddings and associated document metadata.
6. When a user asks a question, the retriever searches for the most relevant chunks.
7. The retrieved context is passed to Google Gemini.
8. Gemini generates an answer based on the provided document content.
9. The chatbot displays the answer along with source filenames and page numbers.

## 📦 Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/AI-Powered-Knowledge-Base.git

cd AI-Powered-Knowledge-Base
```

### 2. Open the notebook

Upload or open `AI_Powered_Knowledge_Base.ipynb` using Google Colab.

### 3. Install dependencies

```python
!pip install -q langchain langchain-community langchain-text-splitters langchain-chroma chromadb pypdf sentence-transformers gradio google-generativeai langchain-huggingface langchain-google-genai
```

### 4. Configure Gemini API

- Generate an API key using [Google AI Studio](https://aistudio.google.com/apikey).
- Enter the API key securely when prompted in the notebook.
- Never upload your API key to GitHub.

### 5. Run the notebook

Execute the notebook cells in sequence to:

- Upload PDF documents.
- Extract and split text.
- Generate embeddings.
- Create the ChromaDB vector store.
- Initialize the Gemini model.
- Launch the Gradio chatbot.

## 💬 Example Use Cases

- Research paper analysis.
- Company document search.
- Technical documentation assistance.
- Information retrieval from multiple PDFs.
- AI-powered document question answering.

## 🔒 Important Notes

- Answers are generated using the retrieved document context.
- If the retrieved context does not contain sufficient information, the chatbot is instructed to acknowledge this.
- Source citations identify the retrieved PDF filename and page number; they do not guarantee that every individual claim has been independently verified.
- The ChromaDB database currently uses a local persistence directory in the Colab environment. Runtime storage is temporary.
- A valid Google Gemini API key is required for AI-generated answers.

## 🔮 Future Improvements

- Support for additional document formats such as DOCX and TXT.
- Improved citation accuracy with passage-level references.
- Persistent vector database storage.
- Document upload directly through the chatbot interface.
- Enhanced chatbot UI and conversation management.
- Deployment as a standalone web application.

## 👩‍💻 Author

**Lavanya R**

- GitHub: [@lav2024](https://github.com/lav2024)

---

⭐ If you find this project useful, consider giving the repository a star!
