# 📈 RockyBot: News Research Tool

RockyBot is an AI-powered **News Research Tool** built with **Streamlit**, **LangChain**, **OpenAI embeddings**, and **FAISS**.
It allows you to:
✅ Load news articles from given URLs
✅ Split them into chunks
✅ Create embeddings & store them in a FAISS vector DB
✅ Ask questions and get answers **with sources**

---

## 🚀 Features

* Fetch content from news article URLs
* Convert articles into embeddings using **OpenAI**
* Store and retrieve information via **FAISS**
* Interactive **Streamlit UI**
* Provides **answers with sources**

---


## 🔧 Installation


### 2. Create virtual environment (recommended)

```bash
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## 🔑 API Key Setup

This project uses **OpenAI API** for embeddings and LLMs.

### Option 1: Set API Key in Code (quick test)

Edit `main.py` and replace:

```python
os.environ["OPENAI_API_KEY"] = "your_api_key_here"
```

### Option 2: Use `.env` file (recommended)

1. Create a `.env` file in project root:

   ```
   OPENAI_API_KEY=your_api_key_here
   ```
2. Install dotenv:

   ```bash
   pip install python-dotenv
   ```
3. Add this in `main.py`:

   ```python
   from dotenv import load_dotenv
   load_dotenv()
   ```

---

## ▶️ Running the App

Run the following command:

```bash
streamlit run main.py
```

It will start a local web server and open the app in your browser:

```
http://localhost:8501
```

---

## 🧑‍💻 Usage

1. Enter up to **3 news article URLs** in the sidebar.
2. Click **Process URLs** → the app will fetch, split, embed, and store content in FAISS.
3. Ask a question in the input box.
4. RockyBot will return an **answer with sources**.

---

## 📦 Requirements

Dependencies are in `requirements.txt`. Example:

```
streamlit
langchain
langchain-openai
langchain-community
faiss-cpu
python-dotenv
unstructured
lxml
```

Install with:

```bash
pip install -r requirements.txt
```

---

## ⚡ Example

**Input URLs:**

* [https://www.bbc.com/news/article1](https://www.bbc.com/news/article1)
* [https://www.cnn.com/news/article2](https://www.cnn.com/news/article2)

**Question:**

```
What are the key points about the stock market today?
```

**Output:**
✅ AI-generated summary
📌 With sources from the processed URLs

