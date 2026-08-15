# 🐞 Bug Reports

> This document contains sample bug reports created during manual testing of the BookCart E-commerce Web Application.

---

## 📋 Project Information

| Parameter | Description |
|---|---|
| **Project** | BookCart |
| **Application Type** | E-commerce Web Application |
| **Testing Type** | Manual Functional Testing |
| **Document Type** | Bug Reports |
| **Status** | Active |

---

## 🎯 Purpose

The purpose of this document is to demonstrate the bug reporting process and provide examples of defects identified during testing of the BookCart application.

Each bug report contains the information required for a developer and QA team to understand, reproduce, prioritize, and resolve the issue.

### Each bug report includes:

- **Bug ID**
- **Summary**
- **Preconditions**
- **Steps to Reproduce**
- **Actual Result**
- **Expected Result**
- **Severity**
- **Priority**
- **Environment**
- **Status**

---

# 🐞 BUG-001 — User Can Log In with Incorrect Password

## Summary

The system allows a user to successfully log in when an incorrect password is entered.

---

## Preconditions

- The user is registered in the system.
- The user is on the Login page.
- Valid credentials for an existing user are available.

---

## Steps to Reproduce

1. Open the Login page.
2. Enter a valid registered email address.
3. Enter an incorrect password.
4. Click the **Login** button.

---

## Actual Result

The user is successfully authenticated and redirected to the application.

---

## Expected Result

The system should reject authentication and display an appropriate error message indicating that the email or password is incorrect.

---

## Severity

**Critical**

Authentication is a core application feature. Allowing access with incorrect credentials may result in unauthorized access to user accounts.

---

## Priority

**High**

The issue should be fixed before release because it affects application security and user authentication.

---

## Environment

| Parameter | Value |
|---|---|
| Application | BookCart Web Application |
| Browser | Google Chrome |
| Testing Type | Manual Testing |
| Area | Authentication |

---

## Status

**Open**

---

# 🐞 BUG-002 — User Can Add a Product to Cart Multiple Times

## Summary

The user can add the same product to the shopping cart multiple times by repeatedly clicking the **Add to Cart** button.

---

## Preconditions

- The user is on the Product Catalog page.
- At least one product is available.

---

## Steps to Reproduce

1. Open the Product Catalog page.
2. Select any available product.
3. Click the **Add to Cart** button several times.
4. Open the Shopping Cart.

---

## Actual Result

The same product is added to the cart multiple times, creating duplicate product entries.

---

## Expected Result

The application should add the product only once or increase the quantity of the existing product according to the expected business logic.

---

## Severity

**Major**

The issue affects shopping cart functionality and may lead to incorrect order data.

---

## Priority

**High**

The shopping cart is a core feature of an e-commerce application and should work correctly before release.

---

## Environment

| Parameter | Value |
|---|---|
| Application | BookCart Web Application |
| Browser | Google Chrome |
| Testing Type | Manual Testing |
| Area | Shopping Cart |

---

## Status

**Open**

---

# 🐞 BUG-003 — Search Returns No Results for an Existing Product

## Summary

The product search does not return results when the user searches for the exact name of an existing product.

---

## Preconditions

- The application is available.
- The product catalog contains searchable products.

---

## Steps to Reproduce

1. Open the Product Catalog page.
2. Identify the name of an existing product.
3. Enter the exact product name into the search field.
4. Execute the search.

---

## Actual Result

No products are displayed, even though the product exists in the catalog.

---

## Expected Result

The application should display the product matching the search query.

---

## Severity

**Major**

The issue affects the user's ability to find products and directly impacts the main purchasing flow.

---

## Priority

**High**

Search functionality is important for product discovery and should be fixed before release.

---

## Environment

| Parameter | Value |
|---|---|
| Application | BookCart Web Application |
| Browser | Google Chrome |
| Testing Type | Manual Testing |
| Area | Product Search |

---

## Status

**Open**

---

# 🐞 BUG-004 — Checkout Allows Order Submission with Empty Required Fields

## Summary

The checkout form allows the user to submit an order without completing all required fields.

---

## Preconditions

- The user has at least one product in the shopping cart.
- The user is on the Checkout page.

---

## Steps to Reproduce

1. Add any product to the shopping cart.
2. Proceed to the Checkout page.
3. Leave required fields empty.
4. Click the **Place Order** button.

---

## Actual Result

The order is submitted without validating required fields.

---

## Expected Result

The system should prevent order submission and display validation messages for all required fields.

---

## Severity

**Critical**

The issue may result in incomplete or invalid orders being created in the system.

---

## Priority

**High**

Checkout validation directly affects order processing and must be fixed before release.

---

## Environment

| Parameter | Value |
|---|---|
| Application | BookCart Web Application |
| Browser | Google Chrome |
| Testing Type | Manual Testing |
| Area | Checkout |

---

## Status

**Open**

---

# 🐞 BUG-005 — Error Message Is Not Displayed After Failed Registration

## Summary

The application does not display an informative error message when user registration fails.

---

## Preconditions

- The user is on the Registration page.
- An email address that is already registered in the system is available.

---

## Steps to Reproduce

1. Open the Registration page.
2. Enter valid user data.
3. Enter an email address that already exists in the system.
4. Complete the remaining required fields.
5. Click the **Register** button.

---

## Actual Result

Registration fails, but the user does not receive a clear error message explaining the reason.

---

## Expected Result

The system should display an informative message explaining that the email address is already registered.

---

## Severity

**Minor**

The application functionality is not blocked, but the issue negatively affects user experience and makes the cause of the failure unclear.

---

## Priority

**Medium**

The issue should be fixed to improve usability and provide clear feedback to users.

---

## Environment

| Parameter | Value |
|---|---|
| Application | BookCart Web Application |
| Browser | Google Chrome |
| Testing Type | Manual Testing |
| Area | Registration |

---

## Status

**Open**

---

# 📊 Bug Summary

| Bug ID | Area | Severity | Priority | Status |
|---|---|---|---|---|
| BUG-001 | Authentication | Critical | High | Open |
| BUG-002 | Shopping Cart | Major | High | Open |
| BUG-003 | Product Search | Major | High | Open |
| BUG-004 | Checkout | Critical | High | Open |
| BUG-005 | Registration | Minor | Medium | Open |

---

## 📝 Notes

These bug reports are included as part of the QA portfolio for the BookCart project.

The examples demonstrate:

- Bug identification
- Defect documentation
- Writing clear reproduction steps
- Distinguishing between Actual and Expected Results
- Severity assessment
- Priority assessment
- Functional testing of different application areas

---

⬅️ [Back to README](../README.md)
