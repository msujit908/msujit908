# Hi, I'm Sujit Kumar Munda 👋

### M.Tech. Robotics & Artificial Intelligence @ IIT Guwahati
### Software Engineer • AI/ML Engineer • Data Scientist • Robotics

<p align="center">
  <a href="https://github.com/msujit908">
    <img src="https://komarev.com/ghpvc/?username=msujit908&label=Profile%20Views&color=0e75b6&style=flat" alt="Profile Views"/>
  </a>
  <a href="https://github.com/msujit908?tab=followers">
    <img src="https://img.shields.io/github/followers/msujit908?label=Followers&style=flat" alt="GitHub Followers"/>
  </a>
  <a href="https://github.com/msujit908?tab=repositories">
    <img src="https://img.shields.io/github/stars/msujit908?label=Stars&style=flat" alt="GitHub Stars"/>
  </a>
</p>

---

## 👨‍💻 About Me

I am a **Computer Science Engineer** currently pursuing an **M.Tech. in Robotics and Artificial Intelligence at IIT Guwahati**.

My work focuses on building systems at the intersection of:

$$\textbf{Software Engineering} \times \textbf{Artificial Intelligence} \times \textbf{Machine Learning} \times \textbf{Data Science} \times \textbf{Robotics}$$

I enjoy building complete systems rather than isolated prototypes — from **data ingestion and validation** to **ML modeling, backend APIs, real-time communication, explainability and deployment**.

- 🎓 **M.Tech. Robotics & Artificial Intelligence** — Indian Institute of Technology, Guwahati (2025–Present)
- 💻 **B.Tech. Computer Science & Engineering** — 8.75 CGPA (2019–2022)
- 🤖 **Robotics & Intelligent Systems**: Physics-informed telemetry simulation, multi-sensor kinematics
- 🧠 **AI/ML & Explainable AI**: Anomaly detection, failure horizon forecasting, SHAP TreeExplainer
- 📊 **Data Science & Quantitative Analytics**: Financial time-series, macroeconomic transmission, factor models
- ⚙️ **Backend & Real-Time Systems**: Spring Boot, FastAPI, STOMP WebSockets, Redis, PostgreSQL
- 📈 **Time-Series & Quantitative Modeling**: Walk-forward validation, zero look-ahead bias pipelines
- 🔬 **Production AI/ML Engineering**: End-to-end containerized architectures with Docker Compose

---

# 🚀 Featured Projects

## 🤖 01 — Robot Health Intelligence & Predictive Maintenance
### AI/ML • Robotics • Predictive Maintenance • Explainable AI

An end-to-end platform for **robot health monitoring, anomaly detection, failure prediction and prescriptive maintenance**.

### 🌟 What I Built
- **6-DOF Physics-Informed Telemetry Simulator**: Models multi-joint robotic arms with dynamic fault injection (bearing wear, overheating, motor stall).
- **Industrial Predictive Maintenance Pipeline**: Benchmark pipeline on 10,000 AI4I 2020 telemetry records.
- **117 Temporal & Physics-Based Features**: Rolling-window statistics ($W \in [5, 10, 30, 60]$), multi-scale lags, mechanical/electrical power differentials, and thermal accumulation trend slopes.
- **Time-Aware Validation**: Chronological train/val/test split (70%/15%/15%) with 4-fold walk-forward cross-validation ensuring zero data leakage.
- **Composite Anomaly Detection**: Statistical $3\text{-}\sigma$ Z-score detectors combined with tuned Isolation Forest.
- **Class-Weighted XGBoost Model**: Predicts failure probability within the next 30 operational cycles.
- **Explainable AI (SHAP TreeExplainer)**: Local waterfall attribution separating mathematical model output from engineering interpretations.
- **Deterministic 0–100 Robot Health Index**: Transparent scoring framework with configurable risk tiers (Healthy, Warning, High Risk, Critical).
- **High-Throughput Backend & Real-Time Hub**: Async FastAPI REST API and `/ws/telemetry` WebSocket broadcast server with PostgreSQL and Redis caching.
- **Next.js 15+ Monitoring Dashboard**: Live multi-sensor Recharts telemetry graphs, circular health gauges, and interactive fault injection controls.

