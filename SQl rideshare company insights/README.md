# 🚖 Zuber Rideshare BI Analytics Project

Welcome to the **Zuber Rideshare Analytics** project! This business intelligence case study was built using SQL and Python to analyze ride-sharing patterns in Chicago. The objective was to extract insights that would help a new ride-share company, Zuber, understand user behavior and the effects of external factors like weather on ride frequency and duration.

---

## 📊 Project Objective

As a data analyst for **Zuber**, a ride-sharing startup launching in Chicago, your goal is to:

- Identify ride trends and preferences from historical taxi data.
- Compare Zuber to competitors like Flash Cab and Taxi Affiliation Services.
- Test hypotheses about how weather, especially rain and storms, impacts ride durations—specifically for trips from downtown Chicago (the Loop) to O’Hare International Airport on Saturdays.

---

## 🗃️ Dataset Overview

The analysis was performed using a SQL database composed of four main tables:

### `neighborhoods`
| Column Name       | Description                      |
|------------------|----------------------------------|
| `name`           | Name of the neighborhood         |
| `neighborhood_id`| Unique identifier for each area  |

### `cabs`
| Column Name     | Description                     |
|----------------|---------------------------------|
| `cab_id`       | Unique vehicle ID               |
| `vehicle_id`   | Technical vehicle ID            |
| `company_name` | Name of the taxi company        |

### `trips`
| Column Name         | Description                                |
|--------------------|--------------------------------------------|
| `trip_id`          | Unique identifier for each ride            |
| `cab_id`           | Vehicle that completed the trip            |
| `start_ts`         | Start time (rounded to the hour)           |
| `end_ts`           | End time (rounded to the hour)             |
| `duration_seconds` | Duration of the ride in seconds            |
| `distance_miles`   | Distance of the ride in miles              |
| `pickup_location_id` | Neighborhood where the trip started     |
| `dropoff_location_id`| Neighborhood where the trip ended       |

### `weather_records`
| Column Name     | Description                              |
|----------------|------------------------------------------|
| `record_id`     | Unique ID of the weather record          |
| `ts`            | Timestamp of the record (hourly)         |
| `temperature`   | Temperature reading                      |
| `description`   | Weather conditions (e.g. "light rain")   |

> **Note:** No direct relationship exists between `trips` and `weather_records`, but a JOIN was performed using timestamp alignment (`start_ts` ≈ `ts`).

---

## 🧪 Project Tasks

### Step 1: Exploratory Data Analysis

- Analyze trip counts per company for November 15–16, 2017.
- Compare trips for companies with names containing **"Yellow"** or **"Blue"** (November 1–7).
- Aggregate trip counts across all companies, highlighting **Flash Cab**, **Taxi Affiliation Services**, and grouping others as “Other.”

### Step 2: Hypothesis Testing

- Extract `neighborhood_id` values for **the Loop** and **O'Hare International Airport**.
- Use weather descriptions to classify time periods as:
  - **"Bad"** (if includes "rain" or "storm")
  - **"Good"** (all other conditions)
- Isolate rides:
  - From **the Loop** (`neighborhood_id: 50`)
  - To **O'Hare** (`neighborhood_id: 63`)
  - Occurring on **Saturdays**
- Compare ride durations under different weather conditions.

---

## 📈 Key Tools & Skills

- SQL (PostgreSQL): Joins, aggregations, date filtering, CASE statements
- Python: Jupyter Notebook for result visualization and reporting
- Data Wrangling & EDA
- Business hypothesis testing
- Data storytelling for stakeholders

---

## 📄 Project PDF

For detailed analysis, SQL queries, and visualizations, refer to the full report:
**[SQL Rideshare.pdf](./SQL%20Rideshare.pdf)**

---

## ✅ Insights

- The majority of rides during key November periods came from Flash Cab and Taxi Affiliation Services.
- Ride durations from the Loop to O’Hare are noticeably **longer on rainy Saturdays**, supporting the hypothesis that weather impacts ride efficiency.

---

## 🧠 Lessons Learned

This project helped reinforce:
- Relational database concepts in real-world contexts
- Translating business questions into data queries
- Combining disparate data sources for analytical conclusions
- Communicating findings clearly for business decision-making

---

## 📬 Contact

Have questions or want to connect?

**Your Name**  
[Your LinkedIn](https://www.linkedin.com)  
[Your Email](aprilmagallanes76@gmail.com)

---

