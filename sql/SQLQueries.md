# SQL Queries

## Project

**BookCart — E-commerce Web Application**

This document contains SQL queries used to verify application data, including users, products, shopping carts, and orders.

---

## 1. Select All Users

```sql
SELECT *
FROM Users;
```

---

## 2. Find User by Email

```sql
SELECT *
FROM Users
WHERE Email = 'test@example.com';
```

---

## 3. Find Users by Name

```sql
SELECT *
FROM Users
WHERE Name LIKE '%John%';
```

---

## 4. Count Total Users

```sql
SELECT COUNT(*) AS TotalUsers
FROM Users;
```

---

## 5. Select All Products

```sql
SELECT *
FROM Products;
```

---

## 6. Find Products by Category

```sql
SELECT *
FROM Products
WHERE Category = 'Books';
```

---

## 7. Find Products by Price Range

```sql
SELECT *
FROM Products
WHERE Price BETWEEN 10 AND 50;
```

---

## 8. Sort Products by Price

```sql
SELECT *
FROM Products
ORDER BY Price DESC;
```

---

## 9. Find Product by Name

```sql
SELECT *
FROM Products
WHERE Name LIKE '%Python%';
```

---

## 10. Count Products by Category

```sql
SELECT Category, COUNT(*) AS ProductCount
FROM Products
GROUP BY Category;
```

---

## 11. Find All Orders

```sql
SELECT *
FROM Orders;
```

---

## 12. Find Orders for a Specific User

```sql
SELECT *
FROM Orders
WHERE UserId = 1;
```

---

## 13. Get Orders with User Information

```sql
SELECT
    Orders.Id AS OrderId,
    Users.Name AS UserName,
    Users.Email,
    Orders.TotalAmount,
    Orders.Status
FROM Orders
JOIN Users ON Orders.UserId = Users.Id;
```

---

## 14. Find Orders by Status

```sql
SELECT *
FROM Orders
WHERE Status = 'Completed';
```

---

## 15. Count Orders by Status

```sql
SELECT Status, COUNT(*) AS OrderCount
FROM Orders
GROUP BY Status;
```

---

## 16. Find Shopping Cart Items for a User

```sql
SELECT
    Cart.Id AS CartId,
    Products.Name AS ProductName,
    Products.Price,
    Cart.Quantity
FROM Cart
JOIN Products ON Cart.ProductId = Products.Id
WHERE Cart.UserId = 1;
```

---

## 17. Calculate Total Amount in Shopping Cart

```sql
SELECT
    SUM(Products.Price * Cart.Quantity) AS TotalAmount
FROM Cart
JOIN Products ON Cart.ProductId = Products.Id
WHERE Cart.UserId = 1;
```

---

## 18. Find Products That Have Never Been Ordered

```sql
SELECT *
FROM Products
WHERE Id NOT IN (
    SELECT ProductId
    FROM OrderItems
);
```

---

## 19. Find Users Without Orders

```sql
SELECT *
FROM Users
WHERE Id NOT IN (
    SELECT UserId
    FROM Orders
);
```

---

## 20. Find the Most Expensive Product

```sql
SELECT *
FROM Products
ORDER BY Price DESC
LIMIT 1;
```

---

## SQL Concepts Demonstrated

This document demonstrates the following SQL concepts:

- `SELECT`
- `WHERE`
- `LIKE`
- `COUNT()`
- `SUM()`
- `BETWEEN`
- `ORDER BY`
- `GROUP BY`
- `JOIN`
- Subqueries
- Aggregate functions
