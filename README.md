<img width="100%" src="./assets/header.svg" alt="Hatim EL AALGI — Machine Learning & Data Engineering · Generative AI · Anomaly Detection · AI for Cybersecurity · Real-Time Data Systems" />

<p align="center">
  <a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=21&duration=3200&pause=900&color=E07B39&center=true&vCenter=true&width=760&lines=Multimodal+GenAI+%E2%80%94+vision%2C+voice+and+RAG+in+one+app;Natural+language+to+SQL+over+national+statistics;Anomaly+detection+that+survives+a+0.12%25+base+rate;Trust+boundaries+enforced+in+code%2C+not+config;Real-time+pipelines+at+%3E1%2C000+events%2Fsecond;Reproducing+papers+%E2%80%94+and+auditing+what+they+claim" alt="Focus areas" /></a>
</p>

<p align="center">
  <a href="mailto:hatimelaalgi@outlook.com"><img src="https://img.shields.io/badge/Email-hatimelaalgi@outlook.com-E07B39?style=for-the-badge&logo=maildotru&logoColor=white" alt="Email"></a>
  <a href="https://linkedin.com/in/hatim-elaalgi"><img src="https://img.shields.io/badge/LinkedIn-hatim--elaalgi-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <img src="https://img.shields.io/badge/Tangier-Morocco-2E7D32?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Tangier, Morocco">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/%F0%9F%8E%AF%20Seeking%20PFE%20internship-February%20%E2%80%93%20June%202027-E07B39?style=flat-square&labelColor=1A1A1A" alt="Seeking PFE internship, February to June 2027">
  <br>
  <sub>Machine Learning · Generative AI · AI for Cybersecurity · Data Engineering — Casablanca / Rabat</sub>
</p>

---

## <img src="https://media.giphy.com/media/QssGEmpkyEOhBCb7e1/giphy.gif" width="26"> &nbsp;About

I build **end-to-end machine learning systems** — real-time pipelines, models, and the evaluation
that tells you whether a model is actually any good. That last part is where I spend most of my
effort, because it is where projects quietly go wrong: metrics chosen for class imbalance instead of
accuracy, thresholds calibrated on business cost rather than F1, data leakage hunted down and
quantified, guardrails against model hallucination.

That approach travels — my work spans **generative AI**, **anomaly detection**, **real-time data
engineering**, **information retrieval** and **research reproducibility**, applied to public
statistics, finance, healthcare research, tourism and network security.

Currently building an AI-assisted investigation copilot at **Synertic**.
`MSc Artificial Intelligence & Digital Computing · 2025–2027 · Université Moulay Slimane`

---

## <img src="https://media.giphy.com/media/iY8CRBdQXODJSCERIr/giphy.gif" width="26"> &nbsp;Flagship work

### 🧭 Ibn Battuta — Multimodal AI Travel Guide

A generative-AI app taking **text, voice and photos**, answering as an animated guide.

- **Animated 3D avatar with lip-sync**, driven by the generated response
- Text, speech and photos interpreted by a **locally-hosted vision-language model** — no paid API
- **RAG over ChromaDB**, **8 public APIs queried concurrently**, **3-pass itinerary generation**
  streamed over **SSE**

`React` `Three.js` `FastAPI` `ChromaDB` `Sentence-Transformers` &nbsp;·&nbsp; <sub>🔒 private — demo on request</sub>

### 🌐 [NIDS-FL — Privacy-Preserving Distributed Learning](https://github.com/Hatim-elaalgi/NIDS)

Federated learning over network traffic: **models travel, data never does.**

| | |
|---|---|
| Throughput | >1,000 events/sec — capture → FastAPI WebSocket → Kafka |
| Federated | FedAvg over 3 clients — **65 KB/round** vs centralising **1.2 GB** |
| Two-stage | Edge MLP (99.38%, F1 **0.9889**) escalates only uncertain cases to cloud XGBoost (99.44%, 7 classes) |
| Efficiency | **83% of traffic never leaves the edge** |
| Drift | Replay buffer: **−2%** macro-F1 over 8 simulated weeks vs **−16%** static |
| Honest limits | macro-F1 0.862 — held down by F1 0.28 on the two rarest classes |

Tree ensembles can't be aggregated by FedAvg, so the federated model has to be the neural one at the edge.

`Kafka (KRaft)` `FastAPI` `Docker` `Neo4j` `TensorFlow` `XGBoost` `Optuna` `React`

---

## <img src="https://media.giphy.com/media/dWesBcTLavkZuG35MI/giphy.gif" width="26"> &nbsp;Featured repositories

<table>
<tr>
<td width="50%" valign="top">

#### 💳 [fraud-detection-vae](https://github.com/Hatim-elaalgi/fraud-detection-vae)

VAE · Isolation Forest · LSTM-AE at a **0.12% base rate**, no labels at training time.

- Selected on **AUC-PR, not ROC-AUC** — misleading at this imbalance. VAE **0.1139 vs 0.0497** (**+129%**), recall **44.2% vs 26.9%**
- Threshold calibrated on **business cost** → **24% lower operational cost**
- Per-transaction **SHAP** + multi-page Streamlit dashboard

</td>
<td width="50%" valign="top">

#### 🔬 [parkinsons-vcm-reproduction](https://github.com/Hatim-elaalgi/parkinsons-vcm-reproduction)

Reproduction **and** audit of Mall et al. (2022) — implemented **twice**, scikit-learn and pure NumPy.

- Individual accuracies reproduced **exactly**
- **The paper's central claim fails** — the ensemble beats its best member in only **4 of 100 seeds**
- Found **speaker leakage worth 9–17 points**: honest validation **73–84%** vs the **94.87%** reported

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### 🔎 [ResearchWatch](https://github.com/Hatim-elaalgi/ResearchWatchElasticsearch)

