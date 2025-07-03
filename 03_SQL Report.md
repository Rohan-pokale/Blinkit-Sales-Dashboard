# 🛒 Blinkit Analysis (SQL Report)

This File contains SQL queries and insights derived from the Blinkit sales dataset. It includes data cleaning, key performance indicators (KPIs), and detailed visual analysis by various attributes.

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

## 3. NO OF ITEMS
```
sql
SELECT COUNT(*) AS No_of_Orders
FROM blinkit_data;

```
![image](https://github.com/user-attachments/assets/19163bc5-2750-4531-a157-bee9eccd0fb1)

---

## 4. AVG RATING
```
sql
SELECT CAST(AVG(Rating) AS DECIMAL(10,1)) AS Avg_Rating
FROM blinkit_data;

```
![image](https://github.com/user-attachments/assets/f17e75a5-027c-4180-8560-57a76377e37a)

---

## B. Total Sales by Fat Content:
```
sql
SELECT Item_Type, CAST(SUM(Total_Sales) AS DECIMAL(10,2)) AS Total_Sales
FROM blinkit_data
GROUP BY Item_Type
ORDER BY Total_Sales DESC

```
![image](https://github.com/user-attachments/assets/64a09636-7de7-41ec-9ea2-a8e536c5d81b)

---

## D. Fat Content by Outlet for Total Sales

![image](https://github.com/user-attachments/assets/df0f5153-705c-4768-87e6-fbc93adf4e6a)

---

## E. Total Sales by Outlet Establishment
```
sql
SELECT Outlet_Establishment_Year, CAST(SUM(Total_Sales) AS DECIMAL(10,2)) AS Total_Sales
FROM blinkit_data
GROUP BY Outlet_Establishment_Year
ORDER BY Outlet_Establishment_Year

```
![image](https://github.com/user-attachments/assets/6a5c3c26-4206-4ea5-b6ff-f601cc4bc40b)

---

## F. Percentage of Sales by Outlet Size
```
sql
SELECT 
    Outlet_Size, 
    CAST(SUM(Total_Sales) AS DECIMAL(10,2)) AS Total_Sales,
    CAST((SUM(Total_Sales) * 100.0 / SUM(SUM(Total_Sales)) OVER()) AS DECIMAL(10,2)) AS Sales_Percentage
FROM blinkit_data
GROUP BY Outlet_Size
ORDER BY Total_Sales DESC;

```
![image](https://github.com/user-attachments/assets/d96d0a42-e545-4739-bf04-c75de3ab5429)

---

## G. Sales by Outlet Location
```
sql
SELECT Outlet_Location_Type, CAST(SUM(Total_Sales) AS DECIMAL(10,2)) AS Total_Sales
FROM blinkit_data
GROUP BY Outlet_Location_Type
ORDER BY Total_Sales DESC

```
![image](https://github.com/user-attachments/assets/1611a27f-d4a0-4a15-a0c6-baa5d8cc26c7)

---

## H. All Metrics by Outlet Type:
```
sql
SELECT Outlet_Type, 
CAST(SUM(Total_Sales) AS DECIMAL(10,2)) AS Total_Sales,
		CAST(AVG(Total_Sales) AS DECIMAL(10,0)) AS Avg_Sales,
		COUNT(*) AS No_Of_Items,
		CAST(AVG(Rating) AS DECIMAL(10,2)) AS Avg_Rating,
		CAST(AVG(Item_Visibility) AS DECIMAL(10,2)) AS Item_Visibility
FROM blinkit_data
GROUP BY Outlet_Type
ORDER BY Total_Sales DESC

```
![image](https://github.com/user-attachments/assets/d74a74f7-a123-4036-a171-fad7cff11911)

---

