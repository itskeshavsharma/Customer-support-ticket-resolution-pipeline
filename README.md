# 🚀 Customer Support Ticket Resolution Pipeline

An end-to-end Azure Data Engineering project that processes customer support ticket data stored in **Azure Data Lake Storage Gen2 (ADLS Gen2)** using **Azure Databricks (PySpark)**. The pipeline cleans, transforms, validates, and aggregates the data into Gold-layer datasets, which are then visualized in **Power BI** for business insights.

---

## 📌 Project Overview

Customer support ticket data for two consecutive days was stored as CSV files in Azure Data Lake Storage Gen2. The raw data contained invalid records, unresolved tickets, duplicate entries, and resolution times stored as text.

This project builds a complete data pipeline that:

- Ingests raw CSV files from ADLS Gen2
- Cleans and validates the data
- Converts resolution time into numerical minutes
- Applies business rules
- Generates Gold analytical datasets
- Creates an interactive Power BI dashboard for leadership reporting

---

## 🛠️ Tech Stack

- **Azure Data Lake Storage Gen2**
- **Azure Databricks**
- **PySpark**
- **Delta Lake**
- **Power BI**
- **Python**
- **Git & GitHub**

---

## 📂 Project Structure

```
customer-support-ticket-resolution-pipeline/
│
├── data/
│   ├── raw/
│   └── gold/
│
├── notebooks/
│   └── customer_support_pipeline.ipynb
│
├── powerbi/
│   └── Customer_Support_Dashboard.pbix
│
├── screenshots/
│
├── README.md
└── requirements.txt
```

---

## 🔄 Pipeline Workflow

```
Raw CSV Files
        │
        ▼
Azure Data Lake Storage Gen2
        │
        ▼
Azure Databricks (PySpark)
        │
        ▼
Data Cleaning & Validation
        │
        ▼
Business Rule Processing
        │
        ▼
Gold Layer (Delta/Parquet)
        │
        ▼
Power BI Dashboard
```

---

## 📋 Business Rules Implemented

- Only **Resolved** tickets are considered.
- Resolution time must be **greater than 15 minutes**.
- Resolution time is converted from text (`1h 10m 30s`) into total minutes.
- If seconds are **30 or more**, the value is rounded up.
- Only Team Leads **TL01–TL08** are included.
- Agents who successfully resolved tickets on **Day 1** are excluded from **Day 2** (Carry-over Rule).

---

## 📊 Business Questions Solved

### ✅ Q1 – Team Performance

- Total resolved tickets by Team Lead
- Active agents
- Average tickets per agent

### ✅ Q2 – Agent Performance

- Day 1 vs Day 2 resolved tickets
- Total resolved tickets
- Performance trend

### ✅ Q3 – Compliance Analysis

- Resolution quality compliance percentage
- Qualifying tickets (>15 minutes)
- Team-wise compliance analysis

### ✅ Q4 – Carry-over Analysis

- Agents carried over from Day 1
- Day 2 qualifying tickets
- Average, minimum and maximum resolution time

---

## 📈 Power BI Dashboard

The dashboard includes:

- 📌 Total Resolved Tickets
- 📌 Average Compliance %
- 📌 Carry-over Agents
- 📌 Active Agents
- 📌 Team-wise Ticket Resolution
- 📌 Team-wise Compliance Rate
- 📌 Agent-wise Day 1 vs Day 2 Performance
- 📌 Carry-over Agent Details
- 📌 Team Lead Filter

---

## 📸 Screenshots

### Azure Data Lake Storage
> Add screenshot here

### Azure Databricks Pipeline
> Add screenshot here

### Gold Layer Output
> Add screenshot here

### Power BI Dashboard
> Add dashboard screenshot here

---

## ▶️ How to Run

1. Upload the raw CSV files to **Azure Data Lake Storage Gen2**.
2. Import and run the Databricks notebook.
3. The notebook performs data cleaning, transformation, and aggregation.
4. Gold datasets are generated in Delta/Parquet format.
5. Load the Gold datasets into Power BI.
6. Refresh the dashboard to explore the insights.

---

## 🎯 Project Outcome

This pipeline transforms raw customer support data into clean, business-ready datasets that help leadership analyze:

- Team performance
- Agent productivity
- Resolution quality compliance
- Carry-over workload
- Overall customer support efficiency

---

## 📚 Key Learnings

- Azure Data Lake Storage Gen2
- Azure Databricks
- PySpark Data Processing
- Delta Lake
- Data Cleaning & Validation
- Business Rule Implementation
- Power BI Dashboard Development
- End-to-End Azure Data Engineering Pipeline

---

## 👨‍💻 Author

**Keshav Sharma**

B.Tech CSE | Azure Data Engineering Enthusiast

GitHub: https://github.com/ikeshavsharma
