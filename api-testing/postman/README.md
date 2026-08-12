# 📮 Postman Collections

> API testing collections and documentation for the **BookCart** project.

---

## 🎯 Purpose

This section contains Postman-related materials used for API testing.

Postman is used to:

- Send HTTP requests
- Validate API responses
- Test authentication
- Test request parameters
- Validate response data
- Test negative scenarios
- Create reusable collections
- Run API regression tests

---

## 📂 Collection Structure

The API collection should contain the following sections:

```text
BookCart API
│
├── 🔐 Authentication
│   ├── Register User
│   ├── Register Existing User
│   ├── Login
│   └── Login with Invalid Credentials
│
├── 📚 Products
│   ├── Get Product List
│   ├── Get Product Details
│   ├── Get Invalid Product
│   └── Search Products
│
├── 🛒 Shopping Cart
│   ├── Add Product
│   ├── Get Cart
│   ├── Update Quantity
│   └── Remove Product
│
└── 📦 Orders
    ├── Create Order
    ├── Get Order
    └── Validate Order Data
```

---

## ⚙️ Environment Variables

Recommended variables:

| Variable | Description |
|---|---|
| `baseUrl` | Base API URL |
| `token` | Authentication token |
| `userId` | Test user ID |
| `productId` | Test product ID |
| `orderId` | Created order ID |

Example:

```text
baseUrl = https://example.com/api
```

API request example:

```http
GET {{baseUrl}}/products
```

---

## 🔐 Authorization

Protected endpoints should use an authentication token.

Example:

```http
Authorization: Bearer {{token}}
```

After successful login, the token can be saved as an environment variable.

---

## 🧪 Response Validation

The following parameters should be validated:

- [x] HTTP status code
- [x] Response time
- [x] Response headers
- [x] Response body
- [x] JSON structure
- [x] Required fields
- [x] Data types
- [x] Error messages

---

## 📊 Example Postman Tests

### Status Code Validation

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

### Response Time Validation

```javascript
pm.test("Response time is less than 1000ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(1000);
});
```

### JSON Response Validation

```javascript
pm.test("Response contains expected data", function () {
    const jsonData = pm.response.json();

    pm.expect(jsonData).to.have.property("id");
});
```

---

## 🚨 Negative Testing

Negative scenarios include:

- Invalid request body
- Missing required fields
- Invalid email format
- Invalid password
- Invalid authentication token
- Missing authentication token
- Invalid resource ID
- Non-existing resource
- Invalid query parameters

---

## 📌 Expected HTTP Status Codes

| Status Code | Description |
|---|---|
| `200` | Successful request |
| `201` | Resource created |
| `400` | Invalid request |
| `401` | Unauthorized |
| `403` | Forbidden |
| `404` | Resource not found |
| `500` | Internal server error |

---

## 🔗 Related Documentation

- [← API Testing](../ApiTesting.md)
- [API Test Cases](../test-cases/APITestCases.md)
- [Test Strategy](../../docs/test-strategy/TestStrategy.md)