Scientific search over arXiv — bilingual FR/EN analyzer, relevance evaluation (precision@k, MRR),
FastAPI service and Kibana dashboard.

</td>
<td width="50%" valign="top">

#### 💬 [ChatbotRAG_HCP](https://github.com/Hatim-elaalgi/ChatbotRAG_HCP)

RAG over Moroccan statistics — FAISS retrieval with **tabular rows rendered into sentences before
embedding**, plus a correction feedback loop.

</td>
</tr>
</table>

<details>
<summary><b>More public repositories</b></summary>

<br>

| Project | What it is | Stack |
|---|---|---|
| [**TecHorizon**](https://github.com/Hatim-elaalgi/TecHorizon) | Collaborative online magazine — four-level role hierarchy, editorial review workflow | Laravel 11 · PHP |
| [**Advanced_DASHBORD**](https://github.com/Hatim-elaalgi/Advanced_DASHBORD) | Desktop choropleth of Moroccan regions + chart builder (synthetic dataset) | PySide6 · GeoPandas · Folium |
| [**Petit Bac multi-agent**](https://github.com/Hatim-elaalgi/jeux_bac) | JADE agents over ACL; BFS, DFS, UCS and A\* on a trie with an admissible heuristic | Java · JADE |
| [**Deep FFN study**](https://github.com/Hatim-elaalgi/TP2-deeplearning) | Regularisation ablation + grid vs random search — random search won at equal budget | PyTorch |
| [**ETL & dashboard**](https://github.com/Hatim-elaalgi/preProcessingETL_NIFI) | CSV → PostgreSQL star schema, analytical SQL, Streamlit dashboard | NiFi · PostgreSQL |
| [**Segmentation from scratch**](https://github.com/Hatim-elaalgi/customer-segmentation-compare) | KNN + multinomial softmax in NumPy, benchmarked against scikit-learn | NumPy · scikit-learn |

</details>

---

## <img src="https://media.giphy.com/media/LnQjpWaON8nhr21vNW/giphy.gif" width="26"> &nbsp;Professional &amp; private work

<details open>
<summary><b>Not public — happy to walk through any of these</b></summary>

<br>

**SOC Copilot** · *Synertic · Apr 2026 – present* — AI-assisted investigation of compromise incidents
on Linux hosts: event correlation, MITRE ATT&CK mapping, prioritised remediation. A **dual-model
trust boundary enforced in code** (local model sees raw data, cloud model only sanitised context —
not bypassable by configuration) and **no autonomous execution**: every step passes human approval,
a deny-by-default allowlist, and synchronous audit logging.
`Node.js` `local & cloud LLM agents` `SSH` `OIDC/SSO` `nginx` `OCI`

**Chatbot ATLAS** · *Haut-Commissariat au Plan — national statistics institute* — **Natural-language
→ SQL** over national statistical databases, behind a secured Flask REST API, with KPI dashboards
and indicator alerting. The model receives the live schema and geographic hierarchy, so it queries
real tables rather than guessed ones.
`Python` `Flask` `PostgreSQL` `Google Gemini`

**Odoo ERP development** · *Dynamic Horizon · Jul – Nov 2025* — Sales, Stock and Accounting modules
in Python and XML, REST API integrations, PostgreSQL migrations.

</details>

---

## <img src="https://media.giphy.com/media/WFZvB7VIXBgiz3oDXE/giphy.gif" width="26"> &nbsp;Tech

<p align="center">
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch">
<img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white" alt="TensorFlow">
<img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white" alt="scikit-learn">
<img src="https://img.shields.io/badge/Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white" alt="Kafka">
<img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI">
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker">
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL">
<img src="https://img.shields.io/badge/Elasticsearch-005571?style=for-the-badge&logo=elasticsearch&logoColor=white" alt="Elasticsearch">
<img src="https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" alt="LangChain">
<img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React">
<img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Streamlit">
</p>

| | |
|---|---|
| **Languages & data** | Python (Pandas, NumPy, scikit-learn, TensorFlow/Keras) · SQL · PostgreSQL · MongoDB · Java · Git |
| **Data engineering** | Apache Kafka · Apache NiFi · Docker · FastAPI · Flask · ETL pipelines · Elasticsearch · Neo4j |
| **Machine learning** | XGBoost · Random Forest · MLP · LSTM · Variational Autoencoders · Federated Learning · Optuna · SHAP |
| **Generative AI & LLM** | RAG (ChromaDB, FAISS, Sentence-Transformers) · LangChain · Google Gemini · NL→SQL · multi-agent systems · prompt engineering |
| **Visualisation & web** | Streamlit · Power BI · Plotly · Matplotlib · Seaborn · PySide6 · React/TypeScript · Three.js |
| **Also** | Apache Spark · R · Odoo · Laravel/PHP · UML & Merise · n8n |

---

<div align="center">

**MSc — Artificial Intelligence & Digital Computing** · FST, Université Moulay Slimane · 2025–2027
**BSc — Data Analysis** · FST Tanger, Université Abdelmalek Essaâdi · 2022–2025

![Arabic](https://img.shields.io/badge/Arabic-native-2E7D32?style=flat-square)
![French](https://img.shields.io/badge/French-fluent-0055A4?style=flat-square)
![English](https://img.shields.io/badge/English-intermediate-B22234?style=flat-square)

<br>

**Open to PFE internship offers — February to June 2027**
[hatimelaalgi@outlook.com](mailto:hatimelaalgi@outlook.com) · [LinkedIn](https://linkedin.com/in/hatim-elaalgi)

</div>

<img width="100%" src="./assets/footer.svg" alt="" />
