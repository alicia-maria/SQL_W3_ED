# SQL Order by 
- ORDER BY - is used to sort the result-set in ascending or descending order
   Syntax
  SELECT * FROM Products
  ORDER BY Price;

  SELECT column1, column2, ...
  FROM table_name
  ORDER BY column1, column2, ... ASC|DESC;

   *Keep in mind that if you do not indicate how you want the data assorted ASC/DESC - the order by Function automatically sends records in **ASCENDING ORDER**

  ## Order Alphabetically
  - For string values the ORDER BY keyword will order alphabetically
    EX
    SELECT * FROM products
    ORDER BY productnames;

  - If you was the table reverse alphabetically, use DESC keyword
    EX
    SELECT * FROM products
    ORDER BY productname DESC;

    ## ORDER BY Several Columns
    syntax
    SELECT * FROM Customers
    ORDER BY Country, CustomerName;
    In this example its going to collect data from the customer table and sort it by country and customername
    If the country repeats it will use the customername.

## Using Both ASC and DESC 
- you can sort tables if you are using more than 1 column in both ASC and DESC functions like the following example below
- syntax
  SELECT * FROM Customers
  ORDER BY Country ASC, CustomerName DESC;

  # AND Operation
  - WHERE clauses can use 1 or many AND operations
  - AND operations are used to filter records based on 1 or more conditions
    Syntax
    FROM table_name
    WHERE condition1 AND condition2 AND condition3 ...;

    EX
    SELECT *
    FROM Customers
    WHERE Country = 'Spain' AND CustomerName LIKE 'G%';

    ## AND v OR
    AND = ALL true condtions
    OR = if ANY condition is true
    *or operations mean as long as the record contains 1 true statement it will population v. and it means that if there is are more than 1 condition the record must contain ALL statements*

    ## All Constions must be true
      EX
    SELECT * FROM Customers
    WHERE Country = 'Germany'
    AND City = 'Berlin'
    AND PostalCode > 12000;
    
## Combining AND and OR 
ex
SELECT * FROM Customers
WHERE Country = 'Spain' AND (CustomerName LIKE 'G%' OR CustomerName LIKE 'R%');

SELECT * FROM Customers
WHERE Country = 'Spain' AND CustomerName LIKE 'G%' OR CustomerName LIKE 'R%';

# OR Operation
- Where at least 1 or more conditions are true
  syntax
  SELECT column1, column2, ...
  FROM table_name
  WHERE condition1 OR condition2 OR condition3 ...;

  ex
  SELECT *
  FROM Customers
  WHERE Country = 'Germany' OR Country = 'Spain';

  ## NOT Operation
  - This operation is used in combination with other operations to give opposite results also refered to as (-) negative results
  Syntax
SELECT column1, column2, ...
FROM table_name
WHERE NOT condition;

ex
SELECT * FROM Customers
WHERE NOT Country = 'Spain';

### Not Like 
SELECT * FROM Customers
WHERE CustomerName NOT LIKE 'A%';

### Not Between 
SELECT * FROM Customers
WHERE CustomerID NOT BETWEEN 10 AND 60;

### Not In
SELECT * FROM Customers
WHERE City NOT IN ('Paris', 'London');

### Not Greater Than 
SELECT * FROM Customers
WHERE NOT CustomerID > 50;

### Not Less Than 
SELECT * FROM Customers
WHERE NOT CustomerId < 50;

