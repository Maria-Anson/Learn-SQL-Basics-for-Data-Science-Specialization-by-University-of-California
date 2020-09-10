### Module 4 Coding Questions
> 
> Latest Submission Grade
> 
> 97.22%
> 
> 1.
> 
> Question 1
> 
> All of the questions in this quiz refer to the open source Chinook Database. Please familiarize yourself with the [ER diagram](https://ucde-rey.s3.amazonaws.com/DSV1015/ChinookDatabaseSchema.png) in order to familiarize yourself with the table and column names in order to write accurate queries and get the appropriate answers.
> 
> Pull a list of customer ids with the customer’s full name, and address, along with combining their city and country together. Be sure to make a space in between these two and make it UPPER CASE. (e.g. LOS ANGELES USA) 
> SELECT CustomerId,
> 
>        FirstName || " " || LastName AS FullName,
> 
>        Address,
> 
>        UPPER(City || " " || Country) AS CityCountry
> 
> FROM Customers
> 
> WHERE Customerid = 16
> 
> 
> What is the city and country result for CustomerID 16?
> 
> 1 / 1 point
> 

     MOUNTAIN VIEW USA
> 
> Check
> 
> Correct
> 
> 2.
> 
> Question 2
> 
> All of the questions in this quiz refer to the open source Chinook Database. Please familiarize yourself with the [ER diagram](https://ucde-rey.s3.amazonaws.com/DSV1015/ChinookDatabaseSchema.png) in order to familiarize yourself with the table and column names in order to write accurate queries and get the appropriate answers.
> 
> Create a new employee user id by combining the first 4 letters of the employee’s first name with the first 2 letters of the employee’s last name. Make the new field lower case and pull each individual step to show your work.
> 
> SELECT FirstName,
> 
>        LastName,
> 
>        LOWER(SUBSTR(FirstName,1,4)) AS A,
> 
>        LOWER(SUBSTR(LastName,1,2)) AS B,
> 
>        LOWER(SUBSTR(FirstName,1,4)) || LOWER(SUBSTR(LastName,1,2)) AS userId
> 
> FROM Employees
> 
> What is the final result for Robert King?
> 
> 1 / 1 point
> 

     robeki
> 
> Check
> 
> Correct
> 
> 3.
> 
> Question 3
> 
> All of the questions in this quiz refer to the open source Chinook Database. Please familiarize yourself with the [ER diagram](https://ucde-rey.s3.amazonaws.com/DSV1015/ChinookDatabaseSchema.png) in order to familiarize yourself with the table and column names in order to write accurate queries and get the appropriate answers.
> 
> Show a list of employees who have worked for the company for 15 or more years using the current date function. Sort by lastname ascending.
> 
> SELECT FirstName,
> 
>        LastName,
> 
>        HireDate,
> 
>        (STRFTIME('%Y', 'now') - STRFTIME('%Y', HireDate)) 
> 
>           - (STRFTIME('%m-%d', 'now') < STRFTIME('%m-%d', HireDate)) 
> 
>           AS YearsWorked
> 
> FROM Employees
> 
> WHERE YearsWorked >= 15
> 
> ORDER BY LastName ASC
> 
> What is the lastname of the last person on the list returned?
> 
> 1 / 1 point
> 

     Peacock
> 
> Check
> 
> Correct
> 
> 4.
> 
> Question 4
> 
> All of the questions in this quiz refer to the open source Chinook Database. Please familiarize yourself with the [ER diagram](https://ucde-rey.s3.amazonaws.com/DSV1015/ChinookDatabaseSchema.png) in order to familiarize yourself with the table and column names in order to write accurate queries and get the appropriate answers.
> 
> Profiling the Customers table, answer the following question.
> 
> SELECT *
> 
> FROM Customers c
> 
> WHERE c.Company IS NULL or
> 
>       c.FirstName IS NULL or
> 
>       c.Fax IS NULL or
> 
>       c.Address IS NULL or
> 
>       c.Phone IS NULL or
> 
>       c.PostalCode IS NULL 
> 
> Are there any columns with null values? Indicate any below. Select all that apply.
> 
> 1 / 1 point
> 

      Fax 
> 
> Check
> 
> Correct
> 
>  FirstName 
> 

      Company 
> 
> Check
> 
> Correct
> 
>  Address 
> 

      Postal Code 
> 
> Check
> 
> Correct
> 

      Phone 
> 
> 
> 5.
> 
> Question 5
> 
> All of the questions in this quiz refer to the open source Chinook Database. Please familiarize yourself with the [ER diagram](https://ucde-rey.s3.amazonaws.com/DSV1015/ChinookDatabaseSchema.png) in order to familiarize yourself with the table and column names in order to write accurate queries and get the appropriate answers.
> 
> Find the cities with the most customers and rank in descending order.
> 
> SELECT City,
> 
>        COUNT(*)
> 
> FROM Customers
> 
> GROUP BY City
> 
> ORDER BY COUNT(*) DESC
> 
> Which of the following cities indicate having 2 customers?
> 
> 1 / 1 point
> 

      São Paulo 
> 
> Check
> 
> Correct
> 
>  Dublin 
> 

      Mountain View 
> 
> Check
> 
> Correct
> 
>  Frankfurt 
> 
>  Budapest 
> 

      London 
> 
> Check
> 
> Correct
> 
> 6.
> 
> Question 6
> 
> All of the questions in this quiz refer to the open source Chinook Database. Please familiarize yourself with the [ER diagram](https://ucde-rey.s3.amazonaws.com/DSV1015/ChinookDatabaseSchema.png) in order to familiarize yourself with the table and column names in order to write accurate queries and get the appropriate answers.
> 
> Create a new customer invoice id by combining a customer’s invoice id with their first and last name while ordering your query in the following order: firstname, lastname, and invoiceID.
> 
> SELECT C.FirstName,
> 
>        C.LastName,
> 
>        I.InvoiceId,
> 
>        C.FirstName || C.LastName || I.InvoiceID AS NewId
> 
> FROM Customers C INNER JOIN Invoices I
> 
> ON C.CustomerId = I.CustomerID
> 
> WHERE NewId LIKE 'AstridGruber%'
>
> Select all of the correct "AstridGruber" entries that are returned in your results below. Select all that apply.
> 
> 1 / 1 point
> 

      AstridGruber273 
> 
> Check
> 
> Correct
> 

      AstridGruber296 
> 
> Check
> 
> Correct
> 
>  AstridGruber354 
> 

      AstridGruber370 
> 
> Check
> 
> Correct
> 
>  AstridGruber408 
> 
>  AstridGruber456
>
> -- https://www.coursera.org/learn/sql-for-data-science/exam/Lbx1o/module-4-coding-questions/view-attempt#Tunnel Vision Close
