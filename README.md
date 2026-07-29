<h1 align="center">Hatim EL AALGI</h1>

<p align="center">
  <b>Machine Learning &amp; Data Engineering</b> · <b>AI applied to Cybersecurity</b><br/>
  MSc student in Artificial Intelligence &amp; Digital Computing · Tangier, Morocco
</p>

<p align="center">
  <a href="mailto:hatimelaalgi@outlook.com"><img src="https://img.shields.io/badge/Email-hatimelaalgi%40outlook.com-D14836?style=flat-square&logo=microsoftoutlook&logoColor=white" alt="Email"></a>
  <a href="https://linkedin.com/in/hatim-elaalgi"><img src="https://img.shields.io/badge/LinkedIn-hatim--elaalgi-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <img src="https://img.shields.io/badge/Location-Tangier,%20Morocco-2E7D32?style=flat-square&logo=googlemaps&logoColor=white" alt="Location">
</p>

<p align="center">
  <b>🎯 Seeking a final-year (PFE) internship — February to June 2027</b><br/>
  <sub>AI for cybersecurity · Machine Learning · Data Engineering — Casablanca / Rabat / remote</sub>
</p>

---

## About

I build **end-to-end machine learning systems** — real-time pipelines, models, and the evaluation
that tells you whether the model is actually any good.

The evaluation part is where I spend most of my effort, because it is where most projects quietly
go wrong: metrics chosen for imbalanced classes rather than accuracy, thresholds calibrated on
business cost rather than F1, data leakage hunted down and measured, and guardrails against model
hallucination.

Since April 2026 I have been developing an **AI-assisted SOC investigation copilot** for
**Synertic**, an ESN specialising in secure software.

---

## Featured work

### 🛡️ NIDS-FL — Federated-Learning Network Intrusion Detection
`Kafka (KRaft)` `FastAPI` `Docker` `Neo4j` `TensorFlow` `XGBoost` `Optuna` `React`

Real-time intrusion detection where **raw traffic never leaves the site it was captured on**.

- Live pipeline: packet capture → FastAPI WebSocket → Kafka, sustained at **>1,000 packets/sec**
- **Federated learning (FedAvg)** across 3 clients — **65 KB of weights per round** instead of
  centralising 1.2 GB of raw traffic
- **Two-stage hybrid architecture**, designed because tree models cannot be aggregated by FedAvg:
  a federated MLP at the edge (99.38%, F1 0.9889) escalates only uncertain traffic to a cloud
  XGBoost classifier (99.44%, 7 classes) — **83% of traffic never leaves the edge**
- **Continual learning** with a replay buffer: −2% macro-F1 across 8 weeks of simulated concept
  drift, against −16% for a static model
- Limits documented rather than hidden — macro-F1 is 0.862, held down by an F1 of 0.28 on the two
  ultra-minority attack classes

