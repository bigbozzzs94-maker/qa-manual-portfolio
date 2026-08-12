# 🗄️ SQL Queries

> SQL queries and database validation examples for the **BookCart — E-commerce Web Application**.

---

## 📋 Project Information

| Parameter | Description |
|---|---|
| **Project** | BookCart |
| **Application Type** | E-commerce Web Application |
| **Testing Type** | Database Testing |
| **Language** | SQL |
| **Status** | Active |

---

# 🎯 Purpose

This document contains SQL query examples used for database validation during testing.

SQL can be used to:

- Verify user data
- Validate product information
- Check shopping cart data
- Validate orders
- Verify relationships between tables
- Check data consistency
- Investigate defects
- Validate backend operations

---

# 🧩 Database Entities

The following entities are used as examples:

```text
Users
  │
  ├── User ID
  ├── Email
  └── Password
       │
       ▼
Orders
  │
  ├── Order ID
  ├── User ID
  └── Order Date
       │
       ▼
Order Items
  │
  ├── Order ID
  ├── Product ID
  └── Quantity

Products
  │
  ├── Product ID
  ├── Title
  └── Price
```

---

# 👤 1. Users

## Get All Users

```sql
SELECT *
FROM users;
```

### Purpose

Verifies that user records are available in the database.

---

## Find User by Email

```sql
SELECT *
FROM users
WHERE email = 'testuser@example.com';
```

### Purpose

Used to verify that a user was successfully created after registration.

---

## Check Duplicate Emails

```sql
SELECT email, COUNT(*)
FROM users
GROUP BY email
HAVING COUNT(*) > 1;
```

### Expected Result

The query should return no records if duplicate emails are not allowed.

---

## Find User by ID

```sql
SELECT *
FROM users
WHERE id = 1;
```

---

# 📚 2. Products

## Get All Products

```sql
SELECT *
FROM products;
```

---

## Find Product by ID

```sql
SELECT *
FROM products
WHERE id = 1;
```

---

## Find Products by Title

```sql
SELECT *
FROM products
WHERE title LIKE '%Book%';
```

### Purpose

Validates product search results in the database.

---

## Find Products with Invalid Price

```sql
SELECT *
FROM products
WHERE price <= 0;
```

### Expected Result

The query should return no products with zero or negative prices.

---

## Count Products

```sql
SELECT COUNT(*) AS total_products
FROM products;
```

---

# 🛒 3. Shopping Cart

## Get Cart Items

```sql
SELECT *
FROM cart_items
WHERE user_id = 1;
```

### Purpose

Validates products stored in a user's shopping cart.

---

## Get Cart with Product Information

```sql
SELECT
    cart_items.user_id,
    products.title,
    products.price,
    cart_items.quantity
FROM cart_items
JOIN products
    ON cart_items.product_id = products.id
WHERE cart_items.user_id = 1;
```

### Purpose

Verifies that cart items correctly reference existing products.

---

## Find Invalid Cart Quantities

```sql
SELECT *
FROM cart_items
WHERE quantity <= 0;
```

### Expected Result

The query should return no records.

---

# 📦 4. Orders

## Get All Orders

```sql
SELECT *
FROM orders;
```

---

## Find Orders by User

```sql
SELECT *
FROM orders
WHERE user_id = 1;
```

---

## Get Order Details

```sql
SELECT
    orders.id AS order_id,
    orders.user_id,
    orders.order_date,
    products.title,
    order_items.quantity,
    products.price
FROM orders
JOIN order_items
    ON orders.id = order_items.order_id
JOIN products
    ON order_items.product_id = products.id
WHERE orders.id = 1;
```

### Purpose

Validates that the order contains correct products and quantities.

---

## Count Orders by User

```sql
SELECT
    user_id,
    COUNT(*) AS total_orders
FROM orders
GROUP BY user_id;
```

---

# 🔗 5. JOIN Queries

## Users and Orders

```sql
SELECT
    users.id,
    users.email,
    orders.id AS order_id,
    orders.order_date
FROM users
JOIN orders
    ON users.id = orders.user_id;
```

### Purpose

Verifies the relationship between users and orders.

---

## Orders and Products

```sql
SELECT
    orders.id AS order_id,
    products.title,
    products.price,
    order_items.quantity
FROM orders
JOIN order_items
    ON orders.id = order_items.order_id
JOIN products
    ON order_items.product_id = products.id;
```

---

# 📊 6. Aggregate Functions

## Count Users

```sql
SELECT COUNT(*) AS total_users
FROM users;
```

---

## Average Product Price

```sql
SELECT AVG(price) AS average_price
FROM products;
```

---

## Maximum Product Price

```sql
SELECT MAX(price) AS max_price
FROM products;
```

---

## Minimum Product Price

```sql
SELECT MIN(price) AS min_price
FROM products;
```

---

## Total Number of Orders

```sql
SELECT COUNT(*) AS total_orders
FROM orders;
```

---

# 🔍 7. Data Validation Queries

## Find Orders Without User

```sql
SELECT *
FROM orders
WHERE user_id NOT IN (
    SELECT id
    FROM users
);
```

### Expected Result

The query should return no records.

---

## Find Order Items Without Product

```sql
SELECT *
FROM order_items
WHERE product_id NOT IN (
    SELECT id
    FROM products
);
```

### Expected Result

The query should return no records.

---

## Find Invalid Order Quantities

```sql
SELECT *
FROM order_items
WHERE quantity <= 0;
```

### Expected Result

The query should return no records.

---

# 🧪 8. SQL Testing Scenarios

The following scenarios can be validated using SQL:

- [x] New user is created after registration
- [x] Duplicate user is not created
- [x] User data is stored correctly
- [x] Product information is correct
- [x] Product prices are valid
- [x] Cart contains correct products
- [x] Cart quantity is correct
- [x] Order is created successfully
- [x] Order contains correct products
- [x] Order belongs to the correct user
- [x] Database relationships are valid
- [x] Invalid records are not created

---

# 📊 SQL Concepts Used

| SQL Concept | Purpose |
|---|---|
| `SELECT` | Retrieve data |
| `WHERE` | Filter records |
| `JOIN` | Combine related tables |
| `GROUP BY` | Group records |
| `HAVING` | Filter grouped records |
| `COUNT()` | Count records |
| `AVG()` | Calculate average value |
| `MIN()` | Find minimum value |
| `MAX()` | Find maximum value |
| `LIKE` | Search text values |

---

# 🎯 QA Use Cases

SQL can help a QA Engineer:

1. Verify application data after user actions.
2. Validate data stored in the database.
3. Compare frontend and backend data.
4. Investigate defects.
5. Check relationships between entities.
6. Validate business logic.
7. Prepare test data.
8. Remove or update test data when permitted.

---

# 🔗 Related Documentation

- [📌 Project Overview](../docs/project-overview/ProjectOverview.md)
- [🧪 Test Cases](../docs/test-cases/TestCases.md)
- [📋 Test Plan](../docs/test-plan/TestPlan.md)
- [🎯 Test Strategy](../docs/test-strategy/TestStrategy.md)
- [🧩 Test Design](../docs/test-design/TestDesign.md)
- [🔌 API Testing](../api-testing/ApiTesting.md)
- [🐞 Bug Reports](../test-artifacts/BugReports.md)

---

## 📌 Notes

> The table names and database structure in this document are examples created for the QA portfolio project. Actual database schemas may differ depending on the application implementation.
