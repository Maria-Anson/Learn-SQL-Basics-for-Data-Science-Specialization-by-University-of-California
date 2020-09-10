## Module 4 Quiz
> 
> Latest Submission Grade
> 
> 100%
> 
> 1.
> 
> Question 1
> 
> Which of the following are supported in SQL when dealing with strings? (Select all that apply)
> 
> 1 / 1 point
> 

      Substring 
> 
> Check
> 
> Correct
> 
> See the video entitled, " Working with Text Strings" for more information.
> 

      Concatenate 
> 
> Check
> 
> Correct
> 
> See the video entitled, " Working with Text Strings" for more information.
> 

      Upper 
> 
> Check
> 
> Correct
> 
> See the video entitled, " Working with Text Strings" for more information.
> 

      Lower 
> 
> Check
> 
> Correct
> 
> See the video entitled, " Working with Text Strings" for more information.
> 

      Trim 
> 
> Check
> 
> Correct
> 
> See the video entitled, " Working with Text Strings" for more information.
> 
> 2.
> 
> Question 2
> 
> What will the result of the following statement be?
> 
> 
> SELECT SUBSTR('You are beautiful.', 3)
> 
> 1 / 1 point
> 
>  beautiful. 
> 
>  This will return an error 
> 
>  You are beautiful. 
> 

      u are beautiful. 
> 
> Check
> 
> Correct
> 
> See the video entitled, "Working with Text Strings" for more information.
> 
> 3.
> 
> Question 3
> 
> What are the results of the following query?
> 
> 
> select * orders
> 
> where order_date = ‘2017-07-15’
>
> Additional information:
> 
> *   Orders = integer
> *   Order_date = datetime
> 
> 1 / 1 point
> 
>  You will get all of the orders. 
> 

      You won't get any results. 
> 
>  You will get all the orders with an order date of 2017-07-15. 
> 
> Check
> 
> Correct
> 
> This query is missing a from statement, so it won't know where to pull the orders from and you'll get an error. See the videos entitled, "Working with Text Strings" and "Working with Date and Time Strings" for more information.
> 
> 4.
> 
> Question 4
> 
> Case statements can only be used for which of the following statements (select all that apply)?
> 
> 1 / 1 point
> 

      Select 
> 
> Check
> 
> Correct
> 
> See the video entitled, "Case Statements" for more information.
> 

      Delete 
> 
> Check
> 
> Correct
> 
> See the video entitled, "Case Statements" for more information.
> 

      Insert 
> 
> Check
> 
> Correct
> 
> See the video entitled, "Case Statements" for more information.
> 

      Update 
> 
> Check
> 
> Correct
> 
> See the video entitled, "Case Statements" for more information.
> 
> 5.
> 
> Question 5
> 
> Which of the following is FALSE regarding views?
> 
> 1 / 1 point
> 

      Views will remain after the database connection has ended 
> 
>  Views are stored in a query 
> 
>  Views can be used to encapsulate queries 
> 
> Check
> 
> Correct
> 
> See the video entitled, "Views" for more information.
> 
> 6.
> 
> Question 6
> 
> You are only allowed to have one condition in a case statement. True or false?
> 
> 1 / 1 point
> 
>  True 
> 

      False 
> 
> Check
> 
> Correct
> 
> See the video entitled, " Case Statements" for more information.
> 
> 7.
> 
> Question 7
> 
> Select the correct SQL syntax for creating a view.
> 
> 1 / 1 point
> 
> CREATE VIEW AS
> 
> SELECT * 
> 
> FROM customers
> 
> WHERE Name LIKE '%I'
> 

     CREATE VIEW
     
     customers AS
     
     SELECT * 
      
     FROM customers
     
     WHERE Name LIKE '%I'
> 
> 
> INSERT VIEW customers AS
> 
> Select * 
> 
> FROM customers
> 
> WHERE Name LIKE '%I'
> 
> 
> Check
> 
> Correct
> 
> See the video entitled, "Views" for more information.
> 
> 8.
> 
> Question 8
> 
> Profiling data is helpful for which of the following? (Select all that apply)
> 
> 1 / 1 point
> 
>  Joining tables together 
> 

      Understanding your data 
> 
> Check
> 
> Correct
> 
> See the video entitled, "Data Governance and Profiling" for more information.
> 

      Filter out unwanted data elements 
> 
> Check
> 
> Correct
> 
> See the video entitled, "Data Governance and Profiling" for more information.
> 
> 9.
> 
> Question 9
> 
> What is the most important step before beginning to write queries?
> 
> 1 / 1 point
> 
>  Deciding what should be done on the client application vs the RDMS 
> 

      Understanding your data 
> 
>  Deciding what tables you want to join 
> 
> Check
> 
> Correct
> 
> See the 2-part video entitled, "Using SQL for Data Science" for more information.
> 
> 10.
> 
> Question 10
> 
> When debugging a query, what should you always remember to do first?
> 
> 1 / 1 point
> 
>  Make sure you didn’t miss any commas. 
> 

      Start simple and break it down first 
> 
>  Start by examining the joins 
> 
>  Start with the inner most query 
> 
> Check
> 
> Correct
> 
> See the 2-part video entitled, "Using SQL for Data Science" for more information.
>
> -- https://www.coursera.org/learn/sql-for-data-science/exam/fC8aC/module-4-quiz/attempt?redirectToCover=true#Tunnel Vision Close
