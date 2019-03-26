# Stretch

### Add a customer record for _"The Shire"_, the contact name is _"Bilbo Baggins"_ the address is _"1 Hobbit-Hole"_ in _"Bag End"_, postal code _"111"_ and the country is _"Middle Earth"_.

- INSERT INTO Customers (
    - CustomerName,
    - Address,
    - PostalCode,
    - Country
- ) VALUES (
    - 'Bilbo Baggins',
    - '1 Hobbit-Hole in Bag End',
    - '111',
    - 'Middle Earth'
- );


### Update _Bilbo Baggins_ record so that the postal code changes to _"11122"_.

- UPDATE Customers
- SET PostalCode = 11122
- WHERE CustomerID = 92;


### List orders grouped by customer showing the number of orders per customer. _Rattlesnake Canyon Grocery_ should have 7 orders.


/ List orders by CustomerName - showing number of orders per customer  /
- SELECT Customers.CustomersName, 
- COUNT(Orders.OrderID) AS
- NumberOfOrders from Orders 
- LEFT JOIN Customers 
- ON Orders.CustomerID = Customers.CustomerID
- GROUP BY CustomerName;


### List customers names and the number of orders per customer. Sort the list by number of orders in descending order. _Ernst Handel_ should be at the top with 10 orders followed by _QUICK-Stop_, _Rattlesnake Canyon Grocery_ and _Wartian Herkku_ with 7 orders each.




### list orders grouped by customer's city showing number of orders per city. Returns 58 Records with _Aachen_ showing 2 orders and _Albuquerque_ showing 7 orders.



### Delete all users that have no orders. Should delete 17 (or 18 if you haven't deleted the record added) records.
