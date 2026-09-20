# 📉 Customer Churn & Retention Analytics Dashboard

<div align="center">

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

*An end-to-end Business Intelligence solution for evaluating customer retention dynamics, identifying churn drivers, and quantifying revenue attrition risk.*

</div>

---

## 📌 Project Overview

Customer churn is one of the most critical challenges in any subscription or service-based business. This dashboard provides a **360° view of customer retention performance**, enabling business leaders to:

- Understand **who is churning** and **why**
- Identify **at-risk customer segments** before churn occurs
- Measure the **revenue impact** of customer attrition
- Drive **data-backed retention strategies**

---

## 🎯 Business Objectives

| Objective | Metric |
|-----------|--------|
| Track overall churn rate | Monthly / Quarterly Churn % |
| Identify high-risk segments | Churn by Demographics, Tenure, Product |
| Quantify revenue impact | Revenue Lost to Churn (MRR/ARR) |
| Monitor retention effectiveness | Retention Rate Trend over Time |
| Support proactive intervention | At-Risk Customer Flagging |

---

## 🖼️ Dashboard Preview

> *Add your Power BI dashboard screenshots here*

| Overview Page | Churn Analysis | Risk Categoty |
|---|---|---|
| ![alt text](image-1.png) | ![alt text](image-2.png) | ![alt text](image-3.png) |

---

## 🔑 Key Features

- **📊 Executive Summary Page** — High-level KPIs: Total Customers, Churn Rate, Revenue Retained, Revenue Lost
- **🔍 Churn Driver Analysis** — Multi-dimensional breakdown by age group, contract type, tenure, geography, and product
- **💰 Revenue Attrition Model** — Calculates MRR/ARR at risk and lost due to churn
- **📈 Retention Trend Analysis** — Month-over-month retention performance with trend lines
- **🎯 Segment Risk Scoring** — Visual flags for high-risk customer cohorts
- **🔄 Interactive Drill-Through** — Click-through from summary to granular customer-level detail

---

## 🗂️ Data Model

```
Customers (Fact)
    ├── DimDate         → Time intelligence (Month, Quarter, Year)
    ├── DimProduct      → Product/Plan details
    ├── DimGeography    → Region, City, Country
    └── DimSegment      → Demographics, Tenure Band, Risk Category
```

**Key Calculated Measures (DAX):**
```dax
Churn Rate = DIVIDE([Churned Customers], [Total Customers], 0)

Revenue Lost = SUMX(FILTER(Customers, Customers[Status] = "Churned"), Customers[MRR])

Retention Rate = 1 - [Churn Rate]

At-Risk Customers = CALCULATE([Total Customers], Customers[Risk Score] = "High")
```

---

## 📂 Repository Structure

```
customer-churn-retention-dashboard/
│
├── 📁 data/
│   ├── raw/                    # Raw source data (CSV/Excel)
│   └── processed/              # Cleaned & transformed data
│
├── 📁 dashboard/
│   └── Customer_Churn_Dashboard.pbix   # Power BI file
│
├── 📁 sql/
│   └── data_preparation.sql    # SQL queries for data preparation
│
├── 📁 screenshots/
│   └── *.png                   # Dashboard screenshots
│
└── README.md
```

---

## 💡 Key Insights Uncovered

> *(Update with your actual findings)*

- 📌 **Churn Rate:** X% of customers churned in the analyzed period
- 💰 **Revenue at Risk:** \$X revenue identified as high-risk
- 🔍 **Top Churn Driver:** Customers on [Month-to-Month contracts / Short tenure] showed X% higher churn
- 📍 **Highest Risk Segment:** [Segment name] with X% churn rate
- ✅ **Retention Opportunity:** Targeting [segment] could recover \$X in annual revenue

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Power BI Desktop** | Dashboard design, DAX measures, data modelling |
| **SQL** | Data extraction, transformation, and cleaning |
| **Advanced Excel** | Initial data exploration and validation |
| **Power Query (M)** | ETL — data shaping and transformation |

---

## 📬 Connect With Me

**Megharaju Vakiti** — Data Analyst

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Megharaju%20Vakiti-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/megharaju-vakiti)
[![GitHub](https://img.shields.io/badge/GitHub-Megharaju--Vakiti-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Megharaju-Vakiti)

---

<div align="center">
  <em>⭐ If you found this project useful, please give it a star!</em>
</div>
