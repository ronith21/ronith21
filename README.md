<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=180&color=0:0f2027,50:203a43,100:2c5364&text=Ronith%20Bandaru&fontColor=ffffff&fontSize=46&fontAlignY=36&desc=ML%20%26%20Data%20Engineer%20%C2%B7%20M.Sc.%20Big%20Data%20%26%20AI%20%C2%B7%20Berlin&descAlignY=58&descSize=16" alt="Ronith Bandaru" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Location-Berlin%2C%20Germany-2c5364?style=flat-square" alt="Location: Berlin">
  <img src="https://img.shields.io/badge/Open%20to-Internships%20%26%20Working--student%20roles-2ea44f?style=flat-square" alt="Open to internships and working-student roles">
  <img src="https://img.shields.io/badge/Focus-RAG%20%C2%B7%20Agents%20%C2%B7%20Risk%20Analytics-203a43?style=flat-square" alt="Focus areas">
</p>

## About me

I'm an **M.Sc. Computer Science (Big Data & AI) student at SRH University Berlin**. I build machine-learning and data applications in Python, from the model through the API to the UI.

My projects are tested, evaluated on held-out data, and honest about their limits. I care most about the parts that usually get skipped: refusing when the evidence is weak, measuring results without inflating them, and protecting personal data.

## What I care about

| | Principle | Where it shows up |
|---|---|---|
| 🧪 | **Measured, not claimed** | Held-out benchmarks, ablations, and every error listed by ID ([RAGLens](https://github.com/ronith21/raglens)) |
| 🛡️ | **Safe by default** | A refusal gate that checks the evidence before the LLM is called, a crisis circuit-breaker, and deterministic triage scoring |
| 🔒 | **Privacy-aware** | PII masking (e-mail, IBAN, card, phone) before anything is logged |
| ⚙️ | **Production habits** | High test coverage, strict typing, CI, Docker, metrics and request tracing |

## ⭐ Featured project: [RAGLens](https://github.com/ronith21/raglens)

> **Answers you can check, refusals you can trust.** RAGLens answers questions about banking regulation. Every sentence cites the exact source sentence it came from, and when the documents don't cover a question, it says "I don't know".

```mermaid
flowchart LR
    Q[Question] --> R[Hybrid retrieval<br/>BM25 + FAISS, fused with RRF]
    R --> X[Optional<br/>cross-encoder rerank]
    X --> G{Learned<br/>refusal gate}
    G -- evidence too weak --> N["I don't know"]
    G -- answerable --> L[LLM]
    L --> A[Answer with<br/>sentence-level citations]
```

| Result (held-out data) | Value |
|---|---|
| Unanswerable questions correctly refused | **87.5%** with the learned gate vs 50% with a hand-tuned rule |
| Answerable questions wrongly refused | **4.2%**, down from 16.7% |
| Retrieval hit@5 on the banking corpus (hybrid) | **0.96 to 1.00** across chunk sizes |
| Engineering | 188 tests · 98% coverage · strict mypy · CI on Python 3.11 / 3.12 · Docker |

<sub>Python · FastAPI · Streamlit · FAISS · rank-bm25 · scikit-learn · Prometheus · Hugging Face Spaces</sub>

## 🚧 Currently building

| Project | What it does | Stack |
|---|---|---|
| **TaskHive** | Multi-agent harness: a lead agent splits a job into tasks, helper agents work them over a shared SQLite board, and a grader checks the results | Python · SQLite · pytest |
| **Card Risk: SQL + Excel** | Fraud-risk analysis of card transactions with SQL queries and a formula-driven Excel workbook | SQL · SQLite · Excel · Python |
| **Lead Intelligence Engine** | Ingests company lists, scores leads with explainable rules and drafts outreach in German and English | Python · FastAPI · SQLite · Streamlit |

## 📁 More projects

| Project | What it does | Stack |
|---|---|---|
| **Sage Clinical Assistant** | Safety-first triage assistant: deterministic ESI v4 scoring, a crisis circuit-breaker, and failover across several LLMs | Python · FastAPI · NiceGUI |
| **Berlin Transit Intelligence** | Transit data platform that predicts arrival delays on Deutsche Bahn data | Python · FastAPI · NiceGUI · scikit-learn · Docker |
| **Fraud Anomaly Analytics** | Streaming fraud detection with cost-based thresholds, an analyst case queue and PSI drift monitoring | Python · scikit-learn · FastAPI · NiceGUI |

<sub>Projects without links are private for now. I'm happy to share them on request.</sub>

## 🧰 Tech stack

**Languages**<br>
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=flat-square&logo=postgresql&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white)

**ML & AI**<br>
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![FAISS](https://img.shields.io/badge/FAISS-0467DF?style=flat-square&logo=meta&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)

**Backend & apps**<br>
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)
![NiceGUI](https://img.shields.io/badge/NiceGUI-5898D4?style=flat-square)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat-square&logo=pydantic&logoColor=white)

**Data**<br>
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=flat-square&logo=microsoftexcel&logoColor=white)

**Engineering**<br>
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)
![mypy](https://img.shields.io/badge/mypy-2A6DB2?style=flat-square)
![Ruff](https://img.shields.io/badge/Ruff-D7FF64?style=flat-square&logo=ruff&logoColor=black)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

## 🎓 Education

| Degree | Institution |
|---|---|
| **M.Sc. Computer Science (Big Data & AI)**, in progress | SRH University Berlin, Germany |
| **B.Tech** | GITAM University, India |

## 🌍 Languages

English (IELTS 7.0) · German (A1, still learning)

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=90&section=footer&color=0:0f2027,50:203a43,100:2c5364" alt="" width="100%">
</p>
