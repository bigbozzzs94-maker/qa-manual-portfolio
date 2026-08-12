# Bug Reports

## Project

**BookCart — E-commerce Web Application**

This document contains sample bug reports identified during functional testing of the BookCart application.

---

# BUG-001 — Registration allows invalid email format

**Severity:** Major  
**Priority:** High  
**Status:** Open

### Environment

- OS: Windows 11
- Browser: Google Chrome
- Application: BookCart Web Application

### Preconditions

- User is on the Registration page.

### Steps to Reproduce

1. Open the Registration page.
2. Enter `test@` in the Email field.
3. Enter a valid password.
4. Confirm the password.
5. Click the **Register** button.

### Actual Result

The registration request is accepted with an invalid email format.

### Expected Result

A validation error message should be displayed, and the user should not be registered.

---

# BUG-002 — User can submit registration form with empty required fields

**Severity:** Major  
**Priority:** High  
**Status:** Open

### Environment

- OS: Windows 11
- Browser: Google Chrome
- Application: BookCart Web Application

### Preconditions

- User is on the Registration page.

### Steps to Reproduce

1. Open the Registration page.
2. Leave all required fields empty.
3. Click the **Register** button.

### Actual Result

The form is submitted without displaying validation messages.

### Expected Result

Validation messages should be displayed for all required fields, and the form should not be submitted.

---

# BUG-003 — Shopping cart quantity accepts negative values

**Severity:** Major  
**Priority:** High  
**Status:** Open

### Environment

- OS: Windows 11
- Browser: Google Chrome
- Application: BookCart Web Application

### Preconditions

- User is logged in.
- At least one product has been added to the shopping cart.

### Steps to Reproduce

1. Open the Shopping Cart.
2. Enter a negative value in the product quantity field.
3. Update the cart.

### Actual Result

The shopping cart accepts a negative quantity value.

### Expected Result

The system should prevent negative values and display a validation message.

---

# BUG-004 — Product search displays incorrect results

**Severity:** Major  
**Priority:** Medium  
**Status:** Open

### Environment

- OS: Windows 11
- Browser: Google Chrome
- Application: BookCart Web Application

### Preconditions

- Product catalog contains products with different names.

### Steps to Reproduce

1. Open the Product Catalog.
2. Enter an existing product name in the Search field.
3. Click the **Search** button.

### Actual Result

The search results contain products that do not match the entered search query.

### Expected Result

Only products matching the entered search query should be displayed.

---

# BUG-005 — Order can be created without required delivery information

**Severity:** Critical  
**Priority:** High  
**Status:** Open

### Environment

- OS: Windows 11
- Browser: Google Chrome
- Application: BookCart Web Application

### Preconditions

- User is logged in.
- At least one product has been added to the shopping cart.

### Steps to Reproduce

1. Open the Shopping Cart.
2. Proceed to Checkout.
3. Leave the required delivery information empty.
4. Click the **Place Order** button.

### Actual Result

The order is successfully created without required delivery information.

### Expected Result

Validation messages should be displayed, and the order should not be created until all required fields are completed.

---

## Bug Summary

| Bug ID | Summary | Severity | Priority | Status |
|---|---|---|---|---|
| BUG-001 | Invalid email is accepted during registration | Major | High | Open |
| BUG-002 | Registration form can be submitted with empty required fields | Major | High | Open |
| BUG-003 | Shopping cart accepts negative product quantity | Major | High | Open |
| BUG-004 | Product search displays incorrect results | Major | Medium | Open |
| BUG-005 | Order can be created without delivery information | Critical | High | Open |
