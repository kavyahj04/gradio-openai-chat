gradio-openai-chat README:
markdown# gradio-openai-chat

A simple Gradio UI for chatting with OpenAI's GPT models with streaming responses.

## What it does

A clothes store assistant that helps customers find items on sale. It dynamically adjusts its behavior based on what the customer asks — for example, redirecting belt or shoe queries toward hats which are 60% off.

## Tech Stack

- Python
- OpenAI API (gpt-4.1-mini)
- Gradio
- python-dotenv

## Project Structure
gradio-openai-chat/
├── main.ipynb    # Main notebook
├── .env          # API keys (not committed)
└── README.md

## Setup

1. Clone the repository
```bash
git clone <your-repo-url>
cd gradio-openai-chat
```

2. Install dependencies
```bash
uv add openai gradio python-dotenv
```

3. Add your OpenAI API key to a `.env` file
OPENAI_API_KEY=sk-proj-your-key-here

4. Run the notebook in Jupyter or Cursor

## Key Concepts

- **Dynamic system prompt** — updates at runtime based on keywords in the user message so the assistant responds contextually
- **Conversation history** — full chat history is passed on every turn so the model has context
- **Streaming** — responses stream token by token using `stream=True` and `yield`
- **gr.ChatInterface** — Gradio's built-in chat UI handles message threading automatically