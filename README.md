# DocGenie

DocGenie is a Python-based chat application designed to interact with PDF documents using local language model (LLM) models. Unlike traditional chat applications that rely on third-party APIs like OpenAI, DocGenie allows users to securely converse with PDF files containing sensitive or confidential information without relying on external services.

## Description

DocGenie provides a simple chat UI and a chatbot QA app that allows users to interact with documents using locally hosted language models. It leverages Ollama and the mistral model for language understanding, LangChain for LLM integration, and Chainlit for deploying the application.

## System Requirements

DocGenie has the following system requirements:

- **RAM:** At least 8GB of RAM is required for running the application. For optimal performance, it is recommended to have 16GB of RAM.
- **GPU:** A dedicated GPU is recommended for better performance, especially when dealing with large documents and complex language processing tasks.

You must also have Python 3.9 or later installed. Earlier versions of Python may not compile.

## Steps to Replicate

1. Fork this repository and create a codespace in GitHub or clone it locally:

    ```bash
    git clone https://github.com/simpostor/DocGenie.git
    cd DocGenie
    ```

2. Rename example.env to .env and input the LangSmith environment variables (optional):

    ```bash
    cp example.env .env
    ```

3. Create a virtual environment and activate it:

    ```bash
    python3 -m venv .venv && source .venv/bin/activate
    ```

4. Install the necessary Python packages:

    ```bash
    pip install -r requirements.txt
    ```

5. Run the following command in your terminal to start the chat UI:
##
Example 1
   ```bash
   chainlit run simple_chatui.py
   ```
## Example 2
   ```bash
   python3 ingest.py
   ```
   ```bash
   chainlit run main.py
   ```
## Example 3
   ```bash
   chainlit run rag.py
   ```

## Authentication Setup

To set up authentication, follow these steps:

1. Run the following command in your terminal:

    ```bash
    chainlit create-secret
    ```

2. Copy the generated user authentication token and paste it in the `.env` file.

3. Add your credentials in the `users.csv` file.

## Google Authentication Setup

To set up Google OAuth, follow these steps:

1. Create a Google Cloud Platform account.

2. Create a project on the Google Cloud Console.

3. Add credentials for authentication. 

4. Google will provide a client ID and client secret, which is to be put in environment variables.