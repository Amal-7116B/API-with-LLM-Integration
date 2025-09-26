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

### 2) Clone & install
  ```bash
  git clone <YOUR_REPO_URL>.git
cd API-with-LLM-Integration

# (optional but recommended) create & activate a venv
python -m venv .venv

# Windows PowerShell:
.\\.venv\\Scripts\\Activate.ps1

# macOS/Linux:
source .venv/bin/activate

# install dependencies
pip install -r requirements.txt

### 3) Environment variable
API_KEY=YOUR_SECRET_KEY


### 4) Run the API server
uvicorn main:app --reload


Using the API
POST /generate
Query param: prompt (string)
Header: x-api-key: <your key>

Example using curl (Linux/macOS)
curl -X POST "http://127.0.0.1:8000/generate?prompt=Hello" \
     -H "x-api-key: YOUR_SECRET_KEY"

Example using curl (Windows PowerShell)
curl -Method POST "http://127.0.0.1:8000/generate?prompt=Hello" `
     -Headers @{ "x-api-key" = "YOUR_SECRET_KEY" }

Example using Python (requests)
import requests

url = "http://127.0.0.1:8000/generate?prompt=Hello"
headers = {"x-api-key": "YOUR_SECRET_KEY"}

response = requests.post(url, headers=headers)
print(response.json())


