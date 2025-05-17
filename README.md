# 🤖 AI Sentiment Analyzer

This project is a modern **Sentiment Analyzer** that utilizes **Google’s Gemini (OpenAI-compatible API)** to classify user-provided reviews as **positive**, **negative**, or **neutral** using a Large Language Model (LLM). Built and deployed via **Google Colab** using **Gradio** for the frontend UI.

---

## 🛠️ Tech Stack

- Python
- Gradio (UI)
- OpenAI-compatible API (Gemini)
- Google Colab
- Google API Key (via `userdata.get()`)

---

## 🚀 Features

- Accepts free-form customer reviews
- Analyzes sentiment using Gemini LLM
- Returns contextual sentiment (Positive/Negative/Neutral)
- User-friendly UI with branding (logo, favicon)
- Real-time output via Gradio Blocks

---

## 📦 Setup & Deployment

> You can run this project directly in [Google Colab](https://colab.research.google.com/) or deploy locally.

### ✅ Colab Setup

1. Open `Sentiment_Analyzer.ipynb` in Google Colab.
2. Set your `GOOGLE_API_KEY` using:
   ```python
   from google.colab import userdata
   userdata.set("GOOGLE_API_KEY", "your_key_here")
Run all cells and launch the Gradio app.

💡 Sample Code Snippet
python
Copy
Edit
def analyze_review(review):
    prompt = f"Identify the sentiment in the following review: '''{review}'''"
    messages = [{"role": "user", "content": prompt}]
    response = client.chat.completions.create(
        model="gemini-1.5-flash-latest",
        messages=messages
    )
    return response.choices[0].message.content
🖼️ UI Preview


🔐 API Usage
You need a Google Gemini API key

Stored securely using userdata.get("GOOGLE_API_KEY")

