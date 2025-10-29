# 1 Relational Database Basics:
# 1.1 Database
A database is an organized collection of data that can be easily stored, accessed, and managed.
For example, an online shopping site stores:
* Customer data
* Product details
* Orders and payments
  All of these are stored in a database.
 # 1.2 Relational Database:
 A Relational Database (RDB) stores data in the form of tables (relations).
* Each table consists of:
  * Rows (records): each row represents one item (e.g., one customer)
  * Columns (fields): each column represents one attribute (e.g., customer name, ID).
  The term “relational” comes from how data in one table relates to data in another.
# 2 Database Management System (DBMS)
A Database Management System (DBMS) is software that helps store, organize, manage, and retrieve data efficiently from a database.
A DBMS acts as a bridge between the user and the database.
 # 3 SQL Syntax:
 SQL syntax is the set of rules that define how SQL statements are written and executed to interact with a database.It’s like grammar for the SQL language.
# 4 DDL:
DDL stands for Data Definition Language.It deals with defining and managing the structure of database objects.
# CREATE
<img width="986" height="417" alt="image" src="https://github.com/user-attachments/assets/777743bc-ddcf-4b68-b700-2c6a217cf99d" />

# ALTER
The ALTER TABLE command is used to modify the structure of an existing table.
<img width="985" height="462" alt="image" src="https://github.com/user-attachments/assets/d172b739-128d-476a-9b77-336e243a396b" />

# DROP
Deletes a database or table permanently
<img width="985" height="433" alt="image" src="https://github.com/user-attachments/assets/23a44bf5-deae-4b05-9013-8e9b629e7dcb" />

