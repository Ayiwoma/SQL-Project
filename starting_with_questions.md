Answer the following questions and provide the SQL queries used to find the answer.

    
**Question 1: Which cities and countries have the highest level of transaction revenues on the site?**

SQL Queries: 
SELECT city, SUM(product_quantity * product_price) AS total_revenue
FROM all_sessions 
GROUP BY city
ORDER BY SUM(product_quantity * product_price) 

Answer:
Results by cities

|city                                               |total_revenue|                                                         
|---------------------------------------------------|-------------|
|Chicago                                            |2800000      |
|Detroit                                            |2990000      |
|Dallas                                             |6990000      |
|Houston                                            |7000000      |
|Bengaluru                                          |16990000     |
|Ann Arbor                                          |18990000     |
|Columbus                                           |18990000     |
|(not set)                                          |24990000     |
|Atlanta                                            |44800000     |
|Los Angeles                                        |51990000     |
|Madrid                                             |89900000     |
|Dublin                                             |99990000     |
|Seattle                                            |119000000    |
|Palo Alto                                          |149000000    |
|San Jose                                           |199000000    |
|San Francisco                                      |268000000    |
|Sunnyvale                                          |318000000    |
|New York                                           |590560000    |
|Salem                                              |639360000    |
|Mountain View                                      |785970000    |


SQL queries
SELECT country, SUM(product_quantity * product_price) AS total_revenue
FROM all_sessions 

GROUP BY country

ORDER BY SUM(product_quantity * product_price)

Result by countries

|country                                            |total_revenue|
|---------------------------------------------------|-------------|
|Finland                                            |1990000      |
|Colombia                                           |16990000     |
|Mexico                                             |16990000     |
|India                                              |16990000     |
|France                                             |17490000     |
|Canada                                             |47970000     |
|Spain                                              |89900000     |
|Ireland                                            |99990000     |
|Argentina                                          |99990000     |
|United States                                      |5435730000   |


**Question 2: What is the average number of products ordered from visitors in each city and country?**


SQL Queries:
SELECT     al.city,    ROUND(AVG(p.ordered_quantity), 2) AS average_quantity_ordered
FROM     all_sessions al
JOIN 
    products p ON al.product_sku = p."SKU"
GROUP BY     al.city
ORDER BY al.city; 

Answer:
This query generates the average quantity ordered per city, followed by country. 

Results for city

|city                                               |average_quantity_ordered|
|---------------------------------------------------|------------------------|
|(not set)                                          |620.19                  |
|Adelaide                                           |54.00                   |
|Ahmedabad                                          |364.64                  |
|Akron                                              |15.00                   |
|Amsterdam                                          |355.64                  |
|Ann Arbor                                          |290.56                  |
|Antalya                                            |0.00                    |
|Antwerp                                            |134.50                  |
|Appleton                                           |66.00                   |
|Ashburn                                            |187.50                  |
|Asuncion                                           |15.00                   |
|Athens                                             |1088.40                 |
|Atlanta                                            |483.09                  |
|Auckland                                           |52.00                   |
|Austin                                             |570.69                  |
|Avon                                               |330.50                  |
|Bandung                                            |53.00                   |
|Bangkok                                            |588.00                  |
|Barcelona                                          |241.53                  |




Results for country
SQL Queries

SELECT     al.country,    ROUND(AVG(p.ordered_quantity),2)
AS average_quantity_ordered								
FROM     all_sessions al
JOIN 
    products p ON al.product_sku = p."SKU"
GROUP BY     al.country
ORDER BY al.country; 

|country             |average_quantity_ordered|
|--------------------|------------------------|
|(not set)           |520.61                  |
|Albania             |510.33                  |
|Algeria             |720.50                  |
|Argentina           |460.03                  |
|Armenia             |1351.00                 |
|Australia           |520.92                  |
|Austria             |319.09                  |
|Bahamas             |498.00                  |
|Bahrain             |226.33                  |
|Bangladesh          |242.74                  |
|Barbados            |25.00                   |
|Belarus             |231.00                  |
|Belgium             |249.25                  |
|Bolivia             |90.00                   |
|Bosnia & Herzegovina|386.67                  |
|Botswana            |215.00                  |
|Brazil              |593.07                  |
|Brunei              |45.50                   |
|Bulgaria            |1231.73                 |
|Cambodia            |362.20                  |
|Canada              |494.81                  |
|Chile               |930.84                  |
|China               |219.32                  |



