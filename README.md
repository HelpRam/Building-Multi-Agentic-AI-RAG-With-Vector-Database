# Building-Multi-Agentic-AI-RAG-With-Vector-Database

🧠 PDF Chat Assistant (CLI) with Phi + pgvector + PostgreSQL
This project creates a command-line assistant that can chat with PDF documents, using the power of Phi, semantic search via pgvector, and persistent chat memory with PostgreSQL.

It currently loads a PDF of Thai recipes and allows natural conversation with it.

🚀 Features
📄 Load and understand a PDF from a URL

🧠 Semantic search with pgvector

🗂️ Resume past conversations via PostgreSQL

🔍 Multi-intent prompt handling

🖥️ Interactive CLI using typer

⚙️ Setup
Clone the repo & install dependencies

bash
Copy
Edit
pip install -r requirements.txt
Add your .env file

ini
Copy
Edit
GROQ_API_KEY=your_groq_api_key
Run the assistant

bash
Copy
Edit
python main.py --new    # Start a new session
python main.py          # Continue an existing session
💡 What Is a Multi-Intent Prompt?
A multi-intent prompt allows users to ask multiple related questions in one go. The assistant parses all the intents and answers them intelligently.

✅ Example:
"Summarize the Thai green curry recipe and list all the ingredients. Also, tell me if it contains any dairy products."

This prompt has three intents:

Summarize the recipe

List the ingredients

Check for dairy

The assistant handles all three in one response — powered by vector search and LLM reasoning.

📚 Knowledge Base
The assistant is currently using:

📄 ThaiRecipes.pdf

You can modify the URL in main.py to load your own PDF.

🧰 Tech Stack
Phi – AI assistant engine

PostgreSQL – Chat history storage

pgvector – Vector DB for semantic search

typer – CLI interface

dotenv – Secure environment config

🛠 Notes
Ensure PostgreSQL is running and pgvector extension is enabled:

sql
Copy
Edit
CREATE EXTENSION IF NOT EXISTS vector;
Default Postgres URL: postgresql+psycopg://ai:ai@localhost:5532/ai

Modify the database URL or PDF URL as needed in the code.

👨‍💻 Author
Ramdular Yadav

Feel free to use, extend, or integrate this into a web app or larger AI tool.

