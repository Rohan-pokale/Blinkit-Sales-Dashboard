# 🛒  End-to-End Blinkit Sales Analytics - (Excel Dashboard,EDA,SQL)  📊  

An interactive sales analytics dashboard created using **Microsoft Excel**, aimed at delivering insightful business intelligence for Blinkit – India’s Last Minute App. This project integrates data validation using SQL and exploratory data analysis (EDA) using Python libraries like pandas, matplotlib, and seaborn.

---

## 🗂 Project Overview

This project helps Blinkit’s stakeholders:
- Understand **total and average sales** across outlet types, locations, and sizes.
- Analyze product **distribution by fat content**, **item type**, and **ratings**.
- Track performance across **outlet establishment years** and **city tiers**.
- Enable smart filtering to explore sales patterns in detail.

The dashboard is built in **Excel** using advanced features like slicers, charts, conditional formatting, pivot tables, and interactive filters.

---

## 🛠 Tools & Technologies Used

| Tool/Technology                      | Purpose                                          |
|--------------------------------------|--------------------------------------------------|
| Microsoft Excel                      | Dashboard creation and visual analytics          |
| SQL                                  | Data validation and query-based checks           |
| Python (pandas, seaborn, matplotlib) | Exploratory data analysis (EDA)                  |

---

## 📊 Dashboard Pages

### 1️⃣ Sales Overview Dashboard  [View Excel Dashboard Page-1](https://github.com/Rohan-pokale/Blinkit-Sales-Dashboard/blob/main/01_Dashboard-Page1(Excel%20Dashboard).PNG)

- Total Sales: $1.20M  
- No. of Items: 8,523  
- Average Rating: 4.0  
- Average Sales: $141

**Key Visuals:**
- Sales by Outlet Size (High, Medium, Small)
- Sales by Outlet Location (Tier 1, Tier 2, Tier 3)
- Sales, Avg Sales, and Item Count by Outlet Type
- Interactive slicers for Outlet Size, Tier Location, and Item Type

---

### 2️⃣ Fat Content & Item Analysis Dashboard  [View Excel Dashboard Page-2](https://github.com/Rohan-pokale/Blinkit-Sales-Dashboard/blob/main/02_Dashboard-Page2%20(Excel%20Dashboard).PNG)

- Fat Content Breakdown: Regular (64.6%), Low Fat (35.4%)

**Key Visuals:**
- Fat Distribution by Item Type (Fruits, Snacks, Household, etc.)
- Fat Content Sales by City Tier
- Year-wise Sales by Outlet Establishment (2011–2022)
- Filter panel for outlet size, tier, and product categories

---

## 🧪 SQL Validation – Clean, Reliable Data [View SQL Report](https://github.com/Rohan-pokale/Blinkit-Sales-Dashboard/blob/main/03_SQL%20Report.md)

Before building the dashboard, SQL was used to ensure that the data was clean and logically structured. Key validation steps included:

- **Standardizing Data Entries:**  
  Cleaned values in columns like `Item_Fat_Content` to ensure consistency (e.g., `LF`, `low fat` → `Low Fat`, `reg` → `Regular`).

- **Checking Data Distribution:**  
  Used SQL queries to count distinct values, check for nulls, and ensure even distribution across item types, outlets, and sizes.

- **Validating KPIs via Queries:**  
  Ensured accuracy of dashboard metrics like Total Sales, Average Sales, Order Counts, and Ratings using `SUM()`, `AVG()`, and `COUNT()` functions in SQL.

- **Segment-Level Grouping:**  
  Verified relationships between sales and dimensions like fat content, item type, outlet type, location, and size.

This SQL-based validation helped maintain data integrity and allowed confident decision-making before visualization.

---

## 📊 Exploratory Data Analysis (Python)

EDA was conducted in Python using **pandas**, **matplotlib**, and **seaborn** to better understand trends, outliers, and hidden patterns.

### Key EDA Steps:

- **Data Overview & Cleaning:**
  - Loaded dataset into pandas DataFrames
  - Checked nulls, datatypes, and unique values
  - Converted numerical columns and handled inconsistencies

- **Univariate & Bivariate Analysis:**
  - Analyzed distribution of sales, ratings, fat content, and visibility
  - Correlation matrix for continuous variables

- **Visual Insights:**
  - Used seaborn & matplotlib for:
    - Bar plots of sales by item type and outlet size
    - Boxplots to spot outliers in sales
    - Line plots for year-wise trend analysis

These EDA results guided the dashboard design by highlighting which KPIs and filters matter most.

---

## 🧠 Key Insights

- **Supermarket Type 1** is the top performer with $787.5K in total sales.
- **Tier 3** locations generate the highest sales at $472.1K.
- **Medium-sized outlets** contribute most to overall sales.
- Majority of products sold are in the **Regular Fat** category.
- Sales peaked in **2018** among all years of outlet establishment.

---

## 🧩 Problem Solved by the Dashboard

> "Raw sales data often lacks structure and insight. This end-to-end project transforms Blinkit’s complex dataset into **clean, reliable, and visual intelligence** using SQL, Python (EDA), and Excel."

---

### ✅ Challenges Addressed & How Each Tool Helped

---

### 1. Disorganized Raw Data → Solved with SQL

- Standardized inconsistent fields like `Item_Fat_Content` using `UPDATE` queries
- Validated core metrics using `SUM()`, `AVG()`, and `COUNT()` to ensure data integrity
- Grouped records by outlet type, year, size, and location for better segmentation

✅ **Result:** A reliable, clean dataset ready for analysis and dashboarding.

---

### 2. Unclear Data Trends → Solved with Python EDA

- Used `pandas` for data loading, cleanup, and initial exploration
- Applied `matplotlib` and `seaborn` to visualize item sales, fat type breakdowns, and regional trends
- Discovered which variables (like outlet type, item category, and tier) drive the most sales

✅ **Result:** Key analytical insights to guide dashboard structure and filtering.

---

### 3. No Clear Visual Summary → Solved with Excel Dashboard

- Created interactive visuals using **pivot tables, slicers, charts, and conditional formatting**
- Visualized sales KPIs, fat content breakdowns, and location-based performance
- Enabled real-time filtering by outlet size, tier, and product category

✅ **Result:** Business users can interact with metrics and trends without writing SQL or Python code.

---

### 🎯 Final Outcome

This project bridges **raw data to insights** by combining:

- 🔍 **SQL** → For cleaning and validation  
- 📊 **Python EDA** → For trend discovery and exploration  
- 📈 **Excel** → For real-time, interactive business dashboards

> _“The dashboard empowers Blinkit’s teams to make smarter, faster, and more data-informed decisions.”_

---

## 👤 About Me

**Rohan Devanand Pokale**  
🎓 B.Tech – Computer Science (Data Science)  
🏫 Vishwakarma Institute of Technology, Pune  
📧 developer.rohan06@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/rohan-pokale-a774b2308)  

> Passionate about data analysis, storytelling through dashboards, and delivering real-world business insights using Excel, SQL, and Python.

---

📌 _“This Excel dashboard empowers Blinkit’s business teams to make smarter, data-driven decisions at every level.”_
