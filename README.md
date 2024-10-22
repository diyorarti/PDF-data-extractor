# PDF Data Extractor Using LLM
This project is a Streamlit-based application that allows users to interact with multiple PDF documents using a conversational interface powered by large language models (LLMs). The tool processes PDF files, extracts text, splits it into manageable chunks, and uses embeddings to provide responses to user queries based on the content of the PDFs.

## Features
- Upload multiple PDF documents and ask questions based on the content.
- Conversational interface that remembers chat history using Langchain's memory management.
- PDF text processing with PyPDF2.
- Text chunking using Langchain's text splitters.
- Embedding generation with OpenAI's embeddings and vector storage using FAISS.
- User-friendly interface built with Streamlit.
- Lightweight and easy to deploy with minimal dependencies.


## Prohject structure
```bash
.
├── .gitignore
├── LICENSE
├── README.md
├── app.py                 # Main Streamlit application
├── htmlTemplates.py        # HTML and CSS templates for the chat UI
├── requirements.txt        # Python dependencies

```

## Files Overview
- **app.py**: This is the main entry point for the Streamlit app. It handles user input, processes PDFs, and manages the conversational flow with the LLM.
- **htmlTemplates.py**: Contains HTML and CSS templates for styling the user and bot chat messages.
- **requirements.txt**: Defines the required Python packages and versions.
- **README.md**: You're reading it!

## How It Works
1. PDF Upload: Users upload one or more PDF files.
2. Text Extraction: The text is extracted from the PDFs using PyPDF2.
3. Text Chunking: The extracted text is split into smaller chunks for better processing by the language model.
4. Vector Store Creation: Text chunks are embedded using OpenAIEmbeddings, and a FAISS vector store is created for efficient retrieval.
5. Conversational Querying: Users can ask questions about the uploaded PDFs, and the system retrieves the relevant information based on the embeddings and context, providing accurate and conversational responses.
6. Chat History: The chat history is managed using ConversationBufferMemory, allowing for multi-turn conversations.


# Setup and Installation
## Prerequisites
- Python 3.8 or later
- An OpenAI API Key for embedding generation
- Hugging Face account (optional, if using HuggingFaceHub LLMs)
## Install Dependencies
1. Clone the repository:
```bash
git clone https://github.com/your-username/pdf-data-extractor.git
cd pdf-data-extractor
```
2. Install the required Python packages:
```bash
pip install -r requirements.txt
```
3. Create a .env file in the root directory and add your OpenAI API Key:
```bash
OPENAI_API_KEY=your-openai-api-key
```
## Run the Application
To start the Streamlit app, run the following command:

```bash
streamlit run app.py
```
This will start a local web server and open the app in your default browser. You can upload PDFs, ask questions, and receive responses from the LLM.

## Usage
- **Upload PDFs**: Click the "Upload your PDFs" button in the sidebar to select and upload one or more PDF files.
- **Ask a Question**: Type your question in the input field at the top of the page. The system will use the content of the uploaded PDFs to answer your question.
- **View Responses**: The responses will be displayed in a chat-like format, with alternating user and bot messages.

## Technologies Used
- **Streamlit**: For the front-end web application.
- **Langchain**: For text chunking, embeddings, and memory management.
- **OpenAI Embeddings**: For generating vector representations of text chunks.
- **FAISS**: For fast and efficient vector-based text retrieval.
- **PyPDF2**: For extracting text from PDF files.
- **Python-dotenv**: For loading environment variables (like API keys).

## Future Enhancements
- Add support for non-English PDFs.
- Enable support for additional document types (e.g., DOCX, TXT).
- Implement more sophisticated document chunking strategies.
- Allow users to switch between different LLMs (OpenAI, HuggingFaceHub, etc.).

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request or open an issue for any improvements or suggestions.

