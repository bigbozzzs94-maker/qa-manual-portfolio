# 📮 BookCart API Collection

This document demonstrates a Postman collection structure and API testing scenarios created for the **BookCart E-commerce Web Application**.

The collection covers positive and negative scenarios for the main API functionality and demonstrates request validation, response validation, authentication testing, and basic Postman test scripts.

---

## 📋 Project Information

| Field | Value |
|---|---|
| Project | BookCart |
| Application Type | E-commerce Web Application |
| API Type | REST API |
| Tool | Postman |
| Data Format | JSON |
| Testing Type | Manual API Testing |
| Protocol | HTTP / HTTPS |

---

## 🎯 Collection Purpose

The purpose of this collection is to verify that API endpoints work correctly and return expected responses.

The following areas are covered:

- Authentication
- User registration
- User login
- Product catalog
- Product details
- Shopping cart
- Order-related functionality
- Request validation
- Response validation
- Positive scenarios
- Negative scenarios
- Error handling

---

# 🔧 Collection Configuration

## Base URL

The API base URL is stored as a collection or environment variable:

```text
{{baseUrl}}
```

Example:

```text
https://bookcart-api.example.com
```

Using variables allows the same collection to be executed against different environments without changing every request manually.

Possible environments:

- Development
- Test
- Staging
- Production

---

## 🔐 Authentication

For endpoints that require authorization, an authentication token can be stored in a variable:

```text
{{authToken}}
```

Example request header:

```http
Authorization: Bearer {{authToken}}
```

After successful authentication, the token can be saved automatically using a Postman test script.

```javascript
const response = pm.response.json();

if (response.token) {
    pm.environment.set("authToken", response.token);
}
```

This allows authorized requests to reuse the token automatically.

---

# 🔑 Authentication

## POST — Register User

**Endpoint:**

```http
POST {{baseUrl}}/api/auth/register
```

### Headers

```http
Content-Type: application/json
```

### Request Body

```json
{
    "email": "testuser@example.com",
    "password": "Password123"
}
```

### Expected Result

The system should:

- Create a new user account
- Return a successful response
- Return valid response data
- Not expose sensitive information

### Expected Status Code

```text
201 Created
```

### Postman Tests

```javascript
pm.test("Status code is 201", function () {
    pm.response.to.have.status(201);
});

pm.test("Response time is less than 1000ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(1000);
});

pm.test("Response is JSON", function () {
    pm.response.to.be.json;
});
```

---

## ❌ Register Existing User

**Endpoint:**

```http
POST {{baseUrl}}/api/auth/register
```

### Request Body

```json
{
    "email": "existinguser@example.com",
    "password": "Password123"
}
```

### Expected Result

The system should reject registration because the user already exists.

### Expected Status Code

```text
400 Bad Request
```

or

```text
409 Conflict
```

depending on the API specification.

### Validation

```javascript
pm.test("User registration is rejected", function () {
    pm.expect(pm.response.code).to.be.oneOf([400, 409]);
});
```

---

## POST — Login with Valid Credentials

**Endpoint:**

```http
POST {{baseUrl}}/api/auth/login
```

### Request Body

```json
{
    "email": "testuser@example.com",
    "password": "Password123"
}
```

### Expected Result

The system should:

- Authenticate the user successfully
- Return a valid authentication token
- Return the expected response structure

### Expected Status Code

```text
200 OK
```

### Postman Tests

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

const response = pm.response.json();

pm.test("Authentication token exists", function () {
    pm.expect(response.token).to.exist;
});

pm.environment.set("authToken", response.token);
```

---

## ❌ Login with Invalid Credentials

**Endpoint:**

```http
POST {{baseUrl}}/api/auth/login
```

### Request Body

```json
{
    "email": "testuser@example.com",
    "password": "WrongPassword"
}
```

### Expected Result

The system should reject authentication and return an appropriate error response.

### Expected Status Code

```text
401 Unauthorized
```

### Postman Tests

```javascript
pm.test("Status code is 401", function () {
    pm.response.to.have.status(401);
});
```

---

# 📚 Products

## GET — Get Product List

**Endpoint:**

```http
GET {{baseUrl}}/api/products
```

### Expected Result

The system should return a list of available products.

### Expected Status Code

```text
200 OK
```

### Postman Tests

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Response time is less than 1000ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(1000);
});

pm.test("Response body is not empty", function () {
    const response = pm.response.json();
    pm.expect(response).to.not.be.empty;
});
```

---

## GET — Get Product by ID

**Endpoint:**

```http
GET {{baseUrl}}/api/products/{{productId}}
```

Example:

```http
GET {{baseUrl}}/api/products/1
```

### Expected Result

The system should return information about the requested product.

### Expected Response

```json
{
    "id": 1,
    "title": "Book Title",
    "price": 19.99
}
```

### Postman Tests

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

const response = pm.response.json();

pm.test("Product ID exists", function () {
    pm.expect(response.id).to.exist;
});

pm.test("Product title exists", function () {
    pm.expect(response.title).to.exist;
});

