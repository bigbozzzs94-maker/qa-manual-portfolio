
API Test Cases
Project

BookCart — E-commerce Web Application

This document contains API test cases for the main BookCart application functionality.

1. Authentication API
API-TC-001 — Register a new user with valid data

Priority: High
Method: POST
Endpoint: /api/auth/register

Preconditions: User with the specified email does not exist.

Request Body:

{
  "name": "Test User",
  "email": "testuser@example.com",
  "password": "Test123!"
}

Steps:

Send a POST request to the registration endpoint.
Provide valid user data.
Check the response.

Expected Result:

Status code is 201 Created.
A new user is successfully created.
Response contains user information.
Password is not returned in the response.
API-TC-002 — Register with an existing email

Priority: High
Method: POST
Endpoint: /api/auth/register

Preconditions: A user with the specified email already exists.

Request Body:

{
  "name": "Test User",
  "email": "existing@example.com",
  "password": "Test123!"
}

Expected Result:

Status code is 400 Bad Request or 409 Conflict.
An error message is returned.
A duplicate user is not created.
API-TC-003 — Login with valid credentials

Priority: High
Method: POST
Endpoint: /api/auth/login

Preconditions: A registered user exists.

Request Body:

{
  "email": "testuser@example.com",
  "password": "Test123!"
}

Expected Result:

Status code is 200 OK.
Authentication is successful.
Response contains an authentication token or session data.
API-TC-004 — Login with invalid credentials

Priority: High
Method: POST
Endpoint: /api/auth/login

Request Body:

{
  "email": "testuser@example.com",
  "password": "WrongPassword"
}

Expected Result:

Status code is 401 Unauthorized.
An appropriate error message is returned.
Authentication token is not returned.
2. Product API
API-TC-005 — Get product list

Priority: High
Method: GET
Endpoint: /api/products

Steps:

Send a GET request to the products endpoint.
Check the response.

Expected Result:

Status code is 200 OK.
Response contains a list of products.
Each product contains valid required fields.
API-TC-006 — Get product by valid ID

Priority: High
Method: GET
Endpoint: /api/products/{id}

Preconditions: A product with the specified ID exists.

Expected Result:

Status code is 200 OK.
Response contains the requested product.
Product ID matches the requested ID.
API-TC-007 — Get product by invalid ID

Priority: Medium
Method: GET
Endpoint: /api/products/{invalid_id}

Expected Result:

Status code is 404 Not Found.
An appropriate error message is returned.
3. Cart API
API-TC-008 — Add product to cart

Priority: High
Method: POST
Endpoint: /api/cart

Preconditions: User is authenticated.

Request Body:

{
  "productId": 1,
  "quantity": 1
}

Expected Result:

Status code is 200 OK or 201 Created.
Product is successfully added to the cart.
Cart contains the selected product.
API-TC-009 — Update product quantity in cart

Priority: High
Method: PUT
Endpoint: /api/cart/{productId}

Preconditions: Product is already added to the cart.

Request Body:

{
  "quantity": 2
}

Expected Result:

Status code is 200 OK.
Product quantity is successfully updated.
Response contains the updated quantity.
API-TC-010 — Remove product from cart

Priority: High
Method: DELETE
Endpoint: /api/cart/{productId}

Preconditions: Product is already added to the cart.

Expected Result:

Status code is 200 OK or 204 No Content.
Product is removed from the cart.
4. Order API
API-TC-011 — Create order with valid data

Priority: High
Method: POST
Endpoint: /api/orders

Preconditions:

User is authenticated.
Cart contains at least one product.

Expected Result:

Status code is 201 Created.
Order is successfully created.
Response contains an order ID.
Order contains correct product information.
API-TC-012 — Create order with an empty cart

Priority: High
Method: POST
Endpoint: /api/orders

Preconditions:

User is authenticated.
Cart is empty.

Expected Result:

Status code is 400 Bad Request.
An appropriate validation error is returned.
Order is not created.
API Validation Checklist

During API testing, the following checks are performed:

Status code validation.
Response body validation.
Response schema validation.
Required fields validation.
Data type validation.
Error message validation.
Authentication and authorization checks.
Positive testing.
Negative testing.
Boundary value testing.
Invalid request data validation.
Response time checks.
HTTP Methods Covered
Method	Purpose
GET	Retrieve data
POST	Create new data
PUT	Update existing data
DELETE	Remove data
