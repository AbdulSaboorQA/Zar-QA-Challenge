# Zar-QA-Challenge-AbdulSaboor

This repository contains automated tests for the ReqRes APIs. The tests are written using **Postman**.

## Table of Contents
1. [Overview](#overview)
2. [Prerequisites](#prerequisites)
3. [Setting Up and Running the Tests](#setting-up-the-tests)
4. [Test Details](#test-details)
6. [Test run Report](#test-run-report)

---

### Overview

This repository includes automated **API tests** using **Postman**. The tests cover 5 API endpoints as required to validate the end to end test flows, regression testing including functionality, data integrity, edge cases and error handling as well.

The tests are written in **Postman Collections** format, and can be imported into the Postman app for execution.

---

### Prerequisites

Before running the tests, you need to have the following installed and set up on your system:

1. **Postman**: A popular API testing tool for sending requests and validating responses.
    - You can download it from [here](https://www.postman.com/downloads/).
  
2. **Postman Collection Runner**: This is included by default with Postman. You'll be using the **Collection Runner** to run all tests in the collection.

3. **API Endpoint(s)**: The API endpoints being tested should be up and running for the tests to execute properly.

---

### Setting Up the Tests

To get started with the test automation, follow these steps:

#### 1. **Clone the Repository**

Clone this repository to your local machine using the following command:

git clone https://github.com/your-username/repository-name.git
Replace your-username with your GitHub username and repository-name with the name of your repository.

#### 2. **Install Postman**
-------------------

If you don't have Postman installed, download it from the Postman Download page. Follow the installation instructions for your operating system.

#### 3. **Import the Postman Collection**
---------------------------------

1.  Open Postman.

2.  Click the **Import** button located in the top-left corner.

3.  Select the **File** tab and choose the API_Test_Collection.json file from this repository.

4.  Once the file is uploaded, you will see the collection appear under the **Collections** tab in Postman.

#### 4. **Run the Tests Manually in Postman**
-------------------------------------

1.  In Postman, open the **Collections** tab and select the imported collection.

2.  To run all tests in the collection, click the **Run** button in the top-right corner of the Postman window.

3.  Postman will execute the tests and display the results.

### Test Details

This **ReqRes API Test Suite** is designed to validate and verify the functionality of the ReqRes API endpoints. The suite covers various API functionalities, organized into the following modules:

#### 1. **Authentication**

Tests to validate login functionality and error handling for different scenarios:

-   **API Endpoint:** `POST /login`
-   **Test Scenarios:**
    -   Valid Credentials
    -   Missing Password
    -   Invalid Email Format
    -   Null Email
    -   Very Long Email
    -   Short Email
    -   Empty Body
    -   Null Password
    -   Empty Password
    -   Long Password

#### 2. **User Retrieval**

Tests to validate user data retrieval and pagination functionality:

-   **API Endpoint:** `GET /users?page=2`
-   **Test Scenarios:**
    -   Valid User
    -   Invalid Page Number
    -   Missing Page Parameter
    -   Invalid Page Parameter
    -   Boundary Testing:
        -   First Page
        -   Last Page

#### 3. **User Creation**

Tests to validate user creation functionality with various input scenarios:

-   **API Endpoint:** `POST /users`
-   **Test Scenarios:**
    -   Valid User Creation
    -   Missing Name
    -   Missing Job
    -   Invalid Name and Job
    -   Very Long Name
    -   Empty Name or Job
    -   Very Long Job

#### 4. **User Update**

Tests to validate the update functionality of user details:

-   **API Endpoint:** `PUT /users/2`
-   **Test Scenarios:**
    -   Successful Update
    -   Missing Name
    -   Missing Job
    -   Invalid User
    -   Empty Name and Job
    -   Very Long Name and Job

#### 5. **User Deletion**

Tests to validate user deletion functionality, including edge cases:

-   **API Endpoint:** `DELETE /users/2`
-   **Test Scenarios:**
    -   Successful Deletion
    -   Invalid User Deletion
    -   Invalid User Format Deletion
    -   Boundary Testing:
        -   First User Deletion
        -   Very Large User ID Deletion
        -   First Valid User ID Deletion
     
There are a total of 65 test cases against these 5 endpoints and all of them ran successfully

### Test Run Report

Here is the visual representation of the latest test run results:

![Test Run Report](./Test%20Run%20Report.png)
