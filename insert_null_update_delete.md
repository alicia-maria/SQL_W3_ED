# Insert into Statement
- INSERT INTO = are used to insert new record into a a table
 Syntax
*Option 1*
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);

*Option 2*
INSERT INTO table_name
VALUES (value1, value2, value3, ...);

*** Primary Key , when you are inserting or adding a new record you dont have to add anything to the key [ for example customerID] this is because the column is _auto-increment_ which means that it will automatically generate a number for a new records 

ex
INSERT INTO Customers (CustomerName, City, Country)
VALUES ('Cardinal', 'Stavanger', 'Norway');

INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
VALUES
('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway'),
('Greasy Burger', 'Per Olsen', 'Gateveien 15', 'Sandnes', '4306', 'Norway'),
('Tasty Tee', 'Finn Egan', 'Streetroad 19B', 'Liverpool', 'L1 0AA', 'UK');
