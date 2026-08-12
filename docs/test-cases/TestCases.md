# Test Cases

## Authentication

| ID | Test Case | Expected Result | Status |
|---|---|---|---|
| TC-001 | Register with valid data | User account is created | Pass |
| TC-002 | Register with existing email | Error message is displayed | Pass |
| TC-003 | Login with valid credentials | User is logged in | Pass |
| TC-004 | Login with invalid credentials | Error message is displayed | Pass |

## Product Catalog

| ID | Test Case | Expected Result | Status |
|---|---|---|---|
| TC-005 | Open product catalog | Product list is displayed | Pass |
| TC-006 | Search for existing product | Matching products are displayed | Pass |
| TC-007 | Search for non-existing product | No products are displayed | Pass |

## Shopping Cart

| ID | Test Case | Expected Result | Status |
|---|---|---|---|
| TC-008 | Add product to cart | Product appears in cart | Pass |
| TC-009 | Remove product from cart | Product is removed | Pass |
| TC-010 | Change product quantity | Cart quantity is updated | Pass |

## Checkout

| ID | Test Case | Expected Result | Status |
|---|---|---|---|
| TC-011 | Checkout with valid data | Order is created | Pass |
| TC-012 | Checkout with missing required fields | Validation error is displayed | Pass |
