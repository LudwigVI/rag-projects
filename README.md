# RAG Projects

RAG and LLM projects from my MSc in Applied Artificial Intelligence at Tecnológico de Monterrey.

## 1. RAG chatbot over PDF documents (LLM + RAG)

Notebook: [chatbot_LLM_RAG.ipynb](chatbot_LLM_RAG.ipynb)

A chatbot that answers questions from two PDF cheat sheets (Python and Machine Learning), one with a multi-column layout and one with real data tables.

- **Extraction:** adaptive strategy per PDF. PyMuPDF text blocks ordered by column for the multi-column file, pdfplumber for the tabular file.
- **Indexing:** chunking with LangChain text splitters, Hugging Face embeddings (`sentence-transformers/all-MiniLM-L6-v2`), ChromaDB vector store.
- **Generation:** LangChain chain with Gemini and Llama 3 (Groq) models.
- **Interface:** Gradio chat UI.

Course: Natural Language Processing (team activity, Equipo 10). This is my version of the notebook.

### Running it

The notebook was written for Google Colab. It reads API keys from Colab Secrets (`GEMINI_KEY`, `API_KEY_GROQ`, `HF_TOKEN`); no keys are stored in this repository.

## Author

Luis Velasco · [LinkedIn](https://www.linkedin.com/in/luismvelasco)
