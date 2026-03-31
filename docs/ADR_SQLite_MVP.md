# Architectural Decision Record (ADR) – SQLite for MVP

**Date:** 25/03/2026  
**Status:** Accepted  

## Context
The initial V1.2 architecture used PostgreSQL (via Supabase) to be scalable from day one.  
During the MVP phase, managing a cloud database adds overhead and slows iteration.

## Decision
Use **SQLite** for local development and initial MVP deployment.

## Rationale
- **Zero infrastructure** – no server setup, no network latency  
- **Portability** – the whole database is a single `.db` file, easy to version on GitHub  
- **Agility** – faster iterations during testing  
- **95% SQL compatibility** – migration to PostgreSQL later will be a simple connection string change

## Consequences
- The core SQL logic will remain standard, ensuring a smooth future migration.
- No architectural lock‑in; the application remains cloud‑ready.
