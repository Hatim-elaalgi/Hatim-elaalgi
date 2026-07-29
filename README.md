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
that tells you whether a model is actually any good.

The evaluation is where I spend most of my effort, because it is where projects quietly go wrong:
metrics chosen for class imbalance instead of accuracy, thresholds calibrated on business cost
rather than F1, data leakage hunted down and quantified, and guardrails against model hallucination.

That approach travels across domains — my work spans **generative AI and LLM systems**,
**anomaly detection**, **real-time data engineering**, **information retrieval**, and
**research reproducibility**, applied to public statistics, finance, healthcare research, tourism
and network security.

Currently building an AI-assisted investigation copilot at **Synertic**, an ESN specialising in
secure software.

<br>

<div align="center">

`MSc Artificial Intelligence & Digital Computing` · `2025–2027` · `Université Moulay Slimane`

</div>

---

## <img src="https://media.giphy.com/media/iY8CRBdQXODJSCERIr/giphy.gif" width="26"> &nbsp;Flagship work

<table>
<tr><td>

### 🧭 Ibn Battuta — Multimodal AI Travel Guide

**A generative-AI application that takes text, voice *and* photos, and answers as an animated guide.**

| | |
|---|---|
| **Multimodal input** | Text, speech, and photographs interpreted by a **locally-hosted vision-language model** |
| **Presentation** | Animated **3D avatar with lip-sync**, driven by the generated response |
| **Retrieval** | **RAG over ChromaDB** for grounded answers about places and history |
| **Aggregation** | **8 public APIs queried concurrently** and merged into one itinerary |
| **Generation** | **3-pass itinerary construction**, streamed to the browser over **SSE** |

Everything runs against a self-hosted model rather than a paid API — the interesting constraint,
and the reason the architecture is built around local inference and concurrency.

`React` `Three.js` `FastAPI` `ChromaDB` `Sentence-Transformers` `SSE`

<sub>🔒 Private — demo available on request</sub>

</td></tr>
<tr><td>

### 🌐 [NIDS-FL — Privacy-Preserving Distributed Learning](https://github.com/Hatim-elaalgi/NIDS)

**Federated learning applied to network traffic: models travel, data never does.**

| | |
|---|---|
| **Throughput** | >1,000 events/sec — capture → FastAPI WebSocket → Kafka |
| **Federated** | FedAvg across 3 clients — **65 KB of weights per round** vs centralising **1.2 GB** of raw data |
| **Two-stage** | Edge MLP (99.38%, F1 **0.9889**) escalates only uncertain cases to cloud XGBoost (99.44%, 7 classes) |
| **Efficiency** | **83% of traffic never leaves the edge** |
| **Drift** | Replay-buffer continual learning: **−2%** macro-F1 over 8 simulated weeks, against **−16%** static |
| **Honest limits** | macro-F1 0.862 — held down by F1 0.28 on the two rarest classes |

The two-stage split exists for a reason: tree ensembles cannot be aggregated by FedAvg, so the
federated model has to be the neural one at the edge.

`Kafka (KRaft)` `FastAPI` `Docker` `Neo4j` `TensorFlow` `XGBoost` `Optuna` `React`

<a href="https://github.com/Hatim-elaalgi/NIDS"><img src="https://img.shields.io/badge/GitHub-NIDS-181717?style=flat-square&logo=github&labelColor=1A1A1A" alt=""></a>
<a href="https://github.com/Hatim-elaalgi/NIDS"><img src="https://img.shields.io/github/languages/top/Hatim-elaalgi/NIDS?style=flat-square&color=E07B39&labelColor=1A1A1A" alt=""></a>
<a href="https://github.com/Hatim-elaalgi/NIDS"><img src="https://img.shields.io/github/last-commit/Hatim-elaalgi/NIDS?style=flat-square&color=555&labelColor=1A1A1A" alt=""></a>

</td></tr>
</table>

---

## <img src="https://media.giphy.com/media/dWesBcTLavkZuG35MI/giphy.gif" width="26"> &nbsp;Featured repositories

<table>
<tr>
<td width="50%" valign="top">

#### 💳 [fraud-detection-vae](https://github.com/Hatim-elaalgi/fraud-detection-vae)

Unsupervised bank-fraud detection — VAE, Isolation Forest and LSTM-AE compared at a 0.12% base rate,
with no labels at training time.

<a href="https://github.com/Hatim-elaalgi/fraud-detection-vae"><img src="https://img.shields.io/github/languages/top/Hatim-elaalgi/fraud-detection-vae?style=flat-square&color=E07B39&labelColor=1A1A1A" alt=""></a>
<a href="https://github.com/Hatim-elaalgi/fraud-detection-vae"><img src="https://img.shields.io/github/last-commit/Hatim-elaalgi/fraud-detection-vae?style=flat-square&color=555&labelColor=1A1A1A" alt=""></a>

