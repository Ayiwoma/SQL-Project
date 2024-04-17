What issues will you address by cleaning the data?

1.	Modifications done to city column in all_sessions table to fill in the empty spaces and input as Null

2.  Modifications done to time column in all_sessions table to change the datatype to show as timestamp


Queries:
Below, provide the SQL queries you used to clean your data.

1. SELECT NULLIF(city, ' ') AS city FROM all_sessions;
   
![image](https://github.com/Ayiwoma/SQL-Project/assets/141646278/a4b6ef7b-2354-4c88-8d29-cd80d1ec702a)

2. SELECT CAST(TO_TIMESTAMP(time) AS time) FROM all_sessions

   ![image](https://github.com/Ayiwoma/SQL-Project/assets/141646278/14e1ebca-2ddd-4cc0-8ec5-44370cf2e329)

