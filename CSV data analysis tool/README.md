# CSV Data Analysis Tool

This project provides a user-friendly interface for analyzing CSV data using natural language queries. Built with `Streamlit`, it allows users to upload CSV files and ask questions about the data. The queries are processed through a powerful AI agent, powered by OpenAI’s `GPT`, and integrated with `LangChain` for efficient data handling. 

## Key Features

- **Natural Language Querying**: Easily ask questions about your CSV data in plain English.
- **AI-Powered Analysis**: Uses OpenAI’s language model to intelligently interpret and process queries.
- **Seamless Integration with Pandas**: Leverages the Pandas library to load, manipulate, and query CSV data.
- **Interactive UI**: Built with `Streamlit`, the application offers a simple, interactive UI for users to upload CSV files and analyze them.
- **Customizable and Extensible**: Easily adaptable for more complex datasets and use cases.

## Why This Project?

I created this project to demonstrate how AI and natural language processing can simplify data analysis. Instead of writing complex code or SQL queries, users can now interact with their data by typing questions in everyday language. This project showcases my skills in:
- AI/ML Integration
- Full-Stack Development
- Data Processing & Analysis
- Cloud Technologies

The codebase is clean, extensible, and follows best practices. 

## Installation

To get started with this project, clone the repository and install the dependencies:

```bash
git clone https://github.com/yourusername/csv-data-analysis-tool.git
cd csv-data-analysis-tool
pip install -r requirements.txt
```

Usage
Once all the dependencies are installed, you can run the application with the following command:
```bash
streamlit run app.py
```

This will launch the Streamlit app in your web browser.

### Step-by-Step Guide

- **Upload CSV File**: Upload a CSV file that contains the data you want to analyze.
- **Enter Your Query**: Type a natural language query in the text area. For example, “What is the average sales for the year 2023?” or “List the top 10 highest selling products.”
- **Generate Response**: Click on the "Generate Response" button to get an answer to your query.

### Project Structure

- **app.py**: The main script that runs the Streamlit application.
- **utils.py**: Contains the core logic for querying the CSV data using LangChain and OpenAI.
- **requirements.txt**: Lists all the required dependencies to run the project.

### Example Queries

- What is the average value in the "Sales" column?
- Show me the top 5 rows of the dataset.
- What is the total count of items in the "Category" column?

### Technical Overview

- **Streamlit**: The front-end framework used for building the interactive UI for uploading files and entering queries.
- **LangChain**: Provides an abstraction for interacting with the Pandas DataFrame and integrates seamlessly with OpenAI’s models.
- **OpenAI’s GPT**: Powers the natural language processing and interpretation of queries to perform intelligent data analysis.
- **Pandas**: Used to load and manipulate the CSV data.
- **dotenv**: Used for loading environment variables such as API keys securely.

### Requirements

Ensure you have the following installed:

- **Python 3.8+**
- **pip** for managing Python packages

Dependencies are listed in the `requirements.txt` file:

- `langchain`
- `streamlit`
- `openai`
- `tiktoken`
- `python-dotenv`
- `pinecone-client`

You can install all dependencies by running:

```bash
pip install -r requirements.txt
```

### Environment Variables

This project requires the following environment variables. You can create a `.env` file in the root directory with the necessary keys:

```bash
OPENAI_API_KEY=your_openai_api_key
PINECONE_API_KEY=your_pinecone_api_key
```


### Contributing

Feel free to fork this repository, open issues, or submit pull requests if you'd like to contribute to this project. Contributions of all kinds are welcome!

### Future Improvements

- Add support for more file types (e.g., Excel).
- Incorporate visualization features for better data insights.
- Enable cloud-based CSV file storage for users.

### License

This project is licensed under the MIT License.

