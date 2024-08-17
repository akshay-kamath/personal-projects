# MCQ Creator App

This app creates multiple-choice questions (MCQs) from document data using text embeddings and a transformer model. It leverages the LangChain, OpenAI, Hugging Face, Pinecone, and other libraries for document processing, text embedding, and vector-based retrieval.

## Table of Contents

- [Introduction](#introduction)
- [Install & Import Dependencies](#install--import-dependencies)
- [Load Documents](#load-documents)
- [Transform Documents](#transform-documents)
- [Generate Text Embeddings](#generate-text-embeddings)
- [Vector Store - PINECONE](#vector-store---pinecone)
- [Retrieve Answers](#retrieve-answers)
- [Structure the Output](#structure-the-output)
- [How to Use](#how-to-use)
- [Credits](#credits)

## Introduction

This project is an MCQ creator that uses text embeddings for efficient data retrieval from documents. It handles document loading, text splitting, and embedding, allowing users to extract key information from documents to generate MCQs.

## Install & Import Dependencies

First, ensure you have all the required libraries installed. You can install them using the following commands:

```bash
pip install unstructured
pip install tiktoken
pip install pinecone-client
pip install pypdf
pip install langchain openai sentence-transformers
```

### Environment Setup

Ensure you have your API keys set up for OpenAI and Hugging Face Hub by configuring your environment variables as shown below:

```python
import os
os.environ["OPENAI_API_KEY"] = "<OPENAI_API_KEY>"
os.environ["HUGGINGFACEHUB_API_TOKEN"] = "<HUGGINGFACEHUB_API_TOKEN>"
```
Replace <OPENAI_API_KEY> and <HUGGINGFACEHUB_API_TOKEN> with your actual API keys from OpenAI and Hugging Face Hub, respectively.

## Load Documents
The app reads PDF files from a directory and loads them into memory using the PyPDF library.

```python
def load_docs(directory):
    loader = PyPDFDirectoryLoader(directory)
    documents = loader.load()
    return documents

# Usage
directory = 'Docs/'
documents = load_docs(directory)
print(len(documents))
```

## Transform Documents
After loading the documents, they are split into smaller chunks for easier processing and text embedding.

```python
def split_docs(documents, chunk_size=1000, chunk_overlap=20):
    text_splitter = RecursiveCharacterTextSplitter(chunk_size=chunk_size, chunk_overlap=chunk_overlap)
    docs = text_splitter.split_documents(documents)
    return docs

# Usage
docs = split_docs(documents)
print(len(docs))
```

## Generate Text Embeddings
You can generate text embeddings using either OpenAI or Hugging Face models.

**Using OpenAI Embeddings**

```python
#Uncomment if using OpenAI for embeddings
#embeddings = OpenAIEmbeddings(model_name="ada")
```

**Using Hugging Face Embeddings**

```python
from langchain.embeddings.sentence_transformer import SentenceTransformerEmbeddings
embeddings = SentenceTransformerEmbeddings(model_name="all-MiniLM-L6-v2")
```

Test the embeddings model with a sample text:

```python
query_result = embeddings.embed_query("Hello Buddy")
print(len(query_result))
print(query_result)
```

## Vector Store - PINECONE
Store the embeddings in Pinecone, which is a vector store for fast and efficient retrieval of documents.

```python
pinecone.init(api_key="<PINECONE_API_KEY>", environment="us-west1-gcp")

index_name = "mcq-app"
if index_name not in pinecone.list_indexes():
    pinecone.create_index(index_name, dimension=384)

index = pinecone.Index(index_name)
```

## Retrieve Answers
Once the embeddings are stored, you can retrieve answers from the documents using vector queries.

```python
def retrieve_answers(query):
    query_embedding = embeddings.embed_query(query)
    result = index.query(queries=[query_embedding], top_k=3)
    return result

# Example usage
query = "What is India's capital?"
results = retrieve_answers(query)
print(results)
```

## Structure the Output
Format the retrieved documents and extract the relevant information for generating MCQs.

```python
def generate_mcq(question, answer, options):
    return {
        "question": question,
        "answer": answer,
        "options": options
    }

# Example usage
mcq = generate_mcq("What is the capital of India?", "Delhi", ["Delhi", "Mumbai", "Kolkata", "Chennai"])
print(mcq)
```

### How to Use

1. **Place your PDF documents in a `Docs/` directory.**
2. **Run the script** to load the documents, generate embeddings, and store them in Pinecone.
3. **Query the documents** using natural language, and retrieve answers based on the embeddings.
4. **Structure the answers** into multiple-choice questions (MCQs) and display them.

### Credits

This project uses the following libraries and APIs:

- [LangChain](https://github.com/hwchase17/langchain)
- [OpenAI](https://openai.com/)
- [Hugging Face](https://huggingface.co/)
- [Pinecone](https://www.pinecone.io/)
- [Unstructured](https://github.com/Unstructured-IO/unstructured)
- [PyPDF](https://pypdf.readthedocs.io/en/latest/)
