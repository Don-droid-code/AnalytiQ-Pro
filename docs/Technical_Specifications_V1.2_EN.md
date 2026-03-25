# 📘 TECHNICAL SPECIFICATIONS – ANALYTIQ PRO (V.1.2)

**Date:** March 25, 2026  
**Status:** Design & Architecture  
**Expertise:** Software Engineering & Business Data Consulting  
**Goal:** MVP (Minimum Viable Product) – Scalable & Multilingual

---

## 1. SYSTEM ARCHITECTURE & STACK

To ensure zero cost at launch and maximum performance:

- **Frontend (UI):** React or Vue.js (for a smoother SaaS‑like experience compared to Streamlit).
- **Backend (Engine):** FastAPI (Python) – high‑performance, modern, and handles asynchronous tasks perfectly.
- **Database:** PostgreSQL (via Supabase or Render free tiers). Scalable from 1 to 1,000,000 users.
- **Artificial Intelligence:** Gemini 1.5 Pro/Flash API (via Google AI Studio – Free Tier).
- **Data Processing:** Pandas / Numpy (Python ecosystem).

---

## 2. MULTILINGUAL & SEMANTIC MODULE

The application is designed to be natively “Language Agnostic.”

- **Support:** English, French, Arabic (Standard).
- **Dynamic Semantic Mapping:** The AI maps user terms to the Excel Matrix (Backend).  
  *Example:* “Chiffre d’affaires” (FR) or “المبيعات” (AR) → Revenue (Excel Matrix EN).
- **Educational Code:** Generated code remains in English/Python (global standard), but code comments are generated in the user’s preferred language.

---

## 3. INGESTION & TIME INTELLIGENCE

The tool adapts to the data, not the other way around.

- **Automatic Mapping:** AI scans the file and identifies columns (Sales, HR, etc.) without requiring a specific pre‑set format.
- **Temporal Granularity Detection:**
  - Automatic analysis of the Date column.
  - Automatic suggestion of analysis periods: Monthly, Quarterly, Yearly based on the detected history.
- **SQL Persistence:** Imported data is immediately structured into temporary SQL tables for fast calculations.

---

## 4. “CLEANING DIALOGUE” (BUSINESS AUDIT)

Cleaning is not just error correction; it is a validation of business reality.

- **Chronological Consistency Alerts:**
  - *Business Rule:* AI checks logic (e.g., Registration Date < Order Date).
  - *Action:* If inconsistent, AI suggests a fix or requests human validation.
- **Negative Values & Outliers Management:**
  - No automatic deletion. AI asks: “Is this a Refund?” or “Is this an exceptional discount?”.
- **Modular Cleaning:** If a file contains both HR and Sales data, the AI processes both separately based on user needs.

---

## 5. BUSINESS VALUATION ENGINE (EXCEL LOGIC)

Your Excel file becomes the invisible calculation engine.

- **Score Calculation (1‑10):** The 6 dimensions (Financial, Market, Operations, Intangibles, Human Capital, Risk/ESG) are calculated via **SQL Views** based on your Excel formulas.
- **“Full Valuation” Mode:**
  - Explicit option at startup.
  - AI acts as an auditor: summarizes existing data and guides the expert to fill in missing information (assisted manual entry).
- **Insights Dashboard:** Replaces the Excel interface with an attractive visual dashboard and an AI‑generated Narrative Report (Storytelling).

---

## 6. TRANSPARENCY & PEDAGOGY

- **Code Visibility:** A collapsible block displays the real‑time SQL/Python code used for each step.
- **Traceability:** Every cleaning decision is commented within the generated code.

---

## 7. COST SUMMARY (STARTUP PHASE)

| Item | Solution | Cost |
|------|----------|------|
| Code Hosting | GitHub (Private) | 0 MAD |
| Server & API | Render / Google AI Studio (Free Tier) | 0 MAD |
| Database | Supabase (PostgreSQL Free) | 0 MAD |
| Domain Name | Hostinger | Already paid |
| **TOTAL ESTIMATED** | | **0 MAD / month** |
