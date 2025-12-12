# 🗄️ LangChain SQL Chatbot
A Streamlit-powered intelligent chatbot that allows users to chat with their SQL databases (SQLite or MySQL) using natural language.
The system uses a LangChain SQL Agent to automatically generate SQL queries, execute them, and return clean, conversational answers — all powered by Groq LLM.

## 🚀 Features
- ✅ Chat with your database using natural language
- ✅ Supports SQLite (Student.db) and MySQL
- ✅ Automatic SQL query generation using LangChain SQL Agent
- ✅ Groq LLM integration (llama-3.1-8b-instant)
- ✅ Streaming responses inside an interactive chat UI
- ✅ Session-based chat memory (UI-level)
- ✅ Error handling for:
- Missing DB credentials
- Missing API key
- Invalid SQL queries
- ✅ Clean, modern interface built with Streamlit


## 🧠 How It Works
The app uses a LangChain Zero-Shot ReAct SQL Agent, which:
- Reads the user’s natural language question
- Analyzes the database schema
- Generates the appropriate SQL query
- Executes it on SQLite or MySQL
- Converts the result into a human-friendly answer
- Streams intermediate reasoning steps in Streamlit (via StreamlitCallbackHandler)
This creates a powerful workflow that blends LLM reasoning + SQL execution.

## 📦 Tech Stack
- Python 3.12+
- Streamlit
- LangChain Classic
- LangChain SQL Toolkit
- Groq LLM API (LLaMA 3.1 8B Instant)
- SQLite / MySQL
- SQLAlchemy

## 📁 Project Structure
```
.
├── app.py              # Main Streamlit application
├── Student.db          # Sample SQLite database (read-only)
├── requirements.txt    # Python dependencies
├── .gitignore
└── README.md           # Documentation
```


## 🔧 Installation & Setup
1️⃣ Clone the repository
```bash
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
```

2️⃣ Create a virtual environment
```bash
python -m venv venv
source venv/bin/activate   # macOS/Linux
venv\Scripts\activate      # Windows
```

3️⃣ Install dependencies
```bash
pip install -r requirements.txt
```

4️⃣ Running the App
```bash
streamlit run app.py
```

5️⃣ Add your Groq API Key
When the app runs, enter your Groq API key in the Streamlit sidebar.

## 🗄️ Database Options
✅ SQLite (Default)
* Uses the included Student.db file in read-only mode.
✅ MySQL (Optional)
* Enter the following in the sidebar:
  - Host
  - Username
  - Password
  - Database name

The app will automatically connect and allow SQL chat.


