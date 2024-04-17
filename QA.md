What are your risk areas? Identify and describe them.
Being unable to identify the values that are not unique in a table like full_visitor_id


QA Process:
Describe your QA process and include the SQL queries used to execute it.

1.	One of the observations made is that in the table for all_sessions , the column full_visitor_id must have some value that are not distinct from the SQL Queries done.

     a.	SELECT full_visitor_id FROM all_sessions
  	      Results = 15,134

     ![image](https://github.com/Ayiwoma/SQL-Project/assets/141646278/b3c0d020-9a4c-4870-a878-14ce130302e3)

     b.	SELECT COUNT( DISTINCT full_visitor_id) FROM all_sessions
  	      Results 14,223
  	
  	![image](https://github.com/Ayiwoma/SQL-Project/assets/141646278/b5c73bcf-cd19-4528-9231-c9a528cfd7df)


2.	I did a filter on date to ensure that the date range is within the specified range.

    a.	SELECT date FROM analytics WHERE date  BETWEEN  '20170601' AND '20170701'

     ![image](https://github.com/Ayiwoma/SQL-Project/assets/141646278/df5e802e-6632-49c2-aa27-66fbdd19ee3b)
