## Personalized Bot with Memory: A Document Understanding AI

Streamlit App -- https://datamokotow-openai-langchain-pdfchat-pdfchat-4pc5mv.streamlit.app/

**Description**
This repository contains a powerful application that demonstrates a personalized Conversational AI bot which can parse, understand, and answer questions from an uploaded PDF document. The bot uses OpenAI's GPT-3 model for natural language understanding and generation, LangChain for linguistic processing, FAISS for efficient similarity search, and Streamlit for user-friendly interactive UI.

**Technical Overview**
The primary components of the bot are:

PDF Parser: This component uses the PyPDF library to extract text from an uploaded PDF document. The extracted text is then chunked into manageable parts, which are treated as distinct documents, with appropriate metadata like page numbers and chunk identifiers.

OpenAI GPT-3 Model: GPT-3 model is utilized for language understanding and generation tasks. The OpenAI API key is required to access this service.

Embeddings and Similarity Search: After the text extraction and chunking process, the documents are transformed into vector embeddings using the OpenAI Embeddings, which are then indexed using a FAISS (Facebook AI Similarity Search) index for efficient similarity search.

Question-Answering System: The RetrievalQA system is set up using the indexed embeddings. The system uses a retriever-ranker architecture for extracting the most relevant chunks of text in response to a query.

Conversational Agent: The conversational agent uses a zero-shot learning approach, using a series of tools including the QA system, to maintain a conversation with the user. The agent uses a Conversation Buffer Memory to store the conversation history, providing context for subsequent questions and responses.

Streamlit UI: Streamlit is used to create an interactive web application where users can upload their PDF documents, input their queries, and receive responses from the AI agent.

**Usage**
To use this application, clone this repository and run the Streamlit app. The user interface will guide you through the process of uploading a PDF file, entering your OpenAI API key, and starting your interaction with the bot.

**Contributions**
Contributions to enhance this bot are welcomed. Please feel free to submit pull requests or raise issues.

**License**
This project is licensed under the terms of the MIT license.




