# NAO Robot Interactive Assistant with OpenAI GPT-4

An interactive assistant for the NAO robot using OpenAI's GPT-4 model for conversational AI, enabling speech recognition and dynamic robot behaviors.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Interactive Commands](#interactive-commands)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)
- [Security Notice](#security-notice)

## Introduction

This project allows a NAO robot to interact with users through speech, utilizing OpenAI's GPT-4 model for generating responses. The robot listens to user input, processes it, and replies accordingly while exhibiting interactive behaviors like blinking, background movement, and gestures.

## Features

- **Speech Recognition**: Uses Google's Speech Recognition API to process user speech.
- **Conversational AI**: Powered by OpenAI GPT-4 for generating human-like responses.
- **Interactive Behaviors**: Includes blinking, background movement, and listening gestures.
- **Contextual Commands**: Supports phrases like "repeat that" or "rephrase that."
- **Physical Interaction Handling**: Responds to touch sensors and physical interactions.

## Prerequisites

- **NAO Robot** with NAOqi SDK installed.
- **Python 3.x**
- **OpenAI API Key**
- **Internet Connection** for API calls.

## Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name
   ```

2. **Install Required Python Packages**

   ```bash
   pip install -r requirements.txt
   ```

   *Note: Ensure you have `pip` installed. You may need to use `pip3` depending on your setup.*

3. **Install NAOqi Python SDK**

   Follow the instructions from the [SoftBank Robotics Developer Center](https://developer.softbankrobotics.com/) to install the NAOqi SDK for Python.

## Configuration

1. **Set the NAO Robot IP Address**

   In the script, update the `ip` parameter when initializing the `Nao` object:

   ```python
   nao = Nao(ip="YOUR_NAO_ROBOT_IP_ADDRESS")
   ```

2. **Set Your OpenAI API Key**

   It's recommended to use an environment variable to store your API key securely.

   - **On Linux/macOS**

     ```bash
     export OPENAI_API_KEY='your-api-key'
     ```

   - **On Windows**

     ```cmd
     set OPENAI_API_KEY=your-api-key
     ```

   In the script, modify the line setting the API key to retrieve it from the environment:

   ```python
   openai.api_key = os.getenv("OPENAI_API_KEY")
   ```

   **Important:** Do not hardcode your API key into your scripts or share it publicly.

## Usage

Run the script using:

```bash
python your_script_name.py
```

- The robot will start and enable interactive behaviors.
- The robot listens for user input via its microphone.
- Press the 'q' key to quit the program.

## Interactive Commands

- **Repeat**: Say "repeat that" or touch the left-side sensors to have the robot repeat its last response.
- **Rephrase**: Say "rephrase that" or touch the right-side sensors to have the robot rephrase its last response.

## Troubleshooting

- **No Response from the Robot**: Ensure the robot is connected to the same network and that the IP address is correct.
- **Speech Recognition Errors**: Check your microphone and ambient noise levels.
- **API Errors**: Make sure your OpenAI API key is valid and that you have internet connectivity.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request with your improvements.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- **OpenAI** for the GPT-4 model.
- **SoftBank Robotics** for the NAO robot and SDK.
- **SpeechRecognition** library for handling speech input.

## Security Notice

Please ensure that you do not expose your OpenAI API key in your code or repository. It's recommended to use environment variables or configuration files to store sensitive information securely.
