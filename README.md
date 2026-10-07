RAG Chatbot with ChromaDB and OpenAI
A simple Retrieval-Augmented Generation (RAG) chatbot built using Python, OpenAI, ChromaDB, and Streamlit. The application ingests company documents, stores vector embeddings in Chroma Vector Database, retrieves relevant context based on user queries, and generates accurate responses using an LLM.

🚀 Features
Document ingestion and vectorization
ChromaDB vector storage
Semantic document retrieval
Retrieval-Augmented Generation (RAG)
OpenAI Embeddings integration
Streamlit-based user interface
Persistent vector database storage
Company document Q&A chatbot
🏗️ Architecture
                +--------------------+
                | Company Documents  |
                | company.txt        |
                +---------+----------+
                          |
                          v
                +--------------------+
                | OpenAI Embeddings  |
                | text-embedding-3-small |
                +---------+----------+
                          |
                          v
                +--------------------+
                | ChromaDB           |
                | Vector Store       |
                +---------+----------+
                          |
                          v
User Question --> Generate Embedding
                          |
                          v
                Retrieve Top Matches
                          |
                          v
                    Build Context
                          |
                          v
                OpenAI GPT Model
                          |
                          v
                     Final Answer

---------------------------------------------------------------------------------------------------------------

📁Project Structure
rag-chroma-vector-db-app/
│
├── app.py # Streamlit UI
├── ingest.py # Document ingestion and embedding creation
├── rag.py # Retrieval and answer generation logic
├── requirements.txt # Project dependencies
│
├── documents/
│ └── company.txt # Source document
│
├── chroma_db/ # ChromaDB persistent storage
│
├── .env # Environment variables
│
└── README.md

🛠️ Technologies Used
Python
Streamlit
OpenAI API
ChromaDB
Retrieval-Augmented Generation (RAG)
Vector Embeddings
Python Dotenv

🔧 Prerequisites

Before running the application, ensure you have:

Python 3.10+
OpenAI API Key
Pip package manager
