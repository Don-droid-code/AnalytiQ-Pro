TECHNICAL SPECIFICATIONS: 
ANALYTIQ PRO (V.1.3) 
Expertise: Software Engineering & Business Data Consulting 
Major Decision: Pivot to a "Local-First" architecture with SQLite. 
1. ARCHITECTURAL DECISION RECORD (ADR) 
Note for Portfolio: This section explains the strategic shift in technology. 
Date 
Decision 
25/03/26 
Pivot: 
PostgreSQL ➔ 
SQLite 
Rationale (Justification) 
MVP Simplification: Eliminates administrative overhead 
(servers, networking). Portability: Database contained in 
a single .db file. Agility: Faster iterations during local 
testing phase. 
25/03/26 Multilingual 
Validation 
Native AR/FR/EN support via Gemini to maximize reach 
(aligned with Morocco 2030 vision). 
2. REVISED TECHNICAL STACK 
• Frontend: React or Vue.js (Modern Web Interface). 
• Backend: FastAPI (Python) – Lightweight server. 
• Database: SQLite. 
o Format: Local file analytiq_pro.db. 
o Advantage: Easy to backup, version on GitHub, and simple to migrate 
later. 
• Artificial Intelligence: Gemini 1.5 Pro API (Mapping & Cleaning Engine). 
• Data Processing: Pandas (Cleaning) & SQLAlchemy (Python ➔ SQLite ORM). 
3. INGESTION & MAPPING LOGIC (PRIORITY 
MODULE) 
Development starts with the "Smart Ingest" module. 
1. Agnostic Ingestion: User uploads any CSV/Excel file. 
2. Semantic Scan (Gemini): AI identifies columns and maps them to the 6 
valuation matrix categories. 
3. SQLite Persistence: * System dynamically creates a table in analytiq_pro.db. 
o Data is stored in a structured format upon import. 
o Added Value: The SQL generated to create these tables is visible to the 
user. 
4. CLEANING & VALIDATION MODULES 
• Chronological Validation: AI uses SQL to compare date columns and trigger 
business logic alerts. 
• Contextual Dialogue: User is prompted regarding anomalies (Refunds, Outliers) 
before any modification to the SQLite database. 
• Time-Intelligence: Automatic detection of date ranges (start/end) and suggestion 
of granularity (Monthly/Quarterly). 
5. VALUATION ENGINE (BACKEND) 
• Excel Matrix Integration: Formulas from your 6 tabs (Financial, Market, 
Operations, Intangibles, Human Capital, Risk/ESG) are translated into Standard 
SQL Queries. 
• Dashboard: SQL query results feed the frontend charts. 
6. DEVELOPMENT WORKFLOW IMPACT 
• Phase 1: Local development with SQLite (.db file). 
• Phase 2: Cloud Deployment. Transitioning to PostgreSQL will be done by simply 
updating the "connection string" in the code, without rewriting the core SQL logic.
