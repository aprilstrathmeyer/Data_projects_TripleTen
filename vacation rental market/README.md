# 🏙️ Analyzing the Manhattan Vacation Rental Market: A Spreadsheet BI Project

## 🧭 Project Overview

This project explores short-term rental trends in Manhattan to help a client determine the **best neighborhoods and property types** to invest in. Using spreadsheet-based data analysis, I examined Airbnb listings, cleaned and transformed the dataset, and built pivot tables to extract key insights.

This analysis was completed as part of **Sprint 1: Spreadsheet Data Analysis** in the **Business Intelligence Analytics Bootcamp** by TripleTen.

📄 **Project PDF Report**: [Vacation Rental Market.pdf](./Vacation%20Rental%20Market.pdf)

---

## 🎯 Business Problem

The client is looking to invest in Airbnb properties in Manhattan and wants to know:

- Which **neighborhoods** and **property sizes** are most attractive to renters?
- How much **revenue** could top-performing listings earn annually?

Using recent Airbnb data and proxy metrics like reviews and price, this project answers these questions with clear visualizations and recommendations.

---

## 📁 Data Sources

- **Listings Table**: Property details, reviews, bedrooms, neighborhood, and ID.
- **Calendar Table**: 30-day data on daily price, availability, and adjusted revenue.

🧹 Data Cleaning Highlights:
- Normalized inconsistent formatting in `neighborhood` → `neighborhood_clean`
- Replaced empty cells in `bedrooms` with 0 → `bedrooms_clean`
- Documented all changes in a dedicated **Change Log** sheet

---

## 📊 Key Analysis Questions & Insights

### 1. 🏘️ Most Attractive Neighborhoods

Using `number_of_reviews_ltm` (last 12 months) as a proxy for rental demand, the top 10 neighborhoods were ranked. The top three were:

- **Lower East Side**
- **Hell's Kitchen**
- **Harlem**

📊 A bar chart was created to display total reviews by neighborhood.

---

### 2. 🛏️ Most Popular Property Sizes

Cleaned bedroom data was used to determine which property sizes are most rented:

- **Studios**
- **1-bedrooms**
- **2-bedrooms**

Each of the top 10 neighborhoods was then cross-analyzed to identify the **preferred size** in each. For instance:

- **Harlem** → 1-bedroom  
- **Midtown** → Studio

---

### 3. 💰 Revenue Estimation for Top Listings

Listings matching both top neighborhoods and preferred property sizes were flagged as `top_listing = 1`.

**Revenue Estimation Process**:
- Created a `revenue_earned` column in the calendar sheet:
  ```excel
  =IF(available="f", adjusted_price, 0)
