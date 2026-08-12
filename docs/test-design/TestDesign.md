# Test Design

## 1. Authentication

### Registration

Test scenarios:

- Register with valid data
- Register with empty required fields
- Register with invalid email format
- Register with an existing email
- Register with a password shorter than the minimum length
- Register with different values in Password and Confirm Password fields

### Login

Test scenarios:

- Login with valid credentials
- Login with invalid email
- Login with invalid password
- Login with empty fields
- Verify error messages
- Verify logout functionality

---

## 2. Product Catalog

Test scenarios:

- Open product catalog
- Verify product information
- Verify product image
- Verify product price
- Search for an existing product
- Search for a non-existing product
- Clear search results

---

## 3. Shopping Cart

Test scenarios:

- Add product to cart
- Add multiple products to cart
- Remove product from cart
- Change product quantity
- Verify total price
- Verify cart after page refresh

---

## 4. Checkout

Test scenarios:

- Checkout with valid data
- Checkout with empty required fields
- Verify validation messages
- Verify order creation
- Verify order information
- Verify order after page refresh

---

## 5. API Testing

Test scenarios:

- Verify successful GET request
- Verify successful POST request
- Verify successful PUT request
- Verify successful DELETE request
- Verify response status code
- Verify response body
- Verify error response
