# REST API Testing with Postman

[![API Tests]([https://github.com/VishmiSiriwardhana/REST-API-Testing/actions/workflows/api-tests.yml/badge.svg)](https://github.com/VishmiSiriwardhana/REST-API-Testing/actions/workflows/api-tests.yml)](https://github.com/VishmiSiriwardhana/REST-API-Testing/actions/workflows/api-tests.yml/badge.svg)](https://github.com/VishmiSiriwardhana/REST-API-Testing/actions/workflows/api-tests.yml))

## 📌 Project Overview

This project demonstrates **REST API functional testing using Postman** against the [Fake REST API](https://fakerestapi.azurewebsites.net/).

The project focuses on validating **CRUD operations**, positive and negative scenarios, response validation, and API behavior for existing and non-existing resources.

### HTTP Methods Covered

- **POST** – Create a Book
- **GET** – Retrieve a Book / Retrieve All Books
- **PUT** – Update a Book
- **DELETE** – Delete a Book

---



## 🛠️ Tools & Technologies

- **Postman** – API testing and collection execution
- **JavaScript** – Postman test scripts and dynamic test data
- **REST API** – API under test
- **Git** – Version control
- **GitHub** – Source code and documentation

---



## 🧪 Test Scenarios

The Postman collection covers the following scenarios:


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
- Non-existing resource behavior
- Response headers
- Content type
- Response time
- Dynamic test data

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

Detailed execution results are available in the `documentation/TEST_EXECUTION_REPORT.md` file.

---



## 📁 Project Structure

```text
REST-API-TESTING/
│
├── README.md
│
├── FakeRestAPI Books.postman_collection.json
│
├── FakeRestAPI.postman_environment.json
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

Import the following file into Postman:

```text
FakeRestAPI Books.postman_collection.json

```



### 4. Import the environment

Import:

```text
FakeRestAPI.postman_environment.json

```

Select the imported **FakeRestAPI** environment in Postman.

### 5. Run the collection

Open the imported collection and select **Run Collection**.

Execute the complete collection using the Postman Collection Runner and review the test results.

---



## 📄 Documentation



### Test Execution Report

The test execution report contains:

- Test execution summary
- Test scenarios
- Test coverage
- Execution results
- Defect status
- Overall test execution conclusion

📄 documentation/TEST_EXECUTION_[REPORT.md](http://REPORT.md)

## 🎯 Testing Approach

The project follows a practical API testing approach covering:

1. **Positive Testing** – Verify valid API operations.
2. **Negative Testing** – Verify API behavior for non-existing resources.
3. **Functional Testing** – Validate API functionality and expected behavior.
4. **Response Validation** – Validate status codes, response data, headers, and content type.
5. **CRUD Testing** – Validate Create, Read, Update, and Delete operations.
6. **Dynamic Test Data** – Generate and reuse test data through Postman scripts and variables.

---



## 🚀 Future Improvements

Potential future enhancements include:

- JSON schema validation
- Invalid request body validation
- Missing required field scenarios
- Invalid data type scenarios
- Invalid Book ID format scenarios
- Boundary-value testing
- Additional negative scenarios
- Automated collection execution using **Newman**
- CI/CD integration for automated API test execution

---



## 👩‍💻 Author

**Vishmi Siriwardhana**  
Software Quality Assurance Engineer

This project is part of my QA testing portfolio and demonstrates practical experience in **REST API testing, Postman test automation, functional testing, positive and negative testing, response validation, and Git/GitHub-based project management**.