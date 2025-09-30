# Task 6 – Sales Trend Analysis (Advanced)

## 📌 Overview
This project is part of my **Data Analyst Internship at Elevate Labs**.  
The goal is to analyze **monthly revenue and order volume** using SQL and generate advanced **time-series metrics** such as Average Order Value (AOV), Month-over-Month (MoM) and Year-over-Year (YoY) growth, cumulative revenue share, and seasonality. These insights help support **business decision-making**.

---

## 🎯 Objectives
- Compute monthly revenue and order volume  
- Calculate **AOV, MoM, and YoY growth**  
- Identify top-performing months and their cumulative contribution  
- Analyze **product-line level trends and seasonality**  
- Apply advanced SQL: **CTEs, window functions, ranking, aggregates**  
- Deliverables: `queries.sql`, result screenshots, and concise insights  

---

## 🛠 Tools & Technologies
- **PostgreSQL 17**  
- **pgAdmin 4** (or any SQL client)  
- CSV dataset (`online_sales.csv`)  
- *(Optional)* Power BI / Excel for visualization  

---

## 📂 Dataset (table: `online_sales`)
**Key columns**:  
- `ORDERNUMBER` – Unique order ID  
- `ORDERDATE` – Order date (or `YEAR_ID`, `MONTH_ID`)  
- `SALES` – Sales amount  
- `QUANTITYORDERED` – Quantity ordered  
- `PRODUCTLINE` – Product category  
- `COUNTRY` – Customer country  
- `MONTH_ID`, `YEAR_ID`, `QTR_ID` – Precomputed date parts (if available)  
- Other columns: `PRICEEACH`, `MSRP`, `CUSTOMERNAME`, `DEALSIZE`  

⚠️ *Note*: If `ORDERDATE` has mixed formats, import as `TEXT` first, then convert to `DATE` in SQL.  

---

## 📜 Queries Implemented (in `queries.sql`)
Key SQL queries included in the repository:
1. Create table & import dataset  
2. Verify data (`COUNT(*)`, `SELECT * LIMIT 10`)  
3. Convert `ORDERDATE` to proper DATE format  
4. Monthly revenue & order volume  
5. Top 3 / Top 5 months by revenue  
6. Compare monthly trends across years  
7. Monthly **AOV (Average Order Value)**  
8. Cumulative revenue share (window functions)  
9. Rank months by AOV (RANK/ROW_NUMBER)  
10. Product-line monthly revenue trend  
11. Seasonality – average revenue by month across years  
12. Advanced growth metrics: **MoM, YoY, cumulative revenue**  

---

## ✅ How to Run
1. Install **PostgreSQL & pgAdmin**  
2. Create a new database (e.g., `sales_db`)  
3. Create the table schema (use included `CREATE TABLE` script)  
4. Import `online_sales.csv` using pgAdmin Import/Export (CSV, Header=Yes, Delimiter=`,`)  
5. Run queries from `queries.sql` in pgAdmin Query Tool  
6. Export results as CSV or capture screenshots for reporting  

---
