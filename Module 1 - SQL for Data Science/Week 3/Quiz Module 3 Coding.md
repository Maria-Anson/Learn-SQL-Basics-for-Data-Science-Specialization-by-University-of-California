## Module 3 Coding Assignment
> 
> Latest Submission Grade
> 
> 100%
> 
> 1.
> 
> Question 1
> 
> All of the questions in this quiz refer to the open source Chinook Database. Please familiarize yourself with the [ER diagram](https://ucde-rey.s3.amazonaws.com/DSV1015/ChinookDatabaseSchema.png) in order to familiarize yourself with the table and column names in order to write accurate queries and get the appropriate answers.
> 
> Using a subquery, find the **name**s of all the **tracks** for the album "Californication".
> 

       select name
       
       from tracks 
       
       where albumid in
       
         (select albumid
       
          from albums
       
          where title = 'Californication')
> 
> 
> +-------------------+
> | Name              |
> +-------------------+
> | Around The World  |
> | Parallel Universe |
> | Scar Tissue       |
> | Otherside         |
> | Get On Top        |
> | Californication   |
> | Easily            |
> | Porcelain         |
> | Emit Remmus       |
> | I Like Dirt       |
> +-------------------+
> (Output limit exceeded, 10 of 15 total rows shown)
> 
> 
> What is the title of the 8th track?
> 
> 1 / 1 point
> 

     Porcelain
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
> Find the total number of invoices for each customer along with the customer's full name, city and email.
> 

       select c.firstname, c.lastname, c.city, c.email, sum(i.invoiceid) as total
       
       from customers c inner join invoices i
       
       on c.customerid = i.customerid
       
       group by c.customerid
> 
> 
> +-----------+-------------+---------------------+--------------------------+-------+
> | FirstName | LastName    | City                | Email                    | total |
> +-----------+-------------+---------------------+--------------------------+-------+
> | Luís      | Gonçalves   | São José dos Campos | luisg@embraer.com.br     |  1582 |
> | Leonie    | Köhler      | Stuttgart           | leonekohler@surfeu.de    |  1029 |
> | François  | Tremblay    | Montréal            | ftremblay@gmail.com      |  1715 |
> | Bjørn     | Hansen      | Oslo                | bjorn.hansen@yahoo.no    |  1162 |
> | František | Wichterlová | Prague              | frantisekw@jetbrains.com |  1435 |
> | Helena    | Holý        | Prague              | hholy@gmail.com          |  1708 |
> | Astrid    | Gruber      | Vienne              | astrid.gruber@apple.at   |  1568 |
> | Daan      | Peeters     | Brussels            | daan_peeters@apple.be    |  1428 |
> | Kara      | Nielsen     | Copenhagen          | kara.nielsen@jubii.dk    |  1288 |
> | Eduardo   | Martins     | São Paulo           | eduardo@woodstock.com.br |  1561 |
> +-----------+-------------+---------------------+--------------------------+-------+
> (Output limit exceeded, 10 of 59 total rows shown)
> 
> </pre>
> 
> </pre>
> 
> **After running the query described above**, what is the email address of the 5th person, František Wichterlová? Enter the answer below (feel free to copy and paste).
> 
> 1 / 1 point
> 

     frantisekw@jetbrains.com
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
> Retrieve the track name, album, artistID, and trackID for all the albums.
> 

     select t.name, a.title, a.artistid, t.trackid
     
     from albums a inner join tracks t
     
     on a.albumid = t.albumid
     
     where t.trackid = 12
> 
> 
> +--------------------+---------------------------------------+----------+---------+
> | Name               | Title                                 | ArtistId | TrackId |
> +--------------------+---------------------------------------+----------+---------+
> | Breaking The Rules | For Those About To Rock We Salute You |        1 |      12 |
> +--------------------+---------------------------------------+----------+---------+
> 
> </pre>
> 
> </pre>
> 
> What is the song title of trackID 12 from the "For Those About to Rock We Salute You" album? Enter the answer below.
> 
> 1 / 1 point
> 

     Breaking The Rules
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
> Retrieve a list with the managers last name, and the last name of the employees who report to him or her.
> 

     select mgr.lastname as Manager, e.lastname as Employee
     
     from employees e left join employees mgr
     
     on e.reportsto = mgr.employeeid
> 
> 
> +----------+----------+
> |  Manager | Employee |
> +----------+----------+
> |     None | Adams    |
> |    Adams | Edwards  |
> |  Edwards | Peacock  |
> |  Edwards | Park     |
> |  Edwards | Johnson  |
> |    Adams | Mitchell |
> | Mitchell | King     |
> | Mitchell | Callahan |
> +----------+----------+
> 
> 
> **After running the query described above**, who are the reports for the manager named Mitchell (select all that apply)?
> 
> 1 / 1 point
> 
>  Park 
> 
>  Johnson 
> 

      King 
> 
> Check
> 
> Correct
> 

      Callahan 
> 
> Check
> 
> Correct
> 
>  Edwards 
> 
> 5.
> 
> Question 5
> 
> All of the questions in this quiz refer to the open source Chinook Database. Please familiarize yourself with the [ER diagram](https://ucde-rey.s3.amazonaws.com/DSV1015/ChinookDatabaseSchema.png) in order to familiarize yourself with the table and column names in order to write accurate queries and get the appropriate answers.
> 
> Find the name and ID of the artists who do not have albums.
>

     select a.title, ar.name, ar.artistid
     
     from artists ar
     
    left join albums a
     
     on ar.artistid = a.artistid
     
     where a.title is NULL
> 
> 
> +-------+----------------------------+----------+
> | Title | Name                       | ArtistId |
> +-------+----------------------------+----------+
> |  None | Milton Nascimento & Bebeto |       25 |
> |  None | Azymuth                    |       26 |
> |  None | João Gilberto              |       28 |
> |  None | Bebel Gilberto             |       29 |
> |  None | Jorge Vercilo              |       30 |
> |  None | Baby Consuelo              |       31 |
> |  None | Ney Matogrosso             |       32 |
> |  None | Luiz Melodia               |       33 |
> |  None | Nando Reis                 |       34 |
> |  None | Pedro Luís & A Parede      |       35 |
> +-------+----------------------------+----------+
> (Output limit exceeded, 10 of 71 total rows shown)
>  
> **After running the query described above**, two of the records returned have the same last name. Enter that name below.
> 
> 1 / 1 point
> 

     Gilberto
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
> Use a UNION to create a list of all the employee's and customer's first names and last names ordered by the last name in descending order.
> 
>

     select e.firstname, e.lastname
     
     from employees e
     
     union
     
     select c.firstname, c.lastname
     
     from customers c
     
     order by c.lastname desc
> 
> 
> RunReset
> 
> <pre class="rc-ConsoleOutput">
> 
> +-------------+--------------+
> | e.firstname | e.lastname   |
> +-------------+--------------+
> | Fynn        | Zimmermann   |
> | Stanisław   | Wójcik       |
> | František   | Wichterlová  |
> | Johannes    | Van der Berg |
> | François    | Tremblay     |
> | Mark        | Taylor       |
> | Ellie       | Sullivan     |
> | Victor      | Stevens      |
> | Puja        | Srivastava   |
> | Jack        | Smith        |
> +-------------+--------------+
> (Output limit exceeded, 10 of 67 total rows shown)
> 
> </pre>
> 
> </pre>
> 
> **After running the query described above**, determine what is the last name of the 6th record? Enter it below. Remember to order things in descending order to be sure to get the correct answer.
> 
> 1 / 1 point
> 

     Taylor
> 
> Check
> 
> Correct
> 
> 7.
> 
> Question 7
> 
> All of the questions in this quiz refer to the open source Chinook Database. Please familiarize yourself with the [ER diagram](https://ucde-rey.s3.amazonaws.com/DSV1015/ChinookDatabaseSchema.png) in order to familiarize yourself with the table and column names in order to write accurate queries and get the appropriate answers.
> 
> See if there are any customers who have a different city listed in their billing city versus their customer city.
> 
> 

     select c.customerid, c.firstname, c.lastname, c.city
     
     from customers c
     
     join invoices i
     
     on c.customerid = i.customerid
     
     where c.city <> i.billingcity
> 
> 
> +------------+-----------+----------+------+
> | CustomerId | FirstName | LastName | City |
> +------------+-----------+----------+------+
> +------------+-----------+----------+------+
> (Zero rows)
>  
> Indicate your answer below.
> 
> 1 / 1 point
> 

      No customers have a different city listed in their billing city versus customer city. 
> 
>  3 customers have a different city listed in their billing city versus customer city. 
> 
>  8 customers have a different city listed in their billing city versus customer city. 
> 
>  17 customers have a different city listed in their billing city versus customer city. 
> 
> Check
> 
> Correct
>
> -- https://www.coursera.org/learn/sql-for-data-science/exam/cCOUv/module-3-coding-assignment/attempt?redirectToCover=true#Tunnel Vision Close
