# REST API Testing with Postman

[![API Tests](https://github.com/VishmiSiriwardhana/REST-API-Testing/actions/workflows/api-tests.yml/badge.svg)](https://github.com/VishmiSiriwardhana/REST-API-Testing/actions/workflows/api-tests.yml)

## 📌 Project Overview

This project demonstrates **REST API functional testing using Postman** against the [Fake REST API](https://fakerestapi.azurewebsites.net/).

The project focuses on validating **CRUD operations**, positive and negative scenarios, request and response validation, dynamic test data generation, automated collection execution using **Newman**, and **CI/CD integration** for automated API test execution.

The goal of this project is to demonstrate practical API testing and automation skills as part of a **QA Engineer portfolio**.

---

## 🌐 API Under Test

**Base URL:**

```text
https://fakerestapi.azurewebsites.net/api/v1

```

The project uses the **Books API** from the Fake REST API.

---

## 🔄 HTTP Methods Covered


| Method | Purpose            |
| ------ | ------------------ |
| POST   | Create a Book      |
| GET    | Retrieve a Book    |
| GET    | Retrieve All Books |
| PUT    | Update a Book      |
| DELETE | Delete a Book      |


---

## 🛠️ Tools & Technologies

- **Postman** – API testing and collection execution
- **JavaScript** – Postman test scripts and dynamic test data
- **Newman** – Command-line Postman collection execution
- **Git** – Version control
- **GitHub** – Source code and documentation
- **GitHub Actions** – CI/CD automation
- **REST API** – API under test

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

## 🔢 Test Data Management

Dynamic test data is generated using a **Postman pre-request script**.

A unique Book ID is generated automatically before creating a new book and stored as a collection variable.

```javascript
const uniqueId = Math.floor(Math.random() * 900000) + 100000;

pm.collectionVariables.set("generatedId", uniqueId);

console.log("Generated Book ID:", uniqueId);

```

The generated ID is then reused by subsequent requests to support dynamic test execution.

---

## 🔍 API Response Validation

The Postman test scripts validate:

- HTTP status codes
- Response time
- Response content type
- Response body
- Book ID
- Book title
- Book description
- Page count
- Excerpt
- Publish date
- Expected error responses

These validations help ensure that the API behaves as expected for both successful and unsuccessful requests.

---

## 🌍 Environment & Variables

The Postman environment contains the base URL used by the API requests.

```text
Base_URL = https://fakerestapi.azurewebsites.net/api/v1

```

The collection also uses variables such as:

```text
generatedId

```

to dynamically share test data between requests.

---

## 🤖 Automated Test Execution with Newman

The Postman collection has been executed using **Newman** for command-line API test automation.

Newman allows Postman collections to be executed without opening the Postman application and makes the API tests suitable for automated environments and CI/CD pipelines.

### Newman Execution

```bash
newman run "FakeRestAPI Books.postman_collection.json" -e "FakeRestAPI.postman_environment.json"

```

The collection was successfully executed using Newman after resolving dynamic test-data and response-validation issues.

---

## 🚀 CI/CD Integration

The API tests have been integrated into a **GitHub Actions CI/CD pipeline**.

The pipeline automatically executes the Postman API collection using Newman and helps identify test failures during the development process.

### CI/CD Workflow

The automated workflow performs the following steps:

1. Checks out the repository
2. Sets up the required Node.js environment
3. Installs Newman
4. Executes the Postman collection
5. Uses the Postman environment
6. Reports the test execution result

The workflow status can be viewed using the badge at the top of this README.

**[View GitHub Actions →](https://github.com/VishmiSiriwardhana/REST-API-Testing/actions)**

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

### 1. Clone the Repository

```bash
git clone https://github.com/VishmiSiriwardhana/REST-API-Testing.git

```

Navigate to the project directory:

```bash
cd REST-API-Testing

```

### 2. Open Postman

Launch Postman on your computer.

### 3. Import the Collection

Import the following collection into Postman:

```text
FakeRestAPI Books.postman_collection.json

```

### 4. Import the Environment

Import:

```text
FakeRestAPI.postman_environment.json

```

Select the imported **FakeRestAPI** environment in Postman.

### 5. Run the Collection

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

📄 `TEST_EXECUTION_REPORT.md`

---

## 🎯 Testing Approach

The project follows a practical API testing approach covering:

1. **Positive Testing** – Verify valid API operations.
2. **Negative Testing** – Verify API behavior for non-existing resources.
3. **Functional Testing** – Validate API functionality and expected behavior.
4. **Response Validation** – Validate status codes, response data, headers, and content type.
5. **CRUD Testing** – Validate Create, Read, Update, and Delete operations.
6. **Dynamic Test Data** – Generate and reuse test data through Postman scripts and variables.
7. **Automated Execution** – Execute the Postman collection using Newman.
8. **Continuous Testing** – Run API tests automatically through GitHub Actions.

---

## ⚠️ Challenges & Resolutions

### 1. Dynamic Book ID Handling

Some requests initially failed because the Book ID used for retrieval did not match the ID generated during book creation.

**Resolution:**  
Implemented dynamic ID generation using Postman pre-request scripts and collection variables.

### 2. Response Time Validation

Some API requests initially exceeded the response-time threshold.

**Resolution:**  
Reviewed the response-time validation and adjusted the test validation approach based on the API's actual response behavior.

### 3. Negative Test Scenarios

Negative scenarios required different expected status codes and response validations compared with successful requests.

**Resolution:**  
Created separate assertions for non-existing resources and validated the expected error responses.

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

---

## 💡 Key Skills Demonstrated

This project demonstrates practical experience in:

- REST API testing
- Postman
- JavaScript test scripting
- Pre-request scripting
- Dynamic test data generation
- Positive and negative testing
- CRUD testing
- Response validation
- Status code validation
- Environment and collection variables
- Newman automation
- CI/CD integration
- Git and GitHub
- GitHub Actions
- Test documentation
- Defect analysis and troubleshooting

---

## 👩‍💻 Author

**Vishmi Siriwardhana**  
Software Quality Assurance Engineer

This project is part of my QA testing portfolio and demonstrates practical experience in **REST API testing, Postman test automation, functional testing, positive and negative testing, response validation, Newman automation, CI/CD integration, and Git/GitHub-based project management**.
