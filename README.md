# Task 7: Basic Sales Summary using SQLite in Python

## Objective
To connect Python with SQLite, run basic SQL queries to get a sales summary, and visualize the revenue data using matplotlib.

## Tools Used
- Python
- SQLite (sqlite3)
- pandas
- matplotlib

## Dataset
Created a small SQLite database (`sales_data.db`) with a `sales` table containing product name, quantity, and price.

## Steps
1. Created `sales_data.db` and inserted sample sales data.
2. Connected to the database using `sqlite3`.
3. Ran an SQL query to group data by product, calculating total quantity and total revenue.
4. Loaded data into a pandas DataFrame.
5. Displayed results using `print`.
6. Visualized revenue per product with a bar chart using matplotlib.

## Output

Bar chart saved as `sales_chart.png`.

## Sample SQL Query Used

```sql
SELECT product, 
       SUM(quantity) AS total_qty, 
       SUM(quantity * price) AS revenue 
FROM sales 
GROUP BY product
