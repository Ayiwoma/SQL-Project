Question 1: What is the ratio to total order from sales report?

SQL Queries: 

SELECT Round(ratio, 2) as ratio, 

total_order FROM sales_report

ORDER BY total_order DESC

Limit 10

Answer: 
This shows the ratio to total_order from sales_report.

Looking at this table shows more quantities ordered did not have an effect on ratio of sales.

sample size of 10

Results

|ratio              |total_order|
|-------------------|-----------|
|0.22               |456        |
|0.24               |334        |
|0.06               |319        |
|0.06               |290        |
|0.06               |253        |
|0.71               |250        |
|0.46               |189        |
|0.59               |167        |
|0.02               |146        |
|0.02               |112        |






Question 2: What is the restocking lead time for each product?

SQL Queries: 

  SELECT  name,  
  
          stock_level, 
          
          restocking_lead_time 
          
  FROM products

  ORDER BY name, 
  
          restocking_lead_time DESC

Answer:
This shows the restocking lead time for each product.

The table shows the stock level for each product did not affect the restocking lead time

sample size of 10


|name                                               |stock_level|restocking_lead_time|
|---------------------------------------------------|-----------|--------------------|
|PC gaming speakers                                 |100        |1                   |
| Women's Colorblock Tee White                      |0          |8                   |
| Men's Quilted Insulated Vest Black                |32         |8                   |
| Women's Scoop Neck Tee Black                      |73         |6                   |
| Bongo Cupholder Bluetooth Speaker                 |115        |8                   |
|Aluminum Handy Emergency Flashlight                |90         |9                   |
| Men's Short Sleeve Hero Tee Charcoal              |104        |12                  |
| Women's Short Sleeve Tri-blend Badge Tee Grey     |33         |15                  |
| Sunglasses                                        |2086       |6                   |
|Red Shine 15 oz Mug                                |1417       |20                  |
|Recycled Paper Journal Set                         |740        |5                   |
| Women's Scoop Neck Tee Black                      |154        |5                   |
| Onesie Green                                      |9          |5                   |
| Learning Thermostat 3rd Gen-USA - White           |1142       |5                   |
|Android Stretch Fit Hat                            |8          |5                   |
| Men's Quilted Insulated Vest Battleship Grey      |39         |5                   |
| Dress Socks                                       |20         |6                   |
|Ballpoint Stylus Pen                               |0          |6                   |
| Women's Fleece Hoodie Black                       |0          |6                   |
|22 oz  Bottle Infuser                              |1944       |7                   |




Question 3: Show unique page title from all sessions and time spent on site?

SQL Queries: 

SELECT  DISTINCT(page_title), 

        Coalesce(To_Timestamp(time_on_site)) time 

FROM all_sessions

WHERE page_title IS NOT NULL 

       AND time_on_site IS NOT NULL
      
ORDER by time 

limit 10


Answer: 
This shows the time visited on each page title from all_sessions

sample size of 10

RESULTS

|page_title                                         |time |
|---------------------------------------------------|-----|
|Google &#124; Shop by Brand &#124; Google Merchandise Store  |1969-12-31 18:00:01-06|
|YouTube &#124; Shop by Brand &#124; Google Merchandise Store |1969-12-31 18:00:01-06|
|The Google Merchandise Store/Google G Noise-reducing Bluetooth Headphones|1969-12-31 18:00:01-06|
|YouTube Custom Decals                              |1969-12-31 18:00:01-06|
|Women's T-Shirts &#124; Apparel &#124; Google Merchandise Store|1969-12-31 18:00:01-06|
|Electronics &#124; Google Merchandise Store             |1969-12-31 18:00:01-06|
|Electronics                                        |1969-12-31 18:00:01-06|
|Office                                             |1969-12-31 18:00:01-06|
|Women's T-Shirts &#124; Apparel &#124; Google Merchandise Store|1969-12-31 18:00:02-06|
|Electronics &#124; Google Merchandise Store             |1969-12-31 18:00:02-06|







Question 4: 

SQL Queries:

Answer:



Question 5: 

SQL Queries:

Answer:
