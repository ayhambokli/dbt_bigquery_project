````markdown
# 🔷 End-to-End Data Engineering Project: dbt, BigQuery & GitHub

> A complete ELT data engineering project integrating dbt with Google BigQuery to perform data transformations on a dataset containing **1 million+ records**. The entire pipeline is built step by step, including data modeling, transformations, and version control using GitHub.

---

## 🛠 Stack

![BigQuery](https://img.shields.io/badge/BigQuery-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694A?style=for-the-badge&logo=dbt&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-24292E?style=for-the-badge&logo=github&logoColor=white)

---

## 🔁 Data Flow

    🔵 Extract          🔵 Load             🟠 Transform          🟣 Output
    ──────────          ──────────          ──────────────        ──────────
    BigQuery SQL   →    BigQuery       →    dbt + Jinja      →    BigQuery
    1M+ rows            Raw dataset         stage_sales.sql       sales_final
    generated           stored              sales_final.sql       views

---

## 📌 Project Overview

- 🗄️ **Generate Sample Data** — Create a synthetic dataset of **1M+ records** in BigQuery
- ⚙️ **Set Up dbt** — Configure dbt to work with BigQuery for efficient data transformations
- 🧱 **Develop dbt Models** — Implement **staging and transformation models** using SQL & Jinja macros
- 🐙 **Use GitHub for Version Control** — Track changes, collaborate, and manage dbt project files
- ▶️ **Run dbt Pipelines** — Execute transformations and validate results in BigQuery

---

## 📁 Project Structure

    dbt_bigquery_project/
    ├── 📂 models/
    │   ├── 📂 staging/          # Raw data staging models
    │   │   └── 📄 stage_sales.sql
    │   └── 📂 marts/            # Final transformed models
    │       └── 📄 sales_final.sql
    ├── 📂 macros/               # Reusable Jinja macros
    │   └── 📄 dynamic_partition.sql
    ├── 📂 seeds/                # Static CSV data for dbt seeds
    ├── 📂 tests/
    │   └── 📄 sales_test.yml
    ├── 📄 dbt_project.yml       # dbt project configuration
    ├── 📄 profiles.yml          # BigQuery credentials (not included for security reasons)
    ├── 📄 .gitignore            # Specifies files to be excluded from GitHub
    └── 📄 README.md             # Project documentation

---

## 🧰 Technologies Used

| Tool | Purpose |
|------|---------|
| ![dbt](https://img.shields.io/badge/dbt-FF694A?style=flat&logo=dbt&logoColor=white) | SQL-based data transformation |
| ![BigQuery](https://img.shields.io/badge/BigQuery-4285F4?style=flat&logo=google-cloud&logoColor=white) | Cloud data warehouse |
| ![GitHub](https://img.shields.io/badge/GitHub-24292E?style=flat&logo=github&logoColor=white) | Version control for dbt project |
| ![Jinja](https://img.shields.io/badge/Jinja-B41717?style=flat&logo=jinja&logoColor=white) | Dynamic SQL for reusable transformations |
| ![SQL](https://img.shields.io/badge/SQL-336791?style=flat&logo=postgresql&logoColor=white) | Data modeling and transformation |

---

## 🚀 Getting Started

### Prerequisites

- ✅ A **Google Cloud Platform (GCP) account**
- ✅ **BigQuery enabled** on GCP
- ✅ **Python 3.7+** installed
- ✅ **dbt CLI** installed — `pip install dbt-bigquery`
- ✅ **Git** installed and GitHub repository set up

### Clone the Repository

    git clone https://github.com/ayhambokli/dbt_bigquery_project.git
    cd dbt_bigquery_project

### Configure dbt

Update `profiles.yml` with your BigQuery project details, then authenticate with GCP:

    gcloud auth application-default login

### Run dbt Models

    dbt debug        # Check connection with BigQuery
    dbt seed         # Load seed data (if applicable)
    dbt run          # Run all models
    dbt test         # Run tests on models
    dbt docs generate && dbt docs serve   # View lineage graph

---

## 👤 Author

**Ayham** — Data Analyst

[![GitHub](https://img.shields.io/badge/GitHub-ayhambokli-24292E?style=flat&logo=github)](https://github.com/ayhambokli)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/your-profile)
````
