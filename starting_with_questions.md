Answer the following questions and provide the SQL queries used to find the answer.

    
**Question 1: Which cities and countries have the highest level of transaction revenues on the site?**

SQL Queries:

```SELECT  city,   

	SUM(product_quantity * product_price) AS total_revenue

FROM all_sessions

WHERE (product_quantity * product_price) IS NOT NULL

GROUP BY city

ORDER BY SUM(product_quantity * product_price) DESC

LIMIT 10```


Answer:
Results by cities

|city                         |total_revenue|
|-----------------------------|-------------|
|not available in demo dataset|2388720000   |
|Mountain View                |785970000    |
|Salem                        |639360000    |
|New York                     |590560000    |
|Sunnyvale                    |318000000    |
|San Francisco                |268000000    |
|San Jose                     |199000000    |
|Palo Alto                    |149000000    |
|Seattle                      |119000000    |
|Dublin                       |99990000     |



SQL queries

```SELECT  country,   

	SUM(product_quantity * product_price) AS total_revenue

FROM all_sessions

WHERE (product_quantity * product_price) IS NOT NULL

GROUP BY country

ORDER BY SUM(product_quantity * product_price) DESC

LIMIT 10```

Result by countries

|country                      |total_revenue|
|-----------------------------|-------------|
|United States                |5435730000   |
|Argentina                    |99990000     |
|Ireland                      |99990000     |
|Spain                        |89900000     |
|Canada                       |47970000     |
|France                       |17490000     |
|Colombia                     |16990000     |
|India                        |16990000     |
|Mexico                       |16990000     |
|Finland                      |1990000      |



**Question 2: What is the average number of products ordered from visitors in each city and country?**


SQL Queries:

```SELECT  al.city,   

	ROUND(AVG(p.ordered_quantity), 2) AS average_quantity_ordered

FROM    all_sessions al

JOIN 

    	products p 
    
    	ON al.product_sku = p."SKU"
    
GROUP BY  al.city

ORDER BY  al.city

LIMIT 10```

Answer:
This query generates the average quantity ordered per city, followed by country. 

Results for city

|city                         |average_quantity_ordered|
|-----------------------------|------------------------|
|(not set)                    |620.19                  |
|Adelaide                     |54.00                   |
|Ahmedabad                    |364.64                  |
|Akron                        |15.00                   |
|Amsterdam                    |355.64                  |
|Ann Arbor                    |290.56                  |
|Antalya                      |0.00                    |
|Antwerp                      |134.50                  |
|Appleton                     |66.00                   |
|Ashburn                      |187.50                  |





Results for country
SQL Queries

```SELECT  al.country,

	ROUND(AVG(p.ordered_quantity),2)
 
	AS average_quantity_ordered	
 
FROM    all_sessions al

JOIN 

    	products p ON al.product_sku = p."SKU"
    
GROUP BY  al.country

ORDER BY  al.country

LIMIT 10```

|country                      |average_quantity_ordered|
|-----------------------------|------------------------|
|(not set)                    |520.61                  |
|Albania                      |510.33                  |
|Algeria                      |720.50                  |
|Argentina                    |460.03                  |
|Armenia                      |1351.00                 |
|Australia                    |520.92                  |
|Austria                      |319.09                  |
|Bahamas                      |498.00                  |
|Bahrain                      |226.33                  |
|Bangladesh                   |242.74                  |




**Question 3: Is there any pattern in the types (product categories) of products ordered from visitors in each city and country?**


SQL Queries:

```SELECT  v2_product_category, 

	al.city,  
 
 	MAX(ordered_quantity) AS orderedquantity
  
FROM     all_sessions al

JOIN     products p
	ON al.product_sku = p."SKU"
 
GROUP BY v2_product_category, al.city

ORDER BY MAX(ordered_quantity) DESC

LIMIT 10```

Answer:
The pattern shows that most products are ordered from the Home/Accessories/Fun from visitors to a city, which is the same as to a country too.


Results for cities

|v2_product_category          |city      |orderedquantity|
|-----------------------------|----------|---------------|
|Home/Accessories/Fun/        |Kirkland  |15170          |
|Home/Accessories/Fun/        |Mountain View|15170          |
|Home/Lifestyle/              |Mountain View|15170          |
|Home/Accessories/Fun/        |Minato    |15170          |
|Home/Lifestyle/              |Santiago  |15170          |
|Home/Accessories/Sports & Fitness/|Mountain View|15170          |
|Home/Accessories/Fun/        |(not set) |15170          |
|Home/Accessories/Fun/        |not available in demo dataset|15170          |
|Home/Accessories/Fun/        |Sunnyvale |15170          |
|Home/Accessories/Fun/        |Los Angeles|15170          |


Results by country

SQL Queries

```SELECT  v2_product_category, 

	al.country,  
 
 	MAX(ordered_quantity) AS orderedquantity
  
FROM    all_sessions al

JOIN    products p
	ON al.product_sku = p."SKU"
 
GROUP BY v2_product_category, al.country

ORDER BY MAX(ordered_quantity) DESC

LIMIT 10```

