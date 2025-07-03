![image](https://github.com/user-attachments/assets/bb3069ab-c4f1-4195-816e-9bf6b74f9439)# 🛒 Blinkit Analysis (SQL Report)

This repository contains SQL queries and insights derived from the Blinkit sales dataset. It includes data cleaning, key performance indicators (KPIs), and detailed visual analysis by various attributes.

---

## 1. View Raw Data:

**Query:**

```
sql
SELECT * FROM blinkit_data;
```

## 2.DATA CLEANING:

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




SELECT CAST(AVG(Rating) AS DECIMAL(10,1)) AS Avg_Rating
FROM blinkit_data;

