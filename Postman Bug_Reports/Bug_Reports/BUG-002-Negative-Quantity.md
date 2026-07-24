# BUG-002 – API Accepts Request with Missing Quantity

## Bug ID
BUG-002

## Title
API accepts a request when the quantity parameter is omitted.

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
| quantity | Not Provided |

## Steps to Reproduce

1. Open Postman.
2. Select the POST request for the Add to Cart endpoint.
3. Add a valid API Token in the Authorization or required header.
4. Set product_id to 40.
5. Do not include the quantity parameter in the request body.
6. Send the request.

## Expected Result

The API should reject the request and indicate that the quantity field is required.

## Actual Result

The API processes the request successfully even though the quantity parameter is missing.

## Status

Open