|v2_product_category          |country   |orderedquantity|
|-----------------------------|----------|---------------|
|Home/Accessories/Sports & Fitness/|United States|15170          |
|Home/Accessories/Fun/        |Taiwan    |15170          |
|Home/Accessories/Fun/        |United States|15170          |
|Home/Accessories/Fun/        |Portugal  |15170          |
|Home/Accessories/Fun/        |Japan     |15170          |
|Home/Accessories/Sports & Fitness/|Russia    |15170          |
|Home/Lifestyle/              |Chile     |15170          |
|(not set)                    |United States|15170          |
|Home/Lifestyle/              |United States|15170          |
|Home/Accessories/Fun/        |United Kingdom|15170          |




**Question 4: What is the top-selling product from each city/country? Can we find any pattern worthy of noting in the products sold?**


SQL Queries:

```SELECT   v2_product_name,

	 al.city, 
 
 	 SUM(product_quantity * product_price) AS top_selling_product
  
FROM     all_sessions al

JOIN     products p

	ON al.product_sku = p."SKU"

WHERE    (product_quantity * product_price) IS NOT NULL

GROUP BY v2_product_name,  
	
 	 al.city 

ORDER BY SUM(product_quantity * product_price) DESC 
	
 
LIMIT 5```


Answer:
Red Spiral Google Notebook is one of the top selling product in the city of Salem.
Nest Cam outdoor Security Camera - USA is the top selling product in the USA for country.

Results by city

|v2_product_name              |city      |top_selling_product|
|-----------------------------|----------|-------------------|
|Nest® Cam Outdoor Security Camera - USA|not available in demo dataset|796000000          |
|Leatherette Journal          |not available in demo dataset|714350000          |
|Red Spiral Google Notebook   |Salem     |639360000          |
|Nest® Learning Thermostat 3rd Gen-USA - Stainless Steel|Mountain View|398000000          |
|Nest® Learning Thermostat 3rd Gen-USA - Stainless Steel|New York  |249000000          |



Results for country

```SELECT  v2_product_name,

	al.country, 
 
 	SUM(product_quantity * product_price) AS top_selling_product
  
FROM    all_sessions al

JOIN    products p
		
	ON al.product_sku = p."SKU"

WHERE   (product_quantity * product_price) IS NOT NULL

GROUP BY v2_product_name,  
	
 	al.country

ORDER by  SUM(product_quantity * product_price) DESC 

LIMIT 5```




|v2_product_name              |country   |top_selling_product|
|-----------------------------|----------|-------------------|
|Nest® Cam Outdoor Security Camera - USA|United States|1114000000         |
|Nest® Learning Thermostat 3rd Gen-USA - Stainless Steel|United States|945000000          |
|Leatherette Journal          |United States|714350000          |
|Red Spiral Google Notebook   |United States|639360000          |
|Nest® Cam Indoor Security Camera - USA|United States|556000000          |





**Question 5: Can we summarize the impact of revenue generated from each city/country?**

```SELECT    city,
 
	  SUM(al.product_price * al.product_quantity) as revenue, 
   
   	  sentiment_score

	
 
FROM 	  products p

FULL OUTER JOIN all_sessions al 

	ON "SKU" = full_visitor_id
	
WHERE    (al.product_price * al.product_quantity) IS NOT NULL 
	
	
 
Group BY  city, sentiment_score 

	
ORDER BY SUM(al.product_price * al.product_quantity) DESC

LIMIT 10```

Answer:

The result from the query shows the cities/countries that had the most impact on revenue.

Results

For cities

|city                         |revenue   |sentiment_score|
|-----------------------------|----------|---------------|
|not available in demo dataset|2388720000|               |
|Mountain View                |785970000 |               |
|Salem                        |639360000 |               |
|New York                     |590560000 |               |
|Sunnyvale                    |318000000 |               |
|San Francisco                |268000000 |               |
|San Jose                     |199000000 |               |
|Palo Alto                    |149000000 |               |
|Seattle                      |119000000 |               |
|Dublin                       |99990000  |               |


For countries

```SELECT    country,
 
	SUM(al.product_price * al.product_quantity) as revenue, sentiment_score

	
 
FROM 	products p

FULL OUTER JOIN all_sessions al 

	ON "SKU" = full_visitor_id
	
	WHERE  (al.product_price * al.product_quantity) IS NOT NULL 
	
	
 
Group by  country, sentiment_score 

	
ORDER BY SUM(al.product_price * al.product_quantity) DESC

LIMIT 10```

|country                      |revenue   |sentiment_score|
|-----------------------------|----------|---------------|
|United States                |5435730000|               |
|Argentina                    |99990000  |               |
|Ireland                      |99990000  |               |
|Spain                        |89900000  |               |
|Canada                       |47970000  |               |
|France                       |17490000  |               |
|Colombia                     |16990000  |               |
|Mexico                       |16990000  |               |
|India                        |16990000  |               |
|Finland                      |1990000   |               |



