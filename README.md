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
## INSERT INTO

```sql
-- The INSERT INTO statement is used to insert new records in a table

-- Can be written in two ways, if you're inserting into only some columns, specify by name, if you're inserting into all columns, you don't have to specify the columns name, but be sure to order the values in the correct order.

-- First Way
-- Insert val1 into col1. val2 into col2, etc...
INSERT INTO tableName (column1, column2, column3) VALUES (value1, value2, value3);

-- Second Way
-- Same outcome as the first way assuming there are only three columns in the table
INSERT INTO tableName VALUES(value1, value2, value3);

-- ex.
INSERT INTO Customers (Name, Age) VALUES ("Adam", "22");
```

## MISC 
```sql
-- NULL VALUES

-- Fields that are optional may contain NULL values
-- Can Query with IS NULL & IS NOT NULL
-- ex. 
SELECT (Age, Name) FROM Customers WHERE Name IS NULL;
SELECT (AGE, Name) FROM Customers WHERE Name IS NOT NULL;
```

## UPDATE
```sql
--- The UPDATE statement is used to modify the existing records in table
-- This example changes the name and age of the record with ID = 1.
UPDATE Customers SET Name = "Adam JL", age = "21" WHERE ID = 1;

-- Be careful! If you omit the WHERE clause every record will be updated!

-- You can also update multiple records at a time if you wanted
-- This example changes every customer with the name Adam to John.
UPDATE Customers SET Name = "Adam" WHERE Name = "John";
```