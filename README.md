# Machine Learning Systems & Agentic AI Portfolio

**Alberto Diaz-Durana**
Senior Data Scientist / ML Engineer | 10+ Years Experience | Production ML & Applied Research

Senior ML practitioner with a decade of international experience building end-to-end machine learning systems, from research prototyping to production deployment. My work focuses on **ML systems design**, **NLP**, **agentic AI**, and **process mining**, with strong emphasis on reproducibility, evaluation, and real-world impact.

This portfolio demonstrates:
- Designing ML systems from scratch
- Translating research ideas into production-ready pipelines
- Working with unstructured text, logs, and sequential data
- Building agentic AI systems that reason, invoke tools, and generate actionable insights

---

## What to Look at First

If you are reviewing this portfolio for **Senior ML Engineer / Research Engineer** roles, start here:

| Project                                                                                                  | Focus                            | Why It Matters                                                       |
| -------------------------------------------------------------------------------------------------------- | -------------------------------- | -------------------------------------------------------------------- |
| [RAG Document Assistant](https://github.com/albertodiazdurana/rag-document-assistant) *(In Development)* | RAG + Multi-Provider LLMs        | Production RAG with vector databases, FastAPI, and MLflow evaluation |
| [DevFlow Analyzer](https://github.com/albertodiazdurana/devflow-analyzer)                                | Agentic AI + Process Mining      | ML applied to code-adjacent artifacts (CI/CD logs, execution traces) |
| [Demand Forecasting](https://github.com/albertodiazdurana/Demand-forecasting-in-retail)                  | End-to-End ML Pipeline           | Full lifecycle ownership at scale (4.8M records)                     |
| [Computer Vision](https://github.com/albertodiazdurana/computer_vision)                                  | Deep Learning + Interpretability | Applied DL with evaluation rigor and explainability                  |
| [NLP Topic Modeling](https://github.com/albertodiazdurana/nlp-topic-modeling)                            | NLP + Sequential Data            | Pre-LLM innovation combining NLP with event-based data               |

These projects best reflect how I approach ML system design, experimentation, and deployment.

---

## Featured Projects

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

### RAG Document Assistant — Production-Ready Retrieval-Augmented Generation *(In Development)*
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

### Demand Forecasting System — Production ML at Scale
**[Repository](https://github.com/albertodiazdurana/Demand-forecasting-in-retail)** | **[Live App](https://demand-forecasting-in-retail-app.streamlit.app/)** | XGBoost, LSTM, MLflow, Streamlit

End-to-end time series forecasting pipeline for inventory optimization.

- **Problem**: Predict daily sales across 2,638 items and 10 stores
- **Scale**: 4.8M transactions; 33 engineered features after ablation studies
- **Hypothesis Tested**: Temporal consistency vs data volume—seasonally aligned training outperformed 7x larger dataset by 54%
- **Results**: RMSE 6.40 (11% improvement); XGBoost won at scale, LSTM won on sample
- **Quality**: 16 MLflow runs, 24 pytest tests, production-hardened codebase

**Why it matters**: Full ML lifecycle ownership from data ingestion to user-facing delivery.

---

### Computer Vision for Manufacturing Quality Control
**[Repository](https://github.com/albertodiazdurana/computer_vision)** | **[Live App](https://steel-defect-segmentation.streamlit.app/)** | TensorFlow, MLflow, Streamlit

Deep learning projects for industrial quality inspection and defect detection.

**Casting Defect Detection** (Anomaly Detection)
- Convolutional autoencoder trained on non-defective samples only; no labeled defect data required
- ROC-AUC: 0.869, 91% defect precision
- Grad-CAM visualizations for model interpretability

**Steel Defect Segmentation** (Semantic Segmentation)
- U-Net (487K parameters) on Severstal Steel dataset (4,000 images)
- Dice: 0.42, IoU: 0.28; handles severely imbalanced data (~3% defect pixels)
- Combined BCE + Dice loss for class imbalance

**CIFAR-10 Classification** (Transfer Learning)
- ResNet50 backbone with custom head; fine-tuning provided 4.7× improvement over frozen features

**Why it matters**: Applied deep learning with evaluation rigor and explainability, not just model training.

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
| **Agentic AI & LLM Integration** | DevFlow Analyzer, multi-provider LLM support                  |
| **NLP & Unstructured Data**      | Topic modeling, text classification, TF-IDF to Transformers   |
| **Sequential & Workflow Data**   | Process mining, CI/CD logs, event traces                      |
| **Production-Grade Engineering** | Streamlit apps, API integration, Windows deployment           |

---

## Technical Skills

**Languages & Core Tools**: Python | SQL | Git | Jupyter

**ML & Data Science**: TensorFlow | XGBoost | scikit-learn | statsmodels | Prophet | SHAP | SMOTE

**NLP & Deep Learning**: LangChain | LangGraph | Sentence Transformers | NLTK | Gensim | U-Net | ResNet | Autoencoders | Transfer Learning

**Data Engineering & MLOps**: Spark | Polars | Dask | MLflow | FastAPI | AWS | Argo Workflows

**Visualization & BI**: Streamlit | Plotly | Power BI | Matplotlib | Seaborn | Dash

**Specialized**: Process Mining (PM4Py) | Time Series Forecasting | LLM Integration | RAG | Energy Systems (German DIN/VDI/GEG standards)

---

## Professional Highlights

- **Alcemy GmbH** (2024-2025): Deployed 5+ ML models optimizing cement production, cutting CO₂ emissions across 35+ customers
- **Appian Software** (2021-2024): Led 10+ process mining assessments, reducing process times ~20% on average
- **TU Berlin** (2019-2021): PhD research in energy access prediction; [CPOTE 2020 publication](https://github.com/albertodiazdurana/Prediction-of-cost-efficient-measures-to-improve-energy-access)
- **HEDERA Sustainable Solutions GmbH** (2018-2021): Co-founded sustainability startup, built cloud-based systems for 15+ international projects

---

## EDUCATION & CERTIFICATIONS

**AI Data Science Program** (LLM, RAG, Agentic AI) – Masterschool | Apr 2025 - May 2026
Specialization in LLM integration, RAG systems, prompt engineering. LangChain, vector databases, embedding techniques.

**MSc Process, Energy & Environmental Systems Engineering** – TU Berlin | 2010-2013
Specialization in thermo-economic modeling, exergy analysis, building energy systems optimization.

**PhD Candidate, Energy Planning & Machine Learning** – TU Berlin | 2019-2021
Research: Energy access prediction using K-Means clustering, PCA, and logistic regression. [CPOTE 2020 publication](https://github.com/albertodiazdurana/Prediction-of-cost-efficient-measures-to-improve-energy-access).

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
