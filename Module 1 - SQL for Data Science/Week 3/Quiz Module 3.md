## Module 3 Quiz
> 
> Latest Submission Grade
> 
> 100%
> 
> 1.
> 
> Question 1
> 
> Which of the following statements is true regarding subqueries?
> 
> 1 / 1 point
> 

      Subqueries always process the innermost query first and the work outward. 
> 
>  Subqueries will process whichever query you indicate for them to process first. 
> 
>  Subqueries always process the outermost query first and the work inward. 
> 
> Check
> 
> Correct
> 
> See the videos on subqueries in the module for more information.
> 
> 2.
> 
> Question 2
> 
> If you can accomplish the same outcome with a join or a subquery, which one should you always choose?
> 
> 1 / 1 point
> 
>  Whichever one you understand better and can write faster. 
> 

      Joins are usually faster, but subqueries can be more reliable, so it depends on your situation. 
> 
>  A subquery because they are always faster 
> 
>  A join because they are always faster 
> 
> Check
> 
> Correct
> 
> See the videos on subqueries in the module for more information.
> 
> 3.
> 
> Question 3
> 
> The following diagram is a depiction of what type of join?
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/N-PGlJTnEeeRmQ5TE1Qolg_46d2d731eb8af88a9b719147019ad72f_Screen-Shot-2017-09-08-at-3.43.46-PM.png?expiry=1599350400000&hmac=hRRLbzrLF9qP1k2zDVklSsPuBtuU68G46JFAScQ0WSs)
> 
> 1 / 1 point
> 
>  Left Join 
> 
>  Right Join 
> 
>  Full Outer Join 
> 

      Inner Join 
> 
> Check
> 
> Correct
> 
> See the videos entitled, "Inner Joins" and "Advanced Joins" for more information.
> 
> 4.
> 
> Question 4
> 
> Select which of the following statements are true regarding inner joins. (Select all that apply)
> 
> 1 / 1 point
> 
>  Inner joins retrieve all matching and nonmatching rows from a table 
> 

      Inner joins are one of the most popular types of joins use 
> 
> Check
> 
> Correct
> 
> See the video entitled, "Inner Joins" for more information.
> 

      Performance will most likely worsen with the more joins you make 
> 
> Check
> 
> Correct
> 
> See the video entitled, "Inner Joins" for more information.
> 

      There is no limit to the number of table you can join with an inner join. 
> 
> Check
> 
> Correct
> 
> See the video entitled, "Inner Joins" for more information.
> 
> 5.
> 
> Question 5
> 
> Which of the following is true regarding Aliases? (Select all that apply.)
> 
> 1 / 1 point
> 

      SQL aliases are used to give a table, or a column in a table, a temporary name. 
> 
> Check
> 
> Correct
> 
> See the video entitled, "Aliases and Self Joins" for more information.
> 

      Aliases are often used to make column names more readable. 
> 
> Check
> 
> Correct
> 
> See the video entitled, "Aliases and Self Joins" for more information.
> 

      An alias only exists for the duration of the query. 
> 
> Check
> 
> Correct
> 
> See the video entitled, "Aliases and Self Joins" for more information.
> 
> 6.
> 
> Question 6
> 
> What is wrong with the following query?
> 
> SELECT Customers.CustomerName, Orders.OrderID
> 
> FROM LEFT JOIN ON Customers.CustomerID = Orders.CustomerID FROM Orders AND 
> 
>   Customers
> 
> ORDER BY
> 
> CustomerName;
> 
> 
> 1 / 1 point
> 

      The table name comes after the join condition 
> 
>  Column names do not have an alias 
> 
>  Should be using an inner join rather than a left join 
> 
> Check
> 
> Correct
> 
> See the videos entitled, "Inner Joins" and "Advanced Joins" for more information.
> 
> 7.
> 
> Question 7
> 
> What is the difference between a left join and a right join?
> 
> 1 / 1 point
> 
>  There is actually no difference between a left and a right join. 
> 

      The only difference between a left and right join is the order in which the tables are relating. 
> 
>  A right join is always used _before_ a full outer join, whereas a left join is always used _after_ a full outer join 
> 
>  A left join always is used before a right join in a query statement 
> 
> Check
> 
> Correct
> 
> See the video entitled, "Advanced Joins: Left, Right, and Full Outer Joins" for more information.
> 
> 8.
> 
> Question 8
> 
> If you perform a cartesian join on a table with 10 rows and a table with 20 rows, how many rows will there be in the output table?
> 
> 1 / 1 point
> 
>  20 
> 
>  10 
> 

      200 
> 
>  15 
> 
> Check
> 
> Correct
> 
> See the video entitled, "Cartesian (Cross) Joins" for more information.
> 
> 9.
> 
> Question 9
> 
> Which of the following statements about Unions is true? (select all that apply)
> 
> 1 / 1 point
> 

      The columns must also have similar data types 
> 
> Check
> 
> Correct
> 
> See the video entitled, "Unions" for more information.
> 
>  The order of the SELECTed columns in a UNION does not matter 
> 

      Each SELECT statement within UNION must have the same number of columns 
> 
> Check
> 
> Correct
> 
> See the video entitled, "Unions" for more information.
> 

      The UNION operator is used to combine the result-set of two or more SELECT statements 
> 
> Check
> 
> Correct
> 
> See the video entitled, "Unions" for more information.
> 
> 10.
> 
> Question 10
> 
> Data scientists need to use joins in order to: (select the best answer)
> 
> 1 / 1 point
> 
>  Filter data from multiple tables. 
> 

      Retrieve data from multiple tables. 
> 
>  Create new tables. 
> 
> Check
> 
> Correct
> 
> See any of the videos on Joins in this module for more information.
>
> -- https://www.coursera.org/learn/sql-for-data-science/exam/YGpe2/module-3-quiz/attempt?redirectToCover=true#Tunnel Vision Close
