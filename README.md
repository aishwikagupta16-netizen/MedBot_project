# 🏥 RAG-Based Grok Medical Assistant

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Flask](https://img.shields.io/badge/Flask-Production--Ready-black)
![RAG](https://img.shields.io/badge/Architecture-RAG-green)
![LLM](https://img.shields.io/badge/LLM-Grok_API-purple)
![License](https://img.shields.io/badge/License-MIT-orange)

A production-ready **Flask web application** that leverages **Retrieval-Augmented Generation (RAG)** with the **Grok API** to deliver authoritative, context-aware, and reliable medical information through an interactive AI assistant.

This system retrieves trusted medical knowledge, reasons over verified context, and generates medically grounded responses — reducing hallucinations and improving factual accuracy.

---

## 🚀 Key Features

- 🔎 Retrieval-Augmented Generation (RAG) architecture  
- 🧠 Context-aware medical reasoning using Grok API  
- 📚 Retrieval from authoritative medical knowledge  
- ⚡ High-performance Flask backend  
- 💬 Interactive chat interface  
- 🔐 Secure environment configuration  
- 🧩 Modular and scalable structure  
- 📈 Production-ready deployment setup  

---

## 🏗️ System Architecture

```
User Query
    ↓
Retriever (Vector Search / Knowledge Base)
    ↓
Context Injection
    ↓
Grok API (LLM Reasoning)
    ↓
Grounded Medical Response
```

### RAG Pipeline Steps

1. Retrieve relevant medical documents
2. Construct context-rich prompt
3. Inject safety constraints
4. Generate grounded response via Grok API
5. Return structured, safe answer

---

## 📂 Project Structure

```
rag-grok-medical-assistant/
│
├── app/
│   ├── __init__.py
│   ├── routes.py
│   ├── rag_pipeline.py
│   ├── retriever.py
│   ├── prompt_template.py
│   └── utils.py
│
├── templates/
│   └── index.html
│
├── static/
│   └── style.css
│
├── config.py
├── run.py
├── requirements.txt
├── .env.example
└── README.md
```

---

## ⚙️ Installation Guide

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/rag-grok-medical-assistant.git
cd rag-grok-medical-assistant
```

### 2️⃣ Create Virtual Environment

```bash
python -m venv venv
```

Activate:

**Mac/Linux**
```bash
source venv/bin/activate
```

**Windows**
```bash
venv\Scripts\activate
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🔐 Environment Configuration

Create a `.env` file in the root directory:

```
GROK_API_KEY=your_grok_api_key_here
FLASK_ENV=production
SECRET_KEY=your_secret_key_here
```

---

## ▶️ Run the Application

```bash
python run.py
```

Application runs at:

```
http://127.0.0.1:5000
```

---

## 🧠 Example Interaction

**User:**
> What are early symptoms of Type 2 Diabetes?

**Assistant:**
- Increased thirst  
- Frequent urination  
- Fatigue  
- Blurred vision  
- Slow-healing wounds  

⚠️ This information is for educational purposes only and not a substitute for professional medical advice.

---

## 📦 Dependencies

```
Flask
python-dotenv
requests
faiss-cpu
sentence-transformers
gunicorn
```

---

## 🚀 Production Deployment

### Using Gunicorn

```bash
gunicorn run:app --workers 4 --bind 0.0.0.0:8000
```

### Using Docker (Optional)

```bash
docker build -t rag-grok-medical .
docker run -p 8000:8000 rag-grok-medical
```

---

## 🔐 Security & Safety

- No hard-coded API keys  
- Environment variable configuration  
- Context-grounded generation  
- Hallucination reduction via RAG  
- Enforced medical disclaimer  

---

## 📈 Future Enhancements

- Vector database integration (Pinecone / Weaviate)
- Conversation memory
- Admin dashboard
- Source citation display
- Rate limiting
- Logging & monitoring

---

## ⚠️ Medical Disclaimer

This application provides informational medical content only.  
It does **not** provide diagnosis, prescription, or treatment.  

Always consult a licensed healthcare professional.

---

## 🤝 Contributing

Contributions are welcome.

1. Fork the repository
2. Create a new branch
3. Submit a pull request

---

## 📜 License

MIT License

---

## 👨‍💻 Author

Built with ❤️ using Flask + RAG + Grok API
