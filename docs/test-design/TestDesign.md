# 🧩 Test Design Techniques

> Test design techniques used for the **BookCart — E-commerce Web Application**.

---

## 📋 Project Information

| Parameter | Description |
|---|---|
| **Project** | BookCart |
| **Application Type** | E-commerce Web Application |
| **Testing Type** | Manual Testing |
| **Document Type** | Test Design Techniques |
| **Status** | Active |

---

## 🎯 Purpose

Test design techniques help create effective test scenarios and improve test coverage.

The following techniques are used in this project:

- Equivalence Partitioning
- Boundary Value Analysis
- Decision Table Testing
- State Transition Testing
- Error Guessing

---

# 1️⃣ Equivalence Partitioning

## 📌 Description

Equivalence Partitioning divides input data into groups where the application is expected to behave similarly.

Instead of testing every possible value, one representative value from each equivalence class can be selected.

---

## Example: Product Quantity

Assume that the allowed product quantity is from `1` to `10`.

### Equivalence Classes

| Class | Values | Expected Result |
|---|---|---|
| Valid | `1–10` | Quantity is accepted |
| Invalid | `< 1` | Validation error |
| Invalid | `> 10` | Validation error |
| Invalid | Non-numeric value | Validation error |

### Example Test Data

```text
0       → Invalid
1       → Valid
5       → Valid
10      → Valid
11      → Invalid
abc     → Invalid
```

---

# 2️⃣ Boundary Value Analysis

## 📌 Description

Boundary Value Analysis focuses on values at the edges of valid and invalid ranges.

Errors often occur near boundary values.

---

## Example: Product Quantity

Allowed range:

```text
Minimum = 1
Maximum = 10
```

### Boundary Test Values

| Value | Expected Result |
|---|---|
| `0` | Invalid |
| `1` | Valid — Minimum boundary |
| `2` | Valid |
| `9` | Valid |
| `10` | Valid — Maximum boundary |
| `11` | Invalid |

### Test Cases

- [x] Verify quantity equal to `0`
- [x] Verify minimum quantity equal to `1`
- [x] Verify value above minimum (`2`)
- [x] Verify value below maximum (`9`)
- [x] Verify maximum quantity equal to `10`
- [x] Verify value above maximum (`11`)

---

# 3️⃣ Decision Table Testing

## 📌 Description

Decision Table Testing is used when the system behavior depends on multiple conditions.

This technique helps verify different combinations of conditions and expected actions.

---

## Example: Order Creation

### Conditions

- User is authenticated
- Shopping cart contains products
- Required checkout fields are completed

### Decision Table

| Rule | User Authenticated | Cart Has Products | Required Fields Valid | Order Created |
|---|---|---|---|---|
| 1 | Yes | Yes | Yes | Yes |
| 2 | No | Yes | Yes | No |
| 3 | Yes | No | Yes | No |
| 4 | Yes | Yes | No | No |
| 5 | No | No | No | No |

### Expected Behavior

An order should be created only when:

```text
User is authenticated
AND
Cart contains at least one product
AND
Required fields are valid
```

---

# 4️⃣ State Transition Testing

## 📌 Description

State Transition Testing verifies application behavior when an object changes from one state to another.

---

## Example: Order Status

### Possible States

```text
Created
   ↓
Processing
   ↓
Completed
```

Additional scenario:

```text
Created
   ↓
Cancelled
```

### State Transition Table

| Current State | Action | Next State |
|---|---|---|
| Created | Start processing | Processing |
| Processing | Complete order | Completed |
| Created | Cancel order | Cancelled |
| Processing | Cancel order | Cancelled |

### Test Scenarios

- [x] Verify order creation
- [x] Verify transition from `Created` to `Processing`
- [x] Verify transition from `Processing` to `Completed`
- [x] Verify order cancellation
- [x] Verify invalid state transitions are rejected

---

# 5️⃣ Error Guessing

## 📌 Description

Error Guessing is based on tester experience and knowledge of common application failures.

The tester predicts areas where defects are likely to occur.

---

## Possible Risk Areas

### 📝 Registration

- Empty fields
- Invalid email format
- Existing email
- Password mismatch
- Very long input values
- Special characters

### 🔐 Authentication

- Invalid password
- Empty credentials
- Expired session
- Invalid authentication token
- Direct access to protected pages

### 📚 Product Catalog

- Missing product information
- Broken product image
- Incorrect product price
- Duplicate products
- Empty catalog

### 🔎 Product Search

- Empty search request
- Long search query
- Special characters
- SQL injection-like input
- Non-existing product

### 🛒 Shopping Cart

- Negative quantity
- Zero quantity
- Quantity greater than allowed limit
- Duplicate products
- Incorrect total calculation
- Cart data loss after page refresh

### 💳 Checkout

- Empty required fields
- Invalid customer data
- Empty cart
- Double-click on order confirmation
- Incorrect total amount

---

# 📊 Test Design Coverage

| Technique | Application Area | Example |
|---|---|---|
| Equivalence Partitioning | Product Quantity | Valid and invalid ranges |
| Boundary Value Analysis | Product Quantity | `0`, `1`, `10`, `11` |
| Decision Table | Order Creation | Condition combinations |
| State Transition | Order Status | Created → Processing → Completed |
| Error Guessing | All Modules | Common risk scenarios |

---

# 🎯 Benefits of Using Test Design Techniques

Using structured test design techniques helps:

- Improve test coverage
- Reduce duplicate test cases
- Identify high-risk scenarios
- Test critical boundaries
- Validate complex business rules
- Create more effective test documentation
- Find defects that may be missed by standard testing

---

# 🔗 Related Documentation

- [📌 Project Overview](../project-overview/ProjectOverview.md)
- [🧠 Mind Map](../mind-maps/MindMap.md)
- [✅ Checklists](../../checklists/Checklists.md)
- [🧪 Test Cases](../test-cases/TestCases.md)
- [📋 Test Plan](../test-plan/TestPlan.md)
- [🎯 Test Strategy](../test-strategy/TestStrategy.md)

---

## 📌 Notes

> Test design techniques are used to improve the quality and coverage of testing by selecting effective test scenarios and test data.
