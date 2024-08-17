# Text To SQL Query Helper Tool

The **Text To SQL Query Helper Tool** is a Python application designed to convert natural language descriptions into SQL query snippets. This tool leverages Hugging Face's transformer models and LangChain's pipelines to generate accurate and efficient SQL queries from textual input.

## Features

- Convert natural language descriptions into SQL queries.
- Use state-of-the-art models from Hugging Face.
- Customizable and extendable for various SQL query needs.

## Prerequisites

- Python 3.7 or higher
- An active Hugging Face account to obtain an API token for model access
- Required Python packages

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/Text_To_SQL_Query_Helper_Tool.git
   cd Text_To_SQL_Query_Helper_Tool
    ```
2. **Install the required Python packages**:

```bash
pip install -r requirements.txt
```
3.**Login to Hugging Face**

You need a Hugging Face API token to access the model. Use the following command to log in:

```python
from huggingface_hub import login
login("your_huggingface_token")
```
Replace "your_huggingface_token" with your actual Hugging Face API token.

# Usage

1. **Run the application:**

   ```bash
   python app.py
    ```

2. **Enter your text description for the SQL query**

   For example, you can use the following text:

   ```plaintext
   Extract all the unique values from column "age"
    ```

3. **Get the SQL Query Snippet Output**

The application will process your input and generate a SQL query. For the given example, the output would be:

```sql
SELECT DISTINCT age
FROM table_name;
```

# Project Structure

## `app.py`
The main script that initializes the Hugging Face model and LangChain pipeline, and handles query generation.

## `requirements.txt`
Lists all required Python packages.

## `README.md`
This documentation file.

# Contributing
Feel free to fork the repository and submit pull requests. Contributions are welcome!

# License
This project is licensed under the MIT License - see the LICENSE file for details.

# Acknowledgments
- Hugging Face for providing powerful transformer models.
- LangChain for facilitating prompt-based interactions with language models.

