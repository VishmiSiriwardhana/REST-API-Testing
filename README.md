# REST API Testing

## 📌 Project Overview

This project demonstrates **REST API functional testing using Postman** against the [Fake REST API](https://fakerestapi.net/).

The project focuses on validating CRUD operations using the HTTP methods:

- **POST** – Create a Book
- **GET** – Retrieve a Book / Retrieve all Books
- **PUT** – Update a Book
- **DELETE** – Delete a Book

Both **positive and negative test scenarios** are included to verify expected API behavior.

---

## 🛠️ Tools & Technologies

- **Postman** – API testing and collection execution
- **REST API** – API under test
- **JavaScript** – Postman test scripts
- **Git** – Version control
- **GitHub** – Source code and test documentation

---

## 🧪 Test Scenarios

The Postman collection currently covers the following scenarios:


| ID  | Test Scenario              | Type     |
| --- | -------------------------- | -------- |
| 01  | Create Book                | Positive |
| 02  | Retrieve Book              | Positive |
| 03  | Get All Books              | Positive |
| 04  | Update Book                | Positive |
| 05  | Delete Book                | Positive |
| 06  | Retrieve Non-Existing Book | Negative |
| 07  | Update Non-Existing Book   | Negative |
| 08  | Delete Non-Existing Book   | Negative |


---

## 🔍 API Testing Coverage

The project includes validation of:

- HTTP status codes
- Response body
- Response data
- Required fields
- Book ID
- CRUD operations
- Positive scenarios
- Negative scenarios
- API behavior for non-existing resources
- Response headers

---

## 📊 Test Execution Results

The complete Postman collection was executed successfully.


| Result      | Count    |
| ----------- | -------- |
| Total Tests | **30**   |
| Passed      | **30**   |
| Failed      | **0**    |
| Skipped     | **0**    |
| Errors      | **0**    |
| Pass Rate   | **100%** |


### Execution Status

**✅ PASSED – 100%**

Detailed execution results are available in the [Test Execution Report](https://chatgpt.com/c/documentation/TEST_EXECUTION_REPORT.md).

---

## 📁 Project Structure

```text
REST-API-TESTING/
│
├── README.md
│
├── FakeRestAPI Books.postman_collection.json
│
└── documentation/
    └── TEST_EXECUTION_REPORT.md

```

---

## ▶️ How to Run the Tests

### 1. Clone the repository

```bash
git clone https://github.com/VishmiSiriwardhana/REST-API-Testing.git

```

### 2. Open Postman

Launch Postman on your computer.

### 3. Import the collection

Import:

```text
FakeRestAPI Books.postman_collection.json

```

into Postman.

### 4. Run the collection

Open the imported collection and select **Run Collection**.

Execute the complete collection and review the test results in the Postman Collection Runner.

---

## 📄 Documentation

### Test Execution Report

The test execution report contains:

- Test execution summary
- Test scenarios
- Execution results
- Test coverage
- Defect status
- Overall test execution conclusion

[View Test Execution Report](https://chatgpt.com/c/documentation/TEST_EXECUTION_REPORT.md)

---

## 🎯 Testing Approach

The project follows a practical API testing approach covering:

1. **Positive Testing** – Verify valid API operations.
2. **Negative Testing** – Verify API behavior with non-existing resources.
3. **Functional Validation** – Validate API functionality and expected responses.
4. **Response Validation** – Validate status codes and response data.
5. **CRUD Testing** – Validate Create, Read, Update and Delete operations.

---

## 🚀 Future Improvements

The project can be extended with additional scenarios such as:

- Invalid request body validation
- Missing required fields
- Invalid data types
- Invalid Book ID formats
- Response time validation
- Schema validation
- Additional boundary-value scenarios
- Environment variables for different environments
- Automated collection execution using Newman

---

## 👩‍💻 Author

**Vishmi Siriwardhana**

Software Quality Assurance Engineer

---

This project is part of my QA testing portfolio and demonstrates practical REST API testing using Postman.

