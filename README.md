##Task 7: Basic Sales Summary using SQLite and Python

##Objective
As part of the Data Analyst Internship, this task focused on extracting simple sales insights from an SQLite database using Python. The goal was to:
- Connect to a SQLite database
- Run SQL queries to summarize sales data
- Display results using `print()` and a basic bar chart

---

## Tools Used
- Python
- SQLite3
- Pandas
- Matplotlib

---

## Dataset
A small SQLite database (`sales_data.db`) was created with one table called `sales` having the following columns:
- `product` (TEXT): Product name
- `quantity` (INTEGER): Quantity sold
- `price` (REAL): Price per unit

---

##SQL Query Used
```sql
SELECT product, 
       SUM(quantity) AS total_quantity, 
       SUM(quantity * price) AS total_revenue
FROM sales
GROUP BY product;
