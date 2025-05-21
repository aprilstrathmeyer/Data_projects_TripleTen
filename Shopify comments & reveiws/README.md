# 🛍️ Shopify App Landscape Analysis: A Power BI Project

## 🧭 Project Overview

This project explores the Shopify App Store to uncover what drives app success on the platform. Using Power BI, I created a multi-page dashboard that visualizes app activity, review quality, developer responsiveness, and category breakdowns. The goal is to help Shopify stakeholders understand key factors behind high-performing apps.

This analysis was completed as part of the **Business Intelligence Analytics Bootcamp** by TripleTen.

📄 **Project Report (PDF Screenshots)**: [Shopify Reviews.pdf](./Shopify%20Reviews.pdf)

---

## 🎯 Business Problem

Shopify offers thousands of apps—but not all are created equal. This project aims to answer:

- How many apps are on the platform?
- What is the relationship between reviews, ratings, and app performance?
- How does developer engagement affect review quality?
- Which developers and apps are standing out?

---

## 📁 Data Source

**Dataset:** `shopify.xlsx`  
Data was scraped from public Shopify app pages and includes:

- **Apps Table**: App metadata (ID, developer, last update, etc.)
- **Categories Table**: Category names for apps
- **Apps_Categories Table**: Join table linking apps to multiple categories
- **Reviews Table**: Ratings, helpful votes, and developer replies

---

## 📊 Power BI Pages & Visual Insights

### 1. 📈 App Landscape

> Power BI Page: `App Landscape`

- **KPI Card**: Count of unique apps on the platform
- **Line Chart**: Review count trend over time using `lastmod` date
- **Scatterplot**: Reviews count (X-axis) vs. Average rating (Y-axis)  
  📝 Annotated insights from scatterplot: Identified clusters of apps with high review volumes but moderate ratings—suggesting quality doesn't always scale with popularity

---

### 2. 💬 Reviews

> Power BI Page: `Reviews`

- **New Column (DAX)**: `helpful_reviews = rating * (1 + helpful_count)`
  - 📊 Card visual shows the **average helpful review score**
- **New Column (DAX)**: `developer_answered = IF(ISBLANK(developer_reply), 0, 1)`
  - 📉 Scatterplot: `developer_answered` vs. Average rating  
    Revealed that apps with more developer responses often have higher average ratings

---

### 3. 🧾 App Reviews

> Power BI Page: `App Reviews`

- **New Relationship**: Connected `Reviews[app_id]` to `Apps[id]` (Many-to-One)
- **Bar Chart 1**: Developer vs. **sum of all review ratings**
  - ⚠️ Limitation: Sum of ratings can be misleading without weighting by quality
- **Bar Chart 2**: Developer vs. **average helpful_review**  
  - Provided a more balanced view of customer sentiment
- **Bar Chart 3**: Developer responsiveness  
  - Developer vs. `developer_answered`  
  - Filtered by `reviews_count > 500`  
    📍 Insight: Certain developers with large review volumes stand out for active engagement

---

## 🛠 Tools & Techniques

- **Power BI**: Data modeling, KPI cards, custom DAX columns, scatterplots, line/bar charts
- **DAX**: Calculated columns for new performance and responsiveness metrics
- **Relationships**: Joined tables to build multi-layered dashboards
- **Storytelling**: Structured pages for different analytical themes

---

## 🧠 Skills Demonstrated

- Data visualization for app store performance
- Creation of calculated fields in Power BI using DAX
- Designing interactive dashboards with meaningful KPIs
- Analyzing user engagement through reviews and developer actions
- Visual storytelling with insights annotated directly in Power BI

---

## 📬 Contact

**Your Name**  
Business Intelligence Analyst  
[LinkedIn](https://www.linkedin.com/in/yourprofile) | [Email](aprilmagallanes76@gmail.com)

---

> _"Turning app reviews into strategic insights on the Shopify marketplace."_  
