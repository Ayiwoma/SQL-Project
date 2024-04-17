Question 1: What is the ratio to total order from sales report?

SQL Queries: 
SELECT Round(ratio, 2) as ratio, total_order FROM sales_report
ORDER BY total_order DESC
Limit 10

Answer: 
This shows the ratio to total_order from sales_report.
Looking at this bar chart shows more quantities ordered did not have an effect on ratio of sales.


![image](https://github.com/Ayiwoma/SQL-Project/assets/141646278/878e30c0-ccbc-44b8-8f6a-6b022c6db0e7)




Question 2: What is the restocking lead time for each product?

SQL Queries: 
SELECT  name,  stock_level, restocking_lead_time FROM products

ORDER BY name,  restocking_lead_time DESC

Answer:
This shows the restocking lead time for each product.
The picture show the stock level for each product did not affect the restocking lead time


![image](https://github.com/Ayiwoma/SQL-Project/assets/141646278/58e45a19-8877-4a13-86ac-65942da04cc4)



Question 3: Show unique page title from all sessions and time spent on site?

SQL Queries: 
SELECT  DISTINCT(page_title), Coalesce(To_Timestamp(time_on_site)) time FROM all_sessions
WHERE page_title IS NOT NULL AND time_on_site IS NOT NULL
ORDER by time 
limit 10


Answer: This shows the time visited on each page title from all_sessions
![image](https://github.com/Ayiwoma/SQL-Project/assets/141646278/dae7691b-0a09-4b36-a70f-3c611a58e414)





Question 4: 

SQL Queries:

Answer:



Question 5: 

SQL Queries:

Answer:
