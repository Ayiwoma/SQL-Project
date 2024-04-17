What issues will you address by cleaning the data?

1.	Modifications done to city column in all_sessions table to fill in the empty spaces and input as Null

2.  Modifications done to time column in all_sessions table to change the datatype to show as timestamp

3.  Modifications done to ecommerce_action_option to fill empty columns


Queries:
Below, provide the SQL queries you used to clean your data.

1. SELECT NULLIF(city, ' ') AS city FROM all_sessions;
   
  Result 
  
||
||


   


3. SELECT CAST(TO_TIMESTAMP(time) AS time) FROM all_sessions

   Result 

||
||

3. Filled the empty columns for ecommerce_action_option with null value

Result 

||
||
