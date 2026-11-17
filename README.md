# Restful Booker – QA Testing Portfolio

## Project Overview

This project demonstrates my practical knowledge of manual API testing using Postman and JavaScript.

I tested the public [Restful Booker API](https://restful-booker.herokuapp.com/) by designing and documenting test cases, executing HTTP requests, and validating API responses with automated assertions.

The project was created as part of my preparation for a Junior QA Engineer role.

## Tools and Technologies

- **Postman** – API requests and automated response validation
- **JavaScript** – Postman test scripts and assertions
- **REST API** – HTTP methods and status codes
- **Google Sheets / CSV** – Manual test case documentation
- **GitHub** – Version control and portfolio documentation

## Test Coverage

The project contains **7 documented API test cases**, covering both positive and negative scenarios.

| Test Case | Scenario | Expected Result |
|---|---|---|
| TC-001 | API health check | HTTP 201 |
| TC-002 | Create a booking | HTTP 200 |
| TC-003 | Retrieve an existing booking | HTTP 200 |
| TC-004 | Update a booking with valid authentication | HTTP 200 |
| TC-005 | Retrieve a non-existent booking | HTTP 404 |
| TC-006 | Update a booking without authentication | HTTP 403 |
| TC-007 | Delete an existing booking | HTTP 201 |

## Automated API Testing

The Postman collection includes **17 automated JavaScript assertions** that validate:

- HTTP response status codes
- Response data types and required values
- Booking ID generation
- Updated booking information
- Unauthorized access responses
- Successful booking deletion

The project also uses Postman collection variables to save the booking ID generated during booking creation and reuse it in subsequent requests.

## Repository Structure

```text
restful-booker-qa-portfolio/
├── README.md
├── Restful_Booker_QA_Portfolio.postman_collection.json
└── test-cases/
    ├── README.md
    └── QA-Portfolio - Test Cases - Restful Booker API.csv
```

## How to Run the Tests

1. Import `Restful_Booker_QA_Portfolio.postman_collection.json` into Postman.
2. Set the collection variables `demoUsername` and `demoPassword` to the public Restful Booker demo credentials.
3. Run **POST – Create Booking** to generate and save a valid `bookingId`.
4. Execute the GET, PUT and negative test requests.
5. Run **DELETE – Delete Booking** last, because it removes the created booking.
6. Check the Postman test results to review the assertions.

The DELETE scenario also includes a manual verification step: requesting the deleted booking should return HTTP 404.

## What I Learned

Through this project, I practiced:

- Designing positive and negative API test scenarios
- Documenting expected and actual results
- Writing JavaScript assertions in Postman
- Working with JSON request and response bodies
- Managing authentication and dynamic test data
- Organizing and publishing QA documentation on GitHub

## Author

Domonkos Ottó Wangler

ISTQB Certified Tester – CTFL 4.0 (2026)

Aspiring Junior QA Engineer
