# TECHNICAL SPECIFICATIONS: ANALYTIQ PRO (V.1.4)

**Strategic Vision:** AI-Agentic Solution Architecture for Business Valuation  
**Core Principles:** Transparency, Human-in-the-loop Governance, and Materiality.

---

## 1. ARCHITECTURAL DECISION RECORD (ADR) – REVISED

| Date | Decision | Rationale (Justification) |
|------|----------|---------------------------|
| 31/03/26 | Agentic Orchestration: LangGraph | Transition to a controlled state-machine. MVP Strategy: Start with a Linear Graph (A → B → C) to manage the learning curve before complexity. |
| 31/03/26 | Governance: The Transparency Ledger | Every AI decision logged in SQLite. Audit focus on Material changes only. |
| 31/03/26 | Strategic Pivot: SQLite-First | Local-first development for rapid prototyping, GitHub portability, and zero-cost scaling. |

---

## 2. UPDATED TECHNICAL STACK (REFINED)

- **Orchestrator:** LangGraph (Open-source)
- **Intelligence:** Gemini 1.5 Pro/Flash (via Google AI Studio)
- **Database & ORM:** SQLite + SQLAlchemy (clean Python-to-SQL mapping)
- **Data Validation:** Pydantic (strict schemas for incoming user data)
- **Backend:** FastAPI (Python)
- **Frontend:** React / Vue (Modern SaaS interface)

---

## 3. AGENTIC WORKFLOW & GUARDRAILS

### Skill 1: The Mapper (Ingestion Agent)
- **Task:** Semantic mapping to the 6-dimension Valuation Matrix.
- **Output:** Lineage Note + Proposed Schema.

### Skill 2: The Auditor (Cleaning Agent)
- **Task:** Logical & Chronological anomaly detection.
- **Loop:** Propose-then-Execute with mandatory Human Gate.

### Skill 3: The Quant (Calculation Agent)
- **Guardrail (Python-based):** Replaces second AI calls for cost efficiency. Includes:
  - Syntax verification
  - Mandatory `WHERE` clause check
  - Strict prohibition of `DELETE` / `DROP` commands without high-level admin override

---

## 4. DATA GOVERNANCE & MATERIALITY

- **The Transparency Ledger:** SQLite table tracking Timestamp, Action, Reasoning, SQL, and Approval.
- **Dynamic Materiality Threshold:**
  - *Default:* 5% impact on final KPIs.
  - *Adjustable:* Users can configure the threshold (1%, 5%, 10%) based on business context (lower for high-precision audit, higher for quick valuation).
- **Cross-Column Logic:** Hard-coded Python rules (e.g., `Order Date >= Signup Date`) that act as immutable truth before AI processing.

---

## 5. GLOBAL & REGIONAL POSITIONING

- **Interface:** Arabic, French, English
- **Outputs / Reports:** Strictly English (standard for UAE & international job markets)
- **Personal Branding:** Positioned as an "AI Solution Architecture" project on GitHub/LinkedIn, demonstrating mastery of the AI Agent trend.

---

## 6. ROADMAP: THE "LOCAL-FIRST" MVP

1. **Phase 1 (The Kernel):** Linear LangGraph script for Ingestion + Mapping + SQLite table creation.
2. **Phase 2 (The Audit):** Integration of the "Cleaning Dialogue" with human validation gates and adjustable materiality.
3. **Phase 3 (The Brain):** Full SQL mapping to the 6-dimension proprietary Matrix.
4. **Phase 4 (The Web UI):** Transition from CLI / Terminal to a full-stack React / FastAPI interface.