**Question 3: Is there any pattern in the types (product categories) of products ordered from visitors in each city and country?**


SQL Queries:
SELECT  v2_product_category, al.city,   MAX(ordered_quantity) AS orderedquantity
FROM     all_sessions al
JOIN     products p ON al.product_sku = p."SKU"
GROUP BY v2_product_category, al.city
ORDER BY MAX(ordered_quantity) DESC

Answer:
The pattern shows that most products are ordered from the Home/Accessories/Fun from visitors to a city, which is the same as to a country too.


Results for cities

|v2_product_category                           |city                         |orderedquantity|
|----------------------------------------------|-----------------------------|---------------|
|Home/Accessories/Fun/                         |Minato                       |15170          |
|Home/Accessories/Fun/                         |Dublin                       |15170          |
|Home/Accessories/Fun/                         |New York                     |15170          |
|Home/Accessories/Sports & Fitness/            |San Diego                    |15170          |
|Home/Accessories/Fun/                         |Los Angeles                  |15170          |
|Home/Lifestyle/                               |San Francisco                |15170          |
|Home/Accessories/Sports & Fitness/            |Santa Clara                  |15170          |
|Home/Accessories/Sports & Fitness/            |San Bruno                    |15170          |
|Home/Accessories/Sports & Fitness/            |Mountain View                |15170          |
|Home/Accessories/Fun/                         |Council Bluffs               |15170          |
|Home/Lifestyle/                               |Mountain View                |15170          |
|Home/Lifestyle/                               |not available in demo dataset|15170          |
|Home/Accessories/Fun/                         |not available in demo dataset|15170          |
|Home/Accessories/Fun/                         |Chicago                      |15170          |
|Home/Accessories/Sports & Fitness/            |Moscow                       |15170          |
|Home/Lifestyle/                               |Santiago                     |15170          |
|Home/Accessories/Fun/                         |(not set)                    |15170          |
|Home/Accessories/Fun/                         |Mountain View                |15170          |
|Home/Accessories/Fun/                         |Sunnyvale                    |15170          |
|Home/Accessories/Sports & Fitness/            |not available in demo dataset|15170          |
|Home/Accessories/Fun/                         |Kirkland                     |15170          |

Results by country





**Question 4: What is the top-selling product from each city/country? Can we find any pattern worthy of noting in the products sold?**


SQL Queries:
SELECT   v2_product_name, al.city, 
    SUM(product_quantity * product_price) AS top_selling_product
FROM     all_sessions al
JOIN     products p ON al.product_sku = p."SKU"
GROUP BY v2_product_name,  al.city 
ORDER by SUM(product_quantity * product_price),  v2_product_name 


Answer:
Red Spiral Google Notebook is one of the top selling product in the city of Salem.
Nest Cam outdoor Security Camera - USA is the top selling product in the USA for country.

Results by city
|v2_product_name                                          |city                         |top_selling_product|
|---------------------------------------------------------|-----------------------------|-------------------|
|Google Laptop and Cell Phone Stickers                    |not available in demo dataset|1990000            |
|Google Sunglasses                                        |Chicago                      |2800000            |
|Four Color Retractable Pen                               |not available in demo dataset|2990000            |
|Google 22 oz Water Bottle                                |Detroit                      |2990000            |
|Android Wool Heather Cap Heather/Black                   |(not set)                    |24990000           |
|Google Men's Long Sleeve Raglan Ocean Blue               |not available in demo dataset|24990000           |
|Google Men's 100% Cotton Short Sleeve Hero Tee White     |New York                     |30580000           |
|Google Men's Pullover Hoodie Grey                        |Los Angeles                  |51990000           |
|Google Men's  Zip Hoodie                                 |New York                     |55990000           |
|Google Bongo Cupholder Bluetooth Speaker                 |not available in demo dataset|59990000           |
|Google Women's Quilted Insulated Vest Black              |Mountain View                |74990000           |
|Nest® Protect Smoke + CO White Wired Alarm-USA           |not available in demo dataset|79000000           |
|Waze Dress Socks                                         |Madrid                       |89900000           |
|Google Women's Convertible Vest-Jacket Black             |Mountain View                |98990000           |
|Google Alpine Style Backpack                             |not available in demo dataset|99990000           |
|Google Laptop Backpack                                   |Dublin                       |99990000           |
|Nest® Cam Indoor Security Camera - USA                   |Seattle                      |119000000          |
|Nest® Cam Indoor Security Camera - USA                   |not available in demo dataset|119000000          |
|Nest® Cam Indoor Security Camera - USA                   |Sunnyvale                    |119000000          |
|Nest® Cam Outdoor Security Camera - USA                  |San Francisco                |119000000          |
|Nest® Protect Smoke + CO White Battery Alarm-USA         |Mountain View                |119000000          |
|Nest® Learning Thermostat 3rd Gen-USA - Stainless Steel  |Palo Alto                    |149000000          |
|Nest® Learning Thermostat 3rd Gen-USA - Stainless Steel  |not available in demo dataset|149000000          |
|Nest® Cam Indoor Security Camera - USA                   |San Jose                     |199000000          |
|Nest® Cam Outdoor Security Camera - USA                  |Sunnyvale                    |199000000          |
|Nest® Protect Smoke + CO White Wired Alarm-USA           |New York                     |238000000          |
|Nest® Learning Thermostat 3rd Gen-USA - Stainless Steel  |New York                     |249000000          |
|Nest® Learning Thermostat 3rd Gen-USA - Stainless Steel  |Mountain View                |398000000          |
|Red Spiral Google Notebook                               |Salem                        |639360000          |
|Leatherette Journal                                      |not available in demo dataset|714350000          |
|Nest® Cam Outdoor Security Camera - USA                  |not available in demo dataset|796000000          |