### 📊 Model Evaluation
| Model Architecture | PR-AUC (Primary) | ROC-AUC | F1-Score | Precision | Recall | Brier Score |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| Logistic Regression (Baseline) | 0.3316 | 0.7456 | 0.3360 | 0.2325 | 0.6057 | 0.1872 |
| Random Forest (Balanced) | 0.6623 | 0.9469 | 0.5825 | 0.6716 | 0.5143 | 0.0603 |
| **XGBoost (Class-Weighted)** | **0.6989** | **0.9511** | **0.7017** | **0.6025** | **0.8400** | **0.0649** |

### 🧪 Validation & Audit
```text
Dataset                : 10,000 industrial records
Engineered Features    : 117
Test Records           : 1,500 unseen future records
Test Failures          : 175
Validation             : 4-Fold Walk-Forward Cross-Validation
Primary Metric         : PR-AUC
Best Model             : Class-Weighted XGBoost
PR-AUC                 : 0.6989
ROC-AUC                : 0.9511
F1-Score               : 0.7017
Recall                 : 84.00%
Automated Test Suite   : 36/36 PASS (Pytest)
Leakage Audit          : ZERO Look-Ahead Bias (PASS)
```

---

## 📈 02 — AI Stock Intelligence & Market Analysis Platform
### Data Science • Financial ML • Quantitative Analytics • NLP

An intelligent full-stack research platform for analyzing Indian equities (NSE & BSE) using fundamental, technical, quantitative, and global macroeconomic signals.

### 🌟 What I Built
- **Universal Indian Equity Discovery**: Multi-identifier search resolving NSE Symbols, BSE Scrip Codes, Company Names, and ISINs with live market feed fallback.
- **100-Point Deterministic Intelligence Scoring Engine**: Transparent, evidence-based score matched across screeners, sector tables, and company profiles.
- **Macroeconomic Geopolitical Transmission Engine**: Models foreign shocks (US Fed yields, Brent crude, China stimulus, Red Sea shipping disruption) to Indian sector margins.
- **Dual-Mode Factor & Index Screener**: Screener across holding horizons (Strategic Compounders, Growth Catalysts, Tactical Momentum, Risk Caution) and benchmark indices (NIFTY 50, BANK, IT, AUTO, SENSEX 30).
- **Plain-English AI Analyst**: 1-Minute Executive Verdicts with strategy badges, automated SWOT cards, and 1-click research report exports.
- **FastAPI & Next.js Full Stack**: Python FastAPI backend with PostgreSQL, Redis caching, APScheduler cron workers, and Next.js 15 UI with Recharts.

### 🏛️ 9-Pillar Scoring Framework
```text
Financial Quality (ROCE & ROE vs 15% hurdle rate)        20%
Growth Engine (3Y/5Y CAGR Revenue & Operating Profit)    15%
Operating Profitability (EBITDA & Net Margin Trajectory)  15%
Balance Sheet Strength (Debt-to-Equity & Interest Cover) 15%
Cash Flow Health (Free Cash Flow & CFO/Net Profit)       10%
Relative Valuation (Trailing/Forward P/E, P/B, EV/EBITDA) 10%
Technical Momentum (RSI 14, MACD, SMA 20/50/200)         5%
News & Macro Sentiment (Entity Tone & Shock Impact)       5%
Risk Headroom (30-day Rolling Volatility & Beta)          5%
------------------------------------------------------------
Total Unified Score                                     100%
```

### 🔄 Quantitative Pipeline
```text
Market Data  ──>  Financial Statements  ──>  News & Macro Transmission
      │
      ▼
Data Validation & Normalization
      │
      ▼
Time-Series & Factor Feature Engineering
      │
      ▼
Fundamental & Technical Quantitative Analysis
      │
      ▼
Peer & Sector Relative Valuation Comparison
      │
      ▼
Walk-Forward Factor Ranking Engine
      │
      ▼
100-Point Score & Plain-English Explainability Hub
      │
      ▼
FastAPI REST Endpoints  ──>  Next.js 15 Interactive Terminal
```

---

## 🚚 03 — Real-Time Logistics & Delivery Platform (LogiFlow)
### Software Engineering • Backend • Real-Time Systems • Full Stack

A production-oriented real-time logistics and dispatch management platform engineered with **Java 21, Spring Boot 3.3, PostgreSQL 16, Redis 7, STOMP WebSockets, and Next.js 14**.

