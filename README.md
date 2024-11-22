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

## Introduction

The project allows the NAO robot to talk with users, using the OpenAI GPT-4 model for response generation. The robot listens to user input, processes the information, and replies accordingly while exhibiting various interactive behaviors: blinking, background movement, or gesturing.

## Features

- **Speech Recognition**: Google's Speech Recognition API to process user speech.
- **Conversational AI**: Powered by OpenAI GPT-4 for human-like response generation.
- **Interactive Behaviors**: Autonomously working and Includes blinking, background movement, and listening gestures.
- **Contextual Commands**: Supports phrases like "repeat that" or "rephrase that, which correspond to different actions."
- **Physical Interaction Handling**: Responds to touch sensors and physical interactions, which lead to rephrasing and repeating.

## Prerequisites

- **NAO Robot** with NAOqi SDK installed.
- **Python 3.x**
- **OpenAI API Key**
- **Internet Connection** for API calls.

## Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/SIR-2024/build-your-own-sir-group-28.git
   cd TBA
   ```

2. **Install Required Python Packages**

   ```bash
   pip install -r requirements.txt (TBA)
   ```


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
python (TBA)
```

- The robot will start and enable interactive behaviors.
- The robot listens for user input via its microphone.
<!-- - Press the 'q' key to quit the program. -->

## Interactive Commands

- **Repeat**: Say any phrase with the keyword "repeat" or touch the left-side sensors to have the robot repeat its last response.
- **Rephrase**: Say any phrase with the keyword "rephrase" or touch the right-side sensors to have the robot rephrase its last response.

## Troubleshooting

- **No Connection to the Robot**: Make sure the robot is connected to the same network. Check the IP address.
- **Speech Recognition Errors**: Check if your microphone is enabled and ambient noise levels.
- **API Errors**: Make sure your OpenAI API key is valid, that you have internet connectivity and you have enough credits. 

## Contributing

Contributions are welcome! Please open an issue or submit a pull request with your improvements.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- **TA's** for their guidance and support.
- **OpenAI** for their GPT model.
- **SoftBank Robotics** for the NAO robot and SDK availability.


