# Test Cases

## Project

**BookCart — E-commerce Web Application**

This document contains detailed test cases for the main functionality of the BookCart application.

---

# Authentication

## TC-001 — Register with valid data

**Priority:** High  
**Preconditions:** User is on the Registration page.

### Steps

1. Open the Registration page.
2. Enter a valid email.
3. Enter a valid password.
4. Confirm the password.
5. Click the **Register** button.

### Expected Result

A new user account is created successfully, and the user is redirected to the appropriate page.

---

## TC-002 — Register with an existing email

**Priority:** High  
**Preconditions:** A user account with the specified email already exists.

### Steps

1. Open the Registration page.
2. Enter an email that is already registered.
3. Enter a valid password.
4. Confirm the password.
5. Click the **Register** button.

### Expected Result

The account is not created. An error message informing the user that the email already exists is displayed.

---

## TC-003 — Login with valid credentials

**Priority:** High  
**Preconditions:** A registered user account exists.

### Steps

1. Open the Login page.
2. Enter a valid email.
3. Enter the correct password.
4. Click the **Login** button.

### Expected Result

The user is successfully authenticated and logged into the application.

---

## TC-004 — Login with invalid credentials

**Priority:** High  
**Preconditions:** User is on the Login page.

### Steps

1. Open the Login page.
2. Enter an invalid email or password.
3. Click the **Login** button.

### Expected Result

The user is not logged in, and an appropriate error message is displayed.

---

# Product Catalog

## TC-005 — Open product catalog

**Priority:** High  
**Preconditions:** The application is available.

### Steps

1. Open the application.
2. Navigate to the Product Catalog page.

### Expected Result

The Product Catalog page opens successfully, and the list of available products is displayed.

---

## TC-006 — Search for an existing product

**Priority:** Medium  
**Preconditions:** The Product Catalog page is open and products are available.

### Steps

1. Open the Product Catalog page.
2. Enter the name of an existing product into the search field.
3. Start the search.

### Expected Result

Products matching the search query are displayed.

---

## TC-007 — Search for a non-existing product

**Priority:** Medium  
**Preconditions:** The Product Catalog page is open.

### Steps

1. Enter a product name that does not exist.
2. Start the search.

### Expected Result

No matching products are displayed, and the application handles the empty search result correctly.

---

# Shopping Cart

## TC-008 — Add product to cart

**Priority:** High  
**Preconditions:** The Product Catalog page is open and at least one product is available.

### Steps

1. Select a product.
2. Click the **Add to Cart** button.
3. Open the Shopping Cart.

### Expected Result

The selected product is added to the Shopping Cart with the correct name, price, and quantity.

---

## TC-009 — Remove product from cart

**Priority:** High  
**Preconditions:** At least one product has been added to the Shopping Cart.

### Steps

1. Open the Shopping Cart.
2. Locate the product.
3. Click the **Remove** button.

### Expected Result

The selected product is removed from the Shopping Cart, and the total amount is updated correctly.

---

## TC-010 — Change product quantity

**Priority:** Medium  
**Preconditions:** At least one product has been added to the Shopping Cart.

### Steps

1. Open the Shopping Cart.
2. Increase the quantity of a product.
3. Verify the updated quantity.
4. Decrease the quantity of the product.

### Expected Result

The product quantity changes correctly, and the Shopping Cart total is recalculated accordingly.

---

# Checkout

## TC-011 — Checkout with valid data

**Priority:** High  
**Preconditions:** The Shopping Cart contains at least one product.

### Steps

1. Open the Shopping Cart.
2. Proceed to Checkout.
3. Enter valid customer information.
4. Fill in all required fields.
5. Confirm the order.

### Expected Result

The order is successfully created, and an order confirmation is displayed.

---

## TC-012 — Checkout with missing required fields

**Priority:** High  
**Preconditions:** The Shopping Cart contains at least one product.

### Steps

1. Open the Shopping Cart.
2. Proceed to Checkout.
3. Leave one or more required fields empty.
4. Attempt to confirm the order.

### Expected Result

The order is not created, and validation messages are displayed for the required fields.

---

# Order Management

## TC-013 — View order list

**Priority:** Medium  
**Preconditions:** The user is authenticated and has at least one order.

### Steps

1. Log in to the application.
2. Navigate to the Orders page.

### Expected Result

The list of user orders is displayed with relevant order information.

---

## TC-014 — Open order details

**Priority:** Medium  
**Preconditions:** The user has at least one order.

### Steps

1. Open the Orders page.
2. Select an existing order.

### Expected Result

Order details are displayed, including ordered products, quantities, prices, and order information.

---

# Test Summary

| Module | Test Cases |
|---|---:|
| Authentication | 4 |
| Product Catalog | 3 |
| Shopping Cart | 3 |
| Checkout | 2 |
| Order Management | 2 |
| **Total** | **14** |
