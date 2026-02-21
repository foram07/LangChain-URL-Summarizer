### AI-Powered YouTube & Website Summarizer using LangChain + Groq

LangChain-URL-Summarizer is a Streamlit-based web app that generates concise AI summaries from:

- 📺 YouTube videos (via transcript extraction)
- 🌐 Website URLs (via content scraping)

Built using **LangChain**, **Groq LLMs**, and **Streamlit**, this project demonstrates practical LLM integration for real-world content summarization.

---

## 🚀 Features

- ✅ Summarize YouTube videos using transcript extraction  
- ✅ Summarize any public website  
- ✅ Powered by Groq’s `llama-3.1-8b-instant` model  
- ✅ Clean Streamlit UI  
- ✅ URL validation  
- ✅ Error handling for missing transcripts  

---

## 🛠 Tech Stack

- **Streamlit** – Frontend UI  
- **LangChain** – LLM orchestration  
- **Groq API** – Fast LLM inference  
- **youtube-transcript-api** – YouTube transcript extraction  
- **UnstructuredURLLoader** – Website content extraction  

---

## 📦 Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/foram07/LangChain-URL-Summarizer.git
cd LangChain-URL-Summarizer
```

### 2️⃣ Create Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate   # macOS/Linux
venv\Scripts\activate      # Windows
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```
###  ▶️ Run the App
```bash
streamlit run app.py
```

## 🧠 How It Works

### 📺 For YouTube URLs

- Extracts the video ID from the provided URL  
- Fetches the transcript using `youtube-transcript-api`  
- Converts the transcript into a LangChain `Document`  
- Sends the content to the Groq LLM for summarization  

---

### 🌐 For Website URLs

- Uses `UnstructuredURLLoader` to scrape content  
- Extracts the webpage text  
- Feeds the content into the LangChain summarization chain  
