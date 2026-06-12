# 🍕 Pizza Sales Dashboard

## 📋 Problem Statement

A pizza restaurant needs to understand its sales performance across different dimensions. The business wants to track key metrics like revenue and order volume, while also identifying popular pizza categories, preferred pizza sizes, and which pizzas are overperforming or underperforming. The goal is to use this data to make informed decisions about inventory, staffing, and menu optimization.

---

## 🖼️ Dashboard Preview

<img width="939" height="490" alt="Screenshot (499)" src="https://github.com/user-attachments/assets/75ab8a8c-4115-4e22-a987-d2fe1bc8ef5b" />



<img width="944" height="492" alt="Screenshot (500)" src="https://github.com/user-attachments/assets/f1ac312e-27ff-46fb-b4f6-76b4b1a34b21" />

---

## 📊 Overview

Power BI dashboard analyzing pizza sales performance. All KPIs and analysis were first calculated using SQL queries to establish a source of truth, then recreated in Power BI using DAX before building visuals.

---

## 📁 Data Source

**pizza_sales.csv** – The raw dataset containing all pizza order transactions including:
- Order date and time
- Pizza name, category, and size
- Quantity and total price

---

## 🎯 Key Performance Indicators (KPIs)

**💰 Total Revenue** – The sum of the total price of all pizza orders. This gives the business a clear picture of overall sales performance. *SQL Result: $817,860*

**💵 Average Order Value** – The average amount spent per order, calculated by dividing total revenue by the total number of orders. This helps understand customer spending behavior. *SQL Result: $38.31*

**🍕 Total Pizzas Sold** – The sum of the quantities of all pizzas sold. This tracks overall volume of pizzas leaving the kitchen. *SQL Result: 49,574*

**📦 Total Orders** – The total number of unique orders placed. This measures customer traffic and order frequency. *SQL Result: 21,350*

**📊 Average Pizzas Per Order** – The average number of pizzas sold per order, calculated by dividing total pizzas sold by total orders. This indicates whether customers are ordering single pizzas or larger quantities. *SQL Result: 2.32*

---

## 📈 Charts Included

**📅 Daily Trend for Total Orders** – A bar chart showing how order volumes fluctuate across different days of the week. This helps identify which days have the highest and lowest order activity.

**🗓️ Monthly Trend for Total Orders** – A bar chart showing order volume trends across months. This helps identify seasonal patterns in pizza demand.

**🥧 Percentage of Sales by Pizza Category** – A pie chart showing how sales are distributed across pizza categories including Classic, Veggie, Supreme, and Chicken. This highlights which categories drive the most revenue.

**📏 Percentage of Sales by Pizza Size** – A pie chart representing the percentage of sales attributed to different pizza sizes including Small, Medium, Large, and X-Large. This helps understand customer size preferences.

**🏆 Total Pizzas Sold by Pizza Category** – A bar chart presenting the total number of pizzas sold for each pizza category. This allows comparison of sales performance across categories.

**🥇 Top 5 Pizzas by Revenue** – A bar chart highlighting the five pizzas generating the most revenue.

**🥉 Bottom 5 Pizzas by Revenue** – A bar chart showcasing the five pizzas generating the least revenue.

**🔥 Top 5 Pizzas by Quantity** – A bar chart showing the five most sold pizzas based on total quantity.

**❄️ Bottom 5 Pizzas by Quantity** – A bar chart showing the five least sold pizzas based on total quantity.

**📝 Top 5 Pizzas by Total Orders** – A bar chart highlighting the five pizzas with the highest number of unique orders.

**📋 Bottom 5 Pizzas by Total Orders** – A bar chart showcasing the five pizzas with the lowest number of unique orders.

---

## 💡 Key Insights from Analysis

* 🥧 **Best Selling Category**
* 📏 **Most Popular Size**
* 📅 **Peak Day**
* ⏰ **Peak Hour**
* 🏆 **Top Pizza by Revenue**
* 🏆 **Top Pizza by Quantity**
* 🏆 **Top Pizza by Orders**
* ⚠️ **Lowest Performing Pizza**
* 📈 **Best Month**
* 📉 **Slowest Month**

---

## 🛠️ SQL Validation Approach

Before building the dashboard in Power BI, all KPIs and analysis were first calculated using SQL queries. This established a reliable source of truth. A total of **16 SQL queries** were written covering:

- 5 KPI calculations (Total Revenue, Average Order Value, Total Pizzas Sold, Total Orders, Average Pizzas Per Order)
- Daily and monthly order trends
- Percentage of sales by pizza category and size
- Total pizzas sold by category (February filter)
- Top and bottom 5 pizzas by revenue, quantity, and total orders

Each SQL result was saved and used as a benchmark. The same metrics were then recreated in Power BI using DAX measures, and results were compared to verify accuracy before any visuals were built.

---

## 📝 Conclusion

This project successfully delivered a pizza sales dashboard that tracks **5 key performance indicators** and includes **11 visualizations**. The SQL validation approach ensured that every metric in the Power BI dashboard matched the source data before any charts were created. All KPIs were validated and matched successfully.

**Key takeaways:**
- 🥧 **Classic** category leads in sales percentage at 26.91%
- 📏 **Large** size pizzas dominate sales at nearly 46%
- 💰 Total revenue reached **$817,860** across 21,350 orders
- 🏆 Top performing pizzas by revenue, quantity, and orders were identified
- ⚠️ Underperforming pizzas were flagged for potential menu review

The dashboard allows the business to easily identify top-selling pizzas, underperforming menu items, customer size preferences, and daily and monthly sales patterns.