</td>
<td width="50%" valign="top">

#### 🔬 [parkinsons-vcm-reproduction](https://github.com/Hatim-elaalgi/parkinsons-vcm-reproduction)

Reproduction **and** reproducibility audit of a published paper — implemented twice, once in
scikit-learn and once from scratch in NumPy.

<a href="https://github.com/Hatim-elaalgi/parkinsons-vcm-reproduction"><img src="https://img.shields.io/github/languages/top/Hatim-elaalgi/parkinsons-vcm-reproduction?style=flat-square&color=E07B39&labelColor=1A1A1A" alt=""></a>
<a href="https://github.com/Hatim-elaalgi/parkinsons-vcm-reproduction"><img src="https://img.shields.io/github/last-commit/Hatim-elaalgi/parkinsons-vcm-reproduction?style=flat-square&color=555&labelColor=1A1A1A" alt=""></a>

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### 🔎 [ResearchWatch](https://github.com/Hatim-elaalgi/ResearchWatchElasticsearch)

Scientific search engine over arXiv — bilingual FR/EN custom analyzer, relevance evaluation
(precision@k, MRR), FastAPI service and a Kibana dashboard.

<a href="https://github.com/Hatim-elaalgi/ResearchWatchElasticsearch"><img src="https://img.shields.io/github/languages/top/Hatim-elaalgi/ResearchWatchElasticsearch?style=flat-square&color=E07B39&labelColor=1A1A1A" alt=""></a>
<a href="https://github.com/Hatim-elaalgi/ResearchWatchElasticsearch"><img src="https://img.shields.io/github/last-commit/Hatim-elaalgi/ResearchWatchElasticsearch?style=flat-square&color=555&labelColor=1A1A1A" alt=""></a>

</td>
<td width="50%" valign="top">

#### 📰 [TecHorizon](https://github.com/Hatim-elaalgi/TecHorizon)

Collaborative online magazine — a four-level role hierarchy and a full editorial review workflow,
built on Laravel 11.

<a href="https://github.com/Hatim-elaalgi/TecHorizon"><img src="https://img.shields.io/github/languages/top/Hatim-elaalgi/TecHorizon?style=flat-square&color=E07B39&labelColor=1A1A1A" alt=""></a>
<a href="https://github.com/Hatim-elaalgi/TecHorizon"><img src="https://img.shields.io/github/last-commit/Hatim-elaalgi/TecHorizon?style=flat-square&color=555&labelColor=1A1A1A" alt=""></a>

</td>
</tr>
</table>

### 💳 Unsupervised fraud detection — VAE · Isolation Forest · LSTM-AE

Three anomaly detectors compared across three datasets at **0.12% fraud prevalence**, with **no
labels at training time**.

- Selection driven by **AUC-PR, not accuracy or ROC-AUC** — at this imbalance ROC-AUC is actively
  misleading. VAE reaches **0.1139 against 0.0497** for Isolation Forest (**+129%**), recall
  **44.2% against 26.9%**
- Threshold calibrated on **business cost** rather than F1 → **24% lower operational cost**
- Per-transaction **SHAP** attribution and a multi-page Streamlit dashboard

### 🔬 Reproducibility audit — Vote Count Model, Parkinson's disease

A faithful reproduction of Mall et al. (2022), then a critical audit. The pipeline is implemented
**twice** — once in scikit-learn, once entirely from scratch in NumPy.

- Individual model accuracies reproduced **exactly**
- **The paper's central claim does not hold** — the voting ensemble beats its best member in only
  **4 of 100 random seeds**
- Found **speaker-level leakage worth 9–17 accuracy points**. Honest subject-wise validation:
  **73–84%**, against the **94.87%** reported

<details>
<summary><b>More public repositories</b></summary>

<br>

