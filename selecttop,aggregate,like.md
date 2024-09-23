## SQL SELECT TOP clause
- SELECT TOP CLAUSE is used to specify the number of records to return
- this clause is useful on large tables with thousands of records. Returning a large number of records can impact performance

** important to note that not all db systems support select top functions MYSQL support limit clauses and oracle uses FETCH FIRST n ROWS ONLY and ROWNUM

Syntax 
1. SQL server / MS Access 
SELECT TOP number/ percentage column_name(s)
FROM table_name
WHERE conditioms;

2. MYSQL
SELECT column_name(s)
FROM table_name
WHERE conditions
LIMIt #;

3. ORACLE 12
SELECT column_name(s)
FROM table_name
ORDER BY column_name(s)
FETCH FIRST number ROWS ONLY;

SQL TOP PERCENTAGE 
SELECT TOP 50 PERCENT * FROM Customers;

## SQL Aggregate Functions 
- Aggregate functions perform calculations on a set of values, and return a single value
- Most often uses the GROUP BY clause of SELECT statement
- GROUP BY split the result-set into group of values and aggregate function can be used to return a single value for each group

  Most Common aggregated functions
  1. MIN() - smallest values return within columns 
  2. MAX() - largest value return within columns
  3. COUNT() - returns number of rows in a set
  4. SUM () - total of a numerical value
  5. AVG() - returns average value of numerical columns
 
     *aggregate functions ignore null values **except count()**

     ## MAX and MIN functions
Syntax ex
SELECT MIN (price)
FROM products; 

SELECT MAX (price)
FROM products; 

SELECT MIN/MAX (column_name)
FROM table_name
WHERE conditions; 

ALIAS 
SELECT MIN(price) AS smallestprice
FROM products;












     

