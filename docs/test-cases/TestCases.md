# 🧪 Test Cases

> Detailed functional test cases for the **BookCart — E-commerce Web Application**.

---

## 📋 Project Information

| Parameter | Description |
|---|---|
| **Project** | BookCart |
| **Application Type** | E-commerce Web Application |
| **Platform** | Web |
| **Testing Type** | Manual Functional Testing |
| **Test Level** | System Testing |
| **Status** | Active |

---

## 🎯 Purpose

This document contains detailed test cases designed to verify the main functionality of the BookCart application.

The test cases cover:

- Registration
- Authentication
- Product Catalog
- Product Search
- Shopping Cart
- Checkout
- Order Management

---

# 📝 Registration

---

## TC-001 — Register User with Valid Data

| Parameter | Value |
|---|---|
| **Priority** | High |
| **Type** | Positive |
| **Preconditions** | Registration page is available |

### Test Data

```text
Email: testuser@example.com
Password: Password123
Confirm Password: Password123
```

### Steps

1. Open the registration page.
2. Enter a valid email address.
3. Enter a valid password.
4. Enter the same password in the confirmation field.
5. Click the **Register** button.

### Expected Result

- User is successfully registered.
- Success message or confirmation is displayed.
- User is redirected to the expected page.
- User account is created.

---

## TC-002 — Register User with Existing Email

| Parameter | Value |
|---|---|
| **Priority** | High |
| **Type** | Negative |
| **Preconditions** | A user with the specified email already exists |

### Steps

1. Open the registration page.
2. Enter an existing email address.
3. Enter a valid password.
4. Confirm the password.
5. Click **Register**.

### Expected Result

- Registration is rejected.
- User account is not duplicated.
- An appropriate error message is displayed.

---

## TC-003 — Register with Invalid Email

| Parameter | Value |
|---|---|
| **Priority** | Medium |
| **Type** | Negative |
| **Preconditions** | Registration page is available |

### Test Data

```text
Email: invalid-email
Password: Password123
Confirm Password: Password123
```

### Expected Result

- Invalid email format is rejected.
- Validation message is displayed.
- Registration is not completed.

---

# 🔐 Authentication

---

## TC-004 — Login with Valid Credentials

| Parameter | Value |
|---|---|
| **Priority** | Critical |
| **Type** | Positive |
| **Preconditions** | Registered user exists |

### Steps

1. Open the login page.
2. Enter valid email credentials.
3. Enter a valid password.
4. Click **Login**.

### Expected Result

- User is successfully authenticated.
- User session is created.
- User is redirected to the expected page.

---

## TC-005 — Login with Invalid Password

| Parameter | Value |
|---|---|
| **Priority** | High |
| **Type** | Negative |
| **Preconditions** | Registered user exists |

### Steps

1. Open the login page.
2. Enter a valid email.
3. Enter an invalid password.
4. Click **Login**.

### Expected Result

- Authentication fails.
- User is not logged in.
- An appropriate error message is displayed.

---

## TC-006 — Login with Empty Fields

| Parameter | Value |
|---|---|
| **Priority** | Medium |
| **Type** | Negative |
| **Preconditions** | Login page is available |

### Steps

1. Open the login page.
2. Leave required fields empty.
3. Click **Login**.

### Expected Result

- Validation prevents submission.
- Required field messages are displayed.
- User is not authenticated.

---

# 📚 Product Catalog

---

## TC-007 — Open Product Catalog

| Parameter | Value |
|---|---|
| **Priority** | High |
| **Type** | Positive |

### Steps

1. Open the main page.
2. Navigate to the product catalog.

### Expected Result

- Product catalog opens successfully.
- Product list is displayed.
- Product information is visible.

---

## TC-008 — Open Product Details

| Parameter | Value |
|---|---|
| **Priority** | High |
| **Type** | Positive |
| **Preconditions** | Product exists |

### Steps

1. Open the product catalog.
2. Select any product.
3. Open the product details page.

### Expected Result

- Product details page opens.
- Correct product information is displayed.
- Product name, price and description are visible.

---

# 🔎 Product Search

---

## TC-009 — Search for Existing Product

| Parameter | Value |
|---|---|
| **Priority** | High |
| **Type** | Positive |
| **Preconditions** | Product exists in the catalog |

### Steps

1. Open the product catalog.
2. Enter an existing product name into the search field.
3. Start the search.

### Expected Result

- Relevant products are displayed.
- Search results match the search query.

---

## TC-010 — Search for Non-Existing Product

| Parameter | Value |
|---|---|
| **Priority** | Medium |
| **Type** | Negative |

