# 📈 **Stock Market Social Network**

### *Network Analysis • Graph ML • Link Prediction • Portfolio Optimization*

This repository contains our **final capstone project** in the **Data
Science & Engineering B.Sc. program at Ben-Gurion University of the
Negev (BGU)**.

The project combines **network science**, **graph machine learning**,
and **quantitative finance** to analyze institutional investment
behavior using **SEC 13F filings**.\
We construct a multi‑layer **bipartite graph of Funds ↔ Stocks**,
analyze its structure over time, predict future investment links, and
build a **data‑driven portfolio strategy** powered by graph-derived
insights.

This repository is designed to serve: - 🎓 Students & researchers
exploring graph-based financial modeling\
- 🧠 Data scientists interested in real-world link prediction\
- 💼 Recruiters evaluating DS/ML engineering and analytical skills\
- 📈 Finance and ML practitioners seeking graph-based investment
insights

We hope this project provides a clear example of how network theory,
machine learning, and real financial data can be integrated into a
unified analytical and predictive pipeline.

------------------------------------------------------------------------

# 📚 **Table of Contents**

1.  [🔍 Project Abstract](#-project-abstract)
2.  [🎯 Core Project Goals](#-core-project-goals)
3.  [🏛 Repository Structure](#-repository-structure)
4.  [⚙️ End-to-End Workflow](#️-end-to-end-workflow)
5.  [🧠 Network Analysis & Graph ML](#-network-analysis--graph-ml)
6.  [📊 Portfolio Construction](#-portfolio-construction)
7.  [👥 Team Git Workflow](#-team-git-workflow)
8.  [🛡 Repository Rules](#-repository-rules)
9.  [🗺 Roadmap](#-roadmap)
10. [🚀 Running Locally](#-running-locally)
11. [🤝 Contributing](#-contributing)
12. [👨‍💻 Team](#-team)

------------------------------------------------------------------------

# 🔍 **Project Abstract**

Institutional investors in the United States must submit quarterly **SEC
13F reports** disclosing equity holdings above \$100M AUM.\
These filings reveal how large, influential market participants allocate
capital --- offering a unique opportunity to model **institutional
behavior as a network**.

In this project, we:

### **1. Build a multi-quarter bipartite graph**

Representing **Funds ↔ Stocks**, based on 13F filings.

### **2. Analyze the graph structure**

Communities, similarity metrics, centrality, ego-networks.

### **3. Train ML models for link prediction**

Predict which fund will invest in which stock next quarter.

### **4. Construct a data-driven investment portfolio**

Using graph signals + financial indicators to outperform naive
baselines.

This project spans ETL engineering, SQL modeling, graph theory, ML,
temporal evaluation, and portfolio optimization --- integrating multiple
disciplines from our academic background.

------------------------------------------------------------------------

# 🎯 **Core Project Goals**

### **1️⃣ Network Construction & Graph Analysis**

-   Build quarterly bipartite graphs\
-   Compute similarity metrics (Jaccard, Adamic--Adar)\
-   Apply community detection (Louvain / Leiden)\
-   Extract temporal and structural insights

### **2️⃣ Machine Learning: Link Prediction**

-   Node2Vec embeddings\
-   Optional GNN-based embeddings\
-   Temporal train/test split\
-   Negative sampling\
-   Predict new fund--stock edges

### **3️⃣ Portfolio Construction**

-   Select stocks with high predicted institutional inflow\
-   Combine graph signals with financial indicators\
-   Evaluate performance vs benchmarks

------------------------------------------------------------------------

# 🏛 **Repository Structure**

    project/
    ├── etl/
    │   ├── src/             # Parsing and normalization of 13F data
    │   ├── tests/           # ETL validation tests
    │   ├── README.md
    ├── network/
    │   ├── src/             # Graph building, metrics, communities
    │   ├── utils/           # Helper functions for network analytics
    │   ├── README.md
    ├── portfolio/
    │   ├── analysis/        # Financial features & insights
    │   ├── optimization/    # Portfolio models
    │   ├── README.md
    ├── models/
    │   ├── feature_store/   # Combined financial + graph feature pipeline
    │   ├── training/        # Link prediction models
    │   ├── inference/       # Running predictions for new quarters
    │   ├── README.md
    ├── notebooks/
    ├── docs/
    ├── data/                # Ignored by git
    └── .gitignore

------------------------------------------------------------------------

# ⚙️ **End-to-End Workflow**

### **1. ETL & Data Modeling**

-   Parse raw 13F XML/CSV\
-   Normalize fund identifiers (CIK)\
-   Load into SQL tables (funds, stocks, holdings, quarters)

### **2. Graph Construction**

-   Build bipartite graphs per quarter\
-   Weight edges using market value or normalized share allocation

### **3. Graph Analytics**

-   Community detection\
-   Similarity metrics\
-   Centrality\
-   Ego networks\
-   Cross-quarter evolution

### **4. Embeddings**

-   Node2Vec baseline\
-   Optional GNN embedding experiment

### **5. ML Training: Link Prediction**

-   Train models using embeddings + metadata\
-   Temporal evaluation\
-   Metrics: ROC-AUC, Precision@TopN, Recall@K

### **6. Portfolio Optimization**

-   Combine graph predictions with financial/risk metrics\
-   Construct an Institutional-Inflow portfolio\
-   Compare vs benchmarks

------------------------------------------------------------------------

# 🧠 **Network Analysis & Graph ML**

Examples of methodologies used:

  Technique                     Purpose
  ----------------------------- ----------------------------------------------
  **Node2Vec**                  Learn dense representations for funds/stocks
  **Adamic--Adar**              Measure similarity between funds
  **Jaccard Coefficient**       Baseline graph similarity
  **Louvain/Leiden**            Community detection
  **Preferential Attachment**   Baseline link prediction
  **GNN (experimental)**        Advanced graph embedding

------------------------------------------------------------------------

# 📊 **Portfolio Construction**

The final portfolio strategy integrates: - Graph-derived signals\
- Similarity-driven predictions\
- Investment clusters\
- Technical indicators\
- Risk modeling

Goal: **generate alpha relative to benchmark strategies using network
insights.**

------------------------------------------------------------------------

# 👥 **Team Git Workflow**

Each developer works **only on their personal branch**:

-   `dev-ilay`\
-   `dev-asaf`\
-   `dev-daniel`\
-   `dev-leor`

Feature branches follow this pattern:

-   `feature/etl-parser`
-   `feature/node2vec`
-   `feature/portfolio-optimizer`

### **PR Requirements**

-   Every change → Pull Request\
-   PR must include a clear description\
-   PR must receive **at least one reviewer approval**\
-   Only then → merge to `main`

------------------------------------------------------------------------

# 🛡 **Repository Rules**

### 🚫 No direct push to `main`

(main is fully protected)

### ✔ Pull Requests are mandatory

### ✔ Reviewer approval required

### ✔ No file deletions or edits without approval

### ✔ No pushing to another developer's branch

### ✔ CODEOWNERS enforce folder responsibility:

    /etl/        @ilay
    /network/     @asaf
    /portfolio/   @daniel
    /models/      @leor

------------------------------------------------------------------------

# 🗺 **Roadmap**

-   ✔ Phase 1 --- ETL\
-   ✔ Phase 2 --- Graph Construction\
-   ✔ Phase 3 --- Graph Analytics\
-   ✔ Phase 4 --- Embeddings\
-   ✔ Phase 5 --- Link Prediction\
-   ✔ Phase 6 --- Portfolio Modeling\
-   [ ] Phase 7 --- Dashboard / Visualization\
-   [ ] Phase 8 --- Final Research Paper

------------------------------------------------------------------------

# 🚀 **Running Locally**

1.  Clone repository\
2.  Create virtual environment\
3.  Install requirements\
4.  Run ETL pipeline\
5.  Build graph data\
6.  Train link prediction model\
7.  Generate portfolio recommendations

(Detailed run instructions will be added as modules finalize.)

------------------------------------------------------------------------

# 🤝 **Contributing**

We welcome: - Issues\
- Suggestions\
- Research ideas\
- Pull Requests\
- Discussion on modeling techniques

------------------------------------------------------------------------

# 👨‍💻 **Team**

-   **Ilay Damari** --- DS, Network Modeling\
-   **Asaf Zenou** --- Financial Modeling\
-   **Daniel Korkevados** --- Portfolio Strategy\
-   **Leor Shulstein** --- Graph ML

------------------------------------------------------------------------

# 🎉 Thank You

This project represents the culmination of our academic training at
Ben‑Gurion University, combining engineering, data science, and real
financial data.\
We hope it serves as a valuable contribution and learning resource for
others.
