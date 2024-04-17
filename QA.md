What are your risk areas? Identify and describe them.
Being unable to identify the values that are not unique in a table like full_visitor_id


QA Process:
Describe your QA process and include the SQL queries used to execute it.

1.	One of the observations made is that in the table for all_sessions , the column full_visitor_id must have some value that are not distinct from the SQL Queries done.

     a.	SELECT full_visitor_id FROM all_sessions Results = 15,134
     b.	SELECT COUNT( DISTINCT full_visitor_id) FROM all_sessions Results 14,223
  	

3.	I did a filter on date to ensure that the date range is within the specified range.

    a.	SELECT date FROM analytics WHERE date  BETWEEN  '20170601' AND '20170701'
