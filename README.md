# 📊 Data Science Portfolio

**Alberto Diaz Durana**  
Senior Data Scientist | 10+ Years Experience | Production ML & Business Process Optimization

Senior Data Scientist with a decade of international experience deploying production-ready ML solutions across manufacturing, sustainability, and financial services. Expertise in time series forecasting, process mining, and end-to-end data engineering pipelines. Currently specializing in LLM integration and RAG systems at Masterschool.

## 🎯 Featured Projects

### 📈 Retail & Demand Forecasting
**[Corporación Favorita Demand Forecasting](https://github.com/albertodiazdurana/Demand-forecasting-in-retail)** | **[Live App](https://demand-forecasting-in-retail-app.streamlit.app/)**  
End-to-end time series forecasting pipeline for Ecuadorian grocery inventory optimization.
- **Production Model**: XGBoost achieving RMSE 6.40 (11% improvement over baseline), deployed via Streamlit
- **Scale**: 4.8M transactions, 10 stores, 2,638 items, 32 product families
- **Features**: 33 optimized features (lag, rolling statistics, calendar, aggregations) after ablation studies removed 12 harmful features
- **Key Finding**: Temporal consistency beats data volume—seasonally aligned training (Q4+Q1) outperformed 7x larger dataset by 54%
- **Experiments**: 16 MLflow runs tracking model evolution; LSTM won on sample (300K), XGBoost won at scale (4.8M)
- **Quality**: 24 pytest tests, production-hardened codebase
- **Tech**: XGBoost, TensorFlow/LSTM, MLflow, Streamlit, WSL2 GPU acceleration, pytest

### 👥 Customer Intelligence
**[TravelTide Customer Segmentation](https://github.com/albertodiazdurana/TravelTide_Customer_Segmentation)**  
Behavioral clustering and propensity modeling for personalized rewards program.
- **Outcome**: 5,765 users segmented, $23M CLV analyzed, 5 perks optimally assigned
- **Methods**: Hierarchical clustering (K=3), PCA, propensity scoring
- **Confidence**: 97.2% HIGH/MEDIUM confidence assignments
- **Tech**: scikit-learn, pandas, matplotlib

### 💰 Financial Risk Modeling
**[Loan Approval Prediction](https://github.com/albertodiazdurana/loan-approval-prediction)**  
Binary classification for credit risk assessment with model interpretability.
- **Performance**: 80% test accuracy with Random Forest, 5-fold cross-validation
- **Features**: SMOTE for class imbalance, GridSearchCV (108 combinations), SHAP analysis
- **Deliverables**: 100-question interview Q&A guide
- **Tech**: scikit-learn, SHAP, imbalanced-learn

### 🖼️ Computer Vision & Deep Learning
**[CIFAR-10 Image Classification](https://github.com/albertodiazdurana/computer_vision)**
Transfer learning study using ResNet50 for image classification on CIFAR-10 dataset.
- **Architecture**: ResNet50 backbone with custom classification head, two-phase training strategy
- **Performance**: 48.9% test accuracy; fine-tuning provided 4.7× improvement over frozen features
- **Key Insight**: Input size compatibility critical—ResNet50's 224×224 requirement limits 32×32 image classification ceiling
- **Data Augmentation**: Random flips, rotations, zoom for robust feature learning
- **Analysis**: Confusion matrix reveals visual similarity drives misclassifications (ship/airplane, deer/horse pairs)
- **Tech**: TensorFlow 2.20, ResNet50, scikit-learn, Jupyter, GPU acceleration (NVIDIA Quadro)

### 🏭 Industrial ML & Manufacturing
**[Cement Strength Prediction](https://github.com/albertodiazdurana/cement-strength-prediction-XGBoost)**
Regression model predicting 28-day compressive strength from analytical measurements.
- **Application**: Real-world manufacturing scenario with dynamic raw materials
- **Methods**: XGBoost with time series cross-validation
- **Features**: XRD, XRF, PSD data; temporal feature extraction
- **Tech**: XGBoost, Python 3.12, scikit-learn

### ⚙️ Business Process Optimization
**[Process Mining & Sentiment Analysis](https://github.com/albertodiazdurana/process-mining-and-sentiment_analysis)**  
End-to-end process mining with NLP sentiment analysis.
- **Analysis**: Directly-Follows Graph (DFG) with frequency and time metrics
- **NLP**: Twitter scraping (Twint), EDA, sentiment analysis
- **Tech**: PM4Py, Python, NLP libraries

## ⚡ Domain Expertise: Energy Systems Engineering

### Thermo-Economic & Exergo-Economic Analysis
Specialized expertise in optimization and simulation of energy systems through advanced thermodynamic and economic modeling.

**Technical Approach:**
- **Exergy Analysis**: Quantifying energy quality and system irreversibilities using second-law thermodynamics
- **Cost Allocation**: Applying exergoeconomic principles to optimize equipment selection and operational parameters
- **System Optimization**: Multi-objective optimization integrating thermodynamic performance with economic feasibility
- **Applications**: Cogeneration systems, renewable energy integration, energy storage systems, building energy systems

**Notable Projects:**
- **GETEC Wärme & Effizienz AG**: Data analysis and budgetary forecasting for 225 real estate energy projects (€71.5M investment portfolio). Calculation, cost estimation, and design of energy generation systems.
- **PhD Research (TU Berlin)**: Energy access prediction in low-income regions using semi-supervised ML and neural networks. Application of comparative analysis and classification for household-level energy planning.
- **Publication**: "Prediction of cost-efficient measures to improve energy access for populations living in energy poverty using modern methods of information technology"

**Methodologies:**
- Mass, energy, and exergy balance modeling under steady-state conditions
- Thermoeconomic optimization for minimizing unit cost of produced exergy
- Integration of process simulators with optimization frameworks
- Variable load condition analysis and off-design operation evaluation

## 🛠️ Technical Skills

**Languages & Core Tools**  
Python | SQL | Git | Jupyter

**ML & Data Science**  
TensorFlow | XGBoost | scikit-learn | statsmodels | Prophet | SHAP | SMOTE

**Data Engineering & MLOps**  
Spark | Polars | Dask | MLflow | FastAPI | AWS | Argo Workflows | Sentry

**Visualization & BI**  
Streamlit | Power BI | Matplotlib | Seaborn | Dash

**Specialized**  
Energy Systems Modeling | Process Mining (PM4Py) | NLP | Time Series Forecasting | LLM Integration | RAG

## 💼 Professional Highlights

- **Alcemy GmbH** (2024-2025): Deployed 5+ ML models optimizing cement production, cutting CO₂ emissions across 35+ customers
- **Appian Software** (2021-2024): Led 10+ process mining assessments, reducing process times ~20% on average
- **HEDERA Solutions** (2018-2021): Co-founded sustainability startup, built cloud-based systems for 15+ international projects
- **TU Berlin** (2019-2021): PhD research in energy access prediction, applied semi-supervised ML to low-income region classification
- **GETEC Wärme & Effizienz** (2014-2015): Energy systems engineering for €71.5M portfolio of 225 projects

## 📜 Certifications

- MLOps Specialization (DeepLearning.AI, 2024)
- Project Management Professional - PMP (PMI, 2016)
- Data Analytics for Six Sigma (University of Amsterdam, 2017)

[View all certifications →](https://github.com/albertodiazdurana/Certificates)

## 🎓 Education

- **Masterschool** - AI Data Science (2025-2026): LLM integration, RAG, prompt engineering
- **TU Berlin** - MSc Process, Energy & Environmental Systems Engineering (2013): Specialization in thermo-economic modeling and sustainable energy systems
- **TU Berlin** - PhD Candidate in Energy Planning & Machine Learning (2019-2021): Energy access prediction, semi-supervised ML for sustainability applications
- **Universidad de Los Andes** - Mechanical Engineering (2006)

## 🌍 Languages

Spanish (Native) | English (C2) | German (C2) | Portuguese (B2)

## 📫 Connect

[LinkedIn](https://linkedin.com/in/albertodiazdurana) | [GitHub](https://github.com/albertodiazdurana)

---

⭐ **Currently open to new opportunities** in data science, ML engineering, and AI product development
