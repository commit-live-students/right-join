![GitHub Logo](https://s3.ap-south-1.amazonaws.com/greyatom-social/GreyAtom-logo.png)

# RIGHT JOINS

The SQL RIGHT JOIN returns all rows from the right table, even if there are no matches in the left table. This means that if the ON clause matches 0 (zero) records in the left table; the join will still return a row in the result, but with NULL in each column from the left table.

This means that a right join returns all the values from the right table, plus matched values from the left table or NULL in case of no matching join predicate.

### Syntax

The basic syntax of a RIGHT JOIN is as follow.

        SELECT table1.column1, table2.column2...
        FROM table1
        RIGHT JOIN table2
        ON table1.common_field = table2.common_field;

Now, let us join these two tables using the RIGHT JOIN as follows.

        SELECT  Customers.CustomerID, Customers.CustomerName, ORDERS.OrderDate
            FROM Customers
            RIGHT JOIN ORDERS
            ON Customers.CustomerID = ORDERS.CustomerID;

This would produce the following result −

| CustomerID | CustomerName | OrderDate |
| ---------- | --------- | --------- |
| 51 | Bottom-Dollar Marketse	| 2017-03-20 |
| 71 | Split Rail Beer & Ale | 2016-11-21 |
| 72 | Princesa Isabel Vinhoss	| 2016-12-29 |
| 73 | Folk och fä HB	| 2017-01-04 |
| 74 | Consolidated Holdings	| 2017-03-28 |
