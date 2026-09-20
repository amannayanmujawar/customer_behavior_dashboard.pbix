# Customer Behavior Dashboard 📊

An interactive **Power BI** dashboard that analyzes customer purchasing behavior — helping uncover patterns in spend, retention, and demographics that drive business decisions.

## 🔍 Overview

An end-to-end customer behavior analysis project — from raw data to an interactive dashboard. Covers data cleaning and feature engineering in Python, business-question analysis in SQL, and a Power BI dashboard for exploring purchase amount, subscription status, category performance, and age-group behavior in real time.

## 🐍 Data Cleaning & Feature Engineering (Python)

- Handled missing `Review Rating` values using category-wise median imputation
- Standardized column names (lowercase, underscores)
- Engineered `age_group` (Young Adult / Adult / Middle-aged / Senior) via quantile binning
- Engineered `purchase_frequency_days` — converted purchase-frequency labels (Weekly, Monthly, etc.) into numeric day counts
- Identified and dropped a redundant column (`promo_code_used`, fully duplicate of `discount_applied`)
- Loaded the cleaned dataset into MySQL for SQL analysis

See `customer_shopping_behaviour_analysis.ipynb` for the full notebook.

## 📌 Key Features

- **KPI Cards** — Number of Customers, Average Purchase Amount, Average Review Rating
- **Category Analysis** — Purchase amount & customer count by product category (clustered column charts)
- **Subscription Breakdown** — Donut chart of active vs. inactive subscription status
- **Age Group Insights** — Purchase amount & customer distribution across age groups (bar charts)
- **Interactive Slicers** — Filter by Gender, Category, Shipping Type, and Subscription Status

## 🛠️ Tools & Tech

- Python (Pandas) — data cleaning & feature engineering
- MySQL — data storage & SQL analysis
- Power BI Desktop — dashboarding
- DAX (measures & calculations)

## 🗃️ SQL Analysis

Beyond the Power BI dashboard, the dataset was also explored with SQL to answer specific business questions:

| Question | Insight |
|---|---|
| Revenue: Male vs. Female | Male customers generate ~2x the revenue of female customers |
| Discount users spending above average | Identified customers who used a discount yet still spent above the average purchase amount |
| Top 5 rated products | Gloves, Sandals, Boots, Hat, Skirt |
| Standard vs. Express shipping spend | Express shipping customers spend slightly more on average (~60.5 vs ~58.5) |
| Subscribers vs. non-subscribers | Subscribers are a smaller segment (1,053 vs 2,847) and spend about the same per order — subscription status barely affects individual spend |

See `customer_behavior.sql` for the full queries.

## 📁 Files

- `customer_shopping_behaviour_analysis.ipynb` — Data cleaning & feature engineering (Python)
- `customer_behavior.sql` — SQL queries used for exploratory analysis
- `customer_behavior_dashboard.pbix` — Full Power BI report file
- `customer_shopping_behavior.csv` — Source dataset

> **Note:** Before pushing, remove any hardcoded DB credentials from the notebook (use environment variables instead).

## 🚀 How to Use

1. Download `customer_behavior_dashboard.pbix`
2. Open in Power BI Desktop
3. Use the slicers to explore customer behavior by segment

## 📈 Insights Explored

- Which categories drive the most revenue vs. footfall
- How purchase behavior differs across age groups
- Subscription retention split across the customer base

---
*Built by Aman — Aspiring Data Analyst / AI-ML Engineer*