### 🌟 What I Built
- **Strict 6-Stage Delivery State Machine**: Enforces formal lifecycle progression (`CREATED` $\to$ `ASSIGNED` $\to$ `PICKED_UP` $\to$ `IN_TRANSIT` $\to$ `OUT_FOR_DELIVERY` $\to$ `DELIVERED`); rejects invalid transitions with `HTTP 409 Conflict`.
- **Low-Latency Telemetry Hub**: STOMP message broker (`/ws/tracking`) broadcasting live driver coordinates, speed, heading, and ETAs in **<10ms**.
- **Redis Fault Tolerance & Caching**: Active driver location caching with automated failover to PostgreSQL.
- **Mathematical ETA Engine**: Spherical Haversine distance computations combined with empirical urban traffic penalty multipliers.
- **Automated Background Schedulers**: Spring `@Scheduled` background workers continuously detecting delayed shipments and broadcasting alerts.
- **Role-Based Access Control (RBAC)**: Fine-grained security separating `ADMIN`, `DISPATCHER`, `DRIVER`, and `ANALYST` capabilities using stateless HMAC-SHA256 JWTs.
- **Interactive Dispatch Radar & GPS Simulator**: Built-in visual fleet radar and simulated GPS controller.

### 🏗️ Architecture
```text
                    Frontend Console
               (Next.js 14 / TypeScript)
                           │
                           ▼
                 Spring Boot 3.3 API
                           │
          ┌────────────────┼────────────────┐
          ▼                ▼                ▼
    PostgreSQL 16       Redis 7       STOMP WebSocket
  (Relational Data)  (Live Cache)    (<10ms Telemetry)
          │                │                │
          └────────────────┼────────────────┘
                           ▼
                   Business Services
              (State Machine & Scheduler)
                           │
                           ▼
                Delivery & Fleet Engine
```

---

## 🧠 Technical Skills

### 💻 Programming Languages
<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java"/>
  <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++"/>
  <img src="https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=black" alt="C"/>
  <img src="https://img.shields.io/badge/SQL-336791?style=for-the-badge&logo=postgresql&logoColor=white" alt="SQL"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript"/>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript"/>
</p>

| Domain | Technologies, Frameworks & Concepts |
| :--- | :--- |
| **AI / Machine Learning** | Supervised/Unsupervised Learning, Time-Series Modeling, Anomaly Detection, Predictive Maintenance, Feature Engineering, Explainable AI (SHAP), NLP, Financial Machine Learning, Quantitative Factor Modeling, Model Evaluation, 4-Fold Walk-Forward CV, XGBoost, Random Forest, Scikit-learn |
| **Data Science & Analytics** | Exploratory Data Analysis (EDA), Statistical Modeling, Time-Series Analysis, Quantitative Scoring, Hypothesis Testing, Pandas, NumPy, SciPy, Matplotlib, Seaborn, Recharts, Data Wrangling, Financial Metrics |
| **Backend & Systems** | Java 21, Spring Boot 3.3, Python, FastAPI, Spring Security, Hibernate/JPA, RESTful APIs, WebSockets, STOMP Protocol, JWT (HMAC-SHA256), PostgreSQL 16, MySQL, Redis 7, SQLAlchemy ORM, Flyway Migrations |
| **Frontend & UI** | Next.js 14/15 (App Router), React 19, TypeScript, Tailwind CSS, Recharts, Lucide React, Axios, HTML5, CSS3 |
| **DevOps & Engineering Tools** | Docker, Docker Compose, Git, GitHub Actions, CI/CD Pipelines, MLflow, Jupyter Notebook, Linux/Unix, VS Code, Postman, Pytest, JUnit 5, Mockito |

---

## 🔬 Machine Learning Workflow

```text
┌───────────────┐      ┌───────────────┐      ┌───────────────┐      ┌───────────────┐
│ Data Sources  │ ───> │ Data Quality  │ ───> │ Normalization │ ───> │ Feature Engg. │
│ (Raw Sensors) │      │  Validation   │      │   & Scaling   │      │ (Lags/Trends) │
└───────────────┘      └───────────────┘      └───────────────┘      └───────┬───────┘
                                                                             │
┌───────────────┐      ┌───────────────┐      ┌───────────────┐              │
│ Model Training│ <─── │ Time-Aware CV │ <────┴───────────────┘              │
│ (XGB/RF/IF)   │      │ (Walk-Forward)│                                     │
└───────┬───────┘      └───────────────┘                                     │
        │                                                                    │
        ▼                                                                    ▼
┌───────────────┐      ┌───────────────┐      ┌───────────────┐      ┌───────────────┐
│  Evaluation   │ ───> │Explainability │ ───> │ API / Server  │ ───> │  Interactive  │
│(PR/ROC/Brier) │      │(SHAP Waterfall│      │(FastAPI Hub)  │      │   Dashboard   │
└───────────────┘      └───────────────┘      └───────────────┘      └───────────────┘
```

