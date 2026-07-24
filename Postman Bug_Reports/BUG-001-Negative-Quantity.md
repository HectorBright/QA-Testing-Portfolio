# BUG-001 – API Accepts Negative Quantity

## Bug ID
BUG-001

## Title
API accepts a negative quantity when adding a product to the cart.

## Module
Cart API

## Endpoint
POST /api/cart/add

## Severity
Medium

## Priority
High

## Environment
- API: OpenCart API
- Tool: Postman
- Test Runner: Newman CLI

## Authorization
API Token

## Request Data

| Parameter | Value |
|-----------|-------|
| product_id | 40 |
| quantity | -5 |

## Steps to Reproduce

1. Open Postman.
2. Select the POST request for the Add to Cart endpoint.
3. Add a valid API Token in the Authorization or required header.
4. Set product_id to 40.
5. Set quantity to -5.
6. Send the request.

## Expected Result

The API should reject the request because quantity cannot be negative. It should return an appropriate error message with a client error status code (such as HTTP 400).

## Actual Result

The API accepts the request and returns a successful response instead of rejecting the invalid quantity.

## Status

Open
