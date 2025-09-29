# plsql-window-functions-BAHATI-Arsene
SQL assignment using window functions for customer segmentation and sales analysis.
# Windows Functions Assignment (DBMS)

This repository contains the implementation of SQL window functions for a business scenario involving **sales transactions, customers, and products**.  
The project is structured step by step to meet assignment requirements, including problem definition, success criteria, schema design, queries, and insights.

---

##  Project Overview
- **Business Context:** A retail company wants to analyze sales performance across regions and customer segments.  
- **Data Challenge:** The company struggles to track top-performing products, customer segmentation, and sales growth over time.  
- **Expected Outcome:** Insights into customer behavior, product performance, and revenue trends using SQL window functions.

---

##  Success Criteria
The analysis addresses 5 measurable goals:
1. **Top 5 products per region/quarter** → `RANK()`
2. **Running monthly sales totals** → `SUM() OVER()`
3. **Month-over-month growth** → `LAG()/LEAD()`
4. **Customer quartiles** → `NTILE(4)`
5. **3-month moving averages** → `AVG() OVER()`

---

## Database Schema
Three related tables with foreign keys:
- **customers** → `(customer_id, name, region)`
- **products** → `(product_id, name, category)`
- **transactions** → `(transaction_id, customer_id, product_id, sale_date, amount)`

 ER diagram and SQL `CREATE TABLE` scripts are included in [`assignment1/`]

---

## Window Functions Implemented
1. **Ranking** → `ROW_NUMBER()`, `RANK()`, `DENSE_RANK()`, `PERCENT_RANK()`  
   *Use case:* Top N customers by revenue  

2. **Aggregate** → `SUM()`, `AVG()`, `MIN()`, `MAX()` with `ROWS` vs `RANGE`  
   *Use case:* Running totals & sales trends  

3. **Navigation** → `LAG()`, `LEAD()`  
   *Use case:* Month-over-month growth analysis  

4. **Distribution** → `NTILE(4)`, `CUME_DIST()`  
   *Use case:* Customer segmentation by spending level  

 SQL scripts available in the word document located [`sql/step4_queries.sql`](assignemnt1/). 
 Screenshots of results are in the [`screenshots/`](screenshoot/) folder.

---

##  Sample File Structure
