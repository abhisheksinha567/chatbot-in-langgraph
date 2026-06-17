# 🤖 LangGraph Conversational Chatbot

A full-stack conversational AI chatbot built with **LangGraph** and **Streamlit**, featuring persistent memory, real-time streaming, multi-thread session management, and RAG-based document querying.



---

## ✨ Features

- 🧠 **Persistent Memory** — Chat history saved to SQLite database across sessions
- 🔄 **Resume Chat** — Pick up any previous conversation thread right where you left off
- ⚡ **Streaming Responses** — Real-time token-by-token response rendering
- 🧵 **Multi-threading** — Manage multiple chat sessions simultaneously
- 📄 **RAG Support** — Upload PDFs and query them using vector similarity search
- 🔧 **Tool Integration** — Web search, stock price lookup, and calculator tools built in
- 🌐 **DuckDuckGo Search** — Real-time web search capability inside the chatbot

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| LLM | Groq (LLaMA 3.1) |
| Embeddings | Google Gemini (`embedding-001`) |
| Orchestration | LangGraph |
| Frontend | Streamlit |
| Vector Store | FAISS |
| Database | SQLite |
| Environment | Python 3.11, python-dotenv |

---

## 📁 Project Structure

```
chatbot-in-langgraph/
│
├── streamlit_frontend.py              # Basic chatbot UI
├── streamlit_frontend_streaming.py    # Streaming responses UI
├── streamlit_frontend_tool.py         # Tool-enabled chatbot UI
├── streamlit_frontend_database.py     # Persistent memory UI
├── streamlit_frontend_mcp.py          # MCP-based chatbot UI
├── streamlit_frontend_threading.py    # Multi-threading UI
├── streamlit_rag_frontend.py          # RAG chatbot UI
│
├── langgraph_backend.py               # Basic LangGraph backend
├── langgraph_tool_backend.py          # Tool-enabled backend
├── langgraph_database_backend.py      # SQLite persistent backend
├── langgraph_mcp_backend.py           # MCP backend
├── langraph_rag_backend.py            # RAG backend
│
├── requirements.txt                   # Python dependencies
├── .env                               # API keys (not committed)
└── .gitignore                         # Ignored files
```

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/abhisheksinha567/chatbot-in-langgraph.git
cd chatbot-in-langgraph
```

### 2. Create and activate virtual environment
```bash
python3.11 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Set up environment variables
Create a `.env` file in the root folder:
```
GROQ_API_KEY=your-groq-api-key-here
GOOGLE_API_KEY=your-google-api-key-here
```

- Get Groq API key free at: https://console.groq.com
- Get Gemini API key free at: https://aistudio.google.com/apikey

### 5. Run the app
```bash
streamlit run streamlit_frontend.py
```

Open your browser at `http://localhost:8501`

---

## 🔐 Environment Variables

| Variable | Description |
|---|---|
| `GROQ_API_KEY` | Groq API key for LLM inference |
| `GOOGLE_API_KEY` | Google Gemini API key for embeddings |

Never commit your `.env` file — it is already in `.gitignore`.

---

## 📌 Available Streamlit Apps

| Command | Description |
|---|---|
| `streamlit run streamlit_frontend.py` | Basic chatbot |
| `streamlit run streamlit_frontend_streaming.py` | With streaming |
| `streamlit run streamlit_frontend_tool.py` | With tools |
| `streamlit run streamlit_frontend_database.py` | With persistent memory |
| `streamlit run streamlit_frontend_threading.py` | With threading |
| `streamlit run streamlit_rag_frontend.py` | With RAG (PDF upload) |

---

## 🙏 Credits

Original project by [CampusX](https://github.com/campusx-official/chatbot-in-langgraph). Extended with Gemini embeddings, Groq LLM, persistent memory, streaming, threading, and RAG enhancements.