pm.test("Product price exists", function () {
    pm.expect(response.price).to.exist;
});
```

---

## ❌ Get Product with Invalid ID

**Endpoint:**

```http
GET {{baseUrl}}/api/products/999999
```

### Expected Result

The system should return an error because the requested product does not exist.

### Expected Status Code

```text
404 Not Found
```

### Postman Test

```javascript
pm.test("Status code is 404", function () {
    pm.response.to.have.status(404);
});
```

---

# 🛒 Shopping Cart

## POST — Add Product to Cart

**Endpoint:**

```http
POST {{baseUrl}}/api/cart
```

### Authorization

```http
Authorization: Bearer {{authToken}}
```

### Request Body

```json
{
    "productId": 1,
    "quantity": 1
}
```

### Expected Result

The selected product should be added to the user's shopping cart.

### Expected Status Code

```text
200 OK
```

or

```text
201 Created
```

depending on the API specification.

---

## GET — Get Shopping Cart

**Endpoint:**

```http
GET {{baseUrl}}/api/cart
```

### Authorization

```http
Authorization: Bearer {{authToken}}
```

### Expected Result

The system should return the current user's shopping cart and the products added to it.

### Validation

```javascript
pm.test("Successful response", function () {
    pm.expect(pm.response.code).to.be.oneOf([200, 201]);
});
```

---

## PUT — Update Product Quantity

**Endpoint:**

```http
PUT {{baseUrl}}/api/cart/{{productId}}
```

### Request Body

```json
{
    "quantity": 2
}
```

### Expected Result

The quantity of the selected product should be updated successfully.

### Expected Status Code

```text
200 OK
```

---

## DELETE — Remove Product from Cart

**Endpoint:**

```http
DELETE {{baseUrl}}/api/cart/{{productId}}
```

### Expected Result

The selected product should be removed from the shopping cart.

### Expected Status Code

```text
200 OK
```

or

```text
204 No Content
```

---

# 📦 Orders

## POST — Create Order

**Endpoint:**

```http
POST {{baseUrl}}/api/orders
```

### Authorization

```http
Authorization: Bearer {{authToken}}
```

### Expected Result

The system should create an order using the products currently available in the user's shopping cart.

### Expected Status Code

```text
201 Created
```

### Validation

```javascript
pm.test("Order was created", function () {
    pm.response.to.have.status(201);
});

const response = pm.response.json();

pm.test("Order ID exists", function () {
    pm.expect(response.id).to.exist;
});
```

---

# ❌ Negative Testing

The collection also includes negative scenarios to verify API error handling.

Examples:

| Scenario | Expected Result |
|---|---|
| Invalid credentials | 401 Unauthorized |
| Missing required field | 400 Bad Request |
| Existing user registration | 400 / 409 |
| Invalid product ID | 404 Not Found |
| Unauthorized request | 401 Unauthorized |
| Invalid token | 401 / 403 |
| Invalid request body | 400 Bad Request |
| Missing authorization header | 401 Unauthorized |

Negative testing helps verify that the API handles incorrect requests safely and returns appropriate error responses.

---

# 🧪 Response Validation

The following checks can be performed in Postman:

### Status Code

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

### Response Time

```javascript
pm.test("Response time is less than 1000ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(1000);
});
```

### Content Type

```javascript
pm.test("Content-Type is JSON", function () {
    pm.expect(pm.response.headers.get("Content-Type"))
        .to.include("application/json");
});
```

### Required Field Exists

```javascript
const response = pm.response.json();

pm.test("Required field exists", function () {
    pm.expect(response.id).to.exist;
});
```

---

# 🔄 Collection Execution

The collection can be executed using:

- Postman Collection Runner
- Different environment variables
- Multiple requests in sequence
- Automated Postman test scripts

Example execution flow:

```text
Register User
      ↓
Login
      ↓
Save Authentication Token
      ↓
Get Products
      ↓
Get Product Details
      ↓
Add Product to Cart
      ↓
Get Shopping Cart
      ↓
Update Product Quantity
      ↓
Create Order
      ↓
Remove Product from Cart
```

---

# 📊 Testing Coverage

The Postman collection demonstrates testing of:

- REST API endpoints
- HTTP methods
- Request headers
- Query parameters
- Path parameters
- JSON request bodies
- JSON responses
- Authentication
- Authorization
- Status codes
- Positive scenarios
- Negative scenarios
- Response validation
- Error handling
- Basic Postman test scripts
- Environment and collection variables

---

# 💡 Key QA Skills Demonstrated

This collection demonstrates practical API testing skills including:

- API testing using Postman
- Understanding of REST API principles
- Working with GET, POST, PUT, and DELETE requests
- Working with HTTP status codes
- Request and response validation
- JSON validation
- Authentication testing
- Negative testing
- API error handling validation
- Using Postman variables
- Writing basic JavaScript tests in Postman
- Organizing API requests into reusable collections

---

## 📝 Conclusion

This Postman collection was created as part of the **BookCart QA Portfolio** to demonstrate API testing skills and understanding of REST API interactions.

The collection includes examples of authentication, product management, shopping cart functionality, order-related operations, positive and negative test scenarios, and automated response checks using Postman test scripts.
