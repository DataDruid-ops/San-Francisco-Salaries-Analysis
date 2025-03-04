# Employee Salary Analysis

## Overview
This project focuses on analyzing employee salary data using SQL queries to answer key questions related to job titles, base pay, overtime pay, and total compensation.

## Data Questions and Queries

1. **Show the number of employees in the table**
   ```sql
   SELECT COUNT(*) AS total_employees FROM employees;
   ```

2. **Show the unique job titles in the table**
   ```sql
   SELECT DISTINCT job_title FROM employees;
   ```

3. **Show the job title and overtime pay for all employees with overtime pay greater than 50,000**
   ```sql
   SELECT job_title, overtime_pay FROM employees WHERE overtime_pay > 50000;
   ```

4. **Show the average base pay for all employees**
   ```sql
   SELECT AVG(base_pay) AS avg_base_pay FROM employees;
   ```

5. **Show the top 10 highest paid employees**
   ```sql
   SELECT * FROM employees ORDER BY total_pay DESC LIMIT 10;
   ```

6. **Show the average of BasePay, OvertimePay, and OtherPay for each employee**
   ```sql
   SELECT employee_name, (base_pay + overtime_pay + other_pay)/3 AS avg_pay FROM employees;
   ```

7. **Show all employees who have the word "Manager" in their job title**
   ```sql
   SELECT * FROM employees WHERE job_title LIKE '%Manager%';
   ```

8. **Show all employees with a job title not equal to "Manager"**
   ```sql
   SELECT * FROM employees WHERE job_title <> 'Manager';
   ```

9. **Show all employees with a total pay between 50,000 and 75,000**
   ```sql
   SELECT * FROM employees WHERE total_pay BETWEEN 50000 AND 75000;
   ```

10. **Show all employees with a base pay less than 50,000 or a total pay greater than 100,000**
    ```sql
    SELECT * FROM employees WHERE base_pay < 50000 OR total_pay > 100000;
    ```

11. **Show all employees with a total pay benefits value between 125,000 and 150,000 and a job title containing the word "Director"**
    ```sql
    SELECT * FROM employees WHERE total_pay_benefits BETWEEN 125000 AND 150000 AND job_title LIKE '%Director%';
    ```

12. **Show all employees ordered by their total pay benefits in descending order**
    ```sql
    SELECT * FROM employees ORDER BY total_pay_benefits DESC;
    ```

13. **Show all job titles with an average base pay of at least 100,000 and order them by the average base pay in descending order**
    ```sql
    SELECT job_title, AVG(base_pay) AS avg_base_pay FROM employees GROUP BY job_title HAVING avg_base_pay >= 100000 ORDER BY avg_base_pay DESC;
    ```

14. **Delete the notes column**
    ```sql
    ALTER TABLE employees DROP COLUMN notes;
    ```

15. **Update the base pay of all employees with the job title containing "Manager" by increasing it by 10%**
    ```sql
    UPDATE employees SET base_pay = base_pay * 1.10 WHERE job_title LIKE '%Manager%';
    ```

16. **Delete all employees who have no overtime pay**
    ```sql
    DELETE FROM employees WHERE overtime_pay = 0 OR overtime_pay IS NULL;
    ```

## How to Use
1. Clone this repository.
2. Load the dataset into your SQL database.
3. Run the provided queries to analyze the data.
4. Modify or extend the queries as needed to gain deeper insights.


## Contributing
If you would like to contribute, feel free to submit a pull request with your enhancements.





