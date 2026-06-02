
# 🚀 Agentic AI Systems Engineering Lab Environment Setup

Welcome to the **Agentic AI Systems Engineering** training environment.  
This repository contains setup instructions for hands-on labs covering:

- LLM APIs (OpenRouter + Qwen)
- Prompt Engineering
- LangChain & LangGraph
- Agent Development
- Function Calling & Tool Integration
- Memory Systems
- RAG (Retrieval-Augmented Generation)
- Vector Databases
- Multi-Agent Architectures
- n8n Workflow Automation
- AI Agent Orchestration
- Capstone Project

Participants must complete the setup below **before Day 1**.


## 💻 Hardware Requirements

### Recommended Specs

| Component | Requirement                          |
|-----------|--------------------------------------|
| OS        | Windows 11 64-bit                    |
| CPU       | Intel i7 / Ryzen 7 or better         |
| RAM       | 16 GB Minimum (32 GB Preferred)      |
| GPU       | NVIDIA RTX 5000 Series or equivalent |
| Storage   | 30 GB Free SSD Space                 |
| Internet  | Stable Broadband Connection          |

---

## 🛠️ Software Installation

### 1. Python
- **Recommended Version:** `Python 3.11.x`  
- [Download Here](https://www.python.org/downloads/)

Verify installation:
```bash
python --version
pip --version
```

Expected:
```text
Python 3.11.x
```

---

### 2. Visual Studio Code
- [Download VS Code](https://code.visualstudio.com/)

**Extensions:**
| Extension                 | Purpose              |
|---------------------------|----------------------|
| Python                    | Python Development   |
| Jupyter                   | Notebook Support     |
| Pylance                   | IntelliSense         |
| GitHub Copilot (Optional) | AI Coding Assistant  |
| Docker                    | Container Management |
| REST Client               | API Testing          |
| YAML                      | Config Files         |

---

### 3. Git
- [Download Git](https://git-scm.com/downloads)

Verify:
```bash
git --version
```

---

### 4. Docker Desktop
Required for:
- n8n
- Qdrant
- Local Services

[Download Docker](https://www.docker.com/products/docker-desktop)

Verify:
```bash
docker --version
docker compose version
```

---

## 📂 Create Lab Workspace

```bash
mkdir AgenticAI-Labs
cd AgenticAI-Labs
python -m venv venv
venv\Scripts\activate
```

Expected:
```text
(venv)
```

---

## 📦 Python Packages

### Core AI Libraries
```bash
pip install openai python-dotenv requests
```

### LangChain
```bash
pip install langchain langchain-core langchain-community langchain-openai langchain-text-splitters
```

### LangGraph
```bash
pip install langgraph
```

### Data Processing
```bash
pip install pandas numpy matplotlib seaborn
```

### Jupyter Environment
```bash
pip install notebook jupyterlab ipykernel
python -m ipykernel install --user --name agentic-ai
```

### RAG Libraries
```bash
pip install sentence-transformers pypdf unstructured tiktoken
```

### Vector Databases
```bash
pip install qdrant-client chromadb faiss-cpu
```

### Search Tools
```bash
pip install tavily-python
```

### API Development
```bash
pip install fastapi uvicorn
```

### Evaluation & Observability
```bash
pip install langsmith
```

---

## 🔑 OpenRouter Setup

1. [Create Account](https://openrouter.ai)  
2. Generate API Key.  
3. Create `.env` file:

```env
OPENROUTER_API_KEY=YOUR_KEY
```

---

## 🧠 Recommended Models

- **Primary Training Model:** `qwen/qwen3-32b`  
- **Lower Cost Option:** `qwen/qwen3-14b`  
- **Advanced Alternative:** `deepseek/deepseek-chat`

---

## 🖥️ Optional Local AI Setup

### Install Ollama
[Download Ollama](https://ollama.com)

Verify:
```bash
ollama --version
```

**Models:**
```bash
ollama pull qwen3:8b
ollama pull qwen3:14b
ollama pull qwen2.5-coder:14b
```

---

## 🗄️ Vector Database Setup

### Option 1 — Qdrant (Recommended)
```bash
docker pull qdrant/qdrant
docker run -p 6333:6333 qdrant/qdrant
```
Open: [http://localhost:6333/dashboard](http://localhost:6333/dashboard)

### Option 2 — ChromaDB
Runs directly in Python (no Docker).

---

## 🔄 n8n Setup

```bash
docker run -it --rm ^
-p 5678:5678 ^
-v n8n_data:/home/node/.n8n ^
docker.n8n.io/n8nio/n8n
```

Open: [http://localhost:5678](http://localhost:5678)

---

## 📁 Lab Folder Structure

```text
AgenticAI-Labs
│
├── notebooks
│   ├── Day1-Agent-Foundations.ipynb
│   ├── Day2-RAG-Memory.ipynb
│   ├── Day3-Multi-Agent.ipynb
│   └── Day4-Capstone.ipynb
│
├── documents
├── vector_db
├── datasets
├── n8n
├── outputs
├── .env
└── requirements.txt
```

---

## 📅 Day-by-Day Lab Requirements

### Day 1 – Agent Foundations
- Topics: OpenRouter, Qwen, Prompt Engineering, LangChain, Function Calling, Tool Usage, ReAct Agents  
- **Output:** Tool-Enabled AI Agent  

### Day 2 – Memory & RAG
- Topics: Embeddings, Vector DBs, Retrieval, Context Engineering, Agentic RAG  
- Tools: Qdrant, ChromaDB, Sentence Transformers  
- **Output:** Memory Enabled RAG Agent  

### Day 3 – Multi-Agent Systems
- Topics: LangGraph, Planner/Executor Agents, State Management, n8n Orchestration  
- **Output:** Multi-Agent Workflow  

### Day 4 – Capstone
- Build: Multi-Agent + RAG + Memory + n8n Workflow + OpenRouter LLM  
- **Output:** Working Agentic AI Prototype  

---

## ✅ Verify Environment

```python
import langchain
import langgraph
import pandas
import qdrant_client

print("Environment Ready")
```

Expected:
```text
Environment Ready
```

---

## 🧑‍🏫 Trainer Recommendation

| Component            | Recommendation |
|----------------------|----------------|
| IDE                  | VS Code        |
| LLM API              | OpenRouter     |
| Primary Model        | Qwen 3 32B     |
| Local Model          | Qwen 3 14B     |
| Agent Framework      | LangChain      |
| Orchestration        | LangGraph      |
| Workflow Automation  | n8n            |
| Vector Database      | Qdrant         |
| Notebook Environment | Jupyter        |
| Observability        | LangSmith      |

---

✨ This README ensures your environment is fully prepared for the **4-Day Agentic AI Systems Engineering Program**.  

```

Would you like me to also create a **badges + banner decorated version** (GitHub-style with shields.io badges for Python, Docker, LangChain, etc.) so it looks visually polished for your repo?
