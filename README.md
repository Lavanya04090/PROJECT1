# README

# Chatbot for Resume-based Q&A

This project implements a Streamlit-based chatbot that can answer questions related to a given resume in a `.docx` file. The chatbot utilizes the LangChain library to build a conversational retrieval chain, enabling it to fetch relevant information from the resume based on user queries. 

# Table of Contents

1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Code Explanation](#code-explanation)
6. [Environment Variables](#environment-variables)

# Project Overview

The objective of this project is to create a chatbot that can read and understand the contents of a resume provided in a `.docx` file and answer any related questions. This is achieved by loading the document, splitting it into manageable chunks, and using a language model to process and respond to user queries.

# Features

- **Conversational Interface**: Uses Streamlit to provide a user-friendly interface for chatting with the bot.
- **Document Loading**: Supports loading of resume documents in `.docx` format.
- **Document Splitting**: Splits the document into chunks for efficient processing and retrieval.
- **Embeddings and Vector Store**: Utilizes HuggingFace embeddings and FAISS for storing and retrieving document chunks.
- **Conversational Chain**: Uses LangChain to create a conversational retrieval chain, allowing the bot to provide relevant answers based on the document content.

# Installation

To run this project, you need to have Python installed on your system. Follow the steps below to set up the environment and run the application:

1. **Clone the repository**:
    ```bash
    git clone <repository_url>
    cd <repository_directory>
    ```

2. **Create a virtual environment**:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. **Install the required packages**:
    ```bash
    pip install -r requirements.txt
    ```

4. **Set up environment variables**:
    - Create a `.env` file in the project root directory.
    - Add necessary environment variables (e.g., API keys) to the `.env` file.

# Usage

1. **Prepare the Resume Document**:
    - Ensure your resume document is in `.docx` format and update the `file_path` variable in the code to point to the location of your resume.

2. **Run the Application**:
    ```bash
    streamlit run app.py
    ```

3. **Interact with the Chatbot**:
    - Open the Streamlit interface in your web browser.
    - Ask questions related to the resume and get answers from the chatbot.

# Code Explanation

The code is structured into several key functions:

- **initialize_session_state()**: Initializes the session state for storing chat history and generated responses.
- **conversation_chat(query, chain, history)**: Processes user queries and returns responses based on the document content.
- **display_chat_history(chain)**: Manages the display of chat history in the Streamlit interface.
- **create_conversational_chain(vector_store)**: Creates a conversational retrieval chain using the loaded resume document.
- **main()**: The main function that ties everything together, loading the document, creating the conversational chain, and displaying the chat interface.

# Environment Variables

Ensure that the following environment variables are set in the `.env` file:

- **REPLICATE_API_KEY**: Your API key for Replicate, used to access the language model.
- **MODEL_NAME**: Name of the language model to be used.

# License

This project is licensed under the MIT License. See the LICENSE file for details.

# Acknowledgements

- **LangChain**: For providing tools to build the conversational retrieval chain.
- **HuggingFace**: For providing pre-trained embedding models.
- **FAISS**: For enabling efficient similarity search and clustering of document chunks.
- **Streamlit**: For offering a seamless way to create interactive web applications.

For more details, please refer to the code and comments within the script. If you encounter any issues or have suggestions for improvements, feel free to create an issue or submit a pull request.

Happy Coding!
