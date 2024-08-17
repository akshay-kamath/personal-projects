# Invoice Extraction Bot

## Overview

The **Invoice Extraction Bot** is a tool designed to help you extract data from PDF invoices. This application uses language models to parse and extract key information such as invoice number, description, quantity, date, unit price, amount, total, email, phone number, and address from your invoices.

## Features

- **PDF Upload**: Upload multiple PDF invoices for data extraction.
- **Data Extraction**: Extracts critical information from invoices using advanced language models.
- **CSV Download**: Download the extracted data in CSV format for further analysis.
- **User-Friendly Interface**: Built with Streamlit for an interactive and intuitive user experience.

## Getting Started

### Prerequisites

Ensure you have the following installed:

- Python 3.7 or higher
- Streamlit
- Other dependencies listed in `requirements.txt`

### Clone the Repository:

```bash
git clone https://github.com/yourusername/invoice-extraction-bot.git
```

### Navigate to the Project Directory

```bash
cd invoice-extraction-bot
```

## Set Up Environment Variables

Create a `.env` file in the project directory and add the following keys:

```bash
OPENAI_API_KEY=your_openai_api_key_here
```

## Install Dependencies
Install the required Python packages using the provided requirements.txt:

```bash
pip install -r requirements.txt
```

## Run the Application

Start the Streamlit app:

```bash
streamlit run app.py
```

# Invoice Extraction Bot

## Usage

1. Open your web browser and navigate to the Streamlit app URL (usually `http://localhost:8501`).
2. Upload your PDF invoices using the file uploader.
3. Click the "Extract Data" button to process the invoices.
4. Review the extracted data displayed below.
5. Download the data as a CSV file if needed.

## Project Structure

- **`app.py`**: The main Streamlit application script that handles file uploads, processes the PDFs, and displays results.
- **`utils.py`**: Contains functions for extracting text from PDFs and processing the extracted text using language models.
- **`requirements.txt`**: A list of required Python packages.
- **`.env`**: Configuration file for environment variables (create this file as needed).

## Example Code

Here is an example of how to use the app:

1. Upload a PDF invoice, such as one in the "Invoice" folder.
2. Click "Extract Data" to extract information from the invoice.
3. Review the extracted data displayed on the page.
4. Download the data as a CSV file if needed.

## Contributing

Feel free to fork the repository and submit pull requests. Contributions are welcome!

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- **Streamlit** for their amazing framework.
- **OpenAI** for providing powerful language models.
- **LangChain** for facilitating prompt-based interactions with language models.
- **PyPDF** for PDF text extraction capabilities.


```
