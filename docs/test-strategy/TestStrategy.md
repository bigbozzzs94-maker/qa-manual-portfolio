# Test Strategy

## 1. Purpose

This document describes the overall testing approach for the BookCart project.

The goal is to ensure that the main application functionality, user flows, and REST API work correctly.

---

## 2. Testing Approach

The testing process includes:

- Manual Functional Testing
- UI Testing
- API Testing
- Smoke Testing
- Regression Testing
- Cross-browser Testing

Testing will be performed using a risk-based approach, with priority given to critical functionality.

---

## 3. Test Levels

### UI Testing

The web application will be tested from the user's perspective.

Main areas:

- Registration
- Authentication
- Product Catalog
- Product Search
- Shopping Cart
- Checkout
- Order History

### API Testing

REST API endpoints will be tested using Postman.

The following will be verified:

- HTTP status codes
- Response body
- Request parameters
- Error responses
- Data validation

---

## 4. Test Techniques

The following test design techniques will be used:

- Equivalence Partitioning
- Boundary Value Analysis
- Decision Table Testing
- State Transition Testing
- Error Guessing

---

## 5. Test Priorities

### High Priority

- User Authentication
- Registration
- Shopping Cart
- Checkout
- Critical API endpoints

### Medium Priority

- Product Search
- User Profile
- Order History

### Low Priority

- Minor UI elements
- Non-critical visual issues

---

## 6. Defect Management

Defects will be reported in Jira.

Each defect report should include:

- Summary
- Preconditions
- Steps to Reproduce
- Actual Result
- Expected Result
- Severity
- Priority
- Screenshots or additional evidence

---

## 7. Tools

| Area | Tool |
|---|---|
| Test Management | Jira |
| API Testing | Postman |
| API Documentation | Swagger |
| Browser Testing | Google Chrome |
| Debugging | Chrome DevTools |
| Proxy | Charles Proxy |
| Database | SQL Server |
| Version Control | Git / GitHub |

---

## 8. Entry Criteria

Testing can start when:

- Application build is available
- Test environment is accessible
- Requirements are available
- Required test data is prepared

---

## 9. Exit Criteria

Testing can be completed when:

- High priority test cases are executed
- Critical defects are fixed
- Regression testing is completed
- Test results are documented
