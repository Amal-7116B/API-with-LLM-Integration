# API-with-LLM-Integration

This project demonstrates how to build a simple REST API using **FastAPI** with integration to **Ollama** (LLM - Large Language Model).
The API exposes an endpoint `/generate` where users can send a prompt and receive AI-generated responses from the **Mistral** model.

## Features
- 🚀 FastAPI server (Uvicorn)
- 🔑 API key authentication with a simple credit system
- 🧠 Ollama integration (model: `mistral`)
- 🧪 Test quickly with curl, Postman, or a small Python snippet
- 🛠️ Optional: run with a Bash script or a Makefile

---

## Quickstart

### 1) Prerequisites
- **Python** 3.11+
- **Ollama** installed and running locally (https://ollama.com)
- Pull the model once:
  ```bash
  ollama pull mistral
