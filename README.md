PDF Query System with Retrieval-Augmented Generation (RAG) Pipeline
Overview
This project implements a Retrieval-Augmented Generation (RAG) pipeline that allows users to interact with semi-structured data extracted from multiple PDF files. The system extracts, chunks, embeds, and stores the data for efficient retrieval. It answers user queries and performs comparisons, leveraging a pre-trained embedding model and OpenAI’s GPT-4 model to generate accurate, context-based responses.

Features
Data Ingestion: Extracts text from PDFs, segments it into logical chunks, and embeds the chunks using a pre-trained model.
Query Handling: Converts user queries into embeddings, performs similarity search in the stored embeddings, and generates detailed responses using OpenAI’s GPT-4 model.
Comparison Queries: Allows the user to request comparisons of data across multiple PDF files.
Response Generation: Generates detailed, context-aware responses by leveraging the retrieved chunks and the LLM model.
Functional Requirements
Data Ingestion:

Input: PDF files containing semi-structured data.
Process: Extract text, segment it into logical chunks, convert these chunks into vector embeddings, and store the embeddings in a vector database.
Query Handling:

Input: User’s natural language question.
Process: Convert the query into vector embeddings, perform a similarity search in the vector database, and generate a response using OpenAI’s GPT-4 model.
Comparison Queries:

Input: A user query requesting comparisons.
Process: Identify and extract relevant fields to compare, retrieve the corresponding chunks, and generate a structured comparison response.
Response Generation:

Input: Retrieved data and user query.
Process: Use OpenAI to generate responses with exact values and context while ensuring factual accuracy.
Installation
To run this project, ensure that you have the following dependencies installed:

PyPDF2: To extract text from PDFs.
sentence-transformers: To generate vector embeddings.
openai: To interact with OpenAI’s GPT models.
