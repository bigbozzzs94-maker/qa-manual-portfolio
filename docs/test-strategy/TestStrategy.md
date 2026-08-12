# 🎯 Test Strategy

> Testing strategy for the **BookCart — E-commerce Web Application**.

---

## 📋 Project Information

| Parameter | Description |
|---|---|
| **Project** | BookCart |
| **Application Type** | E-commerce Web Application |
| **Platform** | Web |
| **Testing Type** | Manual Testing |
| **Document Type** | Test Strategy |
| **Status** | Active |

---

# 🎯 1. Purpose

This document defines the overall testing approach for the BookCart application.

The main purpose of the testing strategy is to identify the most important testing areas, prioritize testing activities, and ensure sufficient coverage of critical business functionality.

---

# 🧭 2. Testing Approach

The testing approach is based on:

- Risk-Based Testing
- Functional Testing
- Positive Testing
- Negative Testing
- Exploratory Testing
- Regression Testing
- Smoke Testing
- API Testing
- Integration Testing

The main focus is placed on critical user flows and business functionality.

---

# ⚠️ 3. Risk-Based Testing

Testing priorities are determined according to the impact of functionality on the application.

## 🔴 Critical Priority

Critical functionality includes:

- User authentication
- Shopping cart
- Checkout
- Order creation
- API authorization

A defect in these areas may prevent users from completing the main business flow.

## 🟠 High Priority

High-priority functionality includes:

- Registration
- Product catalog
- Product details
- Order management
- API request and response validation

## 🟡 Medium Priority

Medium-priority functionality includes:

- Product search
- Navigation
- General UI behavior
- Error message validation

---

# 🔄 4. Testing Levels

The following testing levels are covered in the project:

| Testing Level | Description |
|---|---|
| System Testing | Verification of the complete application |
| Integration Testing | Verification of interaction between modules |
| API Testing | Verification of backend endpoints |
| UI Testing | Verification of user interface behavior |

---

# 🧪 5. Testing Types

## Smoke Testing

Smoke testing is performed to verify that the main functionality is working before detailed testing begins.

Critical smoke scenarios include:

- [ ] Application opens successfully
- [ ] User can register
- [ ] User can log in
- [ ] Product catalog is available
- [ ] Product can be added to the cart
- [ ] Checkout page opens
- [ ] Order can be created

---

## Functional Testing

Functional testing verifies that the application works according to expected requirements.

Main areas:

- Registration
- Authentication
- Product catalog
- Product search
- Shopping cart
- Checkout
- Orders

---

## Positive Testing

Positive testing verifies application behavior using valid input data.

Examples:

- Login with valid credentials
- Registration with valid data
- Search for an existing product
- Add a product to the cart
- Create an order with valid information

---

## Negative Testing

Negative testing verifies how the application handles invalid or unexpected data.

Examples:

- Login with an invalid password
- Registration with an existing email
- Empty required fields
- Invalid email format
- Invalid product ID
- Access to protected pages without authentication
- Order creation with an empty cart

---

## Regression Testing

Regression testing is performed after application changes or defect fixes.

The main focus is on:

- Previously fixed defects
- Related functionality
- Critical user flows
- Main business processes

---

## Exploratory Testing

Exploratory testing is used to investigate the application without following only predefined test cases.

Focus areas include:

- Unexpected user actions
- Invalid input
- Edge cases
- Navigation issues
- UI inconsistencies
- Potential integration issues

---

## API Testing

API testing focuses on backend functionality.

Validation includes:

- HTTP methods
- Status codes
- Request parameters
- Request body
- Response body
- JSON structure
- Authentication
- Authorization
- Error messages

---

# 🧩 6. Test Design Techniques

The following test design techniques are used:

| Technique | Purpose |
|---|---|
| Equivalence Partitioning | Divide input data into valid and invalid groups |
| Boundary Value Analysis | Test values near input boundaries |
| Decision Table Testing | Test combinations of multiple conditions |
| State Transition Testing | Verify changes between application states |
| Error Guessing | Identify likely problem areas |

---

# 🚀 7. Test Execution Strategy

Testing is performed in the following order:

```text
Smoke Testing
      ↓
Critical Functionality Testing
      ↓
Functional Testing
      ↓
Positive Testing
      ↓
Negative Testing
      ↓
API Testing
      ↓
Exploratory Testing
      ↓
Regression Testing
```

---

# 📌 8. Critical User Flows

The following user flows have the highest testing priority.

## Flow 1 — User Registration

```text
Open Registration Page
        ↓
Enter Valid Data
        ↓
Submit Registration Form
        ↓
Account Created
```

## Flow 2 — User Login

```text
Open Login Page
        ↓
Enter Credentials
        ↓
Submit Login Form
        ↓
User Authenticated
```

## Flow 3 — Purchase Flow

```text
Browse Products
        ↓
Select Product
        ↓
Add to Cart
        ↓
Open Cart
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

# 🛠️ 9. Tools

| Tool | Purpose |
|---|---|
| Jira | Task and defect tracking |
| Postman | API testing |
| Swagger | API documentation |
| Chrome DevTools | Browser debugging and network analysis |
| Charles Proxy | Network traffic analysis |
| SQL | Database validation |
| Git | Version control |
| GitHub | QA portfolio and documentation |
| Confluence | Documentation |
| Kibana | Log analysis |

---

# 📊 10. Test Prioritization

| Priority | Description | Examples |
|---|---|---|
| 🔴 Critical | Main business flow is blocked | Login, Checkout, Order Creation |
| 🟠 High | Important functionality is affected | Registration, Cart, Product Catalog |
| 🟡 Medium | Functionality works but has lower impact | Search, Navigation, UI |
| 🟢 Low | Minor impact on user experience | Cosmetic issues |

---

# ⚠️ 11. Risks and Mitigation

| Risk | Impact | Mitigation |
|---|---|---|
| Unclear requirements | High | Clarify requirements before testing |
| Limited testing time | High | Prioritize critical functionality |
| Unstable test environment | High | Report issues and retest |
| Insufficient test data | Medium | Prepare test data in advance |
| Late changes | High | Perform focused regression testing |
| API instability | Medium | Retest endpoints and analyze logs |
| Integration defects | High | Test end-to-end user flows |

---

# 📈 12. Test Coverage

Testing coverage includes:

- [x] Critical business flows
- [x] Positive scenarios
- [x] Negative scenarios
- [x] Boundary values
- [x] Input validation
- [x] API requests
- [x] API responses
- [x] Authentication
- [x] Authorization
- [x] Error handling
- [x] Integration points
- [x] Regression scenarios

---

# 🏁 13. Completion Criteria

Testing can be considered complete when:

- Critical functionality has been tested
- Planned test cases have been executed
- Critical defects have been resolved or documented
- High-priority defects have been resolved or accepted
- Regression testing has been completed
- Test documentation has been updated

---

# 🔗 Related Documentation

- [📌 Project Overview](../project-overview/ProjectOverview.md)
- [🧠 Mind Map](../mind-maps/MindMap.md)
- [🧩 Test Design](../test-design/TestDesign.md)
- [🧪 Test Cases](../test-cases/TestCases.md)
- [📋 Test Plan](../test-plan/TestPlan.md)
- [✅ Checklists](../../checklists/Checklists.md)
- [🔌 API Testing](../../api-testing/ApiTesting.md)
- [🐞 Bug Reports](../../test-artifacts/BugReports.md)

---

## 📌 Notes

> This strategy is focused on risk-based testing and prioritizes critical business functionality to achieve effective test coverage.
