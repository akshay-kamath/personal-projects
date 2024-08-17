# Spotify Playlist Project 🎧

This project is designed to generate custom Spotify playlists based on a given text prompt using OpenAI's GPT model and the Spotify API. The tool will create a playlist by suggesting songs that fit your desired mood, genre, or theme, then add those songs directly to your Spotify account.

## Features

- **Text-based playlist generation**: Input a text prompt (e.g., "super chill vibes") and get a custom playlist.
- **Integration with OpenAI GPT-4**: Uses the GPT-4 model to generate song suggestions based on the prompt.
- **Spotify API integration**: Automatically searches for tracks on Spotify and adds them to a new playlist in your account.
- **Customizable number of songs**: Choose how many songs you want in your playlist (between 1 and 50).

## Project Structure

- **app.py**: The main script that processes the user's prompt, generates a playlist using OpenAI's GPT-4, and interacts with the Spotify API to add the songs.
- **requirements.txt**: Lists all required Python packages.
- **README.md**: This documentation file.

## Installation

1. **Clone the repository**:

    ```bash
    git clone https://github.com/yourusername/spotify-playlist-project.git
    cd spotify-playlist-project
    ```

2. **Install dependencies**:

    Create a virtual environment (optional but recommended) and install the required packages:

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    pip install -r requirements.txt
    ```

3. **Set up your environment variables**:

    - Create a `.env` file in the root of the project and add your **Spotify** and **OpenAI** credentials:

    ```plaintext
    SPOTIFY_CLIENT_ID=your_spotify_client_id
    SPOTIFY_CLIENT_SECRET=your_spotify_client_secret
    OPENAI_API_KEY=your_openai_api_key
    ```

4. **Register a Spotify App**:

    - Go to the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/applications) and create a new application.
    - Copy your **Client ID** and **Client Secret**.
    - In the app settings, add `http://localhost:9999` as a redirect URI.
    - Add your Spotify account to the "Users and Access" section.

## Usage

1. **Run the script**:

    Use the following command to run the script and generate a playlist based on your prompt:

    ```bash
    python app.py -p "super chill vibes" -n 10
    ```

    - **`-p`**: The prompt describing the type of playlist you want to generate (e.g., "super happy songs").
    - **`-n`**: The number of songs you want in the playlist (default: 12, max: 50).

2. **OAuth2 Authorization**:

    The first time you run the script, you will be prompted to authenticate with Spotify. Open the provided link in your browser, log in, and authorize the application. After authorization, Spotify will redirect you to a non-existent `http://localhost:9999` page. Copy the redirected URL and paste it into the console to complete the process.

3. **Example**:

    ```bash
    python app.py -p "super happy summer songs" -n 15
    ```

    The above command will create a playlist with 15 songs based on the provided prompt and add it to your Spotify account.

## Example Output

Upon successfully running the script, you'll see output like this:


Here's a detailed README.md file for the spotify-playlist-project. It includes sections for project description, installation, usage, contributing, license, acknowledgments, and tags for GitHub.

markdown
Copy code
# Spotify Playlist Project 🎧

This project is designed to generate custom Spotify playlists based on a given text prompt using OpenAI's GPT model and the Spotify API. The tool will create a playlist by suggesting songs that fit your desired mood, genre, or theme, then add those songs directly to your Spotify account.

## Features

- **Text-based playlist generation**: Input a text prompt (e.g., "super chill vibes") and get a custom playlist.
- **Integration with OpenAI GPT-4**: Uses the GPT-4 model to generate song suggestions based on the prompt.
- **Spotify API integration**: Automatically searches for tracks on Spotify and adds them to a new playlist in your account.
- **Customizable number of songs**: Choose how many songs you want in your playlist (between 1 and 50).

## Project Structure

- **app.py**: The main script that processes the user's prompt, generates a playlist using OpenAI's GPT-4, and interacts with the Spotify API to add the songs.
- **requirements.txt**: Lists all required Python packages.
- **README.md**: This documentation file.

## Installation

1. **Clone the repository**:

    ```bash
    git clone https://github.com/yourusername/spotify-playlist-project.git
    cd spotify-playlist-project
    ```

2. **Install dependencies**:

    Create a virtual environment (optional but recommended) and install the required packages:

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    pip install -r requirements.txt
    ```

3. **Set up your environment variables**:

    - Create a `.env` file in the root of the project and add your **Spotify** and **OpenAI** credentials:

    ```plaintext
    SPOTIFY_CLIENT_ID=your_spotify_client_id
    SPOTIFY_CLIENT_SECRET=your_spotify_client_secret
    OPENAI_API_KEY=your_openai_api_key
    ```

4. **Register a Spotify App**:

    - Go to the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/applications) and create a new application.
    - Copy your **Client ID** and **Client Secret**.
    - In the app settings, add `http://localhost:9999` as a redirect URI.
    - Add your Spotify account to the "Users and Access" section.

## Usage

1. **Run the script**:

    Use the following command to run the script and generate a playlist based on your prompt:

    ```bash
    python app.py -p "super chill vibes" -n 10
    ```

    - **`-p`**: The prompt describing the type of playlist you want to generate (e.g., "super happy songs").
    - **`-n`**: The number of songs you want in the playlist (default: 12, max: 50).

2. **OAuth2 Authorization**:

    The first time you run the script, you will be prompted to authenticate with Spotify. Open the provided link in your browser, log in, and authorize the application. After authorization, Spotify will redirect you to a non-existent `http://localhost:9999` page. Copy the redirected URL and paste it into the console to complete the process.

3. **Example**:

    ```bash
    python app.py -p "super happy summer songs" -n 15
    ```

    The above command will create a playlist with 15 songs based on the provided prompt and add it to your Spotify account.

## Example Output

Upon successfully running the script, you'll see output like this:

Found: Everybody Hurts [0d28khcov6AiegSCpG5TuT]
Found: Nothing Compares 2 U [4pvb0WLRcMtbPGmtejJJ6y]
...
Created playlist: super happy summer songs (Wed Aug 17 11:34:52 2023)
https://open.spotify.com/playlist/1ZyDx2NxP9Ab9hv8h


## Contributing

Contributions are welcome! Feel free to fork the repository and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- **OpenAI** for providing their GPT models for natural language understanding.
- **Spotify** for making their API available to developers.
- **Spotipy** for simplifying Spotify API access in Python.

## Tags

- `Spotify`
- `OpenAI`
- `GPT`
- `Spotipy`
- `Playlist Generator`
- `Python`
- `CLI`
- `NLP`
- `Music`



