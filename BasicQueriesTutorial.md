# Writing basic SQL Queries against a prepopulated database using Google Chrome
- VisitSQL Try Editor at W3Schools[https://www.w3schools.com/Sql/tryit.asp?filename=trysql_select_top]

## To view the Database and Table
- In chrome browser,
- Right-click then select `Inspect` 
- Find the tool `Application` 

- In the left panel, 
- `Storage > Web SQL > W3SchoolsDemoDatabase`


## Write SQL queries for the following requirements:

### Find all customers that live in London. Returns 6 records.
- SELECT * FROM Customers 
- WHERE City = 'London';


### Find all customers with postal code 1010. Returns 3 customers.
- SELECT * FROM customers 
- WHERE PostalCode = '1010';

### Find the phone number for the supplier with the id 11. Should be (010) 9984510
- SELECT * FROM Customers 
- WHERE CustomerID = '11';

### List orders descending by the order date. The order with date 1997-02-12 should be at the top.
-SELECT OrderDate
-FROM Orders
-ORDER BY '1997-02-12' DESC;

### Find all suppliers who have names longer than 20 characters. You can use length(SupplierName) to get the length of the name. Returns 11 records.
-SELECT SupplierName
-FROM Suppliers
-WHERE LENGTH(SupplierName)>=20;

### Find all customers that include the word "market" in the name. Should return 4 records.
-SELECT * FROM Customers
-WHERE CustomerName LIKE('%market%');

