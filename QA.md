What are your risk areas? Identify and describe them.
Being unable to identify the values that are not unique in a table like full_visitor_id


QA Process:
Describe your QA process and include the SQL queries used to execute it.

1.	One of the observations made is, in the table for all_sessions , the column full_visitor_id must have some value that are not distinct from the SQL Queries done.
   When the queries was done the results gotten was 15,134 rows as against when it was done with searching for unique values which brought about 14,223 rows.

   a.SQL Queries
   
  	```SELECT COUNT(full_visitor_id )
   
       FROM    all_sessions```

|count                        |
|-----------------------------|
|15134                        |




     
     b.	SQL Queries
     
     ```SELECT COUNT( DISTINCT full_visitor_id)
     
        FROM all_sessions```
     
  	  

   Results

   |count                        |
   |-----------------------------|
   |14223                        |


  


2.	I did a filter on v2_product_name to test case sensitive search, this was done to test the quality of the data to see if it could generate a name sensitive search, in doing so the results turned out to be           positive and consistent.

   

SQL Queries

     ```SELECT v2_product_name
     
     FROM all_sessions
     
     WHERE v2_product_name LIKE 'Google%'
     
     LIMIT 10```

     Results

|v2_product_name              |
|-----------------------------|
|Google 22 oz Water Bottle    |
|Google Women's Convertible Vest-Jacket Sea Foam Green|
|Google Wool Heather Cap Heather/Navy|
|Google Bluetooth Speaker-Power Bank|
|Google Women's 1/4 Zip Jacket Charcoal|
|Google Men's 100% Cotton Short Sleeve Hero Tee Navy|
|Google Infant Zip Hood Royal Blue|
|Google Men's Vintage Tank    |
|Google Heavyweight Long Sleeve Hero Tee Navy|
|Google Bib White             |



  


3. I decided to combined multiple tables to get results for the column full_visitor_id, to show the relationship between both tables and even though the data is in separate tables,
    there is obviouslt a relatiionship between them, which can be used to generate information and create a relationship.

 SQL Queries
 
```SELECT DISTINCT al.full_visitor_id

   FROM all_sessions al

   JOIN analytics an

   USING (full_visitor_id)

   LIMIT 10```

|full_visitor_id              |
|-----------------------------|
|5050299044657579745          |
|1382031825972533734          |
|8505858323470957238          |
|2304081328443448245          |
|7144024074762786741          |
|7861840397776577591          |
|4215347458239853405          |
|9018043587410138353          |
|0385264926912597060          |
|3021691607631354046          |





