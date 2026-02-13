# Machine Learning Systems & Agentic AI Portfolio

**Alberto Diaz-Durana**
Senior Data Scientist, ML & Data Engineer | Agentic AI, LLM, RAG | NLP, Process Mining | 10+ Years Experience

Freelance Data Scientist & ML Engineer with 10+ years building production ML systems from scratch. End-to-end ML pipelines serving 35+ B2B customers (Alcemy). Expertise in NLP (topic modeling, text analysis, LLM agents), process mining, and MLOps. Currently focused on agentic AI and LLM integration. Proven ability to design ML systems, establish reproducible experiments, and deliver measurable business impact.

This portfolio demonstrates:
- Designing ML systems from scratch
- Translating research ideas into production-ready pipelines
- Working with unstructured text, logs, and sequential data
- Building agentic AI systems that reason, invoke tools, and generate actionable insights

---

## What to Look at First

If you are reviewing this portfolio for **Senior ML Engineer / Research Engineer** roles, start here:

| Project                                                                                                          | Focus                            | Why It Matters                                                       |
| ---------------------------------------------------------------------------------------------------------------- | -------------------------------- | -------------------------------------------------------------------- |
| [SQL Query Agent](https://github.com/albertodiazdurana/sql-query-agent-ollama)                                   | Agentic AI + Local LLMs          | 84-experiment ablation study; Streamlit UI; Docker deployment        |
| [DSM Graph Explorer](https://github.com/albertodiazdurana/dsm-graph-explorer)                                    | Documentation Integrity + Graphs | Epoch 1 complete; 218 tests, 95% coverage; CLI ready                 |
| [DS Methodology](https://github.com/albertodiazdurana/agentic-ai-data-science-methodology)                       | AI-Agent Collaboration Framework | Structured workflows for data science projects with AI agents        |
| [RAG Document Assistant](https://github.com/albertodiazdurana/rag-document-assistant) *(On Ice)*                 | RAG + Multi-Provider LLMs        | Production RAG with vector databases, FastAPI, and MLflow evaluation |
| [DevFlow Analyzer](https://github.com/albertodiazdurana/devflow-analyzer)                                        | Agentic AI + Process Mining      | ML applied to code-adjacent artifacts (CI/CD logs, execution traces) |
| [Disaster Tweet Classification](https://github.com/albertodiazdurana/tfidf-to-transformers-with-disaster-tweets) | NLP Technique Comparison         | TF-IDF → Embeddings → Transformers; F1: 0.77                         |

These projects best reflect how I approach ML system design, experimentation, and deployment.

---

## How These Projects Connect

The top three projects form a single system developed in parallel. The [DS Methodology](https://github.com/albertodiazdurana/agentic-ai-data-science-methodology) (DSM) defines structured workflows for running data science and software engineering projects with AI agents. The [SQL Query Agent](https://github.com/albertodiazdurana/sql-query-agent-ollama) is a case study built using DSM; it follows DSM's sprint planning, decision logging (DEC-001 through DEC-005), hypothesis-driven experiments, and limitation registries, feeding observations back to DSM through dedicated feedback files. The [DSM Graph Explorer](https://github.com/albertodiazdurana/dsm-graph-explorer) is a dog-fooding project; it uses DSM 4.0 to build tooling that validates the methodology's own documentation integrity across ~10,400 lines of cross-referenced markdown. Both projects create a continuous improvement loop: DSM provides structure, the case studies stress-test it, and their feedback refines the next version.

---

## Featured Projects

### SQL Query Agent — Natural Language to SQL with Local LLMs
**[Repository](https://github.com/albertodiazdurana/sql-query-agent-ollama)** | LangChain, LangGraph, Ollama, SQLGlot, Streamlit, Docker

A text-to-code generation testbed; self-correcting agentic system that converts natural language to SQL, running entirely on local open-source models via Ollama.

- **Problem**: Enable non-technical users to query databases using plain English; use SQL's constrained nature to systematically evaluate LLM code generation
- **Approach**: Five-node LangGraph state machine informed by DIN-SQL, MAC-SQL, CHESS research: schema filtering → SQL generation → post-processing → validation (SQLGlot) → execution → error handling (up to 3 retries)
- **Architecture**: Schema-aware generation, SQL post-processing for dialect normalization, pre-execution validation, self-correction loops, model-aware prompting
- **EXP-001 (Model Comparison)**: 14-query test suite (5 Easy, 5 Medium, 4 Hard); sqlcoder:7b vs llama3.1:8b across 6 metrics. Key finding: SQL fine-tuning did not improve accuracy at 7-8B scale (H1 rejected); llama3.1:8b recommended (100% parsability, zero hallucination, 1.7x faster)
- **EXP-002 (Ablation Study)**: 84 experiments (6 prompt configurations × 14 queries). Counter-intuitive findings: few-shot examples *hurt* performance (−14pp); chain-of-thought degraded accuracy; zero-shot with full schema achieved best results (50%)
- **Production**: Streamlit UI with schema explorer, 33 pytest tests, Docker deployment
- **Documentation**: 5 decision records, 6 structured limitations, 4 blog articles (3 published, 1 in progress)

**Why it matters**: Demonstrates agentic AI design with self-correction loops, hypothesis-driven evaluation, counter-intuitive prompt engineering findings, and local-first production deployment.

---

### DSM Graph Explorer — Documentation Integrity Validator
**[Repository](https://github.com/albertodiazdurana/dsm-graph-explorer)** | Python, pytest, Neo4j, NetworkX

Repository integrity validator and graph database explorer for the DSM framework.

- **Problem**: Large documentation repositories with cross-references break silently as they grow
- **Approach**: Markdown parser extracts hierarchical sections; cross-reference extractor identifies Section X.Y.Z, Appendix, and DSM patterns
- **Features**: Code block awareness (skips fenced blocks), line tracking for precise error reporting, severity levels, recursive directory scanning, strict mode for CI/CD
- **Quality**: 218 tests, 95% coverage
- **Epoch 1 Complete**: Parser → Validation engine → CLI implemented; real-world validation: 448 → 6 errors
- **Epoch 2 Planned**: Exclusions/config, CI integration, semantic similarity validation, graph prototype

**Why it matters**: Practical software engineering applied to documentation maintenance; demonstrates testing discipline, dog-fooding, and graph-based analysis.

---

### Agentic AI Data Science Methodology (DSM)
**[Repository](https://github.com/albertodiazdurana/agentic-ai-data-science-methodology)** | Python, Jupyter, Markdown

A living framework for managing data science and ML projects collaboratively with AI agents; continuously refined through real-world case studies.

- **Dual-Track Architecture**: Separate pathways for data science (notebooks) and software engineering (applications)
- **4-Phase Execution**: Exploration → Features → Analysis → Communication
- **DSM 4.0**: Software Engineering Adaptation for ML applications
- **DSM 5.0**: Documentation Project Adaptation for methodology repos, portfolios, knowledge bases
- **Gateway Review Protocol**: Section 6.5 for multi-project governance
- **Scale**: ~10,400 lines of methodology documentation
- **Battle-Tested**: Applied across customer segmentation, demand forecasting, computer vision, NLP, RAG, and industrial ML projects

**Why it matters**: Codifies structured AI-agent collaboration workflows; addresses the gap between ad-hoc LLM usage and reproducible, professional-grade project delivery.

---

### RAG Document Assistant — Production-Ready Retrieval-Augmented Generation *(On Ice)*
**[Repository](https://github.com/albertodiazdurana/rag-document-assistant)** | LangChain, LangGraph, ChromaDB, FastAPI, MLflow, Streamlit

A document Q&A system that reads your files (PDF, Markdown, TXT), understands their content, and answers questions accurately with source citations.

- **Problem**: Organizations have hundreds of documents but no fast way to extract specific answers
- **Approach**: RAG pipeline with hybrid search (semantic + BM25), multi-provider LLM support (OpenAI, Claude, Ollama)
- **Vector Database**: ChromaDB (local) with Pinecone cloud option; configurable embeddings (OpenAI, HuggingFace multilingual-e5)
- **Evaluation**: MLflow experiment tracking with RAG-specific metrics (faithfulness, relevance, latency)
- **Production Features**: FastAPI REST backend, async document processing, streaming responses
- **German Language Support**: Multilingual embeddings and prompt templates for bilingual operation

**Why it matters**: Demonstrates production RAG architecture with evaluation rigor; directly addresses the most in-demand skill (80%+ of Senior AI/ML roles require RAG experience).

---

### DevFlow Analyzer — Agentic AI for CI/CD & Developer Workflows
**[Repository](https://github.com/albertodiazdurana/devflow-analyzer)** | **[Live App](https://devflow-analyzer.streamlit.app/)** | LangChain, LangGraph, PM4Py, MLflow, Streamlit

An agentic ML system that analyzes CI/CD build data through process mining, identifies operational bottlenecks and failure patterns, and generates actionable insights using LLM-powered natural language generation.

- **Problem**: CI/CD pipelines generate massive logs but lack actionable insights for developers
- **Approach**: ReAct-style agent with tool suite (summary stats, bottleneck detection, failure analysis, project comparison); generates DFG visualizations showing build status transitions
- **Scale**: 10,000+ CI/CD builds across 21 open-source Java projects (TravisTorrent dataset)
- **Evaluation**: MLflow experiment tracking, ROUGE scoring, A/B testing framework, cost monitoring
- **Quality**: 86 pytest tests; automated response metrics (tokens/sec, actionability scoring)
- **Cost Efficiency**: GPT-4o-mini primary ($0.15/1M input tokens); GPT-4o for advanced analysis
- **Architecture**: Modular design (process_analyzer, llm_provider, agent, evaluation); 30 commits, 6-day build cycle

**Why it matters**: Demonstrates how agentic AI + structured workflow data can augment developer productivity—an approach closely aligned with **ML for developer tools and code-adjacent intelligence**.

---

### NLP Topic Modeling — Pre-LLM Text-to-Structure Innovation
**[Repository](https://github.com/albertodiazdurana/nlp-topic-modeling)** | NLTK, Gensim, scikit-learn

Unsupervised text analysis converting Jira comments into structured attributes for process mining.

- **Problem**: Extract actionable patterns from unstructured case management data
- **Methods**: LDA topic modeling (coherence-optimized), hierarchical clustering, K-means with silhouette analysis
- **Pipeline**: Tokenization → lemmatization → bigram/trigram detection → stopword removal
- **Output**: Case-level attributes with cluster assignments, dominant topics, top terms

**Why it matters**: Early example (pre-LLM era) of combining NLP with sequential/event-based data—a transferable skill for ML on logs, traces, and code-adjacent artifacts.

---

### Disaster Tweet Classification — From TF-IDF to Transformers
**[Repository](https://github.com/albertodiazdurana/tfidf-to-transformers-with-disaster-tweets)** | Sentence Transformers, GloVe, FastText, scikit-learn

Comparative study of NLP evolution through binary classification of disaster-related tweets.

- **Problem**: Distinguish contextual meaning in tweets (e.g., "fire" as emergency vs. slang)
- **Methods**: Progressive comparison of TF-IDF → Word Embeddings (GloVe, FastText) → Sentence Transformers (SBERT)
- **Results**: Sentence Transformers achieved F1: 0.770; tuned TF-IDF reached 0.764
- **Key Insight**: "Averaging destroys information"; document-level embeddings via mean pooling lose semantic nuance
- **Scale**: 7,613 labeled tweets from Kaggle NLP competition

**Why it matters**: Demonstrates understanding of NLP technique evolution and trade-offs; contextual embeddings outperform statistical methods for ambiguous text.

---

## Additional Projects

### Data Science for Residential Energy Systems
**[Domain Reference](https://github.com/albertodiazdurana/residential-heating-data-science-guide)** | **[Heating Curve Simulator](https://github.com/albertodiazdurana/DataScience_ResidentialEnergySystems)** | **[Live App](https://data-science-residential-energy-systems-heating-curve.streamlit.app/)**

Domain knowledge repository bridging energy engineering with ML for building optimization.
- **Technical Reference**: German heating standards documentation (DIN, VDI, GEG), ML methodologies for energy time series, production MLOps patterns
- **Heating Curve Simulator**: Interactive tool implementing DIN EN 12831, VDI 6030; real weather data from 8 German cities
- Addresses the [60% skills gap](https://www.iea.org/news/energy-employment-has-surged-but-growing-skills-shortages-threaten-future-momentum) in energy sector data analytics

### Demand Forecasting System
**[Repository](https://github.com/albertodiazdurana/CorporacionFavorita-demand-forecasting-in-retail)** | **[Live App](https://demand-forecasting-in-retail-app.streamlit.app/)**

End-to-end time series forecasting: 4.8M transactions, 33 features, RMSE 6.40 (11% improvement). XGBoost, LSTM, MLflow.

### Computer Vision for Manufacturing Quality Control
**[Repository](https://github.com/albertodiazdurana/computer_vision)** | **[Live App](https://computer-vision-steel-defect-segmentation.streamlit.app/)**

Industrial defect detection: U-Net segmentation, autoencoder anomaly detection (ROC-AUC: 0.869), ResNet transfer learning. TensorFlow, MLflow.

### Customer Segmentation & CLV Analysis
**[Repository](https://github.com/albertodiazdurana/TravelTide_Customer_Segmentation)**

Behavioral clustering for personalized rewards: 5,765 users, $23M CLV analyzed, 97.2% confidence.

### Financial Risk Modeling
**[Repository](https://github.com/albertodiazdurana/loan-approval-prediction)**

Credit risk classification with SHAP interpretability: 80% accuracy, SMOTE for imbalance.

### Log Processor ETL Pipeline
**[Repository](https://github.com/albertodiazdurana/log-processor)**

Production ETL converting BPM operational data into event logs: REST API extraction, deduplication, batch processing, PyInstaller deployment.

### Industrial ML — Cement Strength Prediction
**[Repository](https://github.com/albertodiazdurana/cement-strength-prediction-XGBoost)**

XGBoost regression for 28-day compressive strength from XRD/XRF/PSD measurements.

---

## Core Technical Themes

| Theme                            | Evidence                                                      |
| -------------------------------- | ------------------------------------------------------------- |
| **ML Systems from Scratch**      | Design → deployment → monitoring across all featured projects |
| **Reproducible Experimentation** | MLflow tracking, CI/CD, pytest coverage                       |
| **Agentic AI & LLM Integration** | SQL Query Agent, DevFlow Analyzer, RAG, multi-provider LLMs   |
| **NLP & Unstructured Data**      | Topic modeling, text classification, TF-IDF to Transformers   |
| **Sequential & Workflow Data**   | Process mining, CI/CD logs, event traces                      |
| **Production-Grade Engineering** | Streamlit apps, API integration, Windows deployment           |

---

## Technical Skills

**Languages & Core Tools**: Python | SQL | Git | Jupyter | pytest

**Agentic AI & NLP**: LangChain | LangGraph | Ollama | ChromaDB | Sentence Transformers | NLTK | Gensim | RAG

**ML & Data Science**: scikit-learn | XGBoost | TensorFlow | MLflow | SHAP

**Data Engineering & MLOps**: Spark | Polars | FastAPI | AWS | Docker | Argo Workflows | SQLite | PostgreSQL

**Visualization & BI**: Streamlit | Plotly | Power BI | Matplotlib | Seaborn

**Specialized**: Process Mining (PM4Py) | LLM Evaluation | Time Series Forecasting | Energy Systems (German DIN/VDI/GEG standards)

---

## Professional Highlights

- **Freelance Data Scientist & ML Engineer** (2025-present): Freelance data science and ML engineering projects. Contributor to [IronCalc](https://github.com/ironcalc/IronCalc) (3.7K stars, EU-funded Rust spreadsheet engine). Independently developing [DSM](https://github.com/albertodiazdurana/agentic-ai-data-science-methodology), an open-source methodology for AI-agent collaboration, with prototype projects validating the framework across NLP, agentic AI, and energy engineering
- **Alcemy GmbH** (2024-2025): Deployed 5+ ML models optimizing cement production, cutting CO₂ emissions across 35+ customers
- **Appian Software** (2021-2024): Led 10+ process mining assessments, reducing process times ~20% on average
- **TU Berlin** (2019-2021): PhD research in energy access prediction; [CPOTE 2020 publication](https://github.com/albertodiazdurana/Prediction-of-cost-efficient-measures-to-improve-energy-access)
- **HEDERA Sustainable Solutions GmbH** (2018-2021): Co-founded sustainability startup, built cloud-based systems for 15+ international projects

---

## EDUCATION & CERTIFICATIONS

**AI Data Science Program** (LLM, RAG, Agentic AI) – Masterschool | 08.2025 - 02.2026
Specialization in LLM integration, RAG systems, prompt engineering. LangChain, vector databases, embedding techniques.

**MSc Process, Energy & Environmental Systems Engineering** – TU Berlin | 2010-2013
Specialization in thermo-economic modeling, exergy analysis, building energy systems optimization.

**PhD Candidate, Energy Planning & Machine Learning** – TU Berlin | 2019-2021
Research: Energy access prediction using clustering and logistic regression. [CPOTE 2020 publication](https://github.com/albertodiazdurana/Prediction-of-cost-efficient-measures-to-improve-energy-access).

**Diploma Mechanical Engineering** – Universidad de Los Andes, Colombia | 2001-2006

**Certifications:**
- MLOps Specialization (DeepLearning.AI, 2024)
- future Training & Consulting GmbH – Data Science with Python (2018)
- Data Analytics for Six Sigma (University of Amsterdam, 2017)
- PMP – Project Management Professional (PMI, 2016)

---

[View all certifications →](https://github.com/albertodiazdurana/Certificates)

---

## 🌍 Languages

Spanish (Native) | English (C2) | German (C2) | Portuguese (B2)

---

## 📫 Connect

[LinkedIn](https://linkedin.com/in/albertodiazdurana) | [GitHub](https://github.com/albertodiazdurana)

---

**Note**: This portfolio is intentionally systems-oriented rather than notebook-centric. My goal is to demonstrate how I think about ML as an engineering and research discipline, not just model training.

⭐ **Currently open to opportunities** in ML Engineering, Applied Research, and AI Product Development
