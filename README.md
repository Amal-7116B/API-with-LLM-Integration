# API-with-LLM-Integration

This project demonstrates how to build a simple REST API using **FastAPI** with integration to **Ollama** (LLM - Large Language Model).  
The API exposes an endpoint `/generate` where users can send a prompt and receive AI-generated responses from the **Mistral** model.

## Features
- 🚀 Built with FastAPI  
- 🔑 API key authentication with credit system  
- 🧠 Integration with Ollama (Mistral model)  
- 📦 Easy to run locally with Uvicorn and Postman  

## How It Works
1. Start the FastAPI server:
   ```bash
   uvicorn main:app --reload

2. Send a POST request to:

```bash
http://127.0.0.1:8000/generate?prompt=Hello

with header
x-api-key: YOUR_API_KEY

Example using curl
curl -X POST "http://127.0.0.1:8000/generate?prompt=Hello" \
     -H "x-api-key: YOUR_API_KEY"

Example using Python (requests)
import requests

url = "http://127.0.0.1:8000/generate?prompt=Hello"
headers = {"x-api-key": "YOUR_API_KEY"}

response = requests.post(url, headers=headers)
print(response.json())