| Project | What it is | Stack |
|---|---|---|
| [**Petit Bac multi-agent**](https://github.com/Hatim-elaalgi/jeux_bac) | JADE agents over ACL messages; BFS, DFS, UCS and A\* compared on a trie search problem with an admissible heuristic | Java · JADE |
| [**Deep FFN study**](https://github.com/Hatim-elaalgi/TP2-deeplearning) | Regularisation ablation plus grid and random search — random search won at equal budget | PyTorch |
| [**ETL & dashboard**](https://github.com/Hatim-elaalgi/preProcessingETL_NIFI) | CSV → PostgreSQL star schema, analytical queries, Streamlit dashboard | NiFi · Python · PostgreSQL |
| [**Segmentation from scratch**](https://github.com/Hatim-elaalgi/customer-segmentation-compare) | KNN and multinomial softmax written in NumPy, benchmarked against scikit-learn | NumPy · scikit-learn |

</details>

---

## <img src="https://media.giphy.com/media/LnQjpWaON8nhr21vNW/giphy.gif" width="26"> &nbsp;Professional &amp; private work

<details open>
<summary><b>Not public — happy to walk through any of these</b></summary>

<br>

#### Generative AI &amp; LLM systems

**Chatbot ATLAS** · *Haut-Commissariat au Plan — Morocco's national statistics institute*
Conversational analytics over national statistical databases: a **natural-language → SQL** engine on
PostgreSQL behind a secured Flask REST API, with interactive KPI dashboards and indicator alerting.
The model is given the live schema and a geographic hierarchy, so it writes queries against real
tables rather than guessed ones.
`Python` `Flask` `PostgreSQL` `Google Gemini`

**HCP RAG assistant** · *Retrieval-based counterpart to ATLAS*
Same questions, opposite method — FAISS vector search over uploaded documents, with **statistical
rows rendered into natural-language sentences before embedding** so semantic search works on tabular
data. Feedback loop: user corrections are retrieved as context for later questions.
`FAISS` `Sentence-Transformers` `Flask` `React`

#### Applied ML &amp; security

**SOC Copilot** · *Synertic · Apr 2026 – present*
AI-assisted investigation of compromise incidents on Linux hosts — event correlation, MITRE ATT&CK
mapping, prioritised remediation. A **dual-model trust boundary enforced in code**: the local model
handles raw data, the cloud model only ever receives sanitised context, and the boundary cannot be
bypassed by configuration. **No autonomous execution** — every remediation step passes explicit
human approval, a deny-by-default allowlist, and synchronous audit logging.
`Node.js` `local & cloud LLM agents` `SSH` `OIDC/SSO` `nginx` `OCI`

#### Data, visualisation &amp; enterprise

**Geospatial analytics dashboard** · *Desktop application*
Interactive choropleth of Moroccan regions over a survey dataset, with a chart builder for
conditional distributions across eight categorical dimensions.
`PySide6` `GeoPandas` `Folium` `matplotlib`

**Odoo ERP development** · *Dynamic Horizon · Jul – Nov 2025*
Sales, Stock and Accounting modules in Python and XML, REST API integrations, PostgreSQL migrations.

</details>

---

## <img src="https://media.giphy.com/media/WFZvB7VIXBgiz3oDXE/giphy.gif" width="26"> &nbsp;Tech

<div align="center">

**Languages & data**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

**Data engineering**

![Kafka](https://img.shields.io/badge/Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white)
![NiFi](https://img.shields.io/badge/NiFi-728E9B?style=for-the-badge&logo=apachenifi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![Elasticsearch](https://img.shields.io/badge/Elasticsearch-005571?style=for-the-badge&logo=elasticsearch&logoColor=white)
![Neo4j](https://img.shields.io/badge/Neo4j-4581C3?style=for-the-badge&logo=neo4j&logoColor=white)

**Machine learning**

![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-337AB7?style=for-the-badge)
![Optuna](https://img.shields.io/badge/Optuna-2E5B88?style=for-the-badge)
![SHAP](https://img.shields.io/badge/SHAP-1B9E77?style=for-the-badge)

<sub>Random Forest · MLP · LSTM · Variational Autoencoders · Federated Learning</sub>

**Generative AI & LLM**

![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6B6B?style=for-the-badge)
![Gemini](https://img.shields.io/badge/Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white)

<sub>RAG · Sentence-Transformers · Natural Language → SQL · multi-agent systems · prompt engineering</sub>

**Visualisation & web**

![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)
![PowerBI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=for-the-badge&logo=threedotjs&logoColor=white)
![Qt](https://img.shields.io/badge/PySide6-41CD52?style=for-the-badge&logo=qt&logoColor=white)

<sub>Also: Apache Spark · R · Odoo · Laravel / PHP · UML &amp; Merise · n8n</sub>

</div>

---

---

<div align="center">

### Education

**MSc — Artificial Intelligence & Digital Computing**
FST, Université Moulay Slimane · 2025–2027 *(in progress)*

**BSc — Data Analysis**
FST Tanger, Université Abdelmalek Essaâdi · 2022–2025

<br>

![Arabic](https://img.shields.io/badge/Arabic-native-2E7D32?style=flat-square)
![French](https://img.shields.io/badge/French-fluent%20(professional)-0055A4?style=flat-square)
![English](https://img.shields.io/badge/English-intermediate-B22234?style=flat-square)

</div>

---

<p align="center">
  <b>Open to PFE internship offers — February to June 2027</b><br>
  <a href="mailto:hatimelaalgi@outlook.com">hatimelaalgi@outlook.com</a> ·
  <a href="https://linkedin.com/in/hatim-elaalgi">LinkedIn</a>
</p>

<img width="100%" src="./assets/footer.svg" alt="" />

