# 🐞 Bug Reports

> Sample bug reports for the **BookCart — E-commerce Web Application**.

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

# 🎯 Purpose

This document contains examples of defects identified during testing of the BookCart application.

Each bug report includes:

- Summary
- Preconditions
- Steps to Reproduce
- Actual Result
- Expected Result
- Severity
- Priority
- Environment
- Status

---

# 🐞 BUG-001 — User Can Log In with Incorrect Password

## 📌 Information

| Parameter | Value |
|---|---|
| **Severity** | Critical |
| **Priority** | High |
| **Status** | Open |
| **Module** | Authentication |
| **Environment** | Windows 10, Google Chrome |

### Preconditions

- A registered user exists.

### Steps to Reproduce

1. Open the Login page.
2. Enter a valid registered email.
3. Enter an incorrect password.
4. Click the **Login** button.

### Actual Result

The user is successfully authenticated and gains access to the application.

### Expected Result

The authentication request should be rejected. The user should remain logged out, and an appropriate error message should be displayed.

### Notes

This issue may lead to unauthorized access to user accounts.

---

# 🐞 BUG-002 — Cart Total Is Not Updated After Changing Product Quantity

## 📌 Information

| Parameter | Value |
|---|---|
| **Severity** | Major |
| **Priority** | High |
| **Status** | Open |
| **Module** | Shopping Cart |
| **Environment** | Windows 10, Google Chrome |

### Preconditions

- At least one product is added to the shopping cart.

### Steps to Reproduce

1. Open the shopping cart.
2. Note the current product quantity and total amount.
3. Increase the product quantity.
4. Check the total amount.

### Actual Result

The product quantity increases, but the total cart amount remains unchanged.

### Expected Result

The total cart amount should be recalculated according to the updated product quantity.

---

# 🐞 BUG-003 — Order Can Be Created with an Empty Cart

## 📌 Information

| Parameter | Value |
|---|---|
| **Severity** | Critical |
| **Priority** | Critical |
| **Status** | Open |
| **Module** | Checkout / Orders |
| **Environment** | Windows 10, Google Chrome |

### Preconditions

- User is authenticated.
- Shopping cart is empty.

### Steps to Reproduce

1. Open the checkout page.
2. Enter valid required customer information.
3. Click the **Place Order** button.

### Actual Result

The order is successfully created even though the shopping cart does not contain any products.

### Expected Result

Order creation should be blocked. The application should display a validation message indicating that the cart is empty.

---

# 🐞 BUG-004 — Registration Allows Duplicate Email Addresses

## 📌 Information

| Parameter | Value |
|---|---|
| **Severity** | Major |
| **Priority** | High |
| **Status** | Open |
| **Module** | Registration |
| **Environment** | Windows 10, Google Chrome |

### Preconditions

- A user with `testuser@example.com` already exists.

### Steps to Reproduce

1. Open the Registration page.
2. Enter `testuser@example.com`.
3. Enter a valid password.
4. Confirm the password.
5. Click the **Register** button.

### Actual Result

A new account is successfully created using an email address that already exists.

### Expected Result

Registration should be rejected, and an appropriate error message should indicate that the email address is already in use.

---

# 🐞 BUG-005 — Product Search Returns Incorrect Results

## 📌 Information

| Parameter | Value |
|---|---|
| **Severity** | Minor |
| **Priority** | Medium |
| **Status** | Open |
| **Module** | Product Search |
| **Environment** | Windows 10, Google Chrome |

### Preconditions

- Product catalog contains multiple products.

### Steps to Reproduce

1. Open the product catalog.
2. Enter the name of an existing product in the search field.
3. Start the search.
4. Review the search results.

### Actual Result

The search results contain products that do not match the search query.

### Expected Result

Only products matching the search query should be displayed.

---

# 🐞 BUG-006 — User Can Access Protected Orders Page After Logout

## 📌 Information

| Parameter | Value |
|---|---|
| **Severity** | Major |
| **Priority** | High |
| **Status** | Open |
| **Module** | Authentication / Orders |
| **Environment** | Windows 10, Google Chrome |

### Preconditions

- User is logged in.

### Steps to Reproduce

1. Log in to the application.
2. Open the Orders page.
3. Log out.
4. Enter the Orders page URL directly in the browser.

### Actual Result

The Orders page opens and displays user order information.

### Expected Result

The user should not have access to protected pages after logout and should be redirected to the Login page.

---

# 📊 Bug Summary

| Bug ID | Summary | Severity | Priority |
|---|---|---|---|
| BUG-001 | Login with incorrect password | Critical | High |
| BUG-002 | Cart total is not updated | Major | High |
| BUG-003 | Order created with empty cart | Critical | Critical |
| BUG-004 | Duplicate email registration | Major | High |
| BUG-005 | Incorrect search results | Minor | Medium |
| BUG-006 | Protected page accessible after logout | Major | High |

---

# ⚠️ Severity vs Priority

## Severity

**Severity** indicates how strongly a defect affects the functionality of the application.

| Severity | Description |
|---|---|
| Critical | Main functionality is blocked or a serious security/data issue exists |
| Major | Important functionality works incorrectly |
| Minor | Functionality is affected but the impact is limited |
| Trivial | Cosmetic or low-impact issue |

## Priority

**Priority** indicates how quickly the defect should be fixed.

| Priority | Description |
|---|---|
| Critical | Must be fixed immediately |
| High | Should be fixed as soon as possible |
| Medium | Can be fixed according to the development plan |
| Low | Can be fixed later |

### Examples

> **High Severity + Medium Priority** — the issue is serious but affects functionality that is rarely used.

> **Low Severity + High Priority** — the issue has a low technical impact but is highly visible to users.

---

# 📝 Bug Report Template

## 🐞 BUG-XXX — Short and Clear Summary

| Parameter | Value |
|---|---|
| **Severity** | |
| **Priority** | |
| **Status** | Open |
| **Module** | |
| **Environment** | |

### Preconditions

Describe the required application state before reproducing the defect.

### Steps to Reproduce

1. Step one.
2. Step two.
3. Step three.

### Actual Result

Describe what actually happens.

### Expected Result

Describe what should happen according to the requirements.

### Attachments

- Screenshot
- Video
- Logs
- Console errors
- Network request information

---

# 🔗 Related Documentation

- [📌 Project Overview](../docs/project-overview/ProjectOverview.md)
- [🧠 Mind Map](../docs/mind-maps/MindMap.md)
- [🧪 Test Cases](../docs/test-cases/TestCases.md)
- [📋 Test Plan](../docs/test-plan/TestPlan.md)
- [🎯 Test Strategy](../docs/test-strategy/TestStrategy.md)
- [🧩 Test Design](../docs/test-design/TestDesign.md)
- [✅ Checklists](../checklists/Checklists.md)
- [🔌 API Testing](../api-testing/ApiTesting.md)

---

## 📌 Notes

> These bug reports are sample defects created for the QA portfolio project and demonstrate the structure and level of detail used when reporting issues during software testing.