### 💳 Unsupervised Bank Fraud Detection — VAE · Isolation Forest · LSTM-AE
[![repo](https://img.shields.io/badge/GitHub-fraud--detection--vae-181717?style=flat-square&logo=github)](https://github.com/Hatim-elaalgi/fraud-detection-vae)
`Python` `PyTorch` `scikit-learn` `SHAP` `Streamlit`

Three anomaly-detection models compared across three datasets, at **0.12% fraud prevalence** and
with **no labels at training time**.

- Model selection driven by **AUC-PR, not accuracy or ROC-AUC** — at this imbalance ROC-AUC is
  actively misleading. The VAE reaches **0.1139 vs 0.0497** for Isolation Forest (**+129%**), with
  **44.2% recall against 26.9%**
- Threshold calibrated on **business cost** rather than F1 → **24% lower operational cost**
- Per-transaction **SHAP** explanations and a multi-page Streamlit dashboard (alerts, threshold
  tuning, ROC / Precision-Recall)

### 🔬 Reproducibility Audit — Vote Count Model, Parkinson's Disease
[![repo](https://img.shields.io/badge/GitHub-parkinsons--vcm--reproduction-181717?style=flat-square&logo=github)](https://github.com/Hatim-elaalgi/parkinsons-vcm-reproduction)
`Python` `NumPy` `scikit-learn` `pytest`

A faithful reproduction of Mall et al. (2022), then a critical audit of it. The pipeline is
implemented **twice** — once with scikit-learn, once entirely from scratch in NumPy.

- Individual model accuracies reproduced **exactly**
- **The paper's central claim does not hold**: the voting ensemble beats its best member in only
  **4 of 100 random seeds**
- Identified **speaker-level data leakage worth 9–17 accuracy points**. Honest subject-wise
  validation gives **73–84%**, against the **94.87%** reported

---

## Other public projects

| Project | What it is | Stack |
|---|---|---|
| [**ResearchWatch**](https://github.com/Hatim-elaalgi/ResearchWatchElasticsearch) | Scientific search engine over arXiv — bilingual FR/EN custom analyzer, relevance evaluation (precision@k, MRR), Kibana dashboard | Elasticsearch · Kibana · FastAPI |
| [**TecHorizon**](https://github.com/Hatim-elaalgi/TecHorizon) | Collaborative online magazine with a 4-level role hierarchy and an editorial review workflow | Laravel 11 · PHP · MySQL |
| [**Petit Bac multi-agent**](https://github.com/Hatim-elaalgi/jeux_bac) | JADE agents communicating over ACL messages; BFS, DFS, UCS and A\* compared on a trie search problem with an admissible heuristic | Java · JADE |
| [**Deep FFN study**](https://github.com/Hatim-elaalgi/TP2-deeplearning) | Regularisation ablation plus grid and random search — random search won at equal budget | PyTorch |
| [**ETL & dashboard**](https://github.com/Hatim-elaalgi/preProcessingETL_NIFI) | CSV → PostgreSQL star schema with analytical queries and a Streamlit dashboard | NiFi · Python · PostgreSQL |
| [**Segmentation from scratch**](https://github.com/Hatim-elaalgi/customer-segmentation-compare) | KNN and multinomial softmax regression written in NumPy, benchmarked against scikit-learn | NumPy · scikit-learn |

## Professional &amp; private work

Not public, but happy to discuss:

- **SOC Copilot** *(Synertic, Apr 2026 – present)* — AI-assisted investigation of compromise
  incidents on Linux hosts: event correlation, MITRE ATT&CK mapping, prioritised remediation plans.
  A **dual-model trust boundary enforced in code** — the local model handles raw data, the cloud
  model only ever receives sanitised context, and that boundary cannot be bypassed by configuration.
  **No autonomous execution**: every remediation step passes explicit human approval, a
  deny-by-default allowlist, and synchronous audit logging.
- **Ibn Battuta** — multimodal AI tourist guide. Animated 3D avatar with lip sync, accepting text,
  voice and photo input through a locally-hosted vision-language model, RAG over ChromaDB,
  concurrent aggregation of 8 public APIs, and 3-pass itinerary generation streamed over SSE.
  *(React / Three.js, FastAPI)*
- **Chatbot ATLAS** *(Haut-Commissariat au Plan — Morocco's national statistics institute)* —
  conversational analytics over national statistical databases: a **natural-language → SQL** engine
  on PostgreSQL behind a secured Flask REST API, with interactive KPI dashboards and indicator
  alerting.
- **Odoo ERP development** *(Dynamic Horizon)* — Sales, Stock and Accounting modules in Python and
  XML, REST API integrations, PostgreSQL migrations.

---

## Tech

**Languages &amp; data**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

**Data engineering**

![Kafka](https://img.shields.io/badge/Apache%20Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![NiFi](https://img.shields.io/badge/Apache%20NiFi-728E9B?style=flat-square&logo=apachenifi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![Elasticsearch](https://img.shields.io/badge/Elasticsearch-005571?style=flat-square&logo=elasticsearch&logoColor=white)
![Neo4j](https://img.shields.io/badge/Neo4j-4581C3?style=flat-square&logo=neo4j&logoColor=white)

**Machine learning**

![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=flat-square&logo=keras&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-337AB7?style=flat-square&logo=xgboost&logoColor=white)
![Optuna](https://img.shields.io/badge/Optuna-2E5B88?style=flat-square)
![SHAP](https://img.shields.io/badge/SHAP-1B9E77?style=flat-square)

<sub>Random Forest · MLP · LSTM · Variational Autoencoders · Federated Learning</sub>

**Generative AI &amp; LLM**

![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6B6B?style=flat-square)
![Gemini](https://img.shields.io/badge/Google%20Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white)

<sub>RAG · Sentence-Transformers · Natural Language → SQL · multi-agent systems · prompt engineering</sub>

**Visualisation &amp; web**

![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=flat-square&logo=plotly&logoColor=white)
![PowerBI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat-square&logo=powerbi&logoColor=black)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white)
![Qt](https://img.shields.io/badge/PySide6-41CD52?style=flat-square&logo=qt&logoColor=white)

<sub>Also: Apache Spark · R · Odoo · Laravel / PHP · UML &amp; Merise · n8n</sub>

---

## Education

| | |
|---|---|
| **MSc — Artificial Intelligence &amp; Digital Computing** | FST, Université Moulay Slimane · 2025–2027 *(in progress)* |
| **BSc — Data Analysis** | FST Tanger, Université Abdelmalek Essaâdi · 2022–2025 |

**Languages** — Arabic (native) · French (fluent, professional) · English (intermediate — reading
technical and scientific literature comfortably)

---

<p align="center">
  <sub>Open to PFE internship offers for February–June 2027 · <a href="mailto:hatimelaalgi@outlook.com">hatimelaalgi@outlook.com</a></sub>
</p>
