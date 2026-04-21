# 🃏 FlashGen AI — AI Flashcard Generator + Chatbot

> A Generative AI application that converts any text or PDF into study flashcards, with a built-in AI chatbot — powered by Groq LLM and Gradio.

---

## 📌 Project Overview

FlashGen AI is a BTech Generative AI project that helps students study smarter by:
- Generating Q&A flashcards with hints from any text or PDF
- Choosing difficulty level (Easy / Medium / Hard)
- Navigating cards one by one with Prev / Next
- Exporting flashcards as a `.txt` file
- Chatting with an AI assistant in the same app

---

## 🛠️ Tech Stack

| Component     | Technology                        |
|---------------|-----------------------------------|
| Language      | Python 3.10+                      |
| LLM Provider  | Groq API (free)                   |
| Models        | Llama 3.1 8B, Llama 3.3 70B, Llama 4 Scout |
| GUI           | Gradio 3.50.2                     |
| PDF Parsing   | PyMuPDF (fitz)                    |
| Notebook      | Google Colab                      |

---

## ✨ Features

- 📝 **Text input** — paste notes, articles, or any content
- 📄 **PDF upload** — extract text from PDF files automatically
- 🎯 **Difficulty control** — Easy, Medium, or Hard flashcards
- 🃏 **Card navigation** — browse cards with Prev / Next buttons
- 💬 **AI Chatbot** — ask questions, get explanations
- ⬇️ **Export** — download all flashcards as a `.txt` file
- 🔀 **Model selector** — choose between 3 Groq LLM models

---

## 🚀 How to Run

### Step 1 — Open in Google Colab

Click the badge below or upload `flashcard_chatbot_v2.ipynb` to [colab.research.google.com](https://colab.research.google.com)

### Step 2 — Get a Free Groq API Key

1. Go to [console.groq.com](https://console.groq.com)
2. Sign up / Log in
3. Click **API Keys** → **Create API Key**
4. Copy your key

### Step 3 — Add Your API Key via Colab Secrets
1. In Colab, click the key icon in the left sidebar
2. Click "Add new secret"
3. Name: GROQ_API KEY
4. Value: paste your Groq API key
5. Toggle "Notebook access" to ON
6. Run the notebook - key is loaded automatically

### Step 4 — Run All Cells

Go to **Runtime → Run All** in Colab.

The last cell will output a public Gradio link like:
```
Running on public URL: https://xxxxxxxx.gradio.live
```

Open that link — your app is live! ✅

---

## 📁 Project Structure

```
flashgen-ai/
├── flashcard_chatbot_v2.ipynb   ← Main Colab notebook (GUI + AI logic)
└── README.md                    ← This file
```

---

## 🖼️ App Preview

| Mode | Description |
|------|-------------|
| 💬 Chatbot | Ask any question, get AI responses |
| 🃏 Flashcards | Paste text or upload PDF → generate cards |

---

## 📊 System Architecture

```
Input (Text / PDF)
       ↓
Text Extraction (PyMuPDF)
       ↓
Prompt Engineering (difficulty + JSON format)
       ↓
Groq LLM API (Llama models)
       ↓
JSON Parser → Flashcard objects
       ↓
Gradio GUI (navigate, reveal, export)
```

---

## 👥 Team Members

| Member | Role |
|--------|------|
| Kartik Thakur | LLM Integration & Prompt Engineering |
| Aditya Thakur | PDF Parsing & Text Processing |
| Suryansh | Gradio GUI Development |
| Adarsh Thakur | Notebook Documentation |
| Akhilesh Jaguri | Bug fixes & GitHub Setup |

---

## 📝 Dependencies

```
gradio==3.50.2
groq
PyMuPDF
```

Install via:
```bash
pip install gradio==3.50.2 groq PyMuPDF
```

---

## 🔑 Note on API Key
This project uses Colab Secrets to store the API key securely. Never hardcode your API
key directly in the notebook. Always use userdata.get('GROQ_API_KEY' ) to access it
safely.

---

## 📄 License

MIT License — Free to use for educational purposes.
