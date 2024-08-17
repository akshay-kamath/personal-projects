# Resume Screening Assistant

## Overview

The **Resume Screening Assistant** is a Streamlit-based application designed to streamline the resume screening process for HR professionals. This tool allows users to upload resumes, compare them against a job description, and retrieve the most relevant documents based on a similarity search using Pinecone's vector database.

### Key Features:
- Upload multiple PDF resumes.
- Provide a job description to guide the screening process.
- Retrieve the most relevant resumes based on similarity to the job description.
- Get summaries of the relevant resumes using advanced language models.

## Installation

To get started with the Resume Screening Assistant, follow these steps:

1. **Clone the Repository:**

    ```bash
    git clone https://github.com/yourusername/resume-screening-assistant.git
    cd resume-screening-assistant
    ```

2. **Create a Virtual Environment:**

    ```bash
    python -m venv venv
    ```

3. **Activate the Virtual Environment:**

    - On Windows:
    
        ```bash
        venv\Scripts\activate
        ```

    - On macOS/Linux:
    
        ```bash
        source venv/bin/activate
        ```

4. **Install Required Packages:**

    ```bash
    pip install -r requirements.txt
    ```

5. **Set Up Environment Variables:**

    Create a `.env` file in the root directory and add your Pinecone API key and other necessary environment variables:

    ```env
    PINECONE_API_KEY=your_pinecone_api_key
    ```
6. ## Run the Application

Start the Streamlit app:

```bash
streamlit run app.py
```

## Usage

1. Open your web browser and navigate to the Streamlit app URL (usually http://localhost:8501).
2. Paste the job description into the "Please paste the 'JOB DESCRIPTION' here..." text area.
3. Specify the number of resumes you want to return in the "No.of 'RESUMES' to return" field.
4. Upload your PDF resumes using the file uploader.
5. Click the "Help me with the analysis" button to start the process.
6. Review the relevant resumes and their summaries displayed below.

## Project Structure

- `app.py`: The main Streamlit application script that handles file uploads, processes the PDFs, and displays results.
- `utils.py`: Contains functions for extracting text from PDFs, creating document embeddings, pushing and pulling data from Pinecone, and summarizing documents.
- `requirements.txt`: A list of required Python packages.
- `.env`: Configuration file for environment variables (create this file as needed).
- `Docs/`: Folder containing sample resumes for testing.

## Example Code

Here is an example of how to use the app:

1. Paste a job description, such as "Software Developer with experience in Python."
2. Specify the number of resumes to return, e.g., "5."
3. Upload a set of resumes from the "Docs" folder.
4. Click "Help me with the analysis" to see the relevant resumes and their summaries.

## Contributing

Feel free to fork the repository and submit pull requests. Contributions are welcome!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Streamlit](https://streamlit.io/) for their amazing framework.
- [OpenAI](https://openai.com/) for providing powerful language models.
- [LangChain](https://langchain.com/) for facilitating prompt-based interactions with language models.
- [Pinecone](https://pinecone.io/) for vector storage and similarity search capabilities.
- [PyPDF](https://github.com/py-pdf/pypdf) for PDF text extraction capabilities.

