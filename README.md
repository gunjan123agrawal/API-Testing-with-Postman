API Testing with Postman
Project Overview

This project demonstrates API testing and automation using Postman. It includes API request creation, response validation, dynamic data handling, and data-driven testing using CSV files.

The objective of this project is to validate REST APIs by implementing automated test scripts and reusable test workflows using Postman and JavaScript.

Features
API testing for REST services
CRUD operation validation
Automated response verification
Dynamic data extraction and reuse
Environment and collection variable management
Data-driven testing using CSV files
Version control using GitHub
Technologies Used
Postman
JavaScript
REST APIs
JSON
CSV
GitHub
Postman Scripting Implemented
Response Validation
Status code validation
Response body validation
Header validation
Response time validation
JSON response verification
Dynamic Variable Handling
pm.environment.set()
pm.collectionVariables.set()
pm.response.json()
Assertions Used
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
pm.test("Response time is less than 1000ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(1000);
});
Data-Driven Testing

This project uses CSV files to execute API requests with multiple datasets and validate application behavior against different test scenarios.

Example use cases:

Multiple user records
Different input combinations
Positive and negative test scenarios
Boundary value testing
Sample Dynamic Data Extraction
const jsonData = pm.response.json();
const book_id = jsonData.ID;

pm.environment.set("book_id", book_id);
pm.collectionVariables.set("flag", true);
Repository Structure
API-Testing-with-Postman/
│
├── Library.postman_collection.json
├── TestData.csv
├── README.md
└── Environment.json
Skills Demonstrated
API Testing
Postman Automation
JavaScript Scripting
Data-Driven Testing
REST API Validation
JSON Parsing
Dynamic Variable Handling
GitHub Version Control
Author

Gunjan Agrawal

QA Engineer | API Testing | Postman | Manual Testing | Learning Automation Testing
