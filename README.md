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
