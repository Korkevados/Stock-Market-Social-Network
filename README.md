# 📈 **Stock Market Social Network**

### *Network Analysis • Graph ML • Link Prediction • Portfolio Construction*

ברוכים הבאים לריפו של פרויקט ה-Data Science שלנו --- שילוב של ניתוח
גרפים, ML פיננסי, 13F SEC Filings ו־Portfolio Optimization.

------------------------------------------------------------------------

# 📚 **תוכן עניינים**

1.  [🔍 תקציר הפרויקט (Abstract)](#-תקציר-הפרויקט-abstract)
2.  [🎯 מטרות הליבה](#-מטרות-הפרויקט-core-goals)
3.  [🏛 מבנה הריפו](#-מבנה-הריפו-repository-structure)
4.  [⚙️ תהליך העבודה End-to-End](#️-תהליך-העבודה-end-to-end)
5.  [🧠 ניתוח גרף ו-ML](#-ניתוח-רשת-graph-ml)
6.  [📊 בניית תיק השקעות חכם](#-בניית-תיק-השקעות-חכם-portfolio-strategy)
7.  [👥 מודל עבודה צוותי ו-Git
    Workflow](#-מודל-עבודה-צוותי--git-workflow)
8.  [🛡 חוקי הריפו -- חובה לקריאה](#-חוקי-הריפו--repository-rules)
9.  [🗺 Roadmap](#-roadmap)
10. [🚀 הרצה מקומית](#-הרצה-מקומית)
11. [🤝 תרומה / Issues / PRים](#-תרומה--issues--prs)
12. [👨‍💻 הצוות](#-הצוות)

------------------------------------------------------------------------

# 🔍 תקציר הפרויקט (Abstract)

Institutional investors file quarterly **13F reports** to the SEC. We
build a bipartite graph **Funds ↔ Stocks**, analyze it over time,
extract insights, predict new investment links, and build a
**network‑driven portfolio strategy**.

------------------------------------------------------------------------

# 🎯 מטרות הפרויקט (Core Goals)

### 1️⃣ Network Construction & Graph Analysis

-   Bipartite graph per quarter\
-   Louvain / Leiden\
-   Similarity metrics (Jaccard, Adamic-Adar)

### 2️⃣ Machine Learning & Link Prediction

-   Node2Vec / GNN\
-   Negative sampling\
-   Predict fund→stock edges

### 3️⃣ Portfolio Construction

-   Combine predictions + indicators\
-   Build an Institutional‑Inflow portfolio\
-   Evaluate vs benchmarks

------------------------------------------------------------------------

# 🏛 מבנה הריפו (Repository Structure)

    project/
    ├── etl/
    │   ├── src/
    │   ├── tests/
    │   ├── README.md
    ├── network/
    │   ├── src/
    │   ├── utils/
    │   ├── README.md
    ├── portfolio/
    │   ├── analysis/
    │   ├── optimization/
    │   ├── README.md
    ├── models/
    │   ├── feature_store/
    │   ├── training/
    │   ├── inference/
    │   ├── README.md
    ├── notebooks/
    ├── docs/
    ├── data/
    └── .gitignore

------------------------------------------------------------------------

# ⚙️ תהליך העבודה End-to-End

### 1. ETL

Parsing 13F, cleaning, SQL loading.

### 2. Graph

Quarterly bipartite graphs, weighted edges.

### 3. Analytics

Communities, similarity scores, ego networks.

### 4. Embedding

Node2Vec / optional GNN.

### 5. Link Prediction

ROC-AUC, Precision@K.

### 6. Portfolio

Graph signals + financial indicators.

------------------------------------------------------------------------

# 👥 Git Workflow

Each developer works ONLY on their branch:\
`dev-ilay`, `dev-asaf`, `dev-daniel`, `dev-leor`

Feature branches allowed.\
All changes enter through Pull Request → Reviewer approval → Merge.

------------------------------------------------------------------------

# 🛡 חוקי הריפו (Repository Rules)

-   ❌ No direct push to `main`\
-   ✔ PR required\
-   ✔ Reviewer required\
-   ✔ No deletion/editing without approval\
-   ✔ CODEOWNERS enforce folder responsibility
