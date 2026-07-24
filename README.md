# QA-Testing-Portfolio

# OpenCart Testing Portfolio

## Project

This repository contains my QA testing project using OpenCart.

## Testing Performed

- Manual Testing
- API Testing (Postman)

  

## Manual Testing
[Live Google Sheet for the Opencart Test Cases (https://docs.google.com/spreadsheets/d/1a-9IuxYtpw86dFyPtvLFpmOqhYLkCO1zjFxGiEGAcKY/edit?usp=sharing)]
The Google sheet Preserves the original formatting.

Completed modules include:

- Login
- Registration
- Header Menu
- Downloads
- Reward Points
- Contact Us
- Checkout
- Order History
- Order Information
- Address Book
- Product Page
- Logout
- Homepage
- Forgot Password
- Products Display
- Register Functionality
- Add to Cart
- My Acount Information
- My Account
- Search Functionality

## Tools

- Excel
- OpenCart
- Git
- GitHub
- Playwright


# OpenCart Cart API Testing using Postman

## Overview
API test suite for OpenCart's cart functionality, covering positive 
and negative test scenarios using Postman and Newman.

## Test Coverage
- 10 requests, 31 assertions
- Positive flows: add to cart, session creation, cart content
- Negative testing: invalid quantity, missing fields, invalid product IDs

## Key Findings
🐛 Bug: Negative quantity accepted — POST /api/cart/add returns 
success even when quantity is -5, instead of rejecting the request.

🐛 Bug: Missing quantity accepted — Same endpoint accepts requests 
with no quantity specified, returning success instead of a validation error.

## Bug Reports

| Bug ID | Description | Severity | Status |
|--------|-------------|----------|--------|
| BUG-001 | API accepts negative quantity when adding a product to the cart | Medium | Open |
| BUG-002 | API accepts request with missing quantity parameter | Medium | Open |

See the Bug_Reports folder for detailed bug reports.

⚠️ Performance note: Cart Content endpoint responded in 601ms, 
slightly above the 500ms target threshold.

## Tools Used
Postman, Newman (CLI test runner), JavaScript (test scripts)

## How to Run
\`\`\`
newman run postman/Opencart_RestAPI_CartModule.postman_collection.json \
  -e postman/QA.postman_environment.json
\`\`\`
