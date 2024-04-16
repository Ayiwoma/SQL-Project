Question 1: What is the ratio to total order from sales report?

SQL Queries: SELECT Round(ratio, 2) as ratio, total_order FROM sales_report
ORDER BY total_order DESC

Answer: This shows the ratio to total_order  from sales_repot



Question 2: What is the restocking lead time for each product?

SQL Queries: SELECT  name,  stock_level, restocking_lead_time FROM products

ORDER BY name,  restocking_lead_time DESC

Answer: This shows the restocking lead time for each product.



Question 3: Show unique page title from all sessions and time spent on site?

SQL Queries: SELECT  DISTINCT(page_title), time_on_site FROM all_sessions
WHERE page_title IS NOT NULL AND time_on_site IS NOT NULL


Answer: This shows the time spent on each page title from all_sessions



Question 4: 

SQL Queries:

Answer:



Question 5: 

SQL Queries:

Answer:
