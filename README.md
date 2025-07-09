# FinSecure-AI
AI-powered fraud detection and credit risk API for fintechs.
FinSecure AI - Fraud Detection & Risk Scoring API (Backend)

Welcome to the backend of FinSecure AI, a smart fraud detection and user risk scoring system designed for African fintech companies.


---

🔧 Tech Stack

Language: Python 3.10+

Framework: FastAPI

ML Engine: Scikit-learn (coming soon)

Database: PostgreSQL (via SQLAlchemy + Supabase)

Auth: API key (JWT planned)

Docs: Auto-generated with Swagger UI (at /docs)



---

🚀 Features (v0.1)

/score-user API: Accepts user metadata and returns a fraud and risk score

Fraud flag detection logic (SIM swap, device change, repayment issues)

Logs all requests to the database for future analysis



---

📦 Setup Instructions

1. Clone the Repo

git clone https://github.com/Berine254/FinSecure-AI.git
cd FinSecure-AI/backend

2. Create a Virtual Environment

python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate    # Windows

3. Install Requirements

pip install -r requirements.txt

4. Create a .env file

DATABASE_URL=your_supabase_database_url_here

5. Run the Server

uvicorn main:app --reload

Visit http://localhost:8000/docs for interactive API documentation.


---

📫 API Example: /score-user

Request

{
  "phone": "+254712345678",
  "id_number": "12345678",
  "sim_swapped": true,
  "device_change": true,
  "loan_history": [1000, 3000, -2000, 500],
  "location": "Nairobi"
}

Response

{
  "fraud_score": 340,
  "credit_score": 420,
  "flags": [
    "Recent SIM swap",
    "Multiple device logins",
    "Late repayment history"
  ]
}


---

✅ To-Do

[ ] Integrate ML model (Phase 2)

[ ] Add API Key auth

[ ] Write test cases

[ ] Build Dockerfile for deployment

[ ] Finish admin dashboard UI



---

🧠 Contributing

This is a public project created by Blessed Berine as part of PLP and a real-world fintech solution. For business inquiries, reach out via blessedberine@gmail.com.


---

📄 License

MIT License

