# Sithafal

Project Overview

The project aims to build a simple question-answering system using semantic search. It scrapes content from multiple websites, chunks the text, generates embeddings using Sentence Transformers, and stores them in a FAISS vector database. When a user queries the system, it retrieves relevant chunks based on semantic similarity and presents them as context.

Approach

Data Collection: Scrape content from websites using requests and BeautifulSoup. If a website is JavaScript-rendered, use Selenium for scraping.
Text Processing: Chunk the scraped text into smaller pieces to manage context window size for embeddings.
Embedding: Generate embeddings for each text chunk using a pre-trained Sentence Transformer model (all-MiniLM-L6-v2).
Vector Database: Store the embeddings in a FAISS vector database for efficient similarity search.
Query Handling: Embed the user's query, perform a similarity search against the vector database, and retrieve the most relevant chunks.
Response Generation: Combine the query and relevant context to generate a response.
Outcomes

The project demonstrates a basic question-answering system. When provided with a query, it retrieves relevant passages from the scraped websites, giving users contextual information to answer their questions.

Steps to Clone and Run on Colab

Clone the repository:
 
!git clone https://github.com/ChaitrikaBiswal/Sithafal.git



Navigate to the project directory: 
%cd repository


Install dependencies: 
!pip install requests beautifulsoup4 sentence-transformers faiss-cpu


Additional Notes


The project utilizes various libraries like requests, BeautifulSoup, Sentence Transformers, and faiss. They will be installed automatically during step 3.
