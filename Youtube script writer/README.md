# YouTube Script Writer

Welcome to the **YouTube Script Writer**! This tool helps you generate engaging YouTube video scripts based on your input. By leveraging the power of OpenAI's language models and DuckDuckGo's search engine, you can create compelling content with ease.

## Project Structure

- **app.py**: The main script that initializes the OpenAI model and LangChain pipeline, and handles script generation.
- **utils.py**: Contains utility functions for generating video scripts.
- **requirements.txt**: Lists all required Python packages.
- **README.md**: This documentation file.

## Features

- **Customizable Script Generation**: Enter a topic and specify the video length and creativity level.
- **API Integration**: Requires OpenAI API key to generate content.
- **Search Engine Integration**: Uses DuckDuckGo to enrich video scripts with relevant information.

## Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/yourusername/youtube-script-writer.git
    cd youtube-script-writer
    ```

2. **Install the required packages:**

    ```bash
    pip install -r requirements.txt
    ```

3. **Obtain an OpenAI API key**: [Sign up for an API key](https://platform.openai.com/signup) if you don’t have one.

## Usage

1. **Run the application:**

    ```bash
    python app.py
    ```

2. **Enter your API key** in the sidebar.

3. **Provide the topic of the video** in the text input field.

4. **Specify the expected video length** in minutes.

5. **Set the creativity level** using the slider (0.0 LOW, 1 HIGH).

6. **Click "Generate Script for me"** to create your video script.

7. **Review the generated script** along with a suggested title and relevant search engine results.

   For example, if you enter the text:
   
    ```plaintext
    Extract all the unique values from column "age"
    ```

   You will get a SQL query snippet output like:
   
    ```sql
    SELECT DISTINCT age
    FROM table_name;
    ```

   Note: Replace `table_name` and `age` with your actual table and column names as needed.

## Contributing

Feel free to fork the repository and submit pull requests. Contributions are welcome!

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- **OpenAI** for providing powerful language models.
- **LangChain** for facilitating prompt-based interactions with language models.
- **DuckDuckGo** for search engine capabilities.

## Tags

- `YouTube`
- `Script Generation`
- `OpenAI`
- `LangChain`
- `DuckDuckGo`
- `Python`
- `AI`
- `NLP`
