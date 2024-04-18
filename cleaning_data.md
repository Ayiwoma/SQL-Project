What issues will you address by cleaning the data?



Queries:
Below, provide the SQL queries you used to clean your data.

1. Modifications done to city column in all_sessions table to fill in the empty spaces and input as Null

   SELECT NULLIF(city, ' ') AS city
   
   FROM all_sessions;
   
  Result 
  
|city               |
|-------------------|
|(not set)          |
|not available in demo dataset|
|not available in demo dataset|
|not available in demo dataset|
|London             |
|(not set)          |
|not available in demo dataset|
|not available in demo dataset|
|not available in demo dataset|
|Sydney             |
|Philadelphia       |





   
2 Modifications done to time column in all_sessions table to change the datatype to show as timestamp

   
   SELECT CAST(TO_TIMESTAMP(time) AS time) 
   
   FROM all_sessions

   Result 

|to_timestamp       |
|-------------------|
|03:56:53           |
|20:42:27           |
|11:03:22           |
|20:24:15           |
|18:00:00           |
|01:07:47           |
|22:05:37           |
|04:21:26           |
|20:27:40           |
|04:56:33           |
|18:00:00           |
|18:00:00           |
|18:00:00           |
|11:53:10           |



3. Modifications done to ecommerce_action_option to fill empty columns

   Filled the empty columns for ecommerce_action_option with null value

   SELECT NULLIF(ecommerce_action_option, ' ') AS ecommerceoptions

   FROM all_sessions;

Result 

|ecommerceoptions   |
|-------------------|
|NULL               |
|NULL               |
|NULL               |
|NULL               |
|NULL               |
|NULL               |
|NULL               |
|NULL               |
|Billing and Shipping|
