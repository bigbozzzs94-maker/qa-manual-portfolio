# Test Plan

## 1. Project Information

**Project:** BookCart — E-commerce Web Application  
**Document Type:** Test Plan  
**Testing Type:** Manual Testing  
**Status:** Active  

BookCart is an e-commerce web application that allows users to register, log in, browse products, search for products, manage a shopping cart, and place orders.

---

## 2. Purpose

The purpose of this test plan is to define the scope, objectives, strategy, resources, and approach for testing the BookCart application.

Testing is performed to verify that the main functionality works according to requirements and to identify defects before release.

---

## 3. Test Objectives

The main objectives of testing are:

- Verify user registration functionality.
- Verify user authentication and authorization.
- Verify product catalog functionality.
- Verify product search.
- Verify shopping cart functionality.
- Verify checkout and order creation.
- Verify API responses for key application functionality.
- Verify validation and error messages.
- Identify and document defects.

---

## 4. Scope of Testing

### In Scope

The following functionality will be tested:

#### Authentication

- User registration.
- Registration with valid data.
- Registration with invalid data.
- Registration with an existing email.
- User login with valid credentials.
- User login with invalid credentials.
- Logout functionality.
- Validation of authentication fields.

#### Product Catalog

- Opening the product catalog.
- Displaying products.
- Searching for existing products.
- Searching for non-existing products.
- Opening product details.
- Verifying product information.

#### Shopping Cart

- Adding products to the cart.
- Removing products from the cart.
- Changing product quantity.
- Verifying cart total.
- Verifying cart persistence.

#### Checkout

- Opening the checkout page.
- Completing checkout with valid data.
- Validating required fields.
- Creating an order.
- Verifying successful order confirmation.

#### API Testing

- Verifying request methods.
- Verifying response status codes.
- Verifying response body.
- Verifying response headers.
- Testing positive and negative scenarios.

---

## 5. Out of Scope

The following functionality is not included in the current testing scope:

- Performance testing.
- Load testing.
- Stress testing.
- Security penetration testing.
- Full cross-browser testing.
- Accessibility testing.
- Automated testing.

These areas may be covered in future testing iterations.

---

## 6. Test Approach

Testing will be performed manually using functional and non-functional testing techniques.

The following testing types will be used:

- Functional Testing.
- Smoke Testing.
- Regression Testing.
- Positive Testing.
- Negative Testing.
- Integration Testing.
- API Testing.
- UI Testing.

Testing will be performed based on available application requirements and expected system behavior.

---

## 7. Test Design Techniques

The following test design techniques will be used:

- Equivalence Partitioning.
- Boundary Value Analysis.
- Decision Table Testing.
- State Transition Testing.
- Error Guessing.

These techniques will help cover both valid and invalid application scenarios.

---

## 8. Test Environment

### Operating System

- Windows 11.

### Browsers

- Google Chrome.

### Tools

- Jira — defect tracking and task management.
- Postman — API testing.
- Swagger — API documentation and endpoint verification.
- Chrome DevTools — frontend and network analysis.
- Charles Proxy — HTTP/HTTPS traffic analysis.
- SQL — database queries and data verification.
- GitHub — test documentation storage.
- Git — version control.

---

## 9. Test Data

The following test data categories will be used:

### Valid Data

- Valid email addresses.
- Valid passwords.
- Existing user accounts.
- Existing products.
- Valid checkout information.

### Invalid Data

- Invalid email format.
- Empty required fields.
- Incorrect passwords.
- Non-existing user accounts.
- Non-existing products.
- Invalid checkout data.

Test data should not contain real confidential or personal user information.

---

## 10. Entry Criteria

Testing can begin when:

- The application build is available.
- Main functionality is implemented.
- The test environment is available.
- Required test data is available.
- API documentation is available, if applicable.
- Test cases and checklists are prepared.

---

## 11. Exit Criteria

Testing can be considered complete when:

- All planned test cases have been executed.
- Critical defects have been fixed or accepted.
- High-priority defects have been fixed or accepted.
- Regression testing has been completed.
- Test results have been documented.
- Known issues have been recorded.

---

## 12. Defect Management

All identified defects should contain the following information:

- Bug ID.
- Title.
- Environment.
- Preconditions.
- Steps to reproduce.
- Actual result.
- Expected result.
- Severity.
- Priority.
- Status.
- Attachments, if required.

Defects will be documented and tracked using Jira.

Bug report examples are available in:

[`test-artifacts/BugReports.md`](../../test-artifacts/BugReports.md)

---

## 13. Test Deliverables

The following QA documentation is included in the project:

- Test Plan.
- Checklists.
- Test Cases.
- Bug Reports.
- SQL Queries.
- API Testing documentation.
- Screenshots and supporting artifacts.

Related documents:

- [`Checklists`](../../Checklists/Checklists.md)
- [`Test Cases`](../test-cases/TestCases.md)
- [`Bug Reports`](../../test-artifacts/BugReports.md)
- [`SQL Queries`](../../sql/SQLQueries.md)

---

## 14. Risks

Potential testing risks include:

| Risk | Impact | Mitigation |
|---|---|---|
| Application environment is unavailable | Testing delays | Report the issue and resume testing when the environment is available |
| Requirements are unclear | Incorrect test coverage | Clarify expected behavior before testing |
| Test data is unavailable | Test execution is limited | Prepare test data before testing |
| Critical defects are found late | Release delays | Perform smoke and regression testing regularly |
| Application functionality changes | Existing tests may become outdated | Update test documentation and execute regression testing |

---

## 15. Roles and Responsibilities

### QA Engineer

Responsibilities:

- Analyze requirements.
- Prepare test documentation.
- Create checklists.
- Create test cases.
- Execute manual testing.
- Perform API testing.
- Perform regression testing.
- Create bug reports.
- Verify defect fixes.
- Prepare test results.

### Developers

Responsibilities:

- Implement application functionality.
- Fix identified defects.
- Provide technical information when required.

### Team Lead / Project Manager

Responsibilities:

- Coordinate testing activities.
- Define priorities.
- Support issue resolution.
- Approve testing scope and release decisions.

---

## 16. Test Status

Testing status is tracked during test execution.

Possible test statuses:

- **Not Run**
- **Pass**
- **Fail**
- **Blocked**
- **Skipped**

---

## 17. Approval

The test plan may be updated during the project lifecycle if application requirements, functionality, or testing scope changes.

All significant changes should be reviewed before the next testing cycle.
