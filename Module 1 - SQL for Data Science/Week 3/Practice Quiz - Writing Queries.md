## Practice Quiz - Writing Queries
> 
> Total points 5
> 
> 1.
> 
> Question 1
> 
> All of the questions in this quiz pull from the open source Chinook Database. Please refer to the ER Diagram below and familiarize yourself with the table and column names to write accurate queries and get the appropriate answers.
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UAPENoOVEei4RQ5L9j9nDA_5042a1f0839511e8beb2b5b4ae9fa29a_ER-Diagram.png?expiry=1599350400000&hmac=IjXfLsfy8l2B4Rn58rIdTBN2_dJipWlYpf3l8cQ0_kY)
> 
> How many albums does the artist Led Zeppelin have?
> 
> 

     select count(title)
     
     from albums
     
     where artistid = 
     
       (select distinct(artistid)
     
         from artists 
     
         where name = 'Led Zeppelin')
> 
> 
> +--------------+
> | count(title) |
> +--------------+
> |           14 |
> +--------------+
> 
> 
> 1 / 1 point
> 

     14
> 
> Check
> 
> Correct
> 
> 2.
> 
> Question 2
> 
> All of the questions in this quiz pull from the open source Chinook Database. Please refer to the ER Diagram below and familiarize yourself with the table and column names to write accurate queries and get the appropriate answers.
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UAPENoOVEei4RQ5L9j9nDA_5042a1f0839511e8beb2b5b4ae9fa29a_ER-Diagram.png?expiry=1599350400000&hmac=IjXfLsfy8l2B4Rn58rIdTBN2_dJipWlYpf3l8cQ0_kY)
> 
> Create a list of album titles and the unit prices for the artist "Audioslave".
> 
>

     select a.title, t.unitprice 
     
     from tracks t inner join albums a 
     
     on t.albumid = a.albumid
     
     where a.artistid = 
     
           (select artistid
     
             from artists
     
             where name = 'Audioslave')
> 
> 
> +--------------+-----------+
> | Title        | UnitPrice |
> +--------------+-----------+
> | Audioslave   |      0.99 |
> | Audioslave   |      0.99 |
> | Audioslave   |      0.99 |
> | Audioslave   |      0.99 |
> | Audioslave   |      0.99 |
> | Audioslave   |      0.99 |
> | Audioslave   |      0.99 |
> | Audioslave   |      0.99 |
> | Audioslave   |      0.99 |
> | Audioslave   |      0.99 |
> | Audioslave   |      0.99 |
> | Audioslave   |      0.99 |
> | Audioslave   |      0.99 |
> | Audioslave   |      0.99 |
> | Out Of Exile |      0.99 |
> | Out Of Exile |      0.99 |
> | Out Of Exile |      0.99 |
> | Out Of Exile |      0.99 |
> | Out Of Exile |      0.99 |
> | Out Of Exile |      0.99 |
> | Out Of Exile |      0.99 |
> | Out Of Exile |      0.99 |
> | Out Of Exile |      0.99 |
> | Out Of Exile |      0.99 |
> | Out Of Exile |      0.99 |
> +--------------+-----------+
> (Output limit exceeded, 25 of 40 total rows shown)
> 
> 
> How many records are returned?
> 
> Only 25 records will be shown in the output so please look at the bottom of the output to see how many records were retrieved.
> 
> 1 / 1 point
> 

     40
> 
> Check
> 
> Correct
> 
> 3.
> 
> Question 3
> 
> All of the questions in this quiz pull from the open source Chinook Database. Please refer to the ER Diagram below and familiarize yourself with the table and column names to write accurate queries and get the appropriate answers.
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UAPENoOVEei4RQ5L9j9nDA_5042a1f0839511e8beb2b5b4ae9fa29a_ER-Diagram.png?expiry=1599350400000&hmac=IjXfLsfy8l2B4Rn58rIdTBN2_dJipWlYpf3l8cQ0_kY)
> 
> Find the first and last name of any customer who does not have an invoice. Are there any customers returned from the query?
> 
>

     select c.customerid, i.invoiceid
     
     from customers c left join invoices i 
     
     on c.customerid = i.customerid
    
     where i.invoiceid is null
> 
> 
> +------------+-----------+
> | CustomerId | InvoiceId |
> +------------+-----------+
> +------------+-----------+
> (Zero rows)
> 
> 
> 1 / 1 point
> 
>  Yes 
> 

      No 
> 
> Check
> 
> Correct
> 
> 4.
> 
> Question 4
> 
> All of the questions in this quiz pull from the open source Chinook Database. Please refer to the ER Diagram below and familiarize yourself with the table and column names to write accurate queries and get the appropriate answers.
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UAPENoOVEei4RQ5L9j9nDA_5042a1f0839511e8beb2b5b4ae9fa29a_ER-Diagram.png?expiry=1599350400000&hmac=IjXfLsfy8l2B4Rn58rIdTBN2_dJipWlYpf3l8cQ0_kY)
> 
> Find the total price for each album.
> 
>

       select unitprice * (count(*)) as total_price
       
       from tracks
       
       where tracks.albumId in
       
         (select albumId
       
          from albums
       
          where title = 'Big Ones');
> 
> 
> +-------------+
> | total_price |
> +-------------+
> |       14.85 |
> +-------------+
> 
> What is the total price for the album “Big Ones”?
> 
> 1 / 1 point
> 

     14.85
> 
> Check
> 
> Correct
> 
> 5.
> 
> Question 5
> 
> All of the questions in this quiz pull from the open source Chinook Database. Please refer to the ER Diagram below and familiarize yourself with the table and column names to write accurate queries and get the appropriate answers.
> 
> ![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/UAPENoOVEei4RQ5L9j9nDA_5042a1f0839511e8beb2b5b4ae9fa29a_ER-Diagram.png?expiry=1599350400000&hmac=IjXfLsfy8l2B4Rn58rIdTBN2_dJipWlYpf3l8cQ0_kY)
> 
> How many records are created when you apply a Cartesian join to the invoice and invoice items table?
> 
> 

     select count(*) from 
     
     invoices, invoice_items
> 
> +----------+
> | count(*) |
> +----------+
> |   922880 |
> +----------+
> 
> 
> Only 25 records will be shown in the output so please look at the bottom of the output to see how many records were retrieved.
> 
> 1 / 1 point
> 

     922880
> 
> Check
> 
> Correct
>
> -- https://www.coursera.org/learn/sql-for-data-science/quiz/KddLO/practice-quiz-writing-queries/attempt?redirectToCover=true#Tunnel Vision Close
