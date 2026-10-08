# Financial Health Engine
### Asset Vantage Hackathon — Group 5

> From raw financial data to actionable financial insights.

A full-stack financial health analysis platform developed as part of the **Asset Vantage Hackathon**.

The application ingests financial transactions, asset snapshots, and liabilities to calculate financial metrics, detect anomalies, generate a deterministic **0–100 Financial Health Score**, and provide prioritized recommendations.

---

## 👨‍💻 My Contribution

I was primarily responsible for the **backend development** of this project.

I designed and implemented the backend using **Python and FastAPI**, including:

- Designed the backend API structure and application flow
- Implemented financial data ingestion and validation
- Built financial metric calculations using Pandas
- Implemented anomaly detection using IQR-based analysis
- Developed the deterministic **0–100 Financial Health Scoring Engine**
- Implemented SQLite database integration
- Built the AI-powered recommendation module with deterministic fallback logic
- Added Pydantic-based validation for structured AI responses
- Developed and tested backend functionality

The frontend and overall product were developed collaboratively as part of the hackathon team.

---

## 🏗️ System Architecture

```text
                    Financial Data
                          │
                          ▼
                ┌───────────────────┐
                │   Data Ingestion  │
                │   & Validation    │
                └─────────┬─────────┘
                          │
                          ▼
                ┌───────────────────┐
                │ Financial Metrics │
                │   & Calculations  │
                └─────────┬─────────┘
                          │
             ┌────────────┼────────────┐
             ▼            ▼            ▼
        Anomaly       Health Score   Database
        Detection       Engine        Layer
             │            │
             └────────────┼────────────┘
                          ▼
                ┌───────────────────┐
                │ Recommendations   │
                │ AI + Rule Fallback│
                └─────────┬─────────┘
                          │
                          ▼
                    FastAPI REST API
                          │
                          ▼
                     React Frontend

⚙️ Tech Stack
Backend
- Python
- FastAPI
- Pandas
- Pydantic
- SQLite
- REST APIs
AI
- Google Gemini
- Structured output validation
- Deterministic rule-based fallback
Frontend
- React
- Vite
- TypeScript
- Tailwind CSS
- Recharts
🔌 Backend API
The backend exposes REST endpoints for the major financial analysis capabilities.
Endpoint	Purpose
GET /api/health-check	Check backend availability
POST /api/upload	Upload financial data
GET /api/data-quality	Retrieve data quality information
GET /api/financial-summary	Retrieve financial metrics and summary
GET /api/anomalies	Detect anomalous financial records
GET /api/health-score	Calculate the 0–100 financial health score
GET /api/predictions	Retrieve financial predictions
GET /api/recommendations	Generate prioritized recommendations


🧠 Financial Health Engine
The backend processes financial information through several stages.
1. Data Ingestion
Raw financial datasets containing transactions, assets, and liabilities are ingested and processed before being used by the financial engine.
2. Financial Metrics
The system calculates metrics such as:
- Savings Rate
- Debt-to-Asset Ratio
- EMI Burden
- Liquidity
- Cash Flow
- Asset and liability information
3. Anomaly Detection
Financial records are analyzed for unusual values using statistical techniques including IQR-based anomaly detection.
4. Health Score
A deterministic scoring model produces a 0–100 Financial Health Score based on multiple financial dimensions, including:
- Savings
- Liquidity
- Debt
- Solvency
- Cash Flow Stability
The scoring calculations are performed by the backend rather than delegated to the LLM.
5. Recommendations
The system generates prioritized financial recommendations using an AI-assisted recommendation layer.
A deterministic rule-based fallback is also available so the application can continue producing recommendations when the AI service is unavailable or rate-limited.
📁 Project Structure
av-hackathon-group-5/
│
├── backend/
│   ├── app/
│   │   ├── main.py
│   │   ├── ingestion.py
│   │   ├── metrics.py
│   │   ├── scoring.py
│   │   ├── anomalies.py
│   │   ├── ai_recommender.py
│   │   ├── database.py
│   │   └── config.py
│   │
│   ├── tests/
│   ├── requirements.txt
│   └── run.py
│
├── frontend/
├── public/
├── src/
├── PLAN.md
└── README.md

🚀 Running the Backend
1. Clone the repository
git clone https://github.com/Sameerraut1308/av-hackathon-group-5.git
cd av-hackathon-group-5

2. Create a virtual environment
python -m venv venv

Activate it on Windows:
venv\Scripts\activate

3. Install dependencies
cd backend
pip install -r requirements.txt

4. Start the backend
python run.py

The FastAPI application can then be accessed through the local server.
📊 Data Processing Pipeline
Raw Financial Data
        ↓
Data Validation
        ↓
Data Ingestion
        ↓
Metric Calculation
        ↓
Anomaly Detection
        ↓
Financial Health Scoring
        ↓
AI / Rule-Based Recommendations
        ↓
REST API Response

🏆 Hackathon
Asset Vantage Hackathon
This project was developed collaboratively by Group 5 as a solution to the hackathon problem statement.
The repository represents the complete team project. My primary responsibility within the team was backend engineering and financial analysis logic.
👥 Team
This is a collaborative hackathon project developed by Group 5.
See the repository contributors and commit history for the complete list of contributors.
📌 Project Plan
The original implementation blueprint and development plan are available in [`PLAN.md`](PLAN.md).
📄 License
This project was developed for the Asset Vantage Hackathon.