### Steps

1. Open the product catalog.
2. Enter a non-existing product name.
3. Start the search.

### Expected Result

- No irrelevant products are displayed.
- Appropriate empty search result message is shown.

---

# 🛒 Shopping Cart

---

## TC-011 — Add Product to Cart

| Parameter | Value |
|---|---|
| **Priority** | Critical |
| **Type** | Positive |
| **Preconditions** | Product exists |

### Steps

1. Open the product catalog.
2. Select a product.
3. Click **Add to Cart**.
4. Open the shopping cart.

### Expected Result

- Product is successfully added.
- Correct product is displayed in the cart.
- Product price is correct.
- Product quantity is correct.

---

## TC-012 — Increase Product Quantity

| Parameter | Value |
|---|---|
| **Priority** | High |
| **Type** | Positive |
| **Preconditions** | Product is already added to the cart |

### Steps

1. Open the shopping cart.
2. Increase the product quantity.

### Expected Result

- Product quantity increases correctly.
- Cart total is recalculated correctly.

---

## TC-013 — Remove Product from Cart

| Parameter | Value |
|---|---|
| **Priority** | High |
| **Type** | Positive |
| **Preconditions** | Product is already added to the cart |

### Steps

1. Open the shopping cart.
2. Click the **Remove** button.

### Expected Result

- Product is removed from the cart.
- Cart total is updated.
- Removed product is no longer displayed.

---

# 💳 Checkout

---

## TC-014 — Open Checkout Page

| Parameter | Value |
|---|---|
| **Priority** | Critical |
| **Type** | Positive |
| **Preconditions** | Shopping cart contains at least one product |

### Steps

1. Open the shopping cart.
2. Click the **Checkout** button.

### Expected Result

- Checkout page opens successfully.
- Order summary is displayed.
- Customer information fields are available.

---

## TC-015 — Place Order with Valid Data

| Parameter | Value |
|---|---|
| **Priority** | Critical |
| **Type** | Positive |
| **Preconditions** | Cart contains at least one product |

### Steps

1. Open the checkout page.
2. Enter valid required information.
3. Verify the order summary.
4. Confirm the order.

### Expected Result

- Order is successfully created.
- Order confirmation is displayed.
- User receives an order identifier or confirmation information.

---

## TC-016 — Checkout with Empty Required Fields

| Parameter | Value |
|---|---|
| **Priority** | High |
| **Type** | Negative |
| **Preconditions** | Checkout page is available |

### Steps

1. Open the checkout page.
2. Leave required fields empty.
3. Attempt to place an order.

### Expected Result

- Order is not created.
- Validation messages are displayed.
- Required fields are highlighted correctly.

---

# 📦 Order Management

---

## TC-017 — View Order List

| Parameter | Value |
|---|---|
| **Priority** | High |
| **Type** | Positive |
| **Preconditions** | User has at least one order |

### Steps

1. Log in to the application.
2. Navigate to the orders page.

### Expected Result

- Order list is displayed.
- Order ID is visible.
- Order date is displayed.
- Order status is displayed.
- Order total is correct.

---

## TC-018 — Open Order Details

| Parameter | Value |
|---|---|
| **Priority** | High |
| **Type** | Positive |
| **Preconditions** | Order exists |

### Steps

1. Open the order list.
2. Select an order.
3. Open order details.

### Expected Result

- Order details are displayed.
- Ordered products are correct.
- Product quantities are correct.
- Total amount is correct.

---

# 📊 Test Case Summary

| Area | Test Cases | Priority |
|---|---:|---|
| 📝 Registration | TC-001 – TC-003 | High |
| 🔐 Authentication | TC-004 – TC-006 | Critical |
| 📚 Product Catalog | TC-007 – TC-008 | High |
| 🔎 Product Search | TC-009 – TC-010 | Medium |
| 🛒 Shopping Cart | TC-011 – TC-013 | Critical |
| 💳 Checkout | TC-014 – TC-016 | Critical |
| 📦 Order Management | TC-017 – TC-018 | High |

---

# 🔗 Related Documentation

- [🧠 Mind Map](../mind-maps/MindMap.md)
- [✅ Checklists](../../checklists/Checklists.md)
- [📋 Test Plan](../test-plan/TestPlan.md)
- [🎯 Test Strategy](../test-strategy/TestStrategy.md)
- [🔌 API Test Cases](../../api-testing/test-cases/APITestCases.md)
- [🐞 Bug Reports](../../test-artifacts/BugReports.md)

---

## 📌 Notes

> Test cases may be updated as application requirements and functionality evolve.
