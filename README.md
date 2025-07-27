# Job-Matching-System

An advanced NLP-based job recommendation system that matches resumes with relevant job descriptions using transformer embeddings and domain-specific keyword techniques. The project integrates Pinecone (a vector database) for efficient similarity search and provides ranked job recommendations.

## Project Overview

The goal is to bridge the gap between job seekers and employers by leveraging semantic understanding of resumes and job descriptions rather than relying solely on keyword matching. The system processes resumes and job descriptions, generates embeddings using the `all-MiniLM-L6-v2` transformer model, and combines them with custom domain-specific embeddings for better accuracy. Pinecone is used as the storage and retrieval backend for high-performance similarity searches.

## Key Features

- Resume Parsing - Extracts text from PDF resumes using PdfReader.
- Transformer-based Embeddings - Uses the 'all-MiniLM-L6-v2' model for generating semantic embeddings.
- Custom Keyword Embeddings - Incorporates domain knowledge by embedding skills and keywords with custom weight relationships.
- Pinecone Vector Database - Stores job embeddings with metadata and supports fast similarity searches.
- Ranked Job Recommendations - Provides top job matches with similarity scores.
- Scalable & Efficient - Optimized for large datasets with real-time querying.

## Methodology

- Text Extraction – Convert PDF resumes into plain text.
- Preprocessing – Lowercasing, tokenization, and splitting long texts into chunks.
- Embedding Generation - Capturing semantic context (Transformer Embeddings) and Skill-based keyword vector representation (Custom Embeddings).
- Embedding Combination – Weighted concatenation of transformer and custom embeddings.
- Indexing & Querying – Storing embeddings in Pinecone and retrieving top matches based on cosine similarity.
- Ranking – Jobs are ranked by similarity scores.

## Getting Started

- Clone the repository and navigate to the project directory.
- Open `NLP_Job_Matching_System.ipynb` in Jupyter Notebook or google colab.
- Install required dependencies.
- Make an account on ngrok and copy the authentication token.
- Place the token on the line !ngrok authtoken "PLACE_YOUR_NGROK_AUTH_TOKEN_HERE"
- Run all cells to generate embeddings and get job recommendations and launch the app using streamlit 
- Open the URL shown in the terminal to access the app in your browser.
- Upload your resume in text/PDF format.
- View the ranked job recommendations with similarity scores.
