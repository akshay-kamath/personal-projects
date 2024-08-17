# Code Review Analyst

Welcome to **Code Review Analyst**, a Streamlit application designed to provide code reviews for Python files. This project leverages OpenAI's ChatGPT model to offer detailed suggestions and improvements for Python code, helping developers enhance their coding practices.

## Features

- **Upload Python Files**: Easily upload your `.py` files for review.
- **Automated Code Review**: Receive detailed feedback on your code with suggestions for improvement.
- **Download Review**: Get a downloadable file with the review comments for your records.

## How It Works

1. **Upload Your Python Code**: Use the file uploader to submit your `.py` file.
2. **Receive a Detailed Review**: The application reads the code and interacts with OpenAI's GPT model to analyze it and provide suggestions.
3. **Download Your Review**: After the review is completed, download the analysis as a text file.

## Installation

### Requirements

Make sure you have Python installed on your machine. You will also need to install the required packages listed in `requirements.txt`. You can install them using pip:

```bash
pip install -r requirements.txt
```

# Setup and Usage

## Setup

### Clone the Repository:

```bash
git clone https://github.com/yourusername/code-review-analyst.git
```

##Navigate to the Project Directory:
```bash
cd code-review-analyst
```

Set Up Environment Variables:

Create a .env file in the project directory and add your OpenAI API key:
```bash
OPENAI_API_KEY=your_openai_api_key_here
```

## Run the Application

Start the Streamlit app:

```bash
streamlit run app.py
```

## Usage

1. Open your web browser and navigate to the Streamlit app URL (usually [http://localhost:8501](http://localhost:8501)).
2. Upload your Python `.py` file using the file uploader.
3. Review the suggestions provided by the ChatGPT model.
4. Download the review file for detailed feedback.

## Project Structure

- `app.py`: The main Streamlit application script.
- `code.py`: An example Python file used for testing the application.
- `requirements.txt`: A list of required Python packages.
- `.env`: Configuration file for environment variables (create this file as needed).


## Contributing

Feel free to fork the repository and submit pull requests. Contributions are welcome!

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Streamlit for their amazing framework.
- OpenAI for providing the powerful GPT models.
