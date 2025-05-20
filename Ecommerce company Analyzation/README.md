# 🛒 E-Commerce Funnel & Cohort Analysis Dashboard

## 📦 Project Overview

This Business Analytics project focuses on turning raw user activity logs into actionable business metrics for an e-commerce company. As a Junior Analyst, I was responsible for building a conversion funnel, preparing cohort data, and calculating retention rates — all within a single structured Google Sheets workflow.

This project was completed as part of Sprint 3 in the Business Intelligence Analytics Bootcamp by TripleTen.

🔗 **View the Project Spreadsheet**: [Google Sheets Link](https://docs.google.com/spreadsheets/d/your_project_link_here)

---

## 💼 Business Case

The executive team needed insights into:

- How users progress through the purchase funnel
- Customer retention and cohort behavior
- Key metrics that drive growth or churn

I used advanced spreadsheet techniques to translate raw event logs into a comprehensive performance report.

---

## 🗂️ Data Source

- **Sheet Name**: `raw_user_activity`
- **Key Fields**:
  - `user_id`: Unique customer identifier
  - `event_type`: Product view, cart open, or purchase
  - `category_code`, `brand`, `price`, `event_date`

---

## 📈 Key Analytical Steps

### 1. 🔻 Conversion Funnel
Created a 3-step funnel:
- **Stage 1**: Product Page Views  
- **Stage 2**: Cart Opens  
- **Stage 3**: Purchases  

**Metrics**:
- Unique users per stage
- Total conversion rate
- Step-to-step conversion rates

📄 Sheet: `conversion_funnel`

---

### 2. 🧾 Cohort Data Preparation
Filtered purchase events into a separate sheet and calculated:
- First purchase date per user (`first_purchase`)
- Mapped each purchase to:
  - `event_month`
  - `first_purchase_month`
  - `cohort_age` (in months)

📄 Sheets: `purchase_activity`, `first_purchase`

---

### 3. 📊 Retention Analysis
Grouped users into acquisition cohorts by first purchase month and tracked retention across 4 months.

📄 Sheets:
- `cohort_analysis`: Unique user count by cohort & age
- `retention_rates`: Monthly retention % for each cohort

---

## 📋 Executive Summary

### 🧾 Results:
- Funnel revealed key drop-off points between views and cart opens.
- Cohort analysis showed that customer retention decreased steadily after the first month.
- Retention rates ranged between **12%–33%** across cohorts in the 2nd month.

### 🔍 Analysis:
- Dataset spanned over multiple months and included over 4,800 purchases.
- Funnel stages were built using **unique user counts**, not event counts.
- Cohorts were based on the **first purchase month**, and retention was calculated using **user presence per cohort age**.

📄 Sheets: `Executive Summary`, `Table of Contents`

---

## 🛠 Tools Used

- **Google Sheets**: All data manipulation and calculations
- **Pivot Tables**: Conversion funnel, cohort setup, and retention analysis
- **Formulas**: `VLOOKUP()`, `TEXT()`, `DATEDIF()`, `% calculations`

---

## 📎 Deliverables

- Organized and formatted spreadsheet with:
  - Conversion Funnel
  - Cohort Analysis
  - Retention Rate Table
  - Executive Summary
  - Table of Contents
- Best practices: clear labels, frozen headers, formatted tables, readable formulas

---

## 📬 Contact

**April Rebecca Strathmeyer**  
Business Intelligence Analyst  
[LinkedIn](https://www.linkedin.com/in/yourprofile) | [Email](mailto:your.email@example.com)

---

> _“Helping companies transform raw data into retention and revenue.”_
