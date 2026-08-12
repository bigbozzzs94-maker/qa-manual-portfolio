# 📋 Test Plan

> Comprehensive test plan for the **BookCart — E-commerce Web Application**.

---

## 📌 Project Information

| Parameter | Description |
|---|---|
| **Project** | BookCart |
| **Application Type** | E-commerce Web Application |
| **Platform** | Web |
| **Testing Type** | Manual Testing |
| **Document Type** | Test Plan |
| **Status** | Active |

---

# 🎯 1. Test Objectives

The main objective of testing is to verify that the BookCart application works according to the expected requirements and provides a stable user experience.

Testing objectives include:

- Verify critical business functionality
- Identify functional defects
- Validate user input
- Verify positive and negative scenarios
- Verify integration between application modules
- Validate API responses
- Verify database data where applicable
- Reduce the risk of critical defects before release

---

# 📦 2. Test Scope

## ✅ In Scope

The following functionality is included in testing:

### 📝 Registration

- User registration
- Email validation
- Password validation
- Required field validation
- Password confirmation
- Existing email validation

### 🔐 Authentication

- User login
- User logout
- Valid credentials
- Invalid credentials
- Session validation
- Protected page access

### 📚 Product Catalog

- Product list
- Product details
- Product information
- Product price
- Product images

### 🔎 Product Search

- Search by product name
- Partial search
- Case-insensitive search
- Empty search
- Non-existing product search

### 🛒 Shopping Cart

- Add products
- Remove products
- Update product quantity
- Cart total calculation
- Empty cart handling

### 💳 Checkout

- Checkout navigation
- Required field validation
- Customer information validation
- Order summary
- Order creation

### 📦 Order Management

- Order list
- Order details
- Order status
- Order information validation

### 🔌 API Testing

- Request validation
- Response validation
- HTTP status codes
- Authentication
- Authorization
- Positive scenarios
- Negative scenarios

---

## ⛔ Out of Scope

The following testing types are outside the scope of the current portfolio project:

- Load Testing
- Stress Testing
- Full Performance Testing
- Penetration Testing
- Full Security Testing
- Accessibility Testing
- Automated End-to-End Testing

---

# 🧪 3. Test Strategy

The following testing types will be performed:

| Test Type | Description |
|---|---|
| Smoke Testing | Verification of critical functionality |
| Functional Testing | Verification of application requirements |
| UI Testing | Verification of interface behavior |
| Positive Testing | Testing with valid data |
| Negative Testing | Testing with invalid data |
| Regression Testing | Verification after changes |
| Exploratory Testing | Investigation of potential defects |
| API Testing | Backend endpoint validation |
| Integration Testing | Verification of module interaction |

---

# 🧩 4. Test Design Techniques

The following techniques are used to design test scenarios:

- Equivalence Partitioning
- Boundary Value Analysis
- Decision Table Testing
- State Transition Testing
- Error Guessing

### Examples

| Technique | Example |
|---|---|
| Equivalence Partitioning | Valid and invalid product quantity ranges |
| Boundary Value Analysis | Test values `0`, `1`, `10`, `11` |
| Decision Table | Order creation conditions |
| State Transition | Order status changes |
| Error Guessing | Invalid input and common risk scenarios |

---

# 🛠 5. Test Environment

## Application Environment

| Component | Description |
|---|---|
| Application | BookCart |
| Platform | Web |
| Browser | Google Chrome |
| Testing | Manual Testing |

## Tools

| Tool | Purpose |
|---|---|
| Jira | Task and defect tracking |
| Postman | API testing |
| Swagger | API documentation |
| Chrome DevTools | Frontend debugging and network analysis |
| Charles Proxy | Network traffic analysis |
| SQL | Database validation |
| Git | Version control |
| GitHub | Documentation and portfolio |
| Confluence | Documentation |
| Kibana | Log analysis |
| Android Studio | Mobile testing |

---

# 👥 6. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| QA Engineer | Test planning and execution |
| QA Engineer | Checklist creation |
| QA Engineer | Test case creation |
| QA Engineer | Functional testing |
| QA Engineer | API testing |
| QA Engineer | Bug reporting |
| QA Engineer | Regression testing |
| Developer | Defect fixing |
| Analyst | Requirement clarification |
| Team Lead | Testing coordination |

---

# 🔄 7. Testing Process

```text
Requirements Analysis
        ↓
Test Planning
        ↓
Test Design
        ↓
Checklist Creation
        ↓
Test Case Creation
        ↓
Test Environment Preparation
        ↓
Test Execution
        ↓
Bug Reporting
        ↓
Bug Verification
        ↓
Regression Testing
        ↓
Test Completion
```

---

# 🚀 8. Entry Criteria

Testing can begin when:

- [x] Requirements are available
- [x] Application build is available
- [x] Test environment is accessible
- [x] Required test data is available
- [x] Critical functionality is implemented
- [x] API documentation is available where required

---

# 🏁 9. Exit Criteria

Testing can be considered complete when:

- [x] Planned test cases have been executed
- [x] Critical functionality has been tested
- [x] Critical defects are resolved or documented
- [x] High-priority defects are resolved or accepted
- [x] Regression testing is completed
- [x] Test results are documented

---

# ⚠️ 10. Risks

| Risk | Impact | Mitigation |
|---|---|---|
| Unclear requirements | High | Clarify requirements with stakeholders |
| Unstable environment | High | Report environment issues and retest |
| Insufficient test data | Medium | Prepare test data in advance |
| Limited testing time | High | Prioritize critical functionality |
| Late changes | High | Perform focused regression testing |
| API instability | Medium | Retest endpoints and validate logs |
| Undetected integration issues | High | Test critical end-to-end flows |

---

# 📊 11. Test Deliverables

The following QA artifacts are created during testing:

- 🧠 Mind Map
- 📌 Project Overview
- ✅ Checklists
- 🧪 Test Cases
- 📋 Test Plan
- 🎯 Test Strategy
- 🧩 Test Design Techniques
- 🔌 API Test Cases
- 🐞 Bug Reports
- 🗄 SQL Queries

---

# 🔗 Related Documentation

- [📌 Project Overview](../project-overview/ProjectOverview.md)
- [🧠 Mind Map](../mind-maps/MindMap.md)
- [🧩 Test Design](../test-design/TestDesign.md)
- [✅ Checklists](../../checklists/Checklists.md)
- [🧪 Test Cases](../test-cases/TestCases.md)
- [🎯 Test Strategy](../test-strategy/TestStrategy.md)
- [🔌 API Testing](../../api-testing/ApiTesting.md)
- [🐞 Bug Reports](../../test-artifacts/BugReports.md)
- [🗄 SQL Queries](../../sql/SQLQueries.md)

---

## 📌 Notes

> This test plan defines the overall scope, objectives, approach, environment, risks, and deliverables for testing the BookCart application.
