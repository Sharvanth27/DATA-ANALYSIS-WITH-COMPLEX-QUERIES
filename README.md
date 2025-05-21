# DATA-ANALYSIS-WITH-COMPLEX-QUERIES

"COMPANY": CODTECH IT SOLUTIONS

"NAME": SHARVANTH BIJJARAPU

"INTERN ID": CT04DL1163 

"DOMAIN": SQL

"DURATION": 4 WEEKS

"MENTOR": NEELA SANTOSH

Task Description

The goal of this task is to utilize advanced SQL features—including window functions, subqueries, and Common Table Expressions (CTEs)—to analyze a simple sales table. These features help uncover sales trends, regional insights, and product performance patterns using concise yet powerful SQL queries.

All queries were executed using the online MySQL editor: www.onlinecompiler.com.


---

Steps and Files

File: analysis.sql

This SQL script performs the following operations:


---

1. Table Creation

Creates a table named sales with the following columns:

id (INT)

product (VARCHAR)

region (VARCHAR)

amount (INT)



2. Sample Data Insertion

Inserts five sample rows representing sales transactions involving different products and regions.

---

3. SQL Analysis Queries Demonstrated

a. Window Function: Total Sales by Region

Uses SUM(amount) OVER (PARTITION BY region)

Purpose: Calculates the total sales within each region without collapsing rows.

Insight: Identifies regional performance trends.

<img width="350" alt="Image" src="https://github.com/user-attachments/assets/0f667753-b41d-4771-958e-362e98b5dc43" />


b. Window Function: Product-wise Ranking

Uses ROW_NUMBER() OVER (PARTITION BY product ORDER BY amount DESC)

Purpose: Assigns a rank to each sale within a product category based on the sale amount (highest first).

Insight: Finds top-performing transactions per product.

<img width="351" alt="Image" src="https://github.com/user-attachments/assets/b3396b61-04bb-43fa-b7d9-5797fe7b3a5c" />


c. Common Table Expression (CTE): Above-Average Sales

Defines a CTE named avg_region to calculate the average sale amount per region.

Filters actual sales that exceed the average in their respective regions.

Insight: Highlights high-performing sales compared to regional averages.


d. Subquery: High-Volume Products

Uses a subquery to:

Aggregate total sales per product.

Filter and return only those products whose total sales exceed a given threshold.


Insight: Identifies best-selling products across all regions.
