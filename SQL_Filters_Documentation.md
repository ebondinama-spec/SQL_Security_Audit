Apply filters to SQL queries
Project description
[As a security professional it's my duty to secure the organization's systems. I investigated security issues that involve employee machines and login attempts that occurred after office hours at ‘18:00’ and used SQL filters to retrieve various  data  and investigate the potential security issues .]
Retrieve after hours failed login attempts
[To retrieve after hours failed login attempts i used the SQL  syntax  which are rules that determine what's correctly structured and the keywords, clauses, functions and operators to format a SQL statement.

SELECT *  
FROM    log_ in_ attempts 
WHERE  login_attempts  > ‘18:00’ AND success = FALSE;   

This query returns all failed login attempts after office hours end at‘18:00’
The syntax icon * placed after the keyword SELECTrefers to select all data from  log_in_attempts
Specific conditions after keyword WHERE return all records having value in the  login_time column] 
Retrieve login attempts on specific dates
[My team investigated a login attempt that occurred on a specific day. To find all login attempts on a specific date on '2022-05-09' or day  before '2022-05-08'  my team used the OR operator  to retrieve login attempts on specific dates. 

SELECT *
FROM     log_in_attempts 
WHERE   login_dates  = '2022-05-09' OR  login_date = '2022-05-08' ;

This query returns all login attempts made on specific dates .The icon *  placed after the keyword SELECT indicates select all FROM log_in_attempts,the WHERE indicates the conditions for a filter  and specific conditions are listed using the OR operator  that connects two conditions specifying that both conditions can be met ]
Retrieve login attempts outside of Mexico
[Our security professional team also investigated login attempts that were suspicious which seem to originate outside of Mexico. To retrieve the login attempts outside Mexico ,we ran a SQL statement as follows:

SELECT *  
FROM    log_in_attempts 
WHERE  NOT country LIKE  ‘MEX’ % ;

This SQL query retrieves all columns from the log_in_attempts table outside  of Mexico.The NOT operator works on a single condition, negates a condition and SQL returns every entry where  login attempts are not from Mexico. Our SQL query involves a pattern with the sign %, we use the LIKE operator which is similar to = sign  with the WHERE clause.]
Retrieve employees in Marketing
[Our security professional team performed security updates on specific employee machines in the Marketing department.We identified all employees in the Marketing department for all offices in the East building by running a SQL statement as follows :

SELECT *
FROM     employees
WHERE  department = ‘Marketing’ AND office LIKE ‘East%’ ;

This SQL query retrieves all information about all the employees in the Marketing department for offices in the East building.The AND  is a logical operator used to filter on two conditions in the WHERE clause and specifies that both conditions must be met simultaneously .The LIKE operator is used with the WHERE clause to filter for pattern  East%
In the office east buildings.]
Retrieve employees in Finance or Sales
[A different security update on machines for employees was made by our cyber security team to identify all employees in the Sales or Finance departments .To retrieve records of employees in the 'Finance' or the 'Sales' department ,we ran a SQL statement as follows:

SELECT *
FROM   employees
WHERE department = 'Finance' OR department =  'Sales’; 

This SQL query retrieves all employees in the Finance and Sales department. The  OR operator connects two conditions in the WHERE clause and specifies that either condition can be met.The OR operator returns results where the first and second conditions in the WHERE clause are both met. ]
Retrieve all employees not in IT
[Our security professional team was tasked to obtain information about employees who are not in the IT department.To retrieve all employees who are not in the IT department ,We ran SQL statements as follows : 


SELECT *
FROM    employees
WHERE   NOT department =  ‘information technology’;

This SQL query returns all employees who at not in the IT department, The keyword SELECT * indicates select all from the employees department, the NOT operator is used directly after the WHERE clause and works on a single condition it returns record that do not meet the specified conditions  ]
Summary
[We ran a SQL query and applied filters AND, OR, NOT to obtain specific information about employees, their machines, and the departments they belong to from the database. We also used the LIKE operator to search for patterns with the % sign.]

## 🛠️ Deployment and Version Control (Git) Notes

To ensure this project was deployed correctly, I overcame significant version control challenges:

* **Challenge:** Resolved complex file path and directory structure conflicts in the Linux command-line environment (CLI) during initial uploads.
* **Solution:** Demonstrated strong command-line proficiency by executing robust cleanup and verification, leading to a successful and clean repository structure.
* **Authentication & Security:** Mastered the use of advanced Git authentication by configuring and utilizing a **Personal Access Token (PAT)** for secure remote pushing to GitHub.
