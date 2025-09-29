
# 📝 NL2SQL – Natural Language to SQL

This project converts **natural language queries** into **SQL statements** and executes them against a sample **SQLite database (`student.db`)**.  
It is a lightweight prototype demonstrating how users can interact with databases using plain English.

---

## 🚀 Features
- Translate English questions into SQL queries automatically.
- Execute generated queries on the provided **student database**.
- Simple, extendable architecture (can be adapted to other databases/schemas).
- Environment configuration using `.env`.

---

## 📂 Project Structure
```

NL2SQL/
│── app.py             # Streamlit app (UI for interacting with NL2SQL)
│── main.py            # Core logic for NL → SQL conversion
│── database.py        # Database connection utilities
│── student.db         # Sample SQLite database
│── .env               # Environment variables (API keys, configs)
│── pyproject.toml     # Project dependencies & metadata
│── requirements.txt   # Python dependencies
│── README.md          # Project documentation

````

---

## 🛠️ Setup & Installation
```bash
# 1. Clone the repo
git clone https://github.com/VoonaSriraj/NL2SQL.git
cd NL2SQL

# 2. Create a virtual environment (recommended)
python -m venv venv
source venv/bin/activate   # Linux / Mac
venv\Scripts\activate      # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Create a .env file and add your API key/configs
echo "GROQ_API_KEY=your_api_key_here" > .env
````

---

## ▶️ Running the Project

```bash
# Option 1: Run Streamlit app
streamlit run app.py

# Option 2: Run CLI script
python main.py
```

---

## 🎓 Example Queries

* **English:** "Show me all students enrolled in the Data Science course."
  **SQL:** `SELECT * FROM STUDENT WHERE COURSE = 'Data Science';`

* **English:** "List the names of students who scored above 80."
  **SQL:** `SELECT NAME FROM STUDENT WHERE SCORE > 80;`

* **English:** "How many students are in the database?"
  **SQL:** `SELECT COUNT(*) FROM STUDENT;`

---

## 📌 Next Steps / Improvements

* Extend support to **arbitrary schemas** (not just `student.db`).
* Improve accuracy using **LLM fine-tuning** or **NL → SQL datasets** (e.g., Spider, WikiSQL).
* Add **unit tests** for reliability.
* Deploy as a **REST API** with FastAPI.

---

## 🤝 Contributing

Pull requests are welcome!
For major changes, please open an issue first to discuss what you’d like to change.

---

## 📜 License

This project is licensed under the MIT License.

---

## 📦 Requirements

Save the following as `requirements.txt`:

```txt
streamlit
langchain
langchain-groq
langchain-community
python-dotenv
sqlite3-binary
```

```



