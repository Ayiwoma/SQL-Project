What issues will you address by cleaning the data?

1.	Modifications done to city column in all_sessions table to fill in the empty spaces and input as Null

2.  Modifications done to time column in all_sessions table to change the datatype to show as timestamp


Queries:
Below, provide the SQL queries you used to clean your data.

1. SELECT NULLIF(city, ‘ ‘) AS city FROM all_sessions;

2. SELECT CAST(TO_TIMESTAMP(time) AS time) FROM all_sessions
