# 🛒 Blinkit Analysis (SQL Report)

This repository contains SQL queries and insights derived from the Blinkit sales dataset. It includes data cleaning, key performance indicators (KPIs), and detailed visual analysis by various attributes.

---

## DATA CLEANING:

```
sql
UPDATE blinkit_data
SET Item_Fat_Content = 
    CASE 
        WHEN Item_Fat_Content IN ('LF', 'low fat') THEN 'Low Fat'
        WHEN Item_Fat_Content = 'reg' THEN 'Regular'
        ELSE Item_Fat_Content
         END;

SELECT DISTINCT Item_Fat_Content FROM blinkit_data;
```
![image](https://github.com/user-attachments/assets/8c0ac9ea-6603-4394-8e86-906cb8f38ba0)

---

# A. KPI’s

## 1. TOTAL SALES:

```
sql
SELECT CAST(SUM(Total_Sales) / 1000000.0 AS DECIMAL(10,2)) AS Total_Sales_Million
FROM blinkit_data

```
![image](https://github.com/user-attachments/assets/6b80e6c9-49d2-4371-82f2-a0630ac47a72)

---

## 2. AVERAGE SALES
```
sql
SELECT CAST(AVG(Total_Sales) AS INT) AS Avg_Sales
FROM blinkit_data;

```
![image](https://github.com/user-attachments/assets/77f6b852-4459-4dac-9eba-740ab09c26fe)

---



