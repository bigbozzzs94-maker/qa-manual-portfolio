
# API Testing

## Project Information

| Field | Value |
|---|---|
| Project | BookCart |
| API Type | REST API |
| Tools | Postman, Swagger |
| Data Format | JSON |

---

## Testing Scope

The following API functionality is covered:

- Authentication
- User registration
- Product catalog
- Product search
- Shopping cart
- Checkout
- Order management

---

## HTTP Methods

| Method | Purpose |
|---|---|
| GET | Retrieve data |
| POST | Create new data |
| PUT | Update existing data |
| DELETE | Remove data |

---

## API Test Scenarios

### Authentication

- Register a new user with valid data
- Register with an existing email
- Register with invalid data
- Login with valid credentials
- Login with invalid credentials
- Verify authentication error messages

### Product Catalog

- Get the list of products
- Get product details
- Search for an existing product
- Search for a non-existing product
- Verify response data structure

### Shopping Cart

- Add a product to the cart
- Get cart contents
- Update product quantity
- Remove a product from the cart
- Verify cart data after each operation

### Checkout

- Create an order with valid data
- Try to create an order with invalid data
- Verify order response
- Verify validation error messages

---

## Response Validation

During API testing, the following checks are performed:

- HTTP status codes
- Response body
- Response headers
- JSON structure
- Required fields
- Data types
- Error messages
- Response time

---

## Status Codes

| Status Code | Description |
|---|---|
| 200 | OK |
| 201 | Created |
| 400 | Bad Request |
| 401 | Unauthorized |
| 404 | Not Found |
| 500 | Internal Server Error |

---

## Tools Used

### Postman

Used for:

- Sending HTTP requests
- Testing REST API endpoints
- Creating request collections
- Validating responses
- Testing positive and negative scenarios

### Swagger

Used for:

- Reviewing API documentation
- Exploring available endpoints
- Checking request parameters
- Checking request and response models
- Understanding API contracts

---

## Testing Types

- Functional Testing
- Positive Testing
- Negative Testing
- Integration Testing
- API Validation
