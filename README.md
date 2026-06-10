# Machine Learning Systems & Agentic AI Portfolio

**Alberto Diaz-Durana**
Senior Data Scientist | AI Product Architect | Creator of Take AI Bite | 10+ Years Experience

Creator of [Take AI Bite](https://github.com/albertodiazdurana/take-ai-bite), a framework for human-AI collaboration where the human stays in control, grows through the work, and retains every lesson learned. Powered by a living methodology DSM (Deliberate Systematic Methodology) that governs the full lifecycle of AI-assisted projects, from research through implementation to governance.

Data Scientist & AI Product Architect with 10+ years building production ML systems from scratch. End-to-end ML pipelines serving 35+ B2B customers (Alcemy). Expertise in NLP, agentic AI, process mining, and AI system design. Every architectural choice, experiment design, and evaluation in this portfolio is mine. Take AI Bite provided the structure that kept the collaboration disciplined, the decisions human, and the outcomes reproducible.

This portfolio demonstrates:
- Designing ML systems from scratch
- Translating research ideas into production-ready pipelines
- Working with unstructured text, logs, and sequential data
- Building agentic AI systems that reason, invoke tools, and generate actionable insights
- Field-testing human-AI collaboration principles across data science, software engineering, and documentation

---

## What to Look at First

If you are reviewing this portfolio for **Senior ML Engineer / Research Engineer** roles, start here:

| Project                                                                                                          | Focus                            | Why It Matters                                                       |
| ---------------------------------------------------------------------------------------------------------------- | -------------------------------- | -------------------------------------------------------------------- |
| [SQL Query Agent](https://github.com/albertodiazdurana/sql-query-agent-ollama)                                   | Agentic AI + Local LLMs          | 84-experiment ablation study; Streamlit UI; Docker deployment        |
| [DSM Graph Explorer](https://github.com/albertodiazdurana/dsm-graph-explorer)                                    | Documentation Integrity + Graphs | Epoch 4 in progress; 664 tests, 91% coverage; v0.4.0                   |
| [Take AI Bite](https://github.com/albertodiazdurana/take-ai-bite)                                            | Human-AI Collaboration Framework | 13 principles + DSM engine; field-tested across 15+ projects      |
| [RAG Document Assistant](https://github.com/albertodiazdurana/rag-document-assistant)*                 | RAG + Multi-Provider LLMs        | Production RAG with vector databases, FastAPI, and MLflow evaluation |
| [DevFlow Analyzer](https://github.com/albertodiazdurana/devflow-analyzer)                                        | Agentic AI + Process Mining      | ML applied to code-adjacent artifacts (CI/CD logs, execution traces) |
| [Disaster Tweet Classification](https://github.com/albertodiazdurana/tfidf-to-transformers-with-disaster-tweets) | NLP Technique Comparison         | TF-IDF → Embeddings → Transformers; F1: 0.77                         |
| [Flower Classification](https://github.com/albertodiazdurana/efficientnet-flower-classification-transfer-learning) | Few-Shot Transfer Learning       | EfficientNetB0; 91.90% accuracy on 102 classes with ~10 images/class |

These projects best reflect how I approach ML system design, experimentation, and deployment.

---

## How These Projects Connect

The top three projects form a single system built on [Take AI Bite](https://github.com/albertodiazdurana/take-ai-bite) principles. Take AI Bite defines 13 principles for human-AI collaboration; DSM (Deliberate Systematic Methodology) is the engine that operationalizes them into versioned workflows, session management, and cross-project governance. The [SQL Query Agent](https://github.com/albertodiazdurana/sql-query-agent-ollama) is a case study built using DSM; it follows sprint planning, decision logging (DEC-001 through DEC-005), hypothesis-driven experiments, and limitation registries, feeding observations back through dedicated feedback files. The [DSM Graph Explorer](https://github.com/albertodiazdurana/dsm-graph-explorer) is a dog-fooding project; it uses DSM 4.0 to build tooling that validates the methodology's own documentation integrity across ~10,400 lines of cross-referenced markdown. Both projects create a continuous improvement loop: Take AI Bite provides the principles, DSM provides the structure, the case studies stress-test both, and their feedback refines the next version.

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
**[Repository](https://github.com/albertodiazdurana/dsm-graph-explorer)** | Python, pytest, FalkorDB, NetworkX

Repository integrity validator and graph database explorer for the DSM framework.

- **Problem**: Large documentation repositories with cross-references break silently as they grow
- **Approach**: Markdown parser extracts hierarchical sections; cross-reference extractor identifies Section X.Y.Z, Appendix, and DSM patterns
- **Features**: Code block awareness (skips fenced blocks), line tracking for precise error reporting, severity levels, recursive directory scanning, strict mode for CI/CD
- **Quality**: 664 tests, 91% coverage
- **Epoch 1 Complete**: Parser → Validation engine → CLI implemented; real-world validation: 448 → 6 errors
- **Epoch 2 Complete**: Exclusions/config, CI integration, semantic validation, graph prototype, convention linting (5 sprints delivered)
- **Epoch 3 Complete**: FalkorDBLite persistence (GraphStore API, Cypher queries), git-ref temporal compilation with diff analysis, entity inventory for cross-repo resolution, cross-repo bridge graph with drift detection (7/7 MUSTs delivered)
- **Epoch 4 In Progress**: Incremental graph updates (`update_files()`), FalkorDB heading indexes, `to_networkx()` roundtrip export, CLI ref-change detection; heading-based section detection, multi-file resilience, four-layer protocol usage analysis (`--protocol-usage`, `--usage-compare`)

**Why it matters**: Practical software engineering applied to documentation maintenance; demonstrates testing discipline, dog-fooding, and graph-based analysis.

---

### Take AI Bite, Human-AI Collaboration Framework
**[Repository](https://github.com/albertodiazdurana/take-ai-bite)** | **[Website](https://take-ai-bite.com/)** | **[Blog](https://blog.take-ai-bite.com/)** | Python, Jupyter, Markdown

A framework for human-AI collaboration where the human stays in control, grows through the work, and retains every lesson learned. 13 principles address specific failure modes in AI-assisted work, from review sizing to knowledge provenance to process transparency.

- **13 Principles**: Take a Bite, The Human Brings the Spark, Earn Your Assertions, Critical Thinking, Know Your Context, Match the Room, Own Your Process, Know What You Own, Think Ahead, We Need to Talk, Read the User's Manual, Don't be a Hero (Delegate the Effort), Introduce Once Then Deepen
- **The Engine (DSM)**: Deliberate Systematic Methodology operationalizes the principles into versioned workflows, session management, cross-project governance, and a hub-spoke feedback loop
- **Avatar Concept**: The ecosystem accumulates your memory, decisions, and expertise across sessions and projects, becoming an extension of your professional self
- **Dual-Track Architecture**: Separate pathways for data science (notebooks) and software engineering (applications)
- **Scale**: ~10,400 lines of methodology documentation across 15+ projects
- **Field-Tested**: Data science, software engineering, open-source contribution, structured documentation, research synthesis, and administrative processes

**Why it matters**: Addresses the gap between ad-hoc LLM usage and reproducible, professional-grade project delivery. Not theoretical; emerged from daily practice with AI agents across multiple domains.

---

### RAG Document Assistant — Production-Ready Retrieval-Augmented Generation
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
- **Historical Analysis**: ChromaDB vector store with semantic search for build pattern retrieval
- **Quality**: 114 pytest tests; automated response metrics (tokens/sec, actionability scoring)
- **Cost Efficiency**: GPT-4o-mini primary ($0.15/1M input tokens); GPT-4o for advanced analysis
- **Architecture**: Modular design (process_analyzer, llm_provider, agent, evaluation); 30 commits, 6-day build cycle

**Why it matters**: Demonstrates how agentic AI + structured workflow data can augment developer productivity—an approach closely aligned with **ML for developer tools and code-adjacent intelligence**.

---

### Flower Classification — Few-Shot Transfer Learning with EfficientNetB0
**[Repository](https://github.com/albertodiazdurana/efficientnet-flower-classification-transfer-learning)** | TensorFlow, EfficientNetB0, Transfer Learning

Transfer learning for 102-class flower species identification using only ~10 labeled images per class.

- **Problem**: Fine-grained image classification with minimal labeled data (Oxford Flowers 102 dataset)
- **Approach**: 3-phase progressive fine-tuning: head-only → top 30% unfreeze → full fine-tune
- **Results**: Baseline CNN 24.56% → EfficientNetB0 91.01% → with Test-Time Augmentation **91.90%** (3.7x improvement)
- **TTA**: 5 augmented views (original, h-flip, ±90° rotation, center crop), averaged softmax
- **Error Analysis**: Systematic confusion-pair analysis revealing color/shape similarity patterns
- **Scale**: 1,734 training images, 6,149 test images, Colab-ready notebook

**Why it matters**: Deep learning done properly, from baseline comparison through progressive fine-tuning to error analysis, not just API calls.

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

### German Adversarial Prompting — LLM Evaluation via Linguistic Impossibility
**[Repository](https://github.com/albertodiazdurana/german-adversarial-prompting)** | GPT-4o, Prompt Engineering

Adversarial evaluation exploiting the German ß/SS round-trip impossibility to test LLM robustness.

- **Core insight**: German uppercasing is lossy (ß → SS), but lowercasing is ambiguous (SS → ss or ß?). This creates an information-theoretic impossibility that no LLM can resolve without external knowledge
- **Method**: 3-turn adversarial conversation design targeting GPT-4o, with multi-pass validation
- **Evaluation**: 5-agent comparison experiment across different LLM configurations
- **Scope**: 8 DSM sessions, structured methodology trail, public research repository

**Why it matters**: Demonstrates adversarial prompt engineering, multilingual LLM evaluation, and systematic red-teaming methodology.

---

## Additional Projects

### Residential Heating DS Guide
**[Repository](https://github.com/albertodiazdurana/residential-heating-data-science-guide)**

6K-line domain knowledge base bridging German energy standards (DIN, VDI, GEG) with data science.
- German heating standards documentation, ML methodologies for energy time series, production MLOps patterns
- Companion to the Residential Energy Apps repository
- Addresses the [60% skills gap](https://www.iea.org/news/energy-employment-has-surged-but-growing-skills-shortages-threaten-future-momentum) in energy sector data analytics

### Residential Energy Apps
**[Repository](https://github.com/albertodiazdurana/dsm-residential-energy)** | **[Live App](https://data-science-residential-energy-systems-heating-curve.streamlit.app/)**

Heating curve simulation bridging German energy standards with ML.
- Interactive Streamlit app implementing DIN EN 12831, VDI 6030; RANSAC regression, real weather data from 8 German cities

### Demand Forecasting System
**[Repository](https://github.com/albertodiazdurana/CorporacionFavorita-demand-forecasting-in-retail)** | **[Live App](https://demand-forecasting-in-retail-app.streamlit.app/)**

End-to-end time series forecasting: 4.8M transactions, 33 features, RMSE 6.40 (11% improvement). XGBoost, LSTM, MLflow.

### Computer Vision for Manufacturing Quality Control
**[Repository](https://github.com/albertodiazdurana/computer_vision)** | **[Live App](https://computer-vision-steel-defect-segmentation.streamlit.app/)**

Industrial defect detection: U-Net segmentation, autoencoder anomaly detection (ROC-AUC: 0.869), ResNet transfer learning. TensorFlow, MLflow.

### Customer Segmentation & CLV Analysis
**[Repository](https://github.com/albertodiazdurana/TravelTide_Customer_Segmentation)**

Behavioral clustering for personalized rewards: 5,765 users, $23M CLV analyzed, 97.2% confidence.

### AI in Data Science — Automation, Sentiment & Explainability
**[Repository](https://github.com/albertodiazdurana/AI-in-Data-Science)** | PyCaret, Hugging Face Transformers, SHAP, LIME

Three-part evaluation of AI-assisted data science tools, each testing a different claim about automation.
- W2: PyCaret AutoML (R² 0.93 vs 0.80 manual baseline); automated model selection delivered 30x more improvement than automated feature engineering
- W3: Hugging Face RoBERTa zero-shot sentiment on Twitter data; patterns confirmed at 50K scale (113 companies analyzed)
- W4: SHAP + LIME explainability on heart disease classification (RF accuracy 0.837, AUC 0.901); both tools agree on top features

### Financial Risk Modeling
**[Repository](https://github.com/albertodiazdurana/loan-approval-prediction)**

Credit risk classification with SHAP interpretability: 80% accuracy, SMOTE for imbalance.

### DSM Stress Tester — Methodology Validation Through Controlled Experiments
**[Repository](https://github.com/albertodiazdurana/dsm-stress-tester)**

Controlled stress-testing of DSM and Take AI Bite through designed experiments.
- Active experiment: DSM vs Vanilla Claude head-to-head comparison on identical RL challenges (DQN Frozen Lake, 6 stages)
- 5 protocol proposals pushed to DSM Central from findings
- Tests specific conditions: empty project bootstrap, autonomous vs guided collaboration, session boundary handling

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

**Agentic AI & NLP**: LangChain | LangGraph | Ollama | ChromaDB | Hugging Face Transformers | Sentence Transformers | NLTK | Gensim | RAG | AWS Bedrock

**ML & Data Science**: scikit-learn | XGBoost | PyCaret | TensorFlow | MLflow | SHAP | LIME

**Data Engineering & MLOps**: Spark | Polars | FastAPI | AWS (Bedrock, SageMaker) | Docker | Argo Workflows | SQLite | PostgreSQL

**Visualization & BI**: Streamlit | Plotly | Power BI | Matplotlib | Seaborn

**Specialized**: Process Mining (PM4Py) | LLM Evaluation | Time Series Forecasting | Energy Systems (German DIN/VDI/GEG standards)

---

## Professional Highlights

- **Data Scientist & AI Product Architect, Take AI Bite** (2025-present): Creator of [Take AI Bite](https://github.com/albertodiazdurana/take-ai-bite) ([take-ai-bite.com](https://take-ai-bite.com/)), a framework for structured human-AI collaboration with 13 principles and a living methodology engine (DSM) governing a multi-repository ecosystem. Publishing at [take-ai-bite.com](https://take-ai-bite.com/) and [blog.take-ai-bite.com](https://blog.take-ai-bite.com/)
- **Alcemy GmbH** (2024-2025): Deployed 5+ ML models optimizing cement production, cutting CO₂ emissions across 35+ customers
- **Appian Software** (2021-2024): Led 10+ process mining assessments, reducing process times ~20% on average
- **TU Berlin** (2019-2021): PhD research in energy access prediction; [CPOTE 2020 publication](https://github.com/albertodiazdurana/Prediction-of-cost-efficient-measures-to-improve-energy-access)
- **HEDERA Sustainable Solutions GmbH** (2018-2021): Co-founded sustainability startup, built cloud-based systems for 15+ international projects

---

## Open Source Contributions

- **[deepset-ai/haystack](https://github.com/deepset-ai/haystack)** (LLM framework, 25K+ stars): two documentation PRs merged into the Haystack ecosystem, adding Ollama tool-calling and streaming-with-tools examples ([haystack #11268](https://github.com/deepset-ai/haystack/pull/11268), invited and merged by a deepset core member on first review; [haystack-integrations #473](https://github.com/deepset-ai/haystack-integrations/pull/473)).
- **[IronCalc](https://github.com/ironcalc/IronCalc)** (EU-funded Rust spreadsheet engine, 3.7K stars): contributed the `ACCRINTM` financial function (accrued interest at maturity) to the calculation engine, merged by the project founder ([PR #865](https://github.com/ironcalc/IronCalc/pull/865)).

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
- AI Data Science Specialization (Masterschool / MSIT GmbH, 2026) – 1,400 hours, AZAV-certified
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

[LinkedIn](https://linkedin.com/in/albertodiazdurana) | [GitHub](https://github.com/albertodiazdurana) | [Blog](https://blog.take-ai-bite.com/) | [Take AI Bite](https://take-ai-bite.com/)

---

**Note**: This portfolio is intentionally systems-oriented rather than notebook-centric. Every decision, from system architecture to experiment design, is mine; [Take AI Bite](https://github.com/albertodiazdurana/take-ai-bite) is the structure that kept the process disciplined and the results reproducible.

**Currently open to opportunities** in ML Engineering, Applied Research, and AI Product Development
