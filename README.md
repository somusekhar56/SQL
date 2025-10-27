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

















         










 

 
 
 

 
 


  









 

 

 

 
 













