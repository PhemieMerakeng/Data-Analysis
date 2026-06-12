# 📊 FinSight – Interactive Banking Analytics Dashboard

An interactive, end-to-end banking intelligence solution designed for a financial organization to monitor and analyze macro transaction growth, operational efficiency, regional performance, and customer demographics.

---

## 📌 Project Objectives & Analytical Focus

The primary aim of this project is to calculate, discover, and isolate critical financial and operational performance indicators across the bank's networks. Specifically, the dashboard is built to determine:
* **🚀 Revenue Drivers & Growth Velocity**: Quantify real-time transaction volumes and track exact Year-over-Year (YoY) financial growth trajectories.
* **💎 Segment Value & Regional Contribution**: Identify high-performing customer segments and pinpoint the top revenue-generating states to optimize regional capital allocation.
* **⚠️ Operational Leakage & System Latency**: Measure systemic transaction failures to calculate lost revenue potential and identify friction points within payment pipelines.
* **📈 Product Profitability Channels**: Dissect and compare different banking transaction types to see exactly which services yield the highest processing fees and tax margins.
* **👥 Portfolio Demographics**: Analyze customer engagement patterns based on gender and occupation to drive targeted, data-backed promotional campaigns.

---

## 🖼️ Dashboard Preview

The final analytical report consists of two distinct views connected by a centralized styling framework and an interactive sidebar navigation system:

### 1. Executive Overview Analysis
<img width="945" height="512" alt="Screenshot (524)" src="https://github.com/user-attachments/assets/8bc8ff29-2903-4051-84c8-f64c9abe4be5" />

### 2. Detailed Transactions Record Grid
<img width="948" height="516" alt="Screenshot (525)" src="https://github.com/user-attachments/assets/5cb3db5e-16d8-4080-aa44-9e75027ec8c7" />

### 🎛️ Dynamic Top-Ribbon Features
To enhance user experience and maintain clarity during data exploration, the top banner of the dashboard includes an intelligent context feature:
* **📅 Dynamic Context Display**: A dedicated indicator at the top of the report instantly updates to show exactly which **Year** is currently being evaluated and which specific **Dynamic Metric** (e.g., Total Amount, Total Transactions, etc.) is being visualized across the charts. This ensures stakeholders never lose context while using the sidebar filters.

---

## ⚙️ Dashboard Architecture & Visualizations

### 🛠️ Core Project Competencies
* **🧠 Power BI DAX & Data Modeling**: Built using star-schema relationship modeling and advanced DAX expressions to calculate robust time-intelligence comparisons and dynamic switches.
* **🧹 Power Query & Data Cleaning**: Managed the end-to-end extraction and transformation pipeline, ensuring absolute precision data handling, text standardization, duplicate filtration, and localized data type conversions.
* **🎨 Dashboard Design & Interactive Dashboards**: Engineered with an intuitive, user-centric interface that balances dense financial matrices with macro scorecard components for rapid executive scanning.
* **📢 Data Visualization & Business Intelligence Reporting**: Constructed using clear, un-cluttered visual design frameworks to tell a compelling operational story, transforming raw row-level records into structured insights.

### 🎯 Key Performance Indicators (KPIs)

* 💰 **Total Amount** – The total monetary volume processed across all banking transactions. This provides stakeholders with a clear assessment of overall sales velocity and gross financial scale. **Result: R137.53M** *(▲ +1.41% Year-over-Year growth)*
* 💳 **Total Transactions** – The absolute number of unique transaction records processed. This measures the total throughput and overall transaction frequency handled by the banking network. **Result: 14.94K** *(▼ -0.57% Year-over-Year change)*
* 💵 **Average Transaction Value** – The average financial value distributed per transaction, calculated by dividing the total amount by total transactions. This helps the business understand average ticket sizes and consumer spending patterns. **Result: R9.20K** *(▲ +1.98% Year-over-Year growth)*
* 📈 **Total Fees** – The collective fee revenue accumulated from processed bank transactions. This tracks baseline platform monetization and transactional channel profitability. **Result: R216.94K** *(▼ -0.17% Year-over-Year change)*
* 🏛️ **Total Tax** – The total tax revenue generated from all consumer and corporate banking activities. This calculates the regulatory tax footprint derived across transaction categories. **Result: R39.04K** *(▼ -0.26% Year-over-Year change)*

### 🔍 Analytical Trends & Visual Components
* **📉 Trend Analysis (Line/Area Chart)**: Used for **Total Amount by Month** to analyze historical performance fluctuations and pinpoint specific seasonal spikes or volume drops.
* **🩺 System Health (Donut Chart)**: Used for **Total Amount by Transaction Status** to benchmark operational efficiency by segregating Success, Failed, and Pending transactions.
* **👑 Customer Segmentation (Horizontal Bar Chart)**: Used for **Total Amount by Customer Segment** to classify and rank institutional value across Retail, Premium, SME, Corporate, and Wealth banking groups.
* **📍 Geographic Distribution (Horizontal Bar Chart)**: Used for **Total Amount by State** to run localized performance comparisons and map top-tier banking regions.
* **🧮 Profitability Matrix (Heatmap Table)**: Used for **Transaction Type Analysis** to map specific banking vectors (such as *Loan EMI, Transfers, Deposits, and Withdrawals*) directly against conditional volume, fee, and tax metrics.
* **🧬 Demographic Participation (Donut Chart)**: Used for **Total Amount by Gender** to analyze portfolio split variations and monitor target profile alignment.
* **📋 Granular Audit Grid**: Features an underlying transactional records view facilitating drill-down reporting for financial compliance and deep-dive transaction audits.

---

## 🏁 Conclusion

In conclusion, this project provides a reliable banking analytics solution by turning raw transaction data into interactive visual insights. Used Power Query to successfully clean the tables by standardizing currencies, correcting local data types,Trimming, and removing duplicate entries. A solid data model connects these tables to a dedicated calendar dimension, enabling smooth sorting and accurate year-over-year calculations. Ultimately, the finished dashboard gives the management team an effective tool to monitor revenue growth, analyze transaction performance, and make data-driven financial decisions.
