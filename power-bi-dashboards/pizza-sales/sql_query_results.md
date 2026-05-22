# 🍕 SQL Validation Report - Pizza Sales Dashboard

## 📋 Overview

This document serves as the validation benchmark for the Pizza Sales Power BI dashboard. All SQL queries were run first, and results were compared against DAX measures in Power BI to ensure 100% accuracy.

---

## 📊 A. KEY PERFORMANCE INDICATORS (KPIs)

---

### 1. 💰 Total Revenue

**Description:** The sum of the total price of all pizza orders.

**SQL Query:**
SELECT SUM(total_price) AS Total_Revenue 
FROM pizza_sales;

**Result:**

<img width="173" height="78" alt="Screenshot (501)" src="https://github.com/user-attachments/assets/cb4759f1-84b0-4538-a04c-661b814bf115" />


---

### 2. 📈 Average Order Value

**Description:** The average amount spent per order, calculated by dividing the total revenue by the total number of orders.

**SQL Query:**
SELECT CAST(SUM(total_price) / COUNT(DISTINCT order_id) AS DECIMAL(10,2)) AS Average_Order_Value 
FROM pizza_sales;

**Result:**

<img width="392" height="117" alt="Screenshot (502)" src="https://github.com/user-attachments/assets/728e7f53-8364-4e4b-9c70-db7861035a27" />

---

### 3. 🍕 Total Pizzas Sold

**Description:** The sum of the quantities of all pizzas sold.

**SQL Query:**
SELECT SUM(quantity) AS Total_Pizzas_Sold 
FROM pizza_sales;

**Result:**

<img width="310" height="133" alt="Screenshot (503)" src="https://github.com/user-attachments/assets/418bf23b-864c-4687-89b2-267f86c8c039" />

---

### 4. 📦 Total Orders

**Description:** The total number of orders placed.

**SQL Query:**
SELECT COUNT(DISTINCT order_id) AS Total_Orders 
FROM pizza_sales;

**Result:**

<img width="287" height="92" alt="Screenshot (504)" src="https://github.com/user-attachments/assets/4c432c8d-aa8a-4414-964b-f77ebe671b9b" />


---

### 5. 📊 Average Pizzas Per Order

**Description:** The average number of pizzas sold per order, calculated by dividing the total number of pizzas sold by the total number of orders.

**SQL Query:**
SELECT 
    CAST(SUM(quantity) * 1.0 / COUNT(DISTINCT order_id) AS DECIMAL(10,2)) AS avg_pizzas_per_order
FROM pizza_sales;

**Result:**

<img width="330" height="120" alt="Screenshot (505)" src="https://github.com/user-attachments/assets/9bfdb1ad-c61b-41d0-b567-676c72c44500" />


---

## 📈 B. CHARTS & TRENDS

---

### 6. 📅 Daily Trend for Total Orders

**Description:** Displays the daily trend of total orders over a specific time period to identify patterns or fluctuations in order volumes on a daily basis.

**SQL Query:**
SELECT 
    DATENAME(DW, order_date) AS order_day, 
    COUNT(DISTINCT order_id) AS total_orders 
FROM pizza_sales
GROUP BY DATENAME(DW, order_date)

**Result:**

<img width="390" height="179" alt="Screenshot (506)" src="https://github.com/user-attachments/assets/e511b4b0-c921-49f5-b432-382c34a44337" />

---

### 7. 🗓️ Monthly Trend for Orders

**Description:** Shows the monthly trend of total orders to identify seasonal patterns.

**SQL Query:**
SELECT 
    DATENAME(MONTH, order_date) AS Month_Name, 
    COUNT(DISTINCT order_id) AS Total_Orders
FROM pizza_sales
GROUP BY DATENAME(MONTH, order_date), MONTH(order_date)
ORDER BY MONTH(order_date);

**Result:**

<img width="480" height="267" alt="Screenshot (507)" src="https://github.com/user-attachments/assets/1bd5c927-1ded-4b27-8f8d-4864f4ea4b32" />

---

### 8. 🥧 Percentage of Sales by Pizza Category

**Description:** Shows the distribution of sales across different pizza categories, providing insights into the popularity of various pizza categories and their contribution to overall sales.

**SQL Query:**
SELECT 
    pizza_category, 
    CAST(SUM(total_price) AS DECIMAL(10,2)) AS total_revenue,
    CAST(SUM(total_price) * 100.0 / (SELECT SUM(total_price) FROM pizza_sales) AS DECIMAL(10,2)) AS Percentage
FROM pizza_sales
GROUP BY pizza_category
ORDER BY Percentage DESC;

**Result:**

<img width="438" height="157" alt="Screenshot (508)" src="https://github.com/user-attachments/assets/aeb31c05-4ae2-4beb-a93f-e4158a62c418" />

---

### 9. 📏 Percentage of Sales by Pizza Size

