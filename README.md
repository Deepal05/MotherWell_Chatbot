# MotherWell Chatbot

MotherWell Bot is a smart pregnancy-focused chatbot that provides guidance on prenatal care, common pregnancy symptoms, and traditional home remedies — powered by LLMs and real-time document retrieval.

---

## Key Features

- Real-time chat support for pregnancy-related queries
- Context-aware conversations using chat history
- Retrieval-Augmented Generation (RAG) with Astra DB vector store
- Uses HuggingFace sentence embeddings (`all-MiniLM-L6-v2`)
- Powered by Groq's LLaMA 3.1-8B for intelligent responses
- Flask + Socket.IO backend for web and socket communication

---

## Tech Stack

- **Backend**: Flask, Flask-SocketIO
- **LLM**: Groq (LLaMA 3.1 via LangChain)
- **Vector Store**: Astra DB (DataStax)
- **Embeddings**: HuggingFace Transformers
- **Framework**: LangChain

---

## API Keys Required

> Store these securely in environment variables or a `.env` file (do not hardcode in production).

- `GROQ_API`: Groq API key for LLaMA model
- `HUGFA_TOKEN`: HuggingFace API key
- `ASTRA_DB_API_ENDPOINT`: Astra DB API endpoint
- `ASTRA_DB_APPLICATION_TOKEN`: Astra DB token
- `ASTRA_DB_KEYSPACE`: Astra DB keyspace (namespace)

---

## How It Works

- User asks a question.
- Chat history is used to contextualize the query.
- Astra DB retrieves relevant documents using semantic similarity.
- Groq’s LLaMA model responds with a clear, helpful answer.

---

## Example Use Case

- User: What are safe remedies for back pain during pregnancy?
- Bot: You can try gentle prenatal yoga, warm compresses, and sleeping on your side with a pillow between your legs. Avoid heavy lifting and consult your doctor if pain persists.

---

## Disclaimer
MotherWell Bot is not a medical tool. It provides general informational support and is not a substitute for professional medical advice. Always consult your healthcare provider for personalized care.
