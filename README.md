# SQL Cheatsheet by Adam Jean-Laurent (Work In Progress)
Most Of The Information Pulled From: [W3Schools](https://www.w3schools.com/sql/default.asp)

### Most Important SQL Commands
```sql
-- Extracts data from a database
SELECT
-- Updates data in a database
UPDATE
-- Deletes data from a database
DELETE
-- inserts new data into a database
INSERT INTO
-- creates a new database 
CREATE DATABASE
 --modifies a table
ALTER TABLE
--deletes a table
DROP TABLE
--creates an index(search key)
CREATE INDEX
 --deletes an index
DROP INDEX
```

## SELECT
```sql
--Select All Records From A Table
SELECT * FROM TableName;

--Select Certain Columns From A Table
SELECT column1, column2 ... FROM TableName;

--This Would Select The CustomerName And City Columns From The Customers Table
ex. SELECT CustomerName, City FROM Customers;

--The DISTINCT key word selects only distinct values

--Selects Only Distinct Values From The Country Column In The Customers Table
SELECT DISTINCT Country FROM Customers;

--Returns The Number Of Distinct Countries In The Customers Table
SELECT COUNT(DISTINCT Country) FROM Customers;
```

## WHERE

```sql
-- The Where Clause Is Used To Extract  Only Records That Fulfill A Specified Condition

ex. SELECT column1, column2 FROM tableName WHERE condition;

-- The WHERE clause is not only used in SELECT Statements, it is also used in UPDATE, DELETE etc.

-- selects all the customers from the country 'Mexico' in the Customers table
SELECT * FROM Customers WHERE Country ='Mexico';

-- WHERE Clauses can be combined with AND, OR, and NOT operators

SELECT column1, column2 FROM tableName WHERE condition1 AND condition2 AND condition3;

SELECT column1, column2 FROM tableName WHERE condition1 OR condition2 OR condition3;

SELECT column1, column2 FROM tableName WHERE  NOT condition1;

-- They can be combined together as well,

SELECT * FROM Customers WHERE Country = 'Germany' AND (City = 'Berlin' OR City = 'Munchen'); 

```
