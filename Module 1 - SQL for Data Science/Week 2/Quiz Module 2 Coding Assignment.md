### Module 2 Coding Assignment
> 
> Latest Submission Grade
> 
> 100%
> 
> 1.
> 
> Question 1
> 
> All of the questions in this quiz refer to the open source Chinook Database. Please familiarize yourself with the [ER diagram](https://ucde-rey.s3.amazonaws.com/DSV1015/ChinookDatabaseSchema.png) to familiarize yourself with the table and column names to write accurate queries and get the appropriate answers.
> 
> 
> select * from tracks 
> 
> where milliseconds > 5000000
> 
> 
> +---------+-------------------------+---------+-------------+---------+----------+--------------+------------+-----------+
> | TrackId | Name                    | AlbumId | MediaTypeId | GenreId | Composer | Milliseconds |      Bytes | UnitPrice |
> +---------+-------------------------+---------+-------------+---------+----------+--------------+------------+-----------+
> |    2820 | Occupation / Precipice  |     227 |           3 |      19 |     None |      5286953 | 1054423946 |      1.99 |
> |    3224 | Through a Looking Glass |     229 |           3 |      21 |     None |      5088838 | 1059546140 |      1.99 |
> +---------+-------------------------+---------+-------------+---------+----------+--------------+------------+-----------+
> 
> 
> How many tracks are returned?
> 
> 1 / 1 point
> 

     2
> 
> Check
> 
> Correct
> 
> 2.
> 
> Question 2
> 
> All of the questions in this quiz refer to the open source Chinook Database. Please familiarize yourself with the [ER diagram](https://ucde-rey.s3.amazonaws.com/DSV1015/ChinookDatabaseSchema.png) to familiarize yourself with the table and column names to write accurate queries and get the appropriate answers.
> 
> 
> select * from invoices
> 
> where total between 5 and 15
> 
> 
> +-----------+------------+---------------------+-------------------------+-------------+--------------+----------------+-------------------+-------+
> | InvoiceId | CustomerId | InvoiceDate         | BillingAddress          | BillingCity | BillingState | BillingCountry | BillingPostalCode | Total |
> +-----------+------------+---------------------+-------------------------+-------------+--------------+----------------+-------------------+-------+
> |         3 |          8 | 2009-01-03 00:00:00 | Grétrystraat 63         | Brussels    |         None | Belgium        | 1000              |  5.94 |
> |         4 |         14 | 2009-01-06 00:00:00 | 8210 111 ST NW          | Edmonton    |           AB | Canada         | T6G 2C7           |  8.91 |
> |         5 |         23 | 2009-01-11 00:00:00 | 69 Salem Street         | Boston      |           MA | USA            | 2113              | 13.86 |
> |        10 |         46 | 2009-02-03 00:00:00 | 3 Chatham Street        | Dublin      |       Dublin | Ireland        | None              |  5.94 |
> |        11 |         52 | 2009-02-06 00:00:00 | 202 Hoxton Street       | London      |         None | United Kingdom | N1 5LH            |  8.91 |
> |        12 |          2 | 2009-02-11 00:00:00 | Theodor-Heuss-Straße 34 | Stuttgart   |         None | Germany        | 70174             | 13.86 |
> |        17 |         25 | 2009-03-06 00:00:00 | 319 N. Frances Street   | Madison     |           WI | USA            | 53703             |  5.94 |
> |        18 |         31 | 2009-03-09 00:00:00 | 194A Chain Lake Drive   | Halifax     |           NS | Canada         | B3S 1C5           |  8.91 |
> |        19 |         40 | 2009-03-14 00:00:00 | 8, Rue Hanovre          | Paris       |         None | France         | 75002             | 13.86 |
> |        24 |          4 | 2009-04-06 00:00:00 | Ullevålsveien 14        | Oslo        |         None | Norway         | 0171              |  5.94 |
> +-----------+------------+---------------------+-------------------------+-------------+--------------+----------------+-------------------+-------+
> (Output limit exceeded, 10 of 168 total rows shown)
> 
> </pre>
> 
> </pre>
> 
> While the query in this example is limited to 10 records, running the query correctly will indicate how many total records there are - enter that number below.
> 
> 1 / 1 point
> 

     168
> 
> Check
> 
> Correct
> 
> 3.
> 
> Question 3
> 
> All of the questions in this quiz refer to the open source Chinook Database. Please familiarize yourself with the [ER diagram](https://ucde-rey.s3.amazonaws.com/DSV1015/ChinookDatabaseSchema.png) to familiarize yourself with the table and column names to write accurate queries and get the appropriate answers.
> 
> 
> select * from customers
> 
> where state in ('RJ', 'DF', 'AB', 'BC', 'CA', 'WA', 'NY')
> 
> 
> +------------+-----------+----------+-----------------------+---------------------------+----------------+-------+---------+------------+--------------------+--------------------+-------------------------------+--------------+
> | CustomerId | FirstName | LastName | Company               | Address                   | City           | State | Country | PostalCode | Phone              | Fax                | Email                         | SupportRepId |
> +------------+-----------+----------+-----------------------+---------------------------+----------------+-------+---------+------------+--------------------+--------------------+-------------------------------+--------------+
> |         12 | Roberto   | Almeida  | Riotur                | Praça Pio X, 119          | Rio de Janeiro | RJ    | Brazil  | 20040-020  | +55 (21) 2271-7000 | +55 (21) 2271-7070 | roberto.almeida@riotur.gov.br |            3 |
> |         13 | Fernanda  | Ramos    | None                  | Qe 7 Bloco G              | Brasília       | DF    | Brazil  | 71020-677  | +55 (61) 3363-5547 | +55 (61) 3363-7855 | fernadaramos4@uol.com.br      |            4 |
> |         14 | Mark      | Philips  | Telus                 | 8210 111 ST NW            | Edmonton       | AB    | Canada  | T6G 2C7    | +1 (780) 434-4554  | +1 (780) 434-5565  | mphilips12@shaw.ca            |            5 |
> |         15 | Jennifer  | Peterson | Rogers Canada         | 700 W Pender Street       | Vancouver      | BC    | Canada  | V6C 1G8    | +1 (604) 688-2255  | +1 (604) 688-8756  | jenniferp@rogers.ca           |            3 |
> |         16 | Frank     | Harris   | Google Inc.           | 1600 Amphitheatre Parkway | Mountain View  | CA    | USA     | 94043-1351 | +1 (650) 253-0000  | +1 (650) 253-0000  | fharris@google.com            |            4 |
> |         17 | Jack      | Smith    | Microsoft Corporation | 1 Microsoft Way           | Redmond        | WA    | USA     | 98052-8300 | +1 (425) 882-8080  | +1 (425) 882-8081  | jacksmith@microsoft.com       |            5 |
> |         18 | Michelle  | Brooks   | None                  | 627 Broadway              | New York       | NY    | USA     | 10012-2612 | +1 (212) 221-3546  | +1 (212) 221-4679  | michelleb@aol.com             |            3 |
> |         19 | Tim       | Goyer    | Apple Inc.            | 1 Infinite Loop           | Cupertino      | CA    | USA     | 95014      | +1 (408) 996-1010  | +1 (408) 996-1011  | tgoyer@apple.com              |            3 |
> |         20 | Dan       | Miller   | None                  | 541 Del Medio Avenue      | Mountain View  | CA    | USA     | 94040-111  | +1 (650) 644-3358  | None               | dmiller@comcast.com           |            4 |
> +------------+-----------+----------+-----------------------+---------------------------+----------------+-------+---------+------------+--------------------+--------------------+-------------------------------+--------------+
> 
> 
> What company does Jack Smith work for?
> 
> 1 / 1 point
> 

      Microsoft Corp 
> 
>  Rogers Canada 
> 
>  Apple Inc. 
> 
>  Google Inc. 
> 
> Check
> 
> Correct
> 
> 4.
> 
> Question 4
> 
> All of the questions in this quiz refer to the open source Chinook Database. Please familiarize yourself with the [ER diagram](https://ucde-rey.s3.amazonaws.com/DSV1015/ChinookDatabaseSchema.png) to familiarize yourself with the table and column names to write accurate queries and get the appropriate answers.
> 
> select * from invoices
> 
> where (total between 1 and 5) and (customerid in (56,58))
> 
> 
> +-----------+------------+---------------------+---------------------+--------------+--------------+----------------+-------------------+-------+
> | InvoiceId | CustomerId | InvoiceDate         | BillingAddress      | BillingCity  | BillingState | BillingCountry | BillingPostalCode | Total |
> +-----------+------------+---------------------+---------------------+--------------+--------------+----------------+-------------------+-------+
> |       119 |         56 | 2010-06-12 00:00:00 | 307 Macacha Güemes  | Buenos Aires |         None | Argentina      | 1106              |  1.98 |
> |       142 |         56 | 2010-09-14 00:00:00 | 307 Macacha Güemes  | Buenos Aires |         None | Argentina      | 1106              |  3.96 |
> |       337 |         56 | 2013-01-28 00:00:00 | 307 Macacha Güemes  | Buenos Aires |         None | Argentina      | 1106              |  1.98 |
> |       120 |         58 | 2010-06-12 00:00:00 | 12,Community Centre | Delhi        |         None | India          | 110017            |  1.98 |
> |       315 |         58 | 2012-10-27 00:00:00 | 12,Community Centre | Delhi        |         None | India          | 110017            |  1.98 |
> |       338 |         58 | 2013-01-29 00:00:00 | 12,Community Centre | Delhi        |         None | India          | 110017            |  3.96 |
> |       412 |         58 | 2013-12-22 00:00:00 | 12,Community Centre | Delhi        |         None | India          | 110017            |  1.99 |
> +-----------+------------+---------------------+---------------------+--------------+--------------+----------------+-------------------+-------+
> 
> 
> What was the invoice date for invoice ID 315?
> 
> 1 / 1 point
> 
>  6-12-2010 
> 
>  12-22-2013 
> 

      10-27-2012 
> 
>  1-29-2013 
> 
> Check
> 
> Correct
> 
> 5.
> 
> Question 5
> 
> All of the questions in this quiz refer to the open source Chinook Database. Please familiarize yourself with the [ER diagram](https://ucde-rey.s3.amazonaws.com/DSV1015/ChinookDatabaseSchema.png) to familiarize yourself with the table and column names to write accurate queries and get the appropriate answers.
> 
> 
> select * from tracks
> 
> where name like 'All%'
> 
> 
> +---------+----------------------------------------+---------+-------------+---------+--------------------------------------------------+--------------+-----------+-----------+
> | TrackId | Name                                   | AlbumId | MediaTypeId | GenreId | Composer                                         | Milliseconds |     Bytes | UnitPrice |
> +---------+----------------------------------------+---------+-------------+---------+--------------------------------------------------+--------------+-----------+-----------+
> |      38 | All I Really Want                      |       6 |           1 |       1 | Alanis Morissette & Glenn Ballard                |       284891 |   9375567 |      0.99 |
> |     134 | All For You                            |      14 |           1 |       3 | None                                             |       235833 |   7726948 |      0.99 |
> |     385 | All Star                               |      33 |           1 |       7 | Nando Reis                                       |       176326 |   5891697 |      0.99 |
> |    1009 | All My Life                            |      81 |           1 |       4 | Foo Fighters                                     |       263653 |   8665545 |      0.99 |
> |    1608 | All My Love                            |     130 |           1 |       1 | Robert Plant & John Paul Jones                   |       356284 |  11684862 |      0.99 |
> |    1892 | All Within My Hands                    |     155 |           1 |       3 | Bob Rock/James Hetfield/Kirk Hammett/Lars Ulrich |       527986 |  17162741 |      0.99 |
> |    2192 | All or None                            |     180 |           1 |       1 | Stone Gossard                                    |       277655 |   9104728 |      0.99 |
> |    2274 | All Dead, All Dead                     |     186 |           1 |       1 | May                                              |       190119 |   6144878 |      0.99 |
> |    2888 | All the Best Cowboys Have Daddy Issues |     230 |           3 |      19 | None                                             |      2555492 | 211743651 |      1.99 |
> |    2969 | All Because Of You                     |     235 |           1 |       1 | Adam Clayton, Bono, Larry Mullen & The Edge      |       219141 |   7198014 |      0.99 |
> +---------+----------------------------------------+---------+-------------+---------+--------------------------------------------------+--------------+-----------+-----------+
> (Output limit exceeded, 10 of 15 total rows shown)
> 
> While only 10 records are shown, the query will indicate how many total records there are for this query - enter that number below.
> 
> 1 / 1 point
> 

     15
> 
> Check
> 
> Correct
> 
> 6.
> 
> Question 6
> 
> All of the questions in this quiz refer to the open source Chinook Database. Please familiarize yourself with the [ER diagram](https://ucde-rey.s3.amazonaws.com/DSV1015/ChinookDatabaseSchema.png) to familiarize yourself with the table and column names to write accurate queries and get the appropriate answers.
> 
> 
> select * from customers
> 
> where email like 'J%gmail.com'
> 
> 
> +------------+-----------+----------+---------+-------------+----------------+-------+---------+------------+-------------------+------+---------------------+--------------+
> | CustomerId | FirstName | LastName | Company | Address     | City           | State | Country | PostalCode | Phone             |  Fax | Email               | SupportRepId |
> +------------+-----------+----------+---------+-------------+----------------+-------+---------+------------+-------------------+------+---------------------+--------------+
> |         28 | Julia     | Barnett  |    None | 302 S 700 E | Salt Lake City | UT    | USA     | 84102      | +1 (801) 531-7272 | None | jubarnett@gmail.com |            5 |
> +------------+-----------+----------+---------+-------------+----------------+-------+---------+------------+-------------------+------+---------------------+--------------+
> 
> 
> Enter the one email address returned (you will likely need to scroll to the right) below.
> 
> 1 / 1 point
> 

     jubarnett@gmail.com
> 
> Check
> 
> Correct
> 
> 7.
> 
> Question 7
> 
> All of the questions in this quiz refer to the open source Chinook Database. Please familiarize yourself with the [ER diagram](https://chinookdatabase.codeplex.com/wikipage?title=Chinook_Schema&referringTitle=Documentation) to familiarize yourself with the table and column names to write accurate queries and get the appropriate answers.
> 
> 
> select * from invoices 
> 
> where billingcity in ('Brasília', 'Edmonton', 'Vancouver')
> 
> order by invoiceid desc
> 
> 
> +-----------+------------+---------------------+---------------------+-------------+--------------+----------------+-------------------+-------+
> | InvoiceId | CustomerId | InvoiceDate         | BillingAddress      | BillingCity | BillingState | BillingCountry | BillingPostalCode | Total |
> +-----------+------------+---------------------+---------------------+-------------+--------------+----------------+-------------------+-------+
> |       362 |         14 | 2013-05-11 00:00:00 | 8210 111 ST NW      | Edmonton    | AB           | Canada         | T6G 2C7           | 13.86 |
> |       351 |         14 | 2013-03-31 00:00:00 | 8210 111 ST NW      | Edmonton    | AB           | Canada         | T6G 2C7           |  1.98 |
> |       328 |         15 | 2012-12-15 00:00:00 | 700 W Pender Street | Vancouver   | BC           | Canada         | V6C 1G8           |  0.99 |
> |       319 |         13 | 2012-11-01 00:00:00 | Qe 7 Bloco G        | Brasília    | DF           | Brazil         | 71020-677         |  8.91 |
> |       276 |         15 | 2012-04-26 00:00:00 | 700 W Pender Street | Vancouver   | BC           | Canada         | V6C 1G8           |  5.94 |
> |       264 |         13 | 2012-03-03 00:00:00 | Qe 7 Bloco G        | Brasília    | DF           | Brazil         | 71020-677         | 13.86 |
> |       254 |         15 | 2012-01-23 00:00:00 | 700 W Pender Street | Vancouver   | BC           | Canada         | V6C 1G8           |  3.96 |
> |       253 |         13 | 2012-01-22 00:00:00 | Qe 7 Bloco G        | Brasília    | DF           | Brazil         | 71020-677         |  1.98 |
> |       231 |         15 | 2011-10-21 00:00:00 | 700 W Pender Street | Vancouver   | BC           | Canada         | V6C 1G8           |  1.98 |
> |       230 |         14 | 2011-10-08 00:00:00 | 8210 111 ST NW      | Edmonton    | AB           | Canada         | T6G 2C7           |  0.99 |
> +-----------+------------+---------------------+---------------------+-------------+--------------+----------------+-------------------+-------+
> (Output limit exceeded, 10 of 21 total rows shown)
> 
> 
> What is the total invoice amount of the first record returned? Enter the number below without a $ sign. _Remember to sort in descending order to get the correct answer._
> 
> 1 / 1 point
> 

     13.86
> 
> Check
> 
> Correct
> 
> 8.
> 
> Question 8
> 
> All of the questions in this quiz refer to the open source Chinook Database. Please familiarize yourself with the [ER diagram](https://ucde-rey.s3.amazonaws.com/DSV1015/ChinookDatabaseSchema.png) to familiarize yourself with the table and column names to write accurate queries and get the appropriate answers.
> 
> 
> select customerid, count(customerid) as count from invoices
> 
> group by  customerid 
> 
> +------------+-------+
> | CustomerId | count |
> +------------+-------+
> |          1 |     7 |
> |          2 |     7 |
> |          3 |     7 |
> |          4 |     7 |
> |          5 |     7 |
> |          6 |     7 |
> |          7 |     7 |
> |          8 |     7 |
> |          9 |     7 |
> |         10 |     7 |
> +------------+-------+
> (Output limit exceeded, 10 of 59 total rows shown)
> 
> 
> What is the number of items placed for the 8th person on this list? Enter that number below.
> 
> 1 / 1 point
> 

     7
> 
> Check
> 
> Correct
> 
> 9.
> 
> Question 9
> 
> All of the questions in this quiz refer to the open source Chinook Database. Please familiarize yourself with the [ER diagram](https://ucde-rey.s3.amazonaws.com/DSV1015/ChinookDatabaseSchema.png) to familiarize yourself with the table and column names to write accurate queries and get the appropriate answers.
> 
> 
> select albumid, count(albumid) as count
> 
> from tracks
> 
> group by albumid
> 
> having count >=12
> 
> 
> +---------+-------+
> | AlbumId | count |
> +---------+-------+
> |       5 |    15 |
> |       6 |    13 |
> |       7 |    12 |
> |       8 |    14 |
> |      10 |    14 |
> |      11 |    12 |
> |      12 |    12 |
> |      14 |    13 |
> |      18 |    17 |
> |      21 |    18 |
> +---------+-------+
> (Output limit exceeded, 10 of 158 total rows shown)
> 
> While the number of records returned is limited to 10, the query, if run correctly, will indicate how many total records there are. Enter that number below.
> 
> 1 / 1 point
> 

     158
> 
> Check
> 
> Correct
>
> -- https://www.coursera.org/learn/sql-for-data-science/exam/QA3wg/module-2-coding-assignment/attempt?redirectToCover=true#Tunnel Vision Close
