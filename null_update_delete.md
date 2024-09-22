## Null Values 
- Null values is a field with no value
- Null values are ones that have been left blank during record creation!

  ## How to Test for NULL values
  it is not possible to test for Null values with comparison operations, such as +,<,>, or <>
  We will have to use the [ IS NULL ] and [ IS NOT NULL] Operations instead

Syntax 
SELECT column_names
FROM table_name
WHERE column_name IS NULL;

SELECT column_names
FROM table_name
WHERE column_name IS NOT NULL;

IS Null operation is used to test for empty values 

IS NOT NULL operation is used to test for non-empty values 

## SQL update statement 
-update is used to modifty the exsisting records in a table 

Syntax 
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;

UPDATE Customers
SET ContactName = 'Alfred Schmidt', City= 'Frankfurt'
WHERE CustomerID = 1;

## updating multiple records 
Where clause that determines how many records will be updated
UPDATE Customers
SET ContactName='Juan'
WHERE Country='Mexico';

## SQL Delete Statement 
-Delete statement is used to delete exsisting records in qa table 

Syntax 
DELETE FROM table_name WHERE condition;

DELETE FROM Customers WHERE CustomerName='Alfreds Futterkiste';

## Delete All Records 
it is possible to delete all rows in a table without deleting the table 
this means that the table structure , attribute, and index will be intact 

syntax
DELETE FROM table_name;


DROP TABLE Customers;
