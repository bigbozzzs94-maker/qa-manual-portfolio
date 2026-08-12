# 🧪 API Test Cases

> Detailed API test cases for the **BookCart E-commerce Web Application**.

---

## 📋 Test Case Information

| Parameter | Description |
|---|---|
| **Project** | BookCart |
| **Testing Type** | API Testing |
| **Tool** | Postman |
| **API Format** | JSON |
| **Protocol** | HTTP / HTTPS |

---

# 🔐 Authentication

---

## TC-API-001 — Register User with Valid Data

**Priority:** High

### Preconditions

- Registration endpoint is available.

### Request

```http
POST /api/auth/register
```

### Request Body

```json
{
  "email": "testuser@example.com",
  "password": "Password123"
}
```

### Steps

1. Open Postman.
2. Select the `POST` method.
3. Enter the registration endpoint.
4. Add valid user data.
5. Send the request.

### Expected Result

- Response status code is `201 Created`.
- User is successfully registered.
- Response contains user information or a success message.

---

## TC-API-002 — Register User with Existing Email

**Priority:** High

### Preconditions

- User with the specified email already exists.

### Steps

1. Send a registration request.
2. Use an existing email.
3. Send the request.

### Expected Result

- Response status code is `400 Bad Request` or another expected validation status.
- User is not created.
- An appropriate error message is returned.

---

## TC-API-003 — Register User with Invalid Email

**Priority:** Medium

### Test Data

```json
{
  "email": "invalid-email",
  "password": "Password123"
}
```

### Expected Result

- Request is rejected.
- Validation error is returned.
- Invalid user is not created.

---

# 🔑 Login

---

## TC-API-004 — Login with Valid Credentials

**Priority:** Critical

### Request

```http
POST /api/auth/login
```

### Request Body

```json
{
  "email": "testuser@example.com",
  "password": "Password123"
}
```

### Expected Result

- Response status code is `200 OK`.
- User is successfully authenticated.
- Authentication token is returned.

---

## TC-API-005 — Login with Invalid Password

**Priority:** High

### Expected Result

- Authentication fails.
- Response status code is `401 Unauthorized` or expected validation status.
- Error message is returned.
- Authentication token is not generated.

---

# 📚 Products

---

## TC-API-006 — Get Product List

**Priority:** High

### Request

```http
GET /api/products
```

### Expected Result

- Response status code is `200 OK`.
- Response body contains a product list.
- Product objects contain expected fields.

Example:

```json
{
  "id": 1,
  "title": "Book Name",
  "price": 19.99
}
```

---

## TC-API-007 — Get Product Details

**Priority:** High

### Request

```http
GET /api/products/{id}
```

### Steps

1. Send a request with a valid product ID.
2. Validate the response.

### Expected Result

- Response status code is `200 OK`.
- Correct product information is returned.
- Product ID matches the requested ID.

---

## TC-API-008 — Get Product with Invalid ID

**Priority:** Medium

### Request

```http
GET /api/products/999999
```

### Expected Result

- Response status code is `404 Not Found`.
- Appropriate error response is returned.

---

# 🛒 Shopping Cart

---

## TC-API-009 — Add Product to Cart

**Priority:** Critical

### Preconditions

- User is authenticated.
- Valid authentication token is available.

### Expected Result

- Product is successfully added to the cart.
- Response contains updated cart information.
- Correct status code is returned.

---

## TC-API-010 — Get Shopping Cart

**Priority:** High

### Expected Result

- Response status code is `200 OK`.
- Cart contains correct products.
- Product quantities are correct.
- Total amount is calculated correctly.

---

## TC-API-011 — Remove Product from Cart

**Priority:** High

### Expected Result

- Product is removed successfully.
- Updated cart data is returned.
- Removed product is no longer present in the cart.

---

# 📦 Orders

---

## TC-API-012 — Create Order

**Priority:** Critical

### Preconditions

- User is authenticated.
- Shopping cart contains at least one product.

### Expected Result

- Order is successfully created.
- Response status code is `201 Created`.
- Response contains order information.
- Order ID is generated.

---

## TC-API-013 — Create Order with Empty Cart

**Priority:** High

### Preconditions

- Shopping cart is empty.

### Expected Result

- Order creation is rejected.
- Appropriate validation error is returned.
- Order is not created.

---

# 🔒 Authorization

---

## TC-API-014 — Access Protected Endpoint Without Token

**Priority:** Critical

### Steps

1. Select a protected API endpoint.
2. Remove the authorization token.
3. Send the request.

### Expected Result

- Response status code is `401 Unauthorized`.
- Protected data is not returned.

---

## TC-API-015 — Access Protected Endpoint with Invalid Token

**Priority:** High

### Expected Result

- Request is rejected.
- Response status code is `401 Unauthorized`.
- Access to protected resources is denied.

---

# 📊 Test Case Summary

| ID | Area | Priority |
|---|---|---|
| TC-API-001 | Registration | High |
| TC-API-002 | Registration | High |
| TC-API-003 | Registration Validation | Medium |
| TC-API-004 | Login | Critical |
| TC-API-005 | Login Validation | High |
| TC-API-006 | Products | High |
| TC-API-007 | Product Details | High |
| TC-API-008 | Product Validation | Medium |
| TC-API-009 | Shopping Cart | Critical |
| TC-API-010 | Shopping Cart | High |
| TC-API-011 | Shopping Cart | High |
| TC-API-012 | Orders | Critical |
| TC-API-013 | Order Validation | High |
| TC-API-014 | Authorization | Critical |
| TC-API-015 | Authorization | High |

---

## 🔗 Related Documentation

- [← API Testing](../ApiTesting.md)
- [Postman Documentation](../postman/README.md)
- [Main Test Cases](../../docs/test-cases/TestCases.md)
- [Bug Reports](../../test-artifacts/BugReports.md)
