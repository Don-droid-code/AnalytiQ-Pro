# 📘 MÉMORANDUM DE TRANSFERT : ANALYTIQ PRO

**Date :** 2 avril 2026  
**Statut :** Infrastructure validée & Alignement Stratégique  
**Objectif :** Continuité de la mémoire projet pour le passage d'une session à une autre.

---

## 1. VISION & FONDATIONS MÉTIER

AnalytiQ Pro est une plateforme de **Business Valuation holistique**.  
Son intelligence repose sur la **Matrice de Critical Thinking (6 dimensions)** et refuse l'effet **"Boîte Noire" (Black Box)**.

### Les 6 Dimensions de la Matrice

Chaque analyse doit être filtrée par ces piliers, avec une flexibilité totale (l'IA s'adapte aux données disponibles) :

- **Financial Performance & Capital** : rentabilité, cash-flow, structure de la dette.
- **Market Position & Strategic Moat** : parts de marché, barrières à l'entrée, rétention client.
- **Operational Efficiency & Scalability** : automatisation, OpEx, agilité de la supply chain.
- **Intangible Assets & IP** : brevets, marque, logiciels propriétaires, valeur des données.
- **Human Capital & Culture** : leadership, turnover, culture d'innovation.
- **Risk, Governance & ESG** : conformité, cybersécurité, indépendance de la gouvernance.

---

## 2. STACK TECHNIQUE ACTUELLE (V.1.4)

L'environnement local est configuré et sécurisé.

- **Langage** : Python 3.13 (environnement virtuel `venv` activé)
- **IA (Moteur)** : Gemini 2.5 Flash (modèle actif sur le compte Google)
- **Orchestration** : LangGraph (logique d'états avec *Human-in-the-loop*)
- **Base de Données** : SQLite (architecture *Local-First* pour la portabilité)
- **Bibliothèques clés** : `google-generativeai`, `python-dotenv`, `SQLAlchemy`, `Pandas`

---

## 3. RÈGLES DE GOUVERNANCE (LANGGRAPH)

Le workflow suit un principe de **"Proposer-puis-Exécuter"** :

- **Pause Obligatoire** : l'agent IA s'arrête après chaque étape critique (Audit, Mapping, Scoring).
- **Raisonnement Exposé** : l'IA présente son raisonnement en langage clair avant toute action.
- **Validation Humaine (Gate)** : l'utilisateur donne son accord explicite pour passer à l'étape suivante.
- **Auditabilité** : toutes les actions (SQL/Python) sont visibles et stockées dans un registre de transparence.

---

## 4. ÉTAT D'AVANCEMENT : `test_api.py`
**Phase 1 – Kernel** : ✅ Finalisé (3 avril 2026)
- 10 tables SQLite, Transparency Ledger, seuil matérialité 5%, 63 traps intégrés
Le fichier `test_api.py` est **100% opérationnel** et sert de preuve de concept (PoC).

- **Succès** : connexion établie avec l'API Google.
- **Découverte** : le système a détecté que le compte utilisateur est sur **Gemini 2.5 Flash**.
- **Sécurité** : la clé API est correctement chargée via le fichier `.env` (protégé par `.gitignore`).
- **Résultat** : l'IA a répondu avec succès à une requête de test confirmant qu'elle est prête pour AnalytiQ Pro.

---

## 5. PROCHAINE ÉTAPE PRIORITAIRE

**Phase 1 – Data Architecture** : création du fichier `database.py`.

- **Objectif** : définir les tables SQLite capables de stocker les données brutes et les scores qualitatifs liés aux 6 dimensions.

---

## 🛡️ Note de Procédure

Pour toute nouvelle session, l'utilisateur doit fournir ce document à l'IA pour **ré-ancrer le contexte** avant de poursuivre le développement.
