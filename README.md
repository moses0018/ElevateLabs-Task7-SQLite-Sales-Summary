# Task 7: Basic Sales Summary Using SQLite & Python

This repository contains the solution for **Task 7** of the Elevate Labs Internship Program.  
The goal is to create a small SQLite database, run SQL queries inside Python, and visualize simple sales insights.

---

## 📌 Objective
- Create a tiny SQLite database (`sales_data.db`)
- Insert sample sales data
- Use Python to connect to SQLite
- Run SQL queries to compute:
  - Total quantity sold per product
  - Total revenue per product
- Display results using `print()` and a bar chart

---

## 🛠 Tools & Libraries Used
- **Python**
- **SQLite (sqlite3 module)**
- **Pandas**
- **Matplotlib**

---

## 📂 Project Files
| File | Description |
|------|-------------|
| `task7_create_db.py` | Creates the SQLite database and inserts sample data |
| `task7_sales_summary.py` | Connects to database, runs SQL, prints results, generates bar chart |
| `sales_data.db` | SQLite database containing the `sales` table |
| `sales_chart.png` | Bar chart showing revenue per product |
| `README.md` | Documentation for Task 7 |

---

## 🧱 Database Schema

### `sales` table:
| Column | Type | Description |
|--------|------|-------------|
| id | INTEGER PRIMARY KEY | Auto-increment |
| product | TEXT | Product name |
| quantity | INTEGER | Quantity sold |
| price | REAL | Unit price |

---

## 🧮 SQL Query Used

```sql
SELECT 
    product, 
    SUM(quantity) AS total_qty, 
    SUM(quantity * price) AS revenue
FROM sales
GROUP BY product;


 Output
✔ Printed Output 
     product  total_qty   revenue
0     Laptop          8  480000.0
1      Mouse         20   10000.0
2   Keyboard         10   15000.0
3    Monitor          6   72000.0
