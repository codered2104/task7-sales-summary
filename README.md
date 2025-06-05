# Task 7 – Sales Summary Using Python & SQLite

## 📌 Objective

This task was part of a Data Analyst internship assignment. The goal was to:

- Connect Python with a SQLite database
- Run basic SQL queries to calculate total quantity and revenue per product
- Load results into pandas
- Plot a simple bar chart using matplotlib

---

## 🧰 Tools Used

- Python
- SQLite (via `sqlite3`)
- pandas
- matplotlib

---

## 📁 Files in this Repo

| File               | Description                                   |
|--------------------|-----------------------------------------------|
| `sales.csv`        | Source data (product, quantity, price)        |
| `sales_data.db`    | SQLite database with a `sales` table          |
| `sales_summary.py` | Python script to load, query, and visualize   |
| `sales_chart.png`  | Bar chart of revenue per product              |
| `README.md`        | This explanation file                         |

---

## 📈 SQL Query Used

```sql
SELECT product, 
       SUM(quantity) AS total_qty, 
       SUM(quantity * price) AS revenue 
FROM sales 
GROUP BY product;
