# LangChain- Develop AI Agents with LangChain & LangGraph 🦜🔗

Summarize text and extract key facts with LangChain and a local Llama 3.2 model via Ollama.

# LangChain Course Project

My hands-on project from learning LangChain. It runs a local AI model through **Ollama** and uses LangChain to summarize text and pull out interesting facts.

## What it does

1. Takes a block of text about a person.
2. Fills it into a **PromptTemplate** that asks for a short summary and two interesting facts.
3. Sends the prompt to a local **Llama 3.2** model through `ChatOllama`.
4. Prints the model's answer.

The prompt and the model are linked into one **chain** (`prompt | llm`), so a single `invoke()` call runs the whole flow.

## Tech stack

| Tool | Purpose |
|---|---|
| LangChain | Prompt templates and chains |
| Ollama | Runs the AI model locally, so no API costs |
| Llama 3.2 | The language model |
| uv | Python package and project manager |
| python-dotenv | Loads settings from a `.env` file |

## Prerequisites

- Python 3.12+
- [uv](https://docs.astral.sh/uv/)
- [Ollama](https://ollama.com/download), installed and running

## Setup

```bash
git clone https://github.com/Tumuluri007/langchain.git
cd langchain
uv sync
ollama pull llama3.2
```

## Run it

```bash
uv run main.py
```

## Key concepts learned

- **PromptTemplate**: a reusable prompt with placeholders such as `{information}`
- **ChatOllama**: connects LangChain to a model running locally in Ollama
- **Chains**: linking steps together with `|`
- **uv**: managing a Python project and its virtual environment
