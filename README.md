# 🔷 End-to-End Data Engineering Project: dbt, BigQuery & GitHub

> This project demonstrates how to integrate **dbt (Data Build Tool)** with **Google BigQuery** to perform data transformations on a dataset containing **1 million+ records**. The entire pipeline is built step by step, including data modeling, transformations, and version control using GitHub.

---

## 🛠 Stack

![BigQuery](https://img.shields.io/badge/BigQuery-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694A?style=for-the-badge&logo=dbt&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-24292E?style=for-the-badge&logo=github&logoColor=white)

---

## 🔁 Data Flow

![Pipeline](YOUR_IMAGE_URL_HERE)

---

## 📌 Project Overview

| # | Step | Description |
|---|------|-------------|
| 1 | 🔵 **Extract** | Generate **1M+ rows** of synthetic sales data directly in BigQuery using SQL |
| 2 | 🟢 **Load** | Store raw table as-is in a BigQuery dataset — no transformation yet |
| 3 | 🟠 **Staging** | dbt `stage_sales.sql` — clean data & apply `dynamic_partition` Jinja macro |
| 4 | 🟣 **Final model** | dbt `sales_final.sql` — aggregate revenue by product |
| 5 | 🟡 **Output** | Analytics-ready BigQuery views + dbt docs lineage graph |
| 6 | ⚫ **GitHub** | Full project version controlled and pushed to GitHub via SSH |

---

## 📁 Project Structure

    dbt_bigquery_project/
    ├── 📂 models/
    │   ├── 📂 staging/               # Raw data staging models
    │   │   └── 📄 stage_sales.sql
    │   └── 📂 marts/                 # Final transformed models
    │       └── 📄 sales_final.sql
    ├── 📂 macros/                    # Reusable Jinja macros
    │   └── 📄 dynamic_partition.sql
    ├── 📂 seeds/                     # Static CSV data for dbt seeds
    ├── 📂 tests/
    │   └── 📄 sales_test.yml
    ├── 📄 dbt_project.yml            # dbt project configuration
    ├── 📄 profiles.yml               # BigQuery credentials (not included for security)
    ├── 📄 .gitignore
    └── 📄 README.md

---

## 🧰 Technologies Used

| Badge | Tool | Purpose |
|-------|------|---------|
| ![dbt](https://img.shields.io/badge/dbt-FF694A?style=flat&logo=dbt&logoColor=white) | dbt (Data Build Tool) | SQL-based data transformation |
| ![BigQuery](https://img.shields.io/badge/BigQuery-4285F4?style=flat&logo=google-cloud&logoColor=white) | Google BigQuery | Cloud data warehouse |
| ![GitHub](https://img.shields.io/badge/GitHub-24292E?style=flat&logo=github&logoColor=white) | GitHub | Version control |
| ![Jinja](https://img.shields.io/badge/Jinja-B41717?style=flat&logo=jinja&logoColor=white) | Jinja macros | Dynamic SQL for reusable transformations |
| ![SQL](https://img.shields.io/badge/SQL-336791?style=flat&logo=postgresql&logoColor=white) | SQL | Data modeling and transformation |
| ![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white) | Python 3.7+ | Runtime environment for dbt |

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

---

> ⭐ If you found this project useful, feel free to star the repo!
