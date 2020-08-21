### Module 1 Coding Questions
> 
> Latest Submission Grade
> 
> 100%
> 
> 1.
> 
> Question 1
> 
> For all of the questions in this quiz, we are using the [Chinook database](https://chinookdatabase.codeplex.com/wikipage?title=Chinook_Schema&referringTitle=Documentation). All of the interactive code blocks have been setup to retrieve data only from this database.
> 
> Retrieve all the records from the Employees table.
> 
> 
> select ADDRESS from EMPLOYEES where FIRSTNAME = 'Robert'
> 
> +-----------------------------+
> | Address                     |
> +-----------------------------+
> | 590 Columbia Boulevard West |
> +-----------------------------+
>  
> What is Robert King's mailing address? **Note: You will have to scroll to the right in order to see it.**
> 
> 1 / 1 point
> 
>  11120 Jasper Ave. NW, Edmonton, AB, CANADA T5K 2N1 
> 

      590 Columbia Boulevard West, Lethbridge, AB, CANADA T1K 5N8 
> 
>  683 10 Street SW, Calgary, AB, CANADA T2P 5G3 
> 
>  1111 6 Ave SW, Calgary, AB, CANADA T2P 5M5 
> 
> Check
> 
> Correct
> 
> 2.
> 
> Question 2
> 
> Retrieve the FirstName, LastName, Birthdate, Address, City, and State from the Employees table.
> 
> select FirstName, LastName, Birthdate, Address, City, State from EMPLOYEES 
>
> 
> +-----------+----------+---------------------+-----------------------------+------------+-------+
> | FirstName | LastName | BirthDate           | Address                     | City       | State |
> +-----------+----------+---------------------+-----------------------------+------------+-------+
> | Andrew    | Adams    | 1962-02-18 00:00:00 | 11120 Jasper Ave NW         | Edmonton   | AB    |
> | Nancy     | Edwards  | 1958-12-08 00:00:00 | 825 8 Ave SW                | Calgary    | AB    |
> | Jane      | Peacock  | 1973-08-29 00:00:00 | 1111 6 Ave SW               | Calgary    | AB    |
> | Margaret  | Park     | 1947-09-19 00:00:00 | 683 10 Street SW            | Calgary    | AB    |
> | Steve     | Johnson  | 1965-03-03 00:00:00 | 7727B 41 Ave                | Calgary    | AB    |
> | Michael   | Mitchell | 1973-07-01 00:00:00 | 5827 Bowness Road NW        | Calgary    | AB    |
> | Robert    | King     | 1970-05-29 00:00:00 | 590 Columbia Boulevard West | Lethbridge | AB    |
> | Laura     | Callahan | 1968-01-09 00:00:00 | 923 7 ST NW                 | Lethbridge | AB    |
> +-----------+----------+---------------------+-----------------------------+------------+-------+
>
> 
> Which of the employees listed below has a birthdate of 3-3-1965?
> 
> 1 / 1 point
> 
>  Jane 
> 
>  Nancy 
> 
>  Michael 
> 
>  Robert 
> 

      Steve 
> 
> Check
> 
> Correct
> 
> 3.
> 
> Question 3
> 
> Retrieve all the columns from the Tracks table, but only return 20 rows.
> 
> 
> select MILLISECONDS from TRACKS limit 20
> 
> 
> +--------------+
> | Milliseconds |
> +--------------+
> |       343719 |
> |       342562 |
> |       230619 |
> |       252051 |
> |       375418 |
> |       205662 |
> |       233926 |
> |       210834 |
> |       203102 |
> |       263497 |
> |       199836 |
> |       263288 |
> |       205688 |
> |       270863 |
> |       331180 |
> |       215196 |
> |       366654 |
> |       267728 |
> |       325041 |
> |       369319 |
> +--------------+
> 
> 
> What is the runtime in milliseconds for the 5th track, entitled "Princess of the Dawn"? Note: **You will need to scroll to the right to see it, and you may want to copy and paste the number to ensure it is entered correctly.**
> 
> 1 / 1 point
> 

     375418
> 
> Check
> 
> Correct
>
> -- https://www.coursera.org/learn/sql-for-data-science/exam/9QZ4J/module-1-coding-questions/attempt?redirectToCover=true#Tunnel Vision Close
