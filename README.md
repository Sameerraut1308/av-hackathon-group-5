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
