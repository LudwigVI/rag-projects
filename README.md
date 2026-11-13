# RAG Projects

RAG and LLM projects from my MSc in Applied Artificial Intelligence at Tecnológico de Monterrey.

## 1. RAG question answering over S&P 500 financial news

Notebooks:
- [news_vector_store_sp500.ipynb](news_vector_store_sp500.ipynb): semantic search and vector stores
- [news_rag_sp500.ipynb](news_rag_sp500.ipynb): retrieval-augmented generation

Individual course project (Fintech and Digital Innovation in Finance).

- **Data:** news for S&P 500 tickers and company metadata fetched with `yfinance`.
- **Embeddings:** `sentence-transformers/all-MiniLM-L6-v2`.
- **Vector search:** a custom vector store with cosine-similarity search and metadata filters (ticker, date), and a FAISS index.
- **RAG pipeline:** retrieves relevant news for a question and generates an answer with an OpenAI model (`gpt-4o-mini`).
- **Prompt engineering and evaluation:** prompts that combine news excerpts with company metadata; answers compared with and without metadata on clarity, accuracy, detail, and contextual relevance.

## 2. RAG chatbot over PDF documents (LLM + RAG)

Notebook: [chatbot_LLM_RAG.ipynb](chatbot_LLM_RAG.ipynb)

A chatbot that answers questions from two PDF cheat sheets (Python and Machine Learning), one with a multi-column layout and one with real data tables.

- **Extraction:** adaptive strategy per PDF. PyMuPDF text blocks ordered by column for the multi-column file, pdfplumber for the tabular file.
- **Indexing:** chunking with LangChain text splitters, Hugging Face embeddings (`sentence-transformers/all-MiniLM-L6-v2`), ChromaDB vector store.
- **Generation:** LangChain chain with Gemini and Llama 3 (Groq) models.
- **Interface:** Gradio chat UI.

Course: Natural Language Processing (team activity, Equipo 10). This is my version of the notebook.

## Running the notebooks

The notebooks were written for Google Colab. They read API keys from Colab Secrets (`OPENAI_API_KEY`, `GEMINI_KEY`, `API_KEY_GROQ`, `HF_TOKEN`); no keys are stored in this repository.

## Author

Luis Velasco · [LinkedIn](https://www.linkedin.com/in/luismvelasco)
