
# 🔗 API Testing

This document describes API testing performed for the **BookCart E-commerce Web Application**.

The purpose of API testing is to verify that backend endpoints work correctly, return expected responses, process data properly, and handle invalid requests appropriately.

---

## 📋 Project Information

| Field | Value |
|---|---|
| **Project** | BookCart |
| **Application Type** | E-commerce Web Application |
| **API Type** | REST API |
| **Tools** | Postman, Swagger |
| **Data Format** | JSON |
| **Testing Type** | Manual API Testing |

---

## 🎯 Testing Scope

The following API functionality is covered:

- Authentication
- User registration
- Product catalog
- Product search
- Shopping cart
- Checkout
- Order management

The main focus of testing is validating API requests and responses, business logic, error handling, and data consistency.

---

## 🌐 HTTP Methods

| Method | Purpose | Example |
|---|---|---|
| **GET** | Retrieve data | Get product list |
| **POST** | Create new data | Create user or order |
| **PUT** | Update existing data | Update user information |
| **PATCH** | Partially update data | Update selected fields |
| **DELETE** | Remove data | Delete an item from the cart |

---

## 🔍 What Was Tested

During API testing, the following checks were performed:

### Request Validation

- Correct HTTP method is used
- Endpoint URL is valid
- Required request parameters are provided
- Request headers are correct
- Request body contains valid data
- Data types match API requirements

### Response Validation

- HTTP status code is correct
- Response body contains expected data
- JSON structure matches expectations
- Required fields are present
- Field values are correct
- Error messages are meaningful

### Authentication and Authorization

- Valid credentials allow successful authentication
- Invalid credentials are rejected
- Unauthorized requests are handled correctly
- Protected endpoints require authentication
- Authentication errors return appropriate status codes

### Negative Testing

Negative scenarios were also tested to verify system behavior when invalid data is provided:

- Invalid email format
- Incorrect password
- Empty required fields
- Missing request parameters
- Invalid data types
- Invalid resource ID
- Unauthorized requests
- Requests for non-existing resources

---

## 📊 HTTP Status Codes Validation

The following status codes were checked during testing:

| Status Code | Meaning | Expected Usage |
|---|---|---|
| **200 OK** | Successful request | Data retrieved successfully |
| **201 Created** | Resource created | User, order, or other resource created |
| **400 Bad Request** | Invalid request | Incorrect or missing data |
| **401 Unauthorized** | Authentication required | Invalid or missing authentication |
| **403 Forbidden** | Access denied | User has no permission |
| **404 Not Found** | Resource not found | Invalid endpoint or resource ID |
| **409 Conflict** | Data conflict | Duplicate or conflicting data |
| **500 Internal Server Error** | Server error | Unexpected backend failure |

---

# 🔐 Authentication Testing

Authentication API functionality was tested using valid and invalid user credentials.

### Positive Scenario

**Request:**

```http
POST /api/login
