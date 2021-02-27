# Consulta-SQL
Comadandos no sql que são necessarios para realizar a consulta da questão 3, no site: https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_all.

Chaves: 
Customers.CustomerID = Orders.CustomerID;
Orders.OrderID = OrderDetails.OrderID;
OrderDetails.ProductID = Products.ProductID;
Products.SupplierID = Suppliers.SupplierID;

SELECT * 
FROM Customers as c
inner join Orders as o 
on c.CustomerID = o.CustomerID
inner join OrderDetails as od
on o.OrderID = od.OrderID
inner join Products as p
on od.ProductID = p.ProductID
inner join Suppliers as s
on s.SupplierID = p.SupplierID
where s.Country = 'Brazil';
