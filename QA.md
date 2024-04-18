What are your risk areas? Identify and describe them.
Being unable to identify the values that are not unique in a table like full_visitor_id


QA Process:
Describe your QA process and include the SQL queries used to execute it.

1.	One of the observations made is that in the table for all_sessions , the column full_visitor_id must have some value that are not distinct from the SQL Queries done.

     a.	SELECT full_visitor_id FROM all_sessions
  	      Results = 15,134

|full_visitor_id    |
|-------------------|
|2817722496551184128|
|6938960486452471698|
|5307554331754279093|
|5256949873742090146|
|7549308697995967647|
|5444913961890272648|
|914760062456295531 |
|4476811245637991248|
|5153038635419747224|
|0719635766852234475|



     
     b.	SELECT COUNT( DISTINCT full_visitor_id) FROM all_sessions
  	      Results 14,223

   Results

   |count                                         |
|----------------------------------------------|
|14223                                         |

  


3.	I did a filter on v2_product_name to test case sensitive search.

SQL Queries
     SELECT v2_product_name
     FROM all_sessions
     WHERE v2_product_name LIKE 'Google%'
     LIMIT 10

     Results

     |v2_product_name                               |
|----------------------------------------------|
|Google 22 oz Water Bottle                     |
|Google Women's Convertible Vest-Jacket Sea Foam Green|
|Google Wool Heather Cap Heather/Navy          |
|Google Bluetooth Speaker-Power Bank           |
|Google Women's 1/4 Zip Jacket Charcoal        |
|Google Men's 100% Cotton Short Sleeve Hero Tee Navy|
|Google Infant Zip Hood Royal Blue             |
|Google Men's Vintage Tank                     |
|Google Heavyweight Long Sleeve Hero Tee Navy  |
|Google Bib White                              |


  


4. Combined multiple tables to get results for the column full_visitor_id

 SQL Queries
 SELECT DISTINCT al.full_visitor_id
FROM all_sessions al
JOIN analytics an USING (full_visitor_id)

|full_visitor_id                               |
|----------------------------------------------|
|5050299044657579745                           |
|1382031825972533734                           |
|8505858323470957238                           |
|2304081328443448245                           |
|7144024074762786741                           |
|7861840397776577591                           |
|4215347458239853405                           |
|9018043587410138353                           |
|0385264926912597060                           |
|3021691607631354046                           |
|3378915086342051274                           |