SELECT   v2_product_name, al.country, 
    SUM(product_quantity * product_price) AS top_selling_product
FROM 
    all_sessions al
JOIN 
    products p ON al.product_sku = p."SKU"
GROUP BY 
	v2_product_name, al.country 
   	ORDER by SUM(product_quantity * product_price),  v2_product_name 


Results for country 

|v2_product_name                               |country                      |top_selling_product|
|----------------------------------------------|-----------------------------|-------------------|
|Google Laptop and Cell Phone Stickers         |Finland                      |1990000            |
|Four Color Retractable Pen                    |United States                |2990000            |
|Google 22 oz Water Bottle                     |United States                |2990000            |
|YouTube Leatherette Notebook Combo            |United States                |6990000            |
|Google Sunglasses                             |United States                |9800000            |
|Google Twill Cap                              |United States                |10990000           |
|YouTube Twill Cap                             |Canada                       |10990000           |
|Google Men's Bike Short Sleeve Tee Charcoal   |United States                |15990000           |
|YouTube Men's Short Sleeve Hero Tee Black     |Colombia                     |16990000           |
|YouTube Men's Short Sleeve Hero Tee White     |United States                |16990000           |
|Android Wool Heather Cap Heather/Black        |France                       |17490000           |
|Google Men's Short Sleeve Badge Tee Charcoal  |United States                |18990000           |
|Nest® Protect Smoke + CO White Battery Alarm-USA|United States                |119000000          |
|Nest® Protect Smoke + CO White Wired Alarm-USA|United States                |317000000          |
|Nest® Cam Indoor Security Camera - USA        |United States                |556000000          |
|Red Spiral Google Notebook                    |United States                |639360000          |
|Leatherette Journal                           |United States                |714350000          |
|Nest® Learning Thermostat 3rd Gen-USA - Stainless Steel|United States                |945000000          |
|Nest® Cam Outdoor Security Camera - USA       |United States                |1114000000         |





**Question 5: Can we summarize the impact of revenue generated from each city/country?**

SELECT  sentiment_score, sentiment_magnitude,   
SUM(al.product_price * al.product_quantity) as revenue
FROM products p
FULL OUTER JOIN all_sessions al ON "SKU" = full_visitor_id
Group by sentiment_score, sentiment_magnitude
ORDER BY sentiment_score DESC

Answer:
The result from the query shows the relationship between sentiment score which shows postive impact of revenue to the sentiment magnitude which fluntuates between positive and negative

Results

|sentiment_score                               |sentiment_magnitude          |revenue|
|----------------------------------------------|-----------------------------|-------|
|NULL                                          |NULL                         |5844030000|
|1.0                                           |1.0                          |NULL   |
|0.9                                           |1.4                          |NULL   |
|0.9                                           |0.2                          |NULL   |
|0.9                                           |1.3                          |NULL   |
|0.9                                           |0.5                          |NULL   |
|0.8                                           |1.9                          |NULL   |
|0.8                                           |0.3                          |NULL   |
|0.8                                           |2.0                          |NULL   |
|0.8                                           |1.3                          |NULL   |
|0.8                                           |0.4                          |NULL   |




