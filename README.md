# VoiceMedi AI 🩺🤖  
*An Edge-AI Chatbot for Symptom Extraction and Appointment Pre-Fill*  

**VoiceMedi AI** is an open-source healthcare chatbot. It helps users describe symptoms naturally, predicts conditions using machine learning, and shares structured appointment data. This prototype is a core module in a broader Edge-AI pipeline to automate clinical intake workflows.

---

## 🧠 Key Features

- 🔍 **Symptom-Based Condition Prediction** – Machine learning-based diagnosis using natural language input  
- 💬 **Conversational Interface** – Interprets user input via Ollama's Chat completion API  
- 📦 **Modular Design** – Can be extended to cover other medical domains and scheduling use cases  
- ⚙️ **Modern Stack** – FastAPI backend, React frontend, containerized with Docker  
- 🧩 **Edge-AI Ready** – Completely offline designed with edge deployment scenarios in mind  

---

## 🚀 Getting Started (with Docker)

### Prerequisites:
- Ollama installed
- Docker & Docker Compose installed  
- Environment variables configured:

  - `backend/.env`:  
    ```
    OLLAMA_URL=http://host.docker.internal:11434 ## incase of local deployment, use localhost
    DEBUG=True  
    ```

  - `frontend/.env`:  
    ```
    BACKEND_URL=http://localhost:8000  
    ```
---

## 🦙 Ollama Setup (for LLaMA 3.2:1b Model Inference)

**VoiceMedi AI** uses [Ollama](https://ollama.com/) to run lightweight LLMs like **LLaMA 3.2:1b** locally or on edge devices.

### 🛠️ Step 1: Install Ollama

#### Linux
```bash
curl -fsSL https://ollama.com/install.sh | sh
```
#### Mac
```bash
brew install ollama
```
#### Windows
Download the official installer:
👉 [ollama](https://ollama.com/download/windows)

### 📥 Step 2: Download the LLaMA 3.2:1b Model
```bash
ollama pull llama3:2.1b
```
This will download and configure the model locally for inference.

### 🚀 Step 3: Run the Model
```bash
ollama run llama3:2.1b
```

### Run the Project:
```bash
# Clone the repository
git clone https://github.com/krishsat9937/voice_chatbot.git
cd voice_chatbot

# Build and launch containers
docker-compose up --build
```

---

## 🧪 Local Development Setup

### Backend (FastAPI)
```bash
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
uvicorn main:app --reload
```

### Frontend (React)
```bash
cd frontend
npm install
npm start
```

---

## 🖥️ System Architecture
<img width="1199" height="514" alt="Screenshot 2025-06-25 at 2 12 29 AM" src="https://github.com/user-attachments/assets/9aafa0b3-c621-46a5-af5a-f8e802af7128" />

![Voicehat architecture](https://github.com/user-attachments/assets/2dbc8da7-8242-4092-ae9e-648ec7838a45)

---
