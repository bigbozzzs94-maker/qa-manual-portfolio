# 📌 Project Overview

> Overview of the **BookCart — E-commerce Web Application** used as a QA portfolio project.

---

## 📋 Project Information

| Parameter | Description |
|---|---|
| **Project Name** | BookCart |
| **Application Type** | E-commerce Web Application |
| **Platform** | Web |
| **Testing Type** | Manual Testing |
| **Project Status** | QA Portfolio Project |

---

## 🎯 Project Description

**BookCart** is an e-commerce web application that allows users to browse products, search for specific items, manage a shopping cart, and place orders.

The project is used as a practical example for demonstrating QA skills and creating testing documentation.

---

## 👥 User Roles

### 👤 Guest User

A guest user can:

- Browse the product catalog
- Search for products
- View product details
- Navigate through the application
- Access registration and login pages

### 🔐 Registered User

An authenticated user can:

- Log in and log out
- Manage the shopping cart
- Add products to the cart
- Update product quantity
- Remove products from the cart
- Proceed to checkout
- Create orders
- View order history
- View order details

---

# 🧩 Main Functional Areas

---

## 📝 Registration

The registration module allows a new user to create an account.

### Main Functionality

- User registration
- Email validation
- Password validation
- Required field validation
- Password confirmation
- Duplicate email validation
- Error message validation

---

## 🔐 Authentication

The authentication module allows registered users to access protected functionality.

### Main Functionality

- User login
- User logout
- Session management
- Authentication validation
- Invalid credentials handling
- Protected page access validation

---

## 📚 Product Catalog

The product catalog allows users to browse available products.

### Main Functionality

- Display product list
- Display product name
- Display product price
- Display product image
- Open product details
- Validate product information

---

## 🔎 Product Search

The search functionality allows users to find products.

### Main Functionality

- Search by product name
- Partial search
- Case-insensitive search
- Empty search handling
- Non-existing product search
- Special character validation

---

## 🛒 Shopping Cart

The shopping cart allows users to manage selected products before checkout.

### Main Functionality

- Add product to cart
- View cart contents
- Update product quantity
- Remove product
- Calculate total amount
- Handle empty cart
- Validate cart data

---

## 💳 Checkout

The checkout process allows users to provide required information and place an order.

### Main Functionality

- Navigate to checkout
- Display order summary
- Validate required fields
- Validate customer information
- Calculate order total
- Confirm order
- Display order confirmation

---

## 📦 Order Management

The order management module allows users to view information about created orders.

### Main Functionality

- View order list
- View order details
- Display order ID
- Display order date
- Display order status
- Display ordered products
- Display order total

---

# 🔄 Main User Flow

```text
Open Application
      ↓
Browse Product Catalog
      ↓
Search / Select Product
      ↓
View Product Details
      ↓
Add Product to Cart
      ↓
Open Shopping Cart
      ↓
Update Quantity
      ↓
Proceed to Checkout
      ↓
Enter Required Information
      ↓
Confirm Order
      ↓
Order Created
```

---

# 🧪 Testing Scope

## ✅ In Scope

The following areas are included in testing:

- [x] Registration
- [x] Authentication
- [x] Product Catalog
- [x] Product Search
- [x] Shopping Cart
- [x] Checkout
- [x] Order Management
- [x] UI Testing
- [x] Functional Testing
- [x] API Testing
- [x] Positive Testing
- [x] Negative Testing
- [x] Regression Testing
- [x] Smoke Testing

## ⛔ Out of Scope

The following areas are not covered in the current portfolio project:

- [ ] Load Testing
- [ ] Stress Testing
- [ ] Full Security Testing
- [ ] Penetration Testing
- [ ] Accessibility Testing
- [ ] Automated End-to-End Testing

---

# 🛠 Tools & Technologies

| Tool | Purpose |
|---|---|
| Jira | Task and defect tracking |
| Postman | API testing |
| Swagger | API documentation |
| Chrome DevTools | Frontend testing and debugging |
| Charles Proxy | Network traffic analysis |
| SQL | Database testing and data validation |
| Git | Version control |
| GitHub | Portfolio and documentation storage |
| Confluence | Documentation |
| Kibana | Log analysis |
| Android Studio | Mobile application testing |

---

# 📂 QA Documentation

This project contains the following QA artifacts:

| Artifact | Description |
|---|---|
| 🧠 Mind Map | Visual project and testing overview |
| ✅ Checklists | High-level functional checks |
| 🧪 Test Cases | Detailed test scenarios |
| 📋 Test Plan | Testing scope and planning |
| 🎯 Test Strategy | Overall testing approach |
| 🔌 API Testing | API documentation and API test cases |
| 🐞 Bug Reports | Examples of identified defects |
| 🗄 SQL Queries | Database queries and data validation |

---

# 📊 Testing Approach

The following testing activities are applied to the project:

1. Requirement and functionality analysis
2. Test scenario identification
3. Test documentation creation
4. Checklist preparation
5. Test case creation
6. Functional testing
7. UI testing
8. API testing
9. Database validation
10. Bug reporting
11. Regression testing

---

# 🔗 Related Documentation

- [🧠 Mind Map](../mind-maps/MindMap.md)
- [✅ Checklists](../../checklists/Checklists.md)
- [🧪 Test Cases](../test-cases/TestCases.md)
- [📋 Test Plan](../test-plan/TestPlan.md)
- [🎯 Test Strategy](../test-strategy/TestStrategy.md)
- [🔌 API Testing](../../api-testing/ApiTesting.md)
- [🐞 Bug Reports](../../test-artifacts/BugReports.md)
- [🗄 SQL Queries](../../sql/SQLQueries.md)

---

## 📌 Notes

> This project is maintained as a QA portfolio project to demonstrate practical skills in software testing, test documentation, API testing, bug reporting, and SQL.
