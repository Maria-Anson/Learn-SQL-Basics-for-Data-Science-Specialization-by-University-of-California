## Module 2 Practice Quiz
> 
> Total points 11
> 
> 1.
> 
> Question 1
> 
> For all the questions in this practice set, you will be using the _Salary by Job Range Table_. This is a single table titled: salary_range_by_job_classification. This table contains the following columns:
> 
> *   SetID
> *   Job_Code
> *   Eff_Date
> *   Sal_End_Date
> *   Salary_setID
> *   Sal_Plan
> *   Grade
> *   Step
> *   Biweekly_High_Rate
> *   Biweekly_Low_Rate
> *   Union_Code
> *   Extended_Step
> *   Pay_Type
> 
> Please refer to this information to write queries to answer the questions. **Are you ready to get started?**
> 
> 1 / 1 point
> 

      Yes, I am ready to begin. 
> 
>  No, I am not ready to begin. 
> 
> Check
> 
> Correct
> 
> Great, let's get started!
> 
> 2.
> 
> Question 2
> 
> Find the distinct values for the extended step. The code has been started for you, but you will need to program the third line yourself before running the query.
> 
> 
> SELECT distinct Extended_step
> 
> from salary_range_by_job_classification
> 
> +---------------+
> | Extended_Step |
> +---------------+
> | 0             |
> | 11            |
> | 6             |
> | 2             |
> +---------------+
> 
> 
> Which of the following values is not a distinct value?
> 
> 1 / 1 point
> 
>  6 
> 
>  2 
> 

      5 
> 
>  11 
> 
>  0 
> 
> Check
> 
> Correct
> 
> Here is what you should have in your script. If you programmed correctly, you will have seen that this number is not a distinct value.
> 
> SELECT 
> 
> distinct Extended_step
> 
> from salary_range_by_job_classification;
> 
> 
> 3.
> 
> Question 3
> 
> Excluding $0.00, what is the minimum bi-weekly high rate of pay _(please include the dollar sign and decimal point in your answer)_? The code has been started for you, but you will need to add onto the last line of code to get the correct answer.
> 
>
> Select 
> 
> min(Biweekly_high_Rate)
> 
> From salary_range_by_job_classification where Biweekly_High_Rate <> '$0.00'
>
> 
> +-------------------------+
> | min(Biweekly_high_Rate) |
> +-------------------------+
> | $100.00                 |
> +-------------------------+
> 
> 
> 1 / 1 point
> 

     $100.00
> 
> Check
> 
> Correct
> 
> Great job! You knew how to complete the query to find the answer!
> 
> 4.
> 
> Question 4
> 
> What is the maximum biweekly high rate of pay (_please include the dollar sign and decimal point in your answer_)? The code has been started for you, but you will need to add onto the last line of code to get the correct answer.
> 
> 
> SELECT 
> 
> max(Biweekly_high_Rate) 
> 
> From salary_range_by_job_classification
> 
> +-------------------------+
> | max(Biweekly_high_Rate) |
> +-------------------------+
> | $9726.38                |
> +-------------------------+
> 
> 
> 1 / 1 point
> 

     $9726.38
> 
> Check
> 
> Correct
> 
> Great job! You knew how to complete the query to find the answer!
> 
> 5.
> 
> Question 5
> 
> What is the pay type for all the job codes that start with '03'? The code has been started for you, but you will need to program the fourth and fifth lines yourself before running the query.
> 
> 
> Select
> 
> job_code, pay_type from salary_range_by_job_classification
> 
> where job_code like '03%'
> 
> 
> +----------+----------+
> | Job_Code | Pay_Type |
> +----------+----------+
> | 0380     | B        |
> | 0381     | B        |
> | 0382     | B        |
> | 0390     | B        |
> | 0395     | B        |
> | 0380     | B        |
> | 0381     | B        |
> | 0382     | B        |
> +----------+----------+
> 
> 
> 1 / 1 point
> 

     B
> 
> Check
> 
> Correct
> 
> Great job! You knew how to complete the query to find the answer!
> 
> 6.
> 
> Question 6
> 
> Run a query to find the Effective Date (eff_date) or Salary End Date (sal_end_date) for grade Q90H0? The code has been started for you, but you will need to program the third through the sixth lines yourself before running the query.
> 
> 
> Select eff_Date, sal_end_date from salary_range_by_job_classification
> 
> where grade = 'Q90H0'
> 
> 
> +------------------------+------------------------+
> | Eff_Date               | Sal_End_Date           |
> +------------------------+------------------------+
> | 12/26/2009 12:00:00 AM | 06/30/2010 12:00:00 AM |
> +------------------------+------------------------+
> 
> 
> What is the _**Salary End Date**_ (sal_end_date) for grade Q90H0? _(Enter date format as follows: mm/dd/yyyy)_
> 
> 1 / 1 point
> 

     06/30/2010