# TRUNCATE
Removes all data from a table (structure remain
The TRUNCATE command is used to delete all the rows (data) from a table, but the table structure (columns, constraints, etc.) remains the same.
<img width="982" height="417" alt="image" src="https://github.com/user-attachments/assets/c29a9072-1f6c-455d-a1b6-ba045f733462" />
# DML:
DML stands for Data Manipulation Language.It is used to manipulate the data stored inside database tables that means adding, changing, and deleting records.
# INSERT
 The INSERT statement is used to add new data into a table in a database.
 INSERT INTO student_details (id, name, phone, marks, city, email)
VALUES
* (2, 'Tarak', '2567489', 86, 'Madanapalli', 'abcde@gmail.com'),
* (3, 'Ram', '1234567890', 65, 'Tirupathi', '1234567@gmail.com'),
* (4, 'Priya', '9876543210', 75, 'Chennai', 'priya@gmail.com');

 # UPDATE
 The UPDATE statement is used to change existing data in a table.You can update one or more columns for one or more rows using a WHERE clause
 UPDATE student_details
* SET marks = 90
* WHERE id = 1;
 # DELETE
 The DELETE statement is used to remove one or more rows from a table based on a condition.
 DELETE FROM student_details
WHERE id = 3;
# SELECT
The SELECT statement is used to retrieve data from a database table.
SELECT * 
FROM student_details
ORDER BY marks DESC
# DCL (Data Control Language):
It is used to control access to the data in the database who can view, modify, or manage data.In simple words, DCL commands deal with database security and user permissions.
 # GRANT
 Gives permission to a user to perform actions
 # REVOKE
 Removes permission from a user
 # 7 DQL (Data Query Language):
 It is used to fetch or retrieve data from the database.
 * SELECT Used to retrieve data from one or more tables
 # 7.1 Aggregating data
 # 7.1.1 COUNT()
 COUNT() is an aggregate function that returns the number of rows that match a specified condition.It’s often used to count rows, records, or values in a table.
* SELECT COUNT(*) 
* FROM student_details;
 # 7.1.2 SUM()
 SUM() is used to calculate the total sum of numeric values in a column.It’s commonly used to add up numbers, such as marks, salaries, or prices.
 <img width="973" height="480" alt="image" src="https://github.com/user-attachments/assets/690dd8c0-e8b1-4d55-b9e8-aac396d62752" />
 # 7.1.4 MIN()
 MIN() is used to find the smallest (minimum) value in a column.It’s commonly used on numeric, date, or even text columns.
 <img width="990" height="425" alt="image" src="https://github.com/user-attachments/assets/6c3512a0-7dce-4fcd-a22f-858d1de75ddc" />
 # 7.1.5 MAX()
 MAX() is used to find the largest (maximum) value in a column. It’s commonly used on numeric, date, or text columns.
 * SELECT MAX(name) AS last_name_alphabetically
 * FROM student_details;
   # 7.2 Group by:
The GROUP BY clause is used to group rows that have the same values in one or more columns.It is usually used with aggregate functions like SUM(), COUNT(), AVG(), MAX(), MIN() to summarize data.
# 7.3 Having clause:
The HAVING clause in SQL is used to filter groups of records created by the GROUP BY clause.Unlike WHERE, which filters individual rows, HAVING filters aggregated data (like SUM, COUNT, AVG, MAX, MIN).
# 7.4 Order by:
The ORDER BY clause is used to sort the result set of a query.By default, it sorts in ascending order (ASC). You can also sort in descending order (DESC).It can sort by one or more columns.
# 8 TCL(Transcation Control Language):
TCL stands for Transaction Control Language.It is used to manage transactions in SQL.
# 8.1 COMMIT
Saves all the changes made in the current transaction permanently.
# 8.2 ROLLBACK
ROLLBACK is a SQL command used to undo changes made in the current transaction.
* It is usually used after INSERT, UPDATE, or DELETE commands.
* It reverts the database to the state before the transaction started.
* Works only when a transaction is active (i.e., after BEGIN TRANSACTION or in databases with autocommit off).
  # 8.3 SAVEPOINT
  SAVEPOINT allows you to set a point within a transaction that you can roll back to without undoing the entire transaction.
  * Think of it like a “checkpoint” in a video game: if you make a mistake, you can go back to this point instead of starting over.
  * It is useful when a transaction has multiple steps and you might want to undo some changes but not all.
 # 9 Constraints:
Constraints are rules applied to table columns to enforce data integrity.They ensure the accuracy and reliability of the data in the database.Constraints can be applied when creating a table or altering a table.
# 9.1 NOT NULL
Ensures that a column cannot have NULL values.
# 9.2 UNIQUE
Ensures that all values in a column are unique.
#9.3 PRIMARY KEY
Uniquely identifies each row in a table. Cannot be NULL.
# 9.4 FOREIGN KEY
Ensures the value in a column matches a value in another table, enforcing referential integrity.
# 9.5 CHECK
Ensures that column values meet a specific condition
# 10 JOINS:
A JOIN in SQL is a clause that retrieves data by linking rows from multiple tables based on a common column.To combine related data from different tables,avoid data duplication (normalize the database) and retrieve meaningful results by connecting tables.

# We using these two tables:
<img width="1006" height="607" alt="image" src="https://github.com/user-attachments/assets/4aca3b6d-1c09-4ea3-bbae-d0f3d7186131" />

# 10.1 INNER JOIN:
Returns only the rows that have matching values in both tables.

# 10.2 LEFT JOIN:
Returns all rows from the left table and matching rows from the right table. If there’s no match, it shows NULL for the right table columns.
All rows from the left table (first table in the query),and the matching rows from the right table (second table in the query).If there is no match, the result will show NULL for columns from the right table.

# 10.3 RIGHT JOIN:
Returns all rows from the right table and matching rows from the left table. If there’s no match, it shows NULL for the left table columns.

# 10.4 FULL JOIN:
Returns all rows from both tables. Rows without a match in the other table will show NULL.

# 10.5 CROSS JOIN:
Returns all possible combinations of rows from both tables (Cartesian product).

# 11 SQL Operator:
An SQL operator is a symbol or keyword used to perform operations on data in SQL queries. Operators are used in conditions, calculations, and logical expressions to filter, compare, or manipulate data.

# 11.1 Arithmetic Operators:
Used for mathematical calculations like Addition,Subtraction,Multiplication and Division .
<img width="1119" height="607" alt="image" src="https://github.com/user-attachments/assets/5a1bf1b6-1b3e-40d3-95ff-1c64e6cc164b" />

# 11.2 Comparison Operators:
Comparison (or Relational) operators are used to compare two values in SQL.They are mostly used in the WHERE clause to filter rows from a table.
Used to compare values in conditions.
= Equal to WHERE Salary = 50000
!= or <> Not equal to WHERE Salary <> 50000
Greater than WHERE Salary > 50000
< Less than WHERE Salary < 50000
= Greater than or equal to WHERE Salary >= 50000
<= Less than or equal to WHERE Salary <= 50000

# 11.3 Logical Operator:
Used to combine multiple conditions.

# AND
Both conditions must be true WHERE DeptID = 101 AND Salary > 50000
<img width="999" height="295" alt="image" src="https://github.com/user-attachments/assets/ef36f341-2e26-4d53-98c1-55a9f669ea4a" />
# OR
Either condition can be true WHERE DeptID = 101 OR Salary > 50000
<img width="984" height="280" alt="image" src="https://github.com/user-attachments/assets/e4200be2-20a3-40e1-a66b-85711fb6b64b" />
OR
Either condition can be true WHERE DeptID = 101 OR Salary > 50000
<img width="1012" height="296" alt="image" src="https://github.com/user-attachments/assets/3ba24392-9431-41b7-ba96-a529f59520ec" />
# 12 Procedures:
A Stored Procedure in SQL is a precompiled group of SQL statements (like SELECT, INSERT, UPDATE, etc.) that are stored in the database and can be executed whenever needed.It helps improve performance, reusability, security, and modularity in database operations.
# 12.1CREATE PROCEDURE:
Used to create a new stored procedure for the first time.
<img width="978" height="491" alt="image" src="https://github.com/user-attachments/assets/42c9981d-059e-44d1-8e3f-65e8e2717936" />

# ALTER PROCEDURE:
Used to modify or update an existing stored procedure (instead of dropping and recreating it).
<img width="1000" height="509" alt="image" src="https://github.com/user-attachments/assets/8ed980c2-4684-4f5f-93e8-2b5cbccedce8" />

# DROP PROCEDURE:
Used to delete (remove) an existing stored procedure permanently.
DROP PROCEDURE is a Data Definition Language (DDL) command that permanently removes a stored procedure from the database.
<img width="1015" height="289" alt="image" src="https://github.com/user-attachments/assets/4e7c74f4-4c3e-4afa-ad1e-0a15ffe1bd5b" />

# EXECUTE Procedure:
Used to run (or call) a stored procedure.
The EXECUTE (or shorthand EXEC) command is used to run a stored procedure that you created using CREATE PROCEDURE.
<img width="961" height="454" alt="image" src="https://github.com/user-attachments/assets/10020a1d-6349-4797-bbf7-b7c67c754c10" />

# 13 Subquery:
A subquery is a query inside another query — it can be in the SELECT, FROM, or WHERE clause.A Subquery (or inner query) is a query inside another query.
SELECT column_name
FROM table_name
WHERE column_name operator (SELECT column_name FROM another_table WHERE condition);

# CTE:(Common Table Expression)
A CTE is like a named temporary result set that exists only for the duration of a single query.It makes queries cleaner, reusable, and easier to read compared to subqueries.
A CTE (Common Table Expression) is a temporary result set that you can reference within a single SQL statement.

WITH cte_name AS (
    SELECT column1, column2, ...
    FROM table_name
    WHERE condition
)
SELECT *
FROM cte_name
WHERE some_condition;

# Views:
A View is a virtual table that is based on the result of an SQL query.It doesn’t store data physically, but instead stores a query that pulls data from one or more tables.So, when you query a view, SQL runs the query behind the scenes and shows you the result like a table.

# Create view:

The CREATE VIEW command is used to create a virtual table based on the result of a SQL query.
CREATE VIEW view_name AS
SELECT column1, column2, ...
FROM table_name
WHERE condition;

# DROP VIEW:

Used to delete a view permanently from the database.
The DROP VIEW statement permanently deletes a view definition from the database.
After dropping, the view can no longer be queried or referenced — though the base tables remain unaffected.

DROP VIEW view_name;

CREATE VIEW HighSalaryEmployees AS
SELECT EmpName, Department, Salary
FROM Employee_Details
WHERE Salary > 55000;































































         










 

 
 
 

 
 


  









 

 

 

 
 













