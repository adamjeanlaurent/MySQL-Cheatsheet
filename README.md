# SQL Cheatsheet by Adam Jean-Laurent

### Most Important SQL Commands
<<<<<<< HEAD
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
CREATE DATABASE`
 --modifies a table
ALTER TABLE
--deletes a table
DROP TABLE
--creates an index(search key)
CREATE INDEX
 --deletes an index
DROP INDEX
```
=======

Extracts data from a database
`sql SELECT`

Updates data in a database
`UPDATE`

deletes data from a database
`DELETE`

inserts new data into a database
`INSERT INTO` 

creates a new database 
`CREATE DATABASE` 

 modifies a table
`ALTER TABLE`

deletes a table
`DROP TABLE`

creates an index(search key)
`CREATE INDEX`

 deletes an index
`DROP INDEX`

>>>>>>> 4b952c0bac153fc4e7b5707b710911ab6bd9f332
## SELECT
```sql
--Select All Records From A Table

<<<<<<< HEAD
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
=======
Select All Records From A Table

`SELECT * FROM TableName;`

Select Certain Columns From A Table

`SELECT column1, column2 ... FROM TableName;`

This Would Select The CustomerName And City Columns From The Customers Table

`ex. SELECT CustomerName, City FROM Customers;`

The DISTINCT key word selects only distinct values

Selects Only Distinct Values From The Country Column In The Customers Table

`SELECT DISTINCT Country FROM Customers;`

Returns The Number Of Distinct Countries In The Customers Table

`SELECT COUNT(DISTINCT Country) FROM Customers;`

>>>>>>> 4b952c0bac153fc4e7b5707b710911ab6bd9f332
## WHERE
