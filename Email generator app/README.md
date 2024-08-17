# Email Generator App

## Overview

The Email Generator App is a Streamlit-based application that utilizes transformer models to generate personalized emails based on user input. By leveraging the Llama-2-7B-Chat model, this app allows users to create emails with various styles and topics, streamlining the email composition process.

## Features

- **Email Generation**: Generate emails with specified topics, sender and recipient details, and styles.
- **Customizable Styles**: Choose from multiple writing styles including Formal, Appreciating, Not Satisfied, and Neutral.
- **Transformer Model**: Uses the Llama-2-7B-Chat model for high-quality email generation.

## Setup

### Clone the Repository

```bash
git clone https://github.com/yourusername/email-generator-app.git
```

### Navigate to the Project Directory:

```bash
cd email-generator-app
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
2. Enter the email topic in the text area.
3. Fill in the sender and recipient names.
4. Select the desired writing style.
5. Click the "Generate" button to create the email.
6. Review the generated email response displayed below the button.

## Project Structure

- **`app.py`**: The main Streamlit application script that handles user input and generates emails.
- **`requirements.txt`**: A list of required Python packages.
- **`.env`**: Configuration file for environment variables (create this file as needed).

## Example Code

Here is an example of how to use the app:

1. Enter a topic, such as "Meeting Reminder."
2. Input the sender and recipient names.
3. Select a style, such as "Formal."
4. Click "Generate" to see the email output.

## Contributing
Feel free to fork the repository and submit pull requests. Contributions are welcome!

## License
This project is licensed under the MIT License
