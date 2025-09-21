<img width="1916" height="862" alt="image" src="https://github.com/user-attachments/assets/a339b37f-32ef-460f-9351-be39bd5b86a0" />

🧠 Project Overview
This application is a Medical Domain Chatbot built using Retrieval-Augmented Generation (RAG). It allows users to upload their own medical documents (e.g., textbooks, reports), and the system intelligently answers queries by retrieving the most relevant content before generating a final response.

🎓 What is RAG?
RAG (Retrieval-Augmented Generation) enhances language models by supplying relevant external context from a knowledge base, preventing hallucinations and improving accuracy, especially for factual or specialized domains like medicine.

🔄 Architecture
User Input
   ↓
Query Embedding → Pinecone Vector DB ← Embedded Chunks ← Chunking ← PDF Loader
   ↓
Retrieved Docs
   ↓
     RAG Chain (Groq + LangChain)
   ↓
LLM-generated Answer

📚 Features
Upload medical PDFs (notes, books, etc.)
Auto-extracts text and splits into semantic chunks
Embeds using Google/BGE embeddings
Stores vectors in Pinecone DB
Uses Groq's LLaMA3-70B via LangChain
FastAPI backend with endpoints for file upload and Q&A

🌐 Tech Stack
Component	    Tech Used

LLM	          Groq API (LLaMA3-70B)
Embeddings  	Google Generative AI / BGE
Vector DB    	Pinecone
Framework     LangChain
Backend	      FastAPI
Deployment	  Render


