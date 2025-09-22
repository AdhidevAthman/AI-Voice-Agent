# Blue: Real-Time Audio Streaming & Function Calling

This project is a Python-based server that connects Twilio audio streams to Deepgram’s STS (Speech-to-Speech) agent using websockets. It supports real-time audio streaming, function calling, and integrates with custom pharmacy functions.

## Features

- Receives audio from Twilio via websockets
- Streams audio to Deepgram STS for processing
- Handles function calls from Deepgram and executes pharmacy-related functions
- Uses environment variables for configuration (`python-dotenv`)
- Modular and extensible function mapping

## Requirements

- Python 3.8+
- `websockets`
- `python-dotenv`

## Installation

1. Clone the repository:
    ```sh
    git clone <your-repo-url>
    cd Blue
    ```

2. Install dependencies:
    ```sh
    pip install websockets python-dotenv
    ```

3. Add your Deepgram API key to a `.env` file:
    ```
    DEEPGRAM_API_KEY=your_deepgram_api_key
    ```

4. Create a `config.json` file with your Deepgram agent configuration.

## Usage

Start the server:
```sh
python main.py
```
The server listens on `localhost:5000` for Twilio websocket connections.

## File Structure

- `main.py` — Main server logic
- `pharmacy_functions.py` — Custom pharmacy-related functions
- `.env` — Environment variables (not committed)
- `config.json` — Deepgram agent configuration

## License

MIT License