**Description:** Represents the percentage of sales attributed to different pizza sizes, helping understand customer preferences for pizza sizes and their impact on sales.

**SQL Query:**
SELECT 
    pizza_size, 
    CAST(SUM(total_price) AS DECIMAL(10,2)) AS total_revenue,
    CAST(SUM(total_price) * 100.0 / (SELECT SUM(total_price) FROM pizza_sales) AS DECIMAL(10,2)) AS Percentage
FROM pizza_sales
GROUP BY pizza_size
ORDER BY Percentage DESC;

**Result:**

<img width="424" height="204" alt="Screenshot (509)" src="https://github.com/user-attachments/assets/885c0944-a741-4dc5-833f-294743f10240" />

---

### 10. 🔥 Total Pizzas Sold by Pizza Category (February)

**Description:** Presents the total number of pizzas sold for each pizza category, allowing comparison of sales performance across different pizza categories.

**SQL Query:**
SELECT pizza_category, SUM(quantity) as Total_Quantity_Sold
FROM pizza_sales
WHERE MONTH(order_date) = 2
GROUP BY pizza_category
ORDER BY Total_Quantity_Sold DESC

**Result:**

<img width="396" height="190" alt="Screenshot (510)" src="https://github.com/user-attachments/assets/f0bcc724-f632-4f4d-b98e-e4fbed3998f3" />


---

### 11. 🏆 Top 5 Best Sellers by Total Pizzas Sold

**Description:** Highlights the top 5 best-selling pizzas based on the total number of pizzas sold to identify the most popular pizza options.

**SQL Query:**
SELECT TOP 5 
    pizza_name, 
    SUM(quantity) AS Total_Pizza_Sold
FROM pizza_sales
GROUP BY pizza_name
ORDER BY Total_Pizza_Sold DESC;

**Result:**

<img width="441" height="196" alt="Screenshot (511)" src="https://github.com/user-attachments/assets/be322371-681f-4353-b9ff-9d4250bf9f0a" />

---

### 12. 📉 Bottom 5 Worst Sellers by Total Pizzas Sold

**Description:** Showcases the bottom 5 worst-selling pizzas based on the total number of pizzas sold to identify underperforming or less popular pizza options.

**SQL Query:**
SELECT TOP 5 
    pizza_name, 
    SUM(quantity) AS Total_Pizza_Sold
FROM pizza_sales
GROUP BY pizza_name
ORDER BY Total_Pizza_Sold ASC;

**Result:**

<img width="537" height="165" alt="Screenshot (512)" src="https://github.com/user-attachments/assets/4790c833-3995-4c61-9b46-031dcff2284b" />


---

### 13. 💎 Top 5 Pizzas by Revenue

**Description:** Identifies the top 5 highest-grossing pizzas by sales revenue.

**SQL Query:**
SELECT TOP 5 
    pizza_name, 
    SUM(total_price) AS Total_Revenue
FROM pizza_sales
GROUP BY pizza_name
ORDER BY Total_Revenue DESC;

**Result:**

<img width="454" height="174" alt="Screenshot (513)" src="https://github.com/user-attachments/assets/cc26ab2f-2c60-4ed3-9579-1464daa9dce5" />

---

### 14. 💩 Bottom 5 Pizzas by Revenue

**Description:** Identifies the bottom 5 lowest-grossing pizzas by sales revenue.

**SQL Query:**
SELECT TOP 5 
    pizza_name, 
    SUM(total_price) AS Total_Revenue
FROM pizza_sales
GROUP BY pizza_name
ORDER BY Total_Revenue ASC;

**Result:**

<img width="548" height="207" alt="Screenshot (514)" src="https://github.com/user-attachments/assets/355f5c09-36ed-49de-8041-a4da31abaa74" />


---

### 15. ⭐ Top 5 Pizzas by Total Orders

**Description:** Identifies the top 5 pizzas that appear in the most unique orders.

**SQL Query:**
SELECT TOP 5 
    pizza_name, 
    COUNT(DISTINCT order_id) AS Total_Orders
FROM pizza_sales
GROUP BY pizza_name
ORDER BY Total_Orders DESC;

**Result:**

<img width="523" height="215" alt="Screenshot (515)" src="https://github.com/user-attachments/assets/2b243797-4706-4aa2-9ecc-098788199878" />

---

### 16. 💔 Bottom 5 Pizzas by Total Orders

**Description:** Identifies the bottom 5 pizzas that appear in the fewest unique orders.

**SQL Query:**
SELECT TOP 5 
    pizza_name, 
    COUNT(DISTINCT order_id) AS Total_Orders
FROM pizza_sales
GROUP BY pizza_name
ORDER BY Total_Orders ASC;

**Result:**

<img width="508" height="221" alt="Screenshot (516)" src="https://github.com/user-attachments/assets/22cdfc51-3b97-42f1-8712-d370a010e752" />

