# Nvidia NIM-Powered RAG Q&A

This project demonstrates how to use NVIDIA NIM (Neural Information Model) with LangChain and FAISS for document retrieval and question-answering. The application processes PDF documents, embeds them using NVIDIAEmbeddings, and enables users to query the embedded knowledge base using a Streamlit web interface.

## Features
- Load and process PDF documents from the `us_census` directory.
- Embed documents using NVIDIA AI endpoints.
- Store and retrieve document vectors using FAISS.
- Answer user queries based on embedded document knowledge.
- Display document similarity search results.

## Installation

Ensure you have Python installed (>=3.8), then install the required dependencies:

```bash
pip install -r requirements.txt
```

## Required Dependencies  
The project relies on the following packages:  

- `openai`  
- `langchain_nvidia_ai_endpoints`  
- `langchain_community`  
- `faiss-cpu`  
- `python-dotenv`  
- `streamlit`  
- `pypdf`  

## Setup  

### Set Up Environment Variables  

Create a `.env` file in the project directory and add your NVIDIA API key: 

```bash
NVIDIA_API_KEY=your_nvidia_api_key  
```

Alternatively, set the environment variable directly in your shell:

```bash
export NVIDIA_API_KEY=your_nvidia_api_key
```

## Usage
Run the Streamlit application:

```bash
streamlit run app.py
```

## Workflow
1. Click the "Documents Embedding" button to process and store document embeddings.
2. Enter a query in the text input field.
3. The system will retrieve and answer the query based on the stored embeddings.
4. Expand "Document Similarity Search" to view the retrieved document chunks.

## Project Structure
```
├── 📜  us_census/              # Directory containing PDF documents
├──  app.py                      # Main Streamlit application
├──  .env                        # Environment variables (ignored in .gitignore)
├──  requirements.txt            # List of dependencies
├──  README.md                   # Project documentation
```
## Performance Considerations

- The vector database is stored in memory; for large scale applications, consider using a persistent vector store.
- NVIDIA AI endpoints require an active API key, ensure you have sufficient quota.
- Document processing may take time depending on file size and number of documents.

## License

This project is open-source and free to use under the MIT License.