> 
> Check
> 
> Correct
> 
> Great job! You knew how to complete the query to find the answer!
> 
> 7.
> 
> Question 7
> 
> Sort the Biweekly low rate in ascending order. There is no starter code, as you need to write and run the query on your own. _Hint: there are 4 lines to run this query._
> 
> 
> select Biweekly_low_Rate 
> 
> from salary_range_by_job_classification
> 
> order by Biweekly_low_Rate asc
> 
> +-------------------+
> | Biweekly_Low_Rate |
> +-------------------+
> | $0.00             |
> | $0.00             |
> | $0.00             |
> | $0.00             |
> | $100.00           |
> | $100.00           |
> | $10059.00         |
> | $10376.00         |
> | $1052.00          |
> | $10630.00         |
> | $10843.00         |
> | $1088.00          |
> | $1112.00          |
> | $11255.00         |
> | $11405.00         |
> | $1162.00          |
> | $12120.77         |
> | $1280.00          |
> | $1284.00          |
> | $1298.00          |
> | $1299.00          |
> | $1381.00          |
> | $1384.00          |
> | $1405.00          |
> | $1464.00          |
> +-------------------+
> (Output limit exceeded, 25 of 1356 total rows shown)
> 
> **Are these values properly sorted?**
> 
> 1 / 1 point
> 

      No 
> 
>  Yes 
> 
> Check
> 
> Correct
> 
> Because this is a varchar field. Here is what your query should have looked like:
> 
> 
> Select
> 
> biweekly_low_rate
> 
> From salary_range_by_job_classification
> 
> order by biweekly_low_rate asc
> 
> 
> 8.
> 
> Question 8
> 
> Write and run a query, with no starter code to answer this question: **What Step are Job Codes 0110-0400?** _Hint: there are 6 lines to run this query._
> 
>
> select step, job_code
> 
> from salary_range_by_job_classification
> 
> where job_code between 0110 and 0400
> 
> +------+----------+
> | Step | Job_Code |
> +------+----------+
> | 1    | 1107     |
> | 1    | 1110     |
> | 1    | 1117     |
> | 1    | 1118     |
> | 1    | 1120     |
> | 1    | 1130     |
> | 1    | 1142     |
> | 1    | 1160     |
> | 1    | 1161     |
> | 1    | 1163     |
> | 1    | 1164     |
> | 1    | 1190     |
> | 1    | 1201     |
> | 1    | 1202     |
> | 1    | 1203     |
> | 1    | 1204     |
> | 1    | 1209     |
> | 1    | 1210     |
> | 1    | 1218     |
> | 1    | 1220     |
> | 1    | 1222     |
> | 1    | 1224     |
> | 1    | 1226     |
> | 1    | 1227     |
> | 1    | 1229     |
> +------+----------+
> (Output limit exceeded, 25 of 540 total rows shown)
> 
> 
> 1 / 1 point
> 

     1
> 
> Check
> 
> Correct
> 
> Great job! You knew how to complete the query to find the answer!
> 
> 9.
> 
> Question 9
> 
> Write and run a query, with no starter code or hints to answer this question: **What is the Biweekly High Rate minus the Biweekly Low Rate for job Code 0170?**
> 
> 
> select Biweekly_high_Rate - Biweekly_low_Rate as diff , job_code
> 
> from salary_range_by_job_classification
> 
> where job_code = '0170'
> 
> 
> +------+----------+
> | diff | Job_Code |
> +------+----------+
> |    0 | 0170     |
> +------+----------+
> 
> 
> 1 / 1 point
> 

     0
> 
> Check
> 
> Correct
> 
> Great job! You knew how to complete the query to find the answer!
> 
> 10.
> 
> Question 10
> 
> Write and run a query, with no starter code or hints to answer this question: **What is the Extended Step for Pay Types M, H, and D?**
> 
> 
> select Extended_Step, pay_type
> 
> from salary_range_by_job_classification
> 
> where pay_type in ('M','H','D')
> 
> 
> +---------------+----------+
> | Extended_Step | Pay_Type |
> +---------------+----------+
> | 0             | D        |
> | 0             | D        |
> | 0             | D        |
> | 0             | M        |
> | 0             | D        |
> | 0             | D        |
> | 0             | M        |
> | 0             | H        |
> | 0             | H        |
> | 0             | H        |
> | 0             | H        |
> | 0             | H        |
> | 0             | H        |
> | 0             | H        |
> | 0             | H        |
> +---------------+----------+
> 
> 
> 1 / 1 point
> 

     0
> 
> Check
> 
> Correct
> 
> Great Job! You knew how to complete the query to find the answer.
> 
> 11.
> 
> Question 11
> 
> Write and run a query, with no starter code or hints to answer this question: **What is the step for Union Code 990 and a Set ID of SFMTA or COMMN?**
> 
> 
> select step, setid 
> 
> from salary_range_by_job_classification
> 
> where (Union_Code = 990) and (setid = 'SFMTA' or setid = 'COMMN') 
> 
> 
> +------+-------+
> | Step | SetID |
> +------+-------+
> | 1    | COMMN |
> +------+-------+
> 
> 
> 1 / 1 point
> 

     1
> 
> Check
> 
> Correct
> 
> Great job! You were able to complete the query to find the answer.
>
> -- https://www.coursera.org/learn/sql-for-data-science/quiz/vzUpi/module-2-practice-quiz/attempt?redirectToCover=true#Tunnel Vision Close
