# ✅ QA Checklists

> Functional checklists for the **BookCart — E-commerce Web Application**.

---

## 📋 Project Information

| Parameter | Description |
|---|---|
| **Project** | BookCart |
| **Application Type** | E-commerce Web Application |
| **Platform** | Web |
| **Testing Type** | Manual Functional Testing |
| **Status** | Active |

---

## 🎯 Purpose

These checklists are designed to verify the main functionality of the BookCart application and provide structured test coverage for critical user flows.

### Main Testing Areas

- 🔐 Authentication
- 📝 Registration
- 📚 Product Catalog
- 🔎 Product Search
- 🛒 Shopping Cart
- 💳 Checkout
- 📦 Order Management
- 🖥️ General UI

---

# 📝 Registration

## Registration Page

- [ ] Registration page opens successfully
- [ ] All required fields are displayed
- [ ] Email field is available
- [ ] Password field is available
- [ ] Confirm Password field is available
- [ ] Register button is displayed and enabled correctly

## Positive Scenarios

- [ ] User can register with valid data
- [ ] Registration is successful with a valid email
- [ ] Registration is successful with a valid password
- [ ] Password confirmation works correctly
- [ ] User is redirected after successful registration

## Negative Scenarios

- [ ] Registration with an existing email is handled correctly
- [ ] Invalid email format is rejected
- [ ] Empty email field is validated
- [ ] Empty password field is validated
- [ ] Empty Confirm Password field is validated
- [ ] Password mismatch is handled correctly
- [ ] Invalid password format is rejected
- [ ] Error messages are displayed correctly

---

# 🔐 Authentication

## Login Page

- [ ] Login page opens successfully
- [ ] Email field is displayed
- [ ] Password field is displayed
- [ ] Login button is displayed
- [ ] Password characters are masked

## Positive Scenarios

- [ ] User can log in with valid credentials
- [ ] User session is created successfully
- [ ] User is redirected after successful login
- [ ] Authenticated user can access protected pages

## Negative Scenarios

- [ ] Invalid email is handled correctly
- [ ] Invalid password is handled correctly
- [ ] Empty fields are validated
- [ ] Error message is displayed for invalid credentials
- [ ] User cannot access protected pages without authentication

## Logout

- [ ] Logout functionality works correctly
- [ ] User session is terminated after logout
- [ ] Protected pages cannot be accessed after logout

---

# 📚 Product Catalog

## Product Display

- [ ] Product catalog opens successfully
- [ ] Product list is displayed
- [ ] Product name is displayed
- [ ] Product price is displayed
- [ ] Product image is displayed correctly
- [ ] Product description is displayed correctly

## Product Details

- [ ] User can open product details
- [ ] Correct product information is displayed
- [ ] Product price matches the catalog price
- [ ] Product image loads successfully

## Catalog Functionality

- [ ] Product list loads correctly
- [ ] Product data remains correct after page refresh
- [ ] No duplicate products are displayed
- [ ] Empty catalog state is handled correctly

---

# 🔎 Product Search

## Positive Scenarios

- [ ] Search field is displayed
- [ ] User can search for an existing product
- [ ] Relevant products are displayed
- [ ] Search results match the search query
- [ ] Search works with partial product names
- [ ] Search works with different letter cases

## Negative Scenarios

- [ ] Search for a non-existing product is handled correctly
- [ ] Empty search request is handled correctly
- [ ] Special characters are handled correctly
- [ ] Long search query is handled correctly
- [ ] No-results message is displayed correctly

---

# 🛒 Shopping Cart

## Add Product

- [ ] User can add a product to the cart
- [ ] Added product appears in the cart
- [ ] Correct product name is displayed
- [ ] Correct product price is displayed
- [ ] Correct quantity is displayed

## Update Quantity

- [ ] User can increase product quantity
- [ ] User can decrease product quantity
- [ ] Cart total updates correctly
- [ ] Product quantity cannot be negative
- [ ] Invalid quantity values are rejected
- [ ] Quantity limits are handled correctly

## Remove Product

- [ ] User can remove a product from the cart
- [ ] Removed product is no longer displayed
- [ ] Cart total updates correctly
- [ ] Empty cart state is displayed correctly

## Cart Persistence

- [ ] Cart data is handled correctly after page refresh
- [ ] Cart data remains consistent during the user session

---

# 💳 Checkout

## Checkout Page

- [ ] User can navigate from the cart to checkout
- [ ] Checkout page opens successfully
- [ ] Customer information fields are displayed
- [ ] Order summary is displayed

## Validation

- [ ] Required fields are validated
- [ ] Empty required fields cannot be submitted
- [ ] Invalid input is rejected
- [ ] Validation messages are displayed correctly

## Order Creation

- [ ] Product information is correct
- [ ] Product prices are correct
- [ ] Total order amount is calculated correctly
- [ ] User can place an order with valid data
- [ ] Order confirmation is displayed
- [ ] Order is not created with missing required information

---

# 📦 Order Management

## Order List

- [ ] Orders page opens successfully
- [ ] User can view the order list
- [ ] Order ID is displayed
- [ ] Order date is displayed
- [ ] Order status is displayed
- [ ] Order total is displayed correctly

## Order Details

- [ ] User can open order details
- [ ] Ordered products are displayed correctly
- [ ] Product quantities are correct
- [ ] Product prices are correct
- [ ] Total order amount is correct

## Data Validation

- [ ] Order status is updated correctly
- [ ] Order data persists after page refresh
- [ ] User cannot access another user's order

---

# 🖥️ General UI

## Navigation

- [ ] Main navigation works correctly
- [ ] All links work correctly
- [ ] Back navigation works correctly
- [ ] Page refresh does not cause unexpected errors

## Interface

- [ ] Text is readable
- [ ] Page layout is displayed correctly
- [ ] Buttons are visible and clickable
- [ ] Input fields are displayed correctly
- [ ] Error messages are understandable
- [ ] Loading states are handled correctly

## Browser Console

- [ ] No critical JavaScript errors occur during normal usage
- [ ] No unexpected console errors occur
- [ ] Network requests complete successfully

---

# 🚨 Priority Areas

| Area | Priority |
|---|---|
| Registration | High |
| Authentication | Critical |
| Product Catalog | High |
| Product Search | Medium |
| Shopping Cart | Critical |
| Checkout | Critical |
| Order Management | High |
| General UI | Medium |

---

# 📊 Checklist Summary

| Module | Main Coverage |
|---|---|
| 📝 Registration | Form validation and account creation |
| 🔐 Authentication | Login, logout and authorization |
| 📚 Product Catalog | Product display and details |
| 🔎 Product Search | Search functionality and validation |
| 🛒 Shopping Cart | Add, update and remove products |
| 💳 Checkout | Validation and order creation |
| 📦 Order Management | Orders and order details |
| 🖥️ General UI | Navigation and interface behavior |

---

## 🔗 Related Documentation

- [🧠 Mind Map](../docs/mind-maps/MindMap.md)
- [🧪 Test Cases](../docs/test-cases/TestCases.md)
- [📋 Test Plan](../docs/test-plan/TestPlan.md)
- [🎯 Test Strategy](../docs/test-strategy/TestStrategy.md)
- [🐞 Bug Reports](../test-artifacts/BugReports.md)

---

## 📌 Notes

> The checklists can be updated as the application functionality and testing scope evolve.
