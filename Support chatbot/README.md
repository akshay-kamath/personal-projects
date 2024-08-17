# Support Chatbot

Welcome to the **Support Chatbot** project! This tool is designed to assist users by integrating advanced AI capabilities to interact with website data and provide relevant information. Utilizing Hugging Face for language models and Pinecone for vector search, this chatbot enables intelligent, context-aware support.

## Project Structure

- **app.py**: The main Streamlit application script. Handles user inputs, manages API keys, and interacts with Pinecone and Hugging Face.
- **utils.py**: Contains utility functions for data fetching, processing, and interaction with Pinecone.
- **constants.py**: Stores configuration constants such as website URL and Pinecone settings.
- **requirements.txt**: Lists all required Python packages.
- **README.md**: This documentation file.

## Features

- **Data Integration**: Fetch data from a website sitemap and process it.
- **Chunking**: Splits data into manageable chunks for better search results.
- **Embeddings**: Creates embeddings for documents using Sentence Transformers.
- **Pinecone Integration**: Pushes and pulls data to/from Pinecone vector store.
- **Search Functionality**: Allows users to search for relevant documents based on queries.

## Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/yourusername/support-chatbot.git
    cd support-chatbot
    ```

2. **Install the required packages:**

    ```bash
    pip install -r requirements.txt
    ```

3. **Obtain API keys**:
   - **Hugging Face**: [Sign up for an API key](https://huggingface.co/signup) if you don’t have one.
   - **Pinecone**: [Get your API key here](https://www.pinecone.io/start/).

## Usage

1. **Run the Streamlit application:**

    ```bash
    streamlit run app.py
    ```

2. **Enter your API keys** in the sidebar:
   - Hugging Face API key
   - Pinecone API key

3. **Load Data to Pinecone**:
   - Click on "Load data to Pinecone" to fetch data from the website, split it into chunks, create embeddings, and push it to Pinecone.

4. **Search for Relevant Documents**:
   - Enter a query in the text input box.
   - Specify the number of links to return using the slider.
   - Click "Search" to retrieve relevant documents from Pinecone.

5. **Review the Results**:
   - The application will display search results including the document content and source links.

## Contributing

Feel free to fork the repository and submit pull requests. Contributions are welcome!

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- **Hugging Face** for providing powerful language models.
- **Pinecone** for its efficient vector database services.
- **Streamlit** for creating an interactive web application interface.

## Tags

- `AI`
- `Chatbot`
- `Support`
- `Hugging Face`
- `Pinecone`
- `Python`
- `Streamlit`
- `NLP`
- `Vector Search`
- `Web Scraping`

