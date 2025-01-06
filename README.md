# REST API Testing
This project demonstrates a REST API testing setup using Postman. The focus is on utilizing the four main HTTP methods—`POST`, `GET`, `PUT`, and `DELETE` along with implementing validations for response codes, body structure, and headers.

## Project Overview

The **FakeRESTAPI** is a free API service that provides mock data for testing purposes. This project uses the service to:
- Create resources (`POST`).
- Retrieve resources (`GET`).
- Update existing resources (`PUT`).
- Delete resources (`DELETE`).

Each request method is validated to ensure the expected behavior of the API. 

## Features and Validations

### 1. **POST Request**
- **Purpose**: Creates a new resource 
- **Endpoint Example**: `https://fakerestapi.net/api/v1/Books`
- **Validations**:
  - Status code: `200 OK`.
  - Response body contains the newly created resource with a valid `id`.
  - Ensure required fields (`title`, `description`, etc.) are present and correct.

---

### 2. **GET Request**
- **Purpose**: Retrieves resources (all or by ID).
- **Endpoint Example**:
  - All resources: `https://fakerestapi.net/api/v1/Books`
  - By ID: `https://fakerestapi.net/api/v1/Books/{{bookID}}`
- **Validations**:
  - Status code: `200 OK`.
  - Check that the `title`, 'description' and other fields match the expected data.

---

### 3. **PUT Request**
- **Purpose**: Updates an existing resource.
- **Endpoint Example**: `https://fakerestapi.net/api/v1/Books/{{bookID}}`
- **Validations**:
  - Status code: `200 OK`.
  - Response body contains the updated resource.
  - Verify that the changes are reflected correctly.

---

### 4. **DELETE Request**
- **Purpose**: Deletes an existing resource.
- **Endpoint Example**: `https://fakerestapi.net/api/v1/Books/{{bookID}}`
- **Validations**:
  - Status code: `200 No Content`.
  - Verify that the resource is no longer accessible via a subsequent `GET` request.
