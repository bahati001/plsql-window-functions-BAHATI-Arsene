# PL/SQL Window Functions Assignment

This repository contains my assignment on using SQL window functions to analyze sales and customer data.  
The project follows the given steps: defining a problem, success criteria, schema design, implementation of queries, analysis of results, GitHub organization, and references.

---

## Step 1: Problem Definition (2 pts)

**Business Context**  
A retail company sells different products such as beverages, groceries, and household items. The sales department wants to measure performance by region and identify which customers and products contribute most to revenue.  

**Data Challenge**  
Managers cannot easily tell which products sell best in each region, which customers are high value, and how sales change from one month to another. Customer segmentation is also missing.  

**Expected Outcome**  
The company expects to use SQL window functions to:  
- Rank top products and customers,  
- Track sales trends over time, and  
- Segment customers into spending categories.  

---

## Step 2: Success Criteria (2 pts)

The analysis is considered successful if it produces the following measurable results:

1. **Top 5 products per region and quarter** → using `RANK()`.  
2. **Running monthly sales totals** → using `SUM() OVER()`.  
3. **Month-over-month growth** → using `LAG()` and `LEAD()`.  
4. **Customer quartiles** → using `NTILE(4)`.  
5. **3-month moving averages** → using `AVG() OVER()`.  

---

## Step 3: Database Schema (2 pts)

Three related tables were designed:

- **customers** → `(customer_id, name, region)`  
- **products** → `(product_id, name, category)`  
- **transactions** → `(transaction_id, customer_id, product_id, sale_date, amount)`  


## Step 4: Window Functions Implementation (4 pts)

Queries for all categories are included in [`sql/step4_queries.sql`](assignment1/).  

- **Ranking** (`ROW_NUMBER`, `RANK`, `DENSE_RANK`, `PERCENT_RANK`) → Top customers by revenue.  
- **Aggregate** (`SUM`, `AVG`, `MIN`, `MAX` with ROWS vs RANGE) → Running totals and moving averages.  
- **Navigation** (`LAG`, `LEAD`) → Month-over-month growth.  
- **Distribution** (`NTILE`, `CUME_DIST`) → Customer segmentation.  

Screenshots of outputs are stored in the [`screenshots/`](screenshoot/) folder.  

---

## Step 5: GitHub Repository (1.5 pts)

- **Repo Name:** `plsql-window-functions-[lastname]-[firstname]`  
- **Visibility:** Public  
- **Contents:**  
  - `sql/` → schema, data, and queries  
  - `docs/` → assignment write-up  
  - `screenshots/` → result images  
  - `README.md` → project overview  

---

## Step 6: Results Analysis (2 pts)

**Descriptive – What happened?**  
Certain products, especially beverages, ranked top in sales. Monthly totals revealed steady growth in some quarters, with a few noticeable dips. Customer quartiles showed that a small group of customers generated most of the revenue.  

**Diagnostic – Why?**  
Seasonal demand, stock levels, and regional preferences likely explain product performance. Sales dips may be tied to supply shortages or off-season months. Customer imbalance shows dependence on a few loyal buyers.  

**Prescriptive – What next?**  
The company should focus on rewarding high-spending customers and design promotions to encourage growth in lower quartiles. Stock management should prepare for seasonal peaks, and top products should receive priority in marketing.  

---

## Step 7: References (0.5 pts)

1. Oracle. *Analytic Functions Documentation*. [https://docs.oracle.com](https://docs.oracle.com)  
2. PostgreSQL. *Window Functions Tutorial*. [https://www.postgresql.org/docs/current/tutorial-window.html](https://www.postgresql.org/docs/current/tutorial-window.html)  
3. MySQL. *Window Functions*. [https://dev.mysql.com/doc/refman/8.0/en/window-functions.html](https://dev.mysql.com/doc/refman/8.0/en/window-functions.html)  
4. Microsoft SQL Server. *Ranking Functions (T-SQL)*. [https://learn.microsoft.com/sql/t-sql/functions/ranking-functions-transact-sql](https://learn.microsoft.com/sql/t-sql/functions/ranking-functions-transact-sql)  
5. W3Schools. *SQL Window Functions*. [https://www.w3schools.com/sql/sql_window.asp](https://www.w3schools.com/sql/sql_window.asp)  
6. GeeksforGeeks. *Window Functions in SQL*. [https://www.geeksforgeeks.org/window-functions-in-sql/](https://www.geeksforgeeks.org/window-functions-in-sql/)  
7. Khan Academy. *Intro to SQL*. [https://www.khanacademy.org/computing/computer-programming/sql](https://www.khanacademy.org/computing/computer-programming/sql)  
8. Stack Overflow. *SQL Window Functions Q&A*. [https://stackoverflow.com/questions/tagged/sql-window-functions](https://stackoverflow.com/questions/tagged/sql-window-functions)  
9. IBM. *SQL Reference: OLAP and Window Functions*. [https://www.ibm.com/docs](https://www.ibm.com/docs)  
10. ResearchGate. *Using SQL Window Functions for Business Analytics*. [https://www.researchgate.net](https://www.researchgate.net)  

 