---

## 🎓 Education

- **Indian Institute of Technology, Guwahati**  
  *M.Tech. — Robotics and Artificial Intelligence* (2025 – Present) | **CGPA: 7.14 (Current)**
- **DAV Institute of Engineering and Technology, Palamu**  
  *B.Tech. — Computer Science and Engineering* (2019 – 2022) | **CGPA: 8.75**
- **Government Polytechnic, Latehar**  
  *Diploma — Computer Science and Engineering* (2013 – 2016) | **Percentage: 68.58%**
- **JAC Board**  
  *Secondary Education* (2013) | **Percentage: 64.6%**

---

## 💼 Professional Experience

- **Technical Trainer — Hi-tech Academy** *(Jan 2024 – Jun 2025 | Ranchi, Jharkhand)*
  - Delivered structured technical training in Python, C, HTML, CSS, and Data Structures to 200+ students.
  - Mentored students through coding drills, debugging workshops, and full-stack mini-project development.
  - Formulated practical programming challenge sets and hands-on laboratory rubrics.

- **Technical Trainer — Brainware Technology** *(Jul 2022 – Dec 2024 | Ranchi, Jharkhand)*
  - Conducted intensive training modules covering Core Java (OOP), Python, DBMS, SQL, C, and Data Structures.
  - Guided candidates in building end-to-end database-driven applications with JDBC, MySQL, and modular backends.

- **Technical Trainer — Hi-tech Academy** *(Aug 2018 – Jun 2019 | Ranchi, Jharkhand)*
  - Taught Object-Oriented Programming using C++ and Core Java to diploma and undergraduate engineers.
  - Assisted students with algorithm optimization, software development best practices, and project implementations.

---

## 🏆 Project Highlights Matrix

| Domain Focus | Featured Project | Core Demonstrated Capabilities |
| :--- | :--- | :--- |
| 🤖 **AI/ML & Robotics** | **Robot Health Intelligence** | Physics Simulator, XGBoost (0.9511 ROC-AUC), Isolation Forest, SHAP XAI, Walk-Forward CV |
| 📊 **Data Science** | **AI Stock Intelligence** | 100-Point 9-Pillar Quantitative Model, Macro Transmission, Factor Screeners, Financial EDA |
| 💻 **SDE / Backend** | **LogiFlow Real-Time Platform** | Java 21, Spring Boot 3.3, STOMP WebSockets (<10ms), PostgreSQL 16, Redis 7, JWT RBAC |

---

## 📈 GitHub Activity & Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=msujit908&show_icons=true&hide_border=true&include_all_commits=true" height="170" alt="GitHub Stats"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=msujit908&layout=compact&hide_border=true" height="170" alt="Top Languages"/>
</p>
<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=msujit908&hide_border=true" alt="GitHub Streak"/>
</p>

---

## 📌 Engineering Philosophy

```text
  Clean Architecture  +  Empirical Validation  +  Robust Testing  +  Explainability  +  Containerized CI/CD
```

The goal is to build systems that demonstrate not only model training or API routing in isolation, but the complete capability to **engineer, validate, explain, test, containerize, and deploy production-grade software and AI systems**.

---

## 📫 Connect With Me

<p>
  <a href="mailto:sujit.munda@iitg.ac.in">
    <img src="https://img.shields.io/badge/IITG_Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="IITG Email"/>
  </a>
  <a href="mailto:msujit908@gmail.com">
    <img src="https://img.shields.io/badge/Personal_Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Personal Email"/>
  </a>
  <a href="https://www.linkedin.com/in/sujit-munda-a62724182/">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  <a href="https://github.com/msujit908">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/>
  </a>
</p>

---

<p align="center">
  <b>Building intelligent systems that connect: 🤖 Robotics × 🧠 AI × 📊 Data × 💻 Software</b><br>
  <i>⭐ Thanks for visiting my profile!</i>
</p>
