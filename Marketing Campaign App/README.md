# Marketing Campaign App

Welcome to the **Marketing Campaign App**! This app is designed to generate marketing content tailored to different age groups and specific tasks. Using advanced language models, it helps create sales copies, tweets, and product descriptions with a touch of personalization.

## Features

- **Custom Content Generation**: Generate content based on selected age group and task type.
- **Versatile Use**: Suitable for creating sales copies, tweets, or product descriptions.
- **Personalization**: Tailor the content for kids, adults, or senior citizens.

## Project Structure

- **`app.py`**: The main Streamlit application script that handles user input, generates content, and displays results.
- **`requirements.txt`**: A list of required Python packages.
- **`.env`**: Configuration file for environment variables (create this file as needed).

## Installation

### Clone the Repository:

```bash
git clone https://github.com/yourusername/marketing-campaign-app.git
```

### Navigate to the Project Directory

```bash
cd marketing-campaign-app
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

## Usage

1. Open your web browser and navigate to the Streamlit app URL (usually [http://localhost:8501](http://localhost:8501)).
2. Enter the text you want to generate content for in the text area.
3. Select the action to be performed:
   - Write a sales copy
   - Create a tweet
   - Write a product description
4. Choose the age group:
   - Kid
   - Adult
   - Senior Citizen
5. Set the word limit using the slider.
6. Click the "Generate" button to create the content.
7. Review the generated content displayed below.

## Example Code

Here is an example of how to use the app:

1. Enter a topic, such as "New Product Launch."
2. Select "Write a sales copy" as the action to be performed.
3. Choose "Adult" as the age group.
4. Set the word limit to 100.
5. Click "Generate" to see the content output.

## Contributing

Feel free to fork the repository and submit pull requests. Contributions are welcome!

## License

This project is licensed under the MIT License

## Acknowledgments

- **Streamlit** for their amazing framework.
- **OpenAI** for providing powerful language models.
- **LangChain** for facilitating prompt-based interactions with language models.

