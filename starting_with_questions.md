Answer the following questions and provide the SQL queries used to find the answer.

    
**Question 1: Which cities and countries have the highest level of transaction revenues on the site?**

SQL Queries: 
SELECT city, country, MAX(total_transaction_revenue) AS highest_transaction_level
FROM all_sessions
GROUP BY city, country
ORDER BY MAX(total_transaction_revenue) ASC
LIMIT 10

Answer:
Top city –San Bruno 
top country – United States
the results were limited to ten to show the city/country with the highest level of transactions.


**Question 2: What is the average number of products ordered from visitors in each city and country?**


SQL Queries:
SELECT     al.city,     al.country,         AVG(p.ordered_quantity) AS average_quantity_ordered
FROM     all_sessions al
JOIN 
    products p ON al.product_sku = p."SKU"
GROUP BY     al.city,     al.country
ORDER BY al.city, al.country;


Answer:
This query generates the average quantity ordered per city, followed by country. An adjustment to the query can also generate average quantity ordered per country.


**Question 3: Is there any pattern in the types (product categories) of products ordered from visitors in each city and country?**


SQL Queries:
SELECT  v2_product_category, al.city,  al.country,   
    MAX(ordered_quantity) AS orderedquantity, al.full_visitor_id
FROM 
    all_sessions al
JOIN 
    products p ON al.product_sku = p."SKU"
GROUP BY 
v2_product_category, al.city, al.country, ordered_quantity,	al.full_visitor_id
ORDER BY ordered_quantity DESC

Answer:
The pattern shows that most products are ordered from the Home/Accessories/Fun from visitors to a city.




**Question 4: What is the top-selling product from each city/country? Can we find any pattern worthy of noting in the products sold?**


SQL Queries:
SELECT 
    al.city, 
    al.country, 
	v2_product_name,
    COUNT(v2_product_name) AS top_selling_product
FROM 
    all_sessions al
JOIN 
    products p ON al.product_sku = p."SKU"
GROUP BY 
	v2_product_name,
    al.city, 
    al.country,
	v2_product_name
	ORDER by COUNT(v2_product_name) DESC;


Answer:
Google Men’s 100% Cotton Short Sleeve Hero Tee White is one of the top selling product and it shows a pattern of more Tee shirts sold as against other products.



**Question 5: Can we summarize the impact of revenue generated from each city/country?**

SQL Queries:
SELECT  city, country,   SUM(product_price * product_quantity) as revenue
From all_sessions
GROUP BY  city, country
order by revenue asc, city, country
limit 10

Answer:
The result from the query shows that the country with the most generated revenue is USA while the city with the most revenue was not revealed from this dataset. This shows that the company got most of his revenue from the USA.






