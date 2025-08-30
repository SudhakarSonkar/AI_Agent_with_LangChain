# ToDoist Assistant with Gemini 

This is a simple ToDoist assistant that uses the Gemini AI to manage your tasks. It leverages the Todoist API to add and view tasks directly from a command-line interface.

## Features

- **Add Tasks**: You can easily add new tasks to your Todoist list with a simple command.
- **View Tasks**: The assistant can fetch and display all your current tasks.
- **Natural Language Interface**: Interact with the assistant using natural language.

## Prerequisites

Before running the assistant, you need to have the following:

- **Python 3.8+** installed.
- **A Todoist account** and a personal API token. You can get your API token from your [Todoist Integrations settings](https://todoist.com/app/settings/integrations).
- **A Google Gemini API key**. You can get this from [Google AI Studio](https://ai.google.dev/docs/gemini_api_overview).

## Installation

1. **Clone the repository**:
   ```bash
   git clone <repository_url>
   cd <repository_name>
````

2.  **Install the required Python packages**:

    ```bash
    pip install -r requirements.txt
    ```

    **Note**: You'll need to create a `requirements.txt` file that lists the dependencies: `langchain-google-genai`, `todoist-api-python`, `langchain-core`, `langchain`, `python-dotenv`.

3.  **Set up your environment variables**:
    Create a `.env` file in the project's root directory and add your API keys:

    ```env
    TODOIST_API_KEY="your_todoist_api_key"
    GEMINI_API_KEY="your_gemini_api_key"
    ```

## Usage

Run the main Python script from your terminal:

```bash
python main.py
```

Once the script is running, you can interact with the assistant by typing commands.

### Examples:

  - **To add a task**:

      - "add a task to buy groceries"
      - "can you create a task to finish the report?"

  - **To view tasks**:

      - "show my tasks"
      - "what are my to-dos?"
      - "can I see my current tasks?"

## Code Overview

  - `main.py`: The core script that initializes the Gemini model, Todoist API, and the LangChain agent.
  - `.env`: A file to securely store your API keys.

The assistant uses **LangChain** to create an agent that can dynamically choose which tool to use (adding a task or showing tasks) based on your input. The **Gemini model** provides the conversational capabilities, while the **Todoist API** handles the task management.

```
```
