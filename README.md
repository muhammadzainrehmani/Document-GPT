# DocumentGPT

DocumentGPT is a Streamlit-based application that enables users to upload documents and interact with their content through natural language queries. The app processes uploaded files by chunking the text, generating embeddings using HuggingFace models, storing them in a Qdrant vector database, and leveraging Gemini 1.5 Flash to answer user queries based on document context.

## Features

- Upload and process PDF or DOCX files
- Automatic text chunking and metadata tagging
- Semantic embeddings using `all-mpnet-base-v2`
- Vector storage with Qdrant
- Conversational interface using Gemini 1.5 Flash
- Real-time document Q&A via LangChain

## Tech Stack

- Python
- Streamlit
- LangChain
- HuggingFace Embeddings
- Qdrant Vector Database
- Gemini 1.5 Flash (via Google Generative AI)

## Installation

```bash
git clone https://github.com/muhammadzainrehmani/document-gpt.git
cd document-gpt
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
````

## Configuration

Create a `.streamlit/secrets.toml` file in the project root:

```toml
genai_api_key = "YOUR_GEMINI_API_KEY"
QDRANT_URL = "https://your-qdrant-instance.com"
QDRANT_API_KEY = "YOUR_QDRANT_API_KEY"
```

## Running the App

```bash
streamlit run app.py
```

## Usage

1. Upload one or more PDF or DOCX files using the sidebar.
2. Click the **Process** button to load and embed the content.
3. Ask questions about the documents in the chat interface.
4. Receive context-based responses powered by Gemini.

## Folder Structure

```
.
├── app.py
├── requirements.txt
└── .streamlit/
    └── secrets.toml
```

## License

This project is licensed under the MIT License.
