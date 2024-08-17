# Customer Care Summary Alert

## Overview

The **Customer Care Summary Alert** project provides an automated solution to summarize customer care call recordings. The application uses OpenAI's language model, Zapier integration for email sending, and Whisper for transcription. This tool is ideal for businesses needing to efficiently handle and respond to customer interactions by summarizing and sending key information via email.

## Features

- Upload and process multiple .mp3 files.
- Automatically transcribe call recordings.
- Generate summaries using OpenAI's language model.
- Send summarized information via email using Zapier integration.

## Setup

### Navigate to the Project Directory:

```bash
cd customer-care-summary-alert
```

## Set Up Environment Variables

Create a `.env` file in the project directory and add the following keys:

```bash
OPENAI_API_KEY=your_openai_api_key_here
ZAPIER_NLA_API_KEY=your_zapier_nla_api_key_here
```

## Run the Application

Start the Streamlit app:

```bash
streamlit run app.py
```

## Usage

1. Open your web browser and navigate to the Streamlit app URL (usually [http://localhost:8501](http://localhost:8501)).
2. Upload your recorded .mp3 files using the file uploader.
3. Review the uploaded files and click "Send Email" to process and send the summary.
4. The system will transcribe the audio, summarize it, and send the summary via email.

## Project Structure

- `app.py`: The main Streamlit application script that handles file uploads and triggers email sending.
- `utils.py`: Contains functions for transcription using Whisper, summarization using OpenAI, and email sending via Zapier.
- `requirements.txt`: A list of required Python packages.
- `.env`: Configuration file for environment variables (create this file as needed).

## Contributing

Feel free to fork the repository and submit pull requests. Contributions are welcome!

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Streamlit for their amazing framework.
- OpenAI for providing the powerful GPT models.
- Whisper for transcription capabilities.
- Zapier for integrating email functionalities.
