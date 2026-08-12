
# QA Checklists

## Project

**BookCart — E-commerce Web Application**

This document contains checklists for testing the main functionality of the BookCart web application.

---

# 1. Registration Checklist

| ID | Check | Status |
|---|---|---|
| REG-01 | Registration page opens successfully | ⬜ |
| REG-02 | Email field is displayed | ⬜ |
| REG-03 | Password field is displayed | ⬜ |
| REG-04 | Confirm Password field is displayed | ⬜ |
| REG-05 | Register button is displayed | ⬜ |
| REG-06 | User can register with valid data | ⬜ |
| REG-07 | Registration with an already existing email is handled correctly | ⬜ |
| REG-08 | Invalid email format validation works correctly | ⬜ |
| REG-09 | Empty email field validation works correctly | ⬜ |
| REG-10 | Empty password field validation works correctly | ⬜ |
| REG-11 | Password confirmation validation works correctly | ⬜ |
| REG-12 | Different passwords cannot be submitted | ⬜ |
| REG-13 | Password field masks entered characters | ⬜ |
| REG-14 | User is redirected correctly after successful registration | ⬜ |

---

# 2. Authentication Checklist

| ID | Check | Status |
|---|---|---|
| AUTH-01 | Login page opens successfully | ⬜ |
| AUTH-02 | Email field is displayed | ⬜ |
| AUTH-03 | Password field is displayed | ⬜ |
| AUTH-04 | Login button is displayed | ⬜ |
| AUTH-05 | User can log in with valid credentials | ⬜ |
| AUTH-06 | Invalid email is handled correctly | ⬜ |
| AUTH-07 | Invalid password is handled correctly | ⬜ |
| AUTH-08 | Empty fields validation works correctly | ⬜ |
| AUTH-09 | Password is masked | ⬜ |
| AUTH-10 | Error message is displayed for invalid credentials | ⬜ |
| AUTH-11 | User session is created after successful login | ⬜ |
| AUTH-12 | Logout functionality works correctly | ⬜ |
| AUTH-13 | User cannot access protected pages after logout | ⬜ |

---

# 3. Product Catalog Checklist

| ID | Check | Status |
|---|---|---|
| CAT-01 | Product catalog page opens successfully | ⬜ |
| CAT-02 | Product list is displayed | ⬜ |
| CAT-03 | Product name is displayed | ⬜ |
| CAT-04 | Product price is displayed | ⬜ |
| CAT-05 | Product image is displayed | ⬜ |
| CAT-06 | Product description is displayed correctly | ⬜ |
| CAT-07 | User can open product details | ⬜ |
| CAT-08 | Search functionality works correctly | ⬜ |
| CAT-09 | Search with an existing product returns results | ⬜ |
| CAT-10 | Search with a non-existing product is handled correctly | ⬜ |
| CAT-11 | Product category filtering works correctly | ⬜ |
| CAT-12 | Sorting functionality works correctly | ⬜ |
| CAT-13 | Product data is displayed correctly after page refresh | ⬜ |

---

# 4. Shopping Cart Checklist

| ID | Check | Status |
|---|---|---|
| CART-01 | Shopping cart page opens successfully | ⬜ |
| CART-02 | User can add a product to the cart | ⬜ |
| CART-03 | Added product appears in the cart | ⬜ |
| CART-04 | Correct product name is displayed | ⬜ |
| CART-05 | Correct product price is displayed | ⬜ |
| CART-06 | Product quantity is displayed | ⬜ |
| CART-07 | User can increase product quantity | ⬜ |
| CART-08 | User can decrease product quantity | ⬜ |
| CART-09 | User cannot set an invalid quantity | ⬜ |
| CART-10 | User can remove a product from the cart | ⬜ |
| CART-11 | Cart total is calculated correctly | ⬜ |
| CART-12 | Cart is empty after removing all products | ⬜ |
| CART-13 | Cart data is handled correctly after page refresh | ⬜ |

---

# 5. Checkout Checklist

| ID | Check | Status |
|---|---|---|
| CHECK-01 | Checkout page opens successfully | ⬜ |
| CHECK-02 | User can proceed to checkout from the cart | ⬜ |
| CHECK-03 | Customer information fields are displayed | ⬜ |
| CHECK-04 | Required fields validation works correctly | ⬜ |
| CHECK-05 | Invalid input validation works correctly | ⬜ |
| CHECK-06 | Order summary is displayed correctly | ⬜ |
| CHECK-07 | Product prices are correct | ⬜ |
| CHECK-08 | Total order amount is calculated correctly | ⬜ |
| CHECK-09 | User can successfully place an order | ⬜ |
| CHECK-10 | Order confirmation is displayed after successful checkout | ⬜ |
| CHECK-11 | Order is not created when required data is missing | ⬜ |

---

# 6. Order Management Checklist

| ID | Check | Status |
|---|---|---|
| ORDER-01 | Orders page opens successfully | ⬜ |
| ORDER-02 | User can view the order list | ⬜ |
| ORDER-03 | Order ID is displayed | ⬜ |
| ORDER-04 | Order date is displayed | ⬜ |
| ORDER-05 | Order status is displayed | ⬜ |
| ORDER-06 | Order total is displayed correctly | ⬜ |
| ORDER-07 | User can open order details | ⬜ |
| ORDER-08 | Correct products are displayed in order details | ⬜ |
| ORDER-09 | Order status is updated correctly | ⬜ |
| ORDER-10 | Order data persists after page refresh | ⬜ |

---

# 7. General UI Checklist

| ID | Check | Status |
|---|---|---|
| UI-01 | All pages open without critical errors | ⬜ |
| UI-02 | Navigation works correctly | ⬜ |
| UI-03 | Buttons are clickable and work correctly | ⬜ |
| UI-04 | Text is readable | ⬜ |
| UI-05 | Page layout is displayed correctly | ⬜ |
| UI-06 | Error messages are understandable | ⬜ |
| UI-07 | Application works correctly after page refresh | ⬜ |
| UI-08 | No unexpected console errors occur during normal usage | ⬜ |
| UI-09 | Application behavior is consistent across supported browsers | ⬜ |

---

## Summary

The checklists cover the following functionality:

- Registration
- Authentication
- Product catalog
- Product search and filtering
- Shopping cart
- Checkout
- Order management
- General UI testing
