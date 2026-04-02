# MapleCare-Health-Claim-Denial-Root-Cause-Analysis-Claim-Denial-Risk-Prediction
Built an end-to-end healthcare analytics solution to analyze claim denials and predict high-risk claims using ML. Enabled proactive risk prioritization, improved revenue visibility, and delivered realistic, governance-driven insights through Power BI dashboards.


**Role:** Lead Data Consultant & AI Architect  
**Domain:** Healthcare Revenue Cycle Analytics  
**Objective:** Identify denial drivers and predict high-risk claims pre-submission using Machine Learning  

---

## 🔗 View Live Demo

👉 **[View Power BI Dashboard](https://app.powerbi.com/)**  

---

## 🧩 Tech Stack

- **Cloud:** Azure  
- **Data Engineering:** Azure Data Factory  
- **Database:** Azure SQL Server  
- **Machine Learning:** Python, Scikit-Learn  
- **Visualization:** Power BI  

---

## 🎯 Business Impact

- Improved visibility into denial drivers  
- Enabled proactive claim prioritization  
- Reduced reactive rework  
- Established ML-driven risk scoring framework  
- Enhanced operational and financial decision-making  

---

## ⚠️ Problem Statement

Healthcare providers face significant revenue leakage due to insurance claim denials caused by:

- Coding errors  
- Missing documentation  
- Eligibility issues  
- Complex payer rules  

Existing reporting was **reactive**, showing *what happened* but not *why it happened* or *what to do next*.

---

## 🧠 Solution Overview

### Data Engineering

- Built automated ingestion pipelines using **Azure Data Factory (ADF)**  
- Centralized claims data into staging and warehouse layers  
- Ensured data freshness with scheduled pipelines  

---

### Data Modeling

- Designed a **Star Schema**

**Fact Table**
- `fact_claim_line`

**Dimension Tables**
- `dim_date`  
- `dim_patient`  
- `dim_provider`  
- `dim_payer`  
- `dim_facility`  
- `dim_denial_reason`  

---

### Machine Learning

- Model: **Gradient Boosting Machine**  
- Output: `Denial_Risk_Score (0–1)`  

**Key Insight:**  
- Initial model showed *perfect accuracy (leakage issue)*  
- Corrected model achieved **~0.65 ROC-AUC**, ensuring realistic performance  

---

### Visualization

- Built a **6-page Power BI dashboard**:

  - Executive Overview  
  - Payer Analysis  
  - Operational Risk (ML-Assisted)  
  - Facility & Provider Analysis  
  - Procedure & Diagnosis Analysis  
  - Executive Action Plan  

---

## 🔥 End-to-End Architecture

```
Data Sources (EHR / Billing Systems)
        ↓
Azure Data Factory (ETL Pipelines)
        ↓
Azure SQL (Staging + Data Warehouse)
        ↓
Feature Engineering (Python)
        ↓
ML Model (Denial Risk Prediction)
        ↓
Power BI Dashboards
```

---

## 📊 Dashboard Insights

### Executive Overview
- Tracks total charges, denial rates, and value at risk  

### Payer Analysis
- Identifies high-denial payers and contract inefficiencies  

### Operational Risk Prioritization
- Highlights high-risk claims using ML scores  

### Facility & Provider Analysis
- Detects performance variations across entities  

### Procedure & Diagnosis Analysis
- Identifies high-risk CPT and ICD combinations  

---

## 📊 Results & ROI

- Enabled **proactive denial prevention strategy**  
- Identified high-risk claims before submission  
- Improved resource prioritization  
- Delivered realistic ML-based decision support  
- Created a unified analytics + ML framework  

---

## 💡 Key Learnings

- **Data leakage can invalidate ML models**  
- Moderate accuracy is *valuable and realistic*  
- Strong **data modeling is critical** for analytics success  
- ML should be used for **decision support, not automation**  

---

## 📁 Project Structure

```text
project-root/
│
├── data/                # Raw and processed datasets
├── notebooks/           # EDA & modeling
├── pipelines/           # ETL pipelines (ADF)
├── dashboards/          # Power BI files
├── images/              # Dashboard screenshots
└── README.md            # Documentation
```


