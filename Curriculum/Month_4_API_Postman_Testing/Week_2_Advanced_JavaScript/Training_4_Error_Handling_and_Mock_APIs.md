# **Month 4: Training 4 - Handling Edge Cases, Error Responses, and Mock APIs**

### **Objective**

This training session focuses on testing edge cases and error responses, alongside an introduction to mock APIs. By the end of this session, students will:

- Understand the importance of testing edge cases and error responses.
- Learn how to identify and simulate common error scenarios like 400 and 404 responses.
- Gain hands-on experience with mock APIs to simulate various server responses.

---

### **Free Online Resources**

1. **[Postman’s Guide to Mock Servers](https://learning.postman.com/docs/designing-and-developing-your-api/mocking-data/overview/)**  
   - A step-by-step guide to creating and using mock APIs in Postman.

2. **[Common HTTP Status Codes (MDN)](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)**  
   - A detailed overview of HTTP status codes and their meaning.

3. **[Error Handling in APIs (REST API Tutorial)](https://restfulapi.net/http-status-codes/)**  
   - An introduction to error responses and their role in API testing.

4. **[Boundary Value Analysis (Guru99)](https://www.guru99.com/equivalence-partitioning-boundary-value-analysis.html)**  
   - Learn how to test edge cases effectively using boundary value analysis.

---

### **Topics Covered**

#### **1. Understanding Edge Cases**

- **Overview**:
  - Edge cases are scenarios that occur at the extreme operating limits of a system, such as maximum input size or invalid formats.
  - Testing edge cases ensures the application handles unexpected inputs gracefully.

- **Examples**:
  - Empty input fields.
  - Submitting excessively large payloads.
  - Using special characters in input fields.

#### **2. Error Response Testing**

- **Common Error Responses**:
  - 400 Bad Request: Invalid input provided to the API.
  - 404 Not Found: Endpoint does not exist.
  - 500 Internal Server Error: Server fails to handle a request properly.

- **Hands-On Practice**:
  - Simulate 400 and 404 responses by providing incorrect input or querying non-existent endpoints.
  - Analyze server responses and document error messages.

#### **3. Introduction to Mock APIs**

- **What Are Mock APIs?**:
  - Mock APIs simulate real APIs by providing predefined responses.
  - They are useful for testing scenarios without relying on a live server.

- **Predefined Mock API**:
  - Students will import a predefined mock API setup into Postman and use it to test various scenarios.

- **Exploration Tasks**:
  - Run mock API endpoints and review responses.
  - Modify an endpoint to simulate specific errors, such as a 500 response.

---

### **Assignment**

#### **Part 1: Testing Edge Cases**

**Objective**: Develop a deeper understanding of edge cases and their impact on API functionality.

**Instructions**:

1. **Create Edge Case Scenarios**:
   - Use the `Postman Echo` API to create **three unique edge case scenarios** for a GET request:
     - **Empty Parameter Values**: Add a parameter without assigning a value and observe how the server handles it.
     - **Excessive Input**: Pass a parameter with a string longer than 1,000 characters.
     - **Uncommon Characters**: Test with special or non-ASCII characters (e.g., emojis, symbols).

2. **Add Validations**:
   - Write assertions in the **Tests** tab to validate server behavior for each case.
   - Example assertions:
     - Ensure the response includes the expected parameter.
     - Verify status codes (e.g., 200 for valid requests, 400 for invalid requests).

   ```javascript
   pm.test("Response includes parameter", function () {
       const jsonData = pm.response.json();
       pm.expect(jsonData.args.key1).to.exist;
   });
   ```

3. **Analyze Results**:
   - Document the behavior observed for each scenario, including:
     - Status codes.
     - Response structure.
     - Unexpected behaviors or errors.

4. **Extend Your Understanding**:
   - Create **one additional edge case** scenario of your choice. Document the setup and results.

---

#### **Part 2: Testing Error Responses**

**Objective**: Gain insight into how APIs handle invalid inputs and error responses.

**Instructions**:

1. **Simulate Errors**:
   - Perform the following error tests using the `Postman Echo` POST endpoint:
     - **Invalid JSON**: Send malformed JSON in the body.
     - **Missing Headers**: Omit the `Content-Type` header and observe the response.
     - **Unsupported HTTP Method**: Attempt a PUT request to an endpoint that does not support it.

2. **Add Error Validations**:
   - Write assertions to verify the error responses:
     - Ensure the status code is correct for each error (e.g., 400 for bad requests).
     - Validate the error message.

   ```javascript
   pm.test("Error message is accurate", function () {
       const jsonData = pm.response.json();
       pm.expect(jsonData.error).to.include("Invalid JSON");
   });
   ```

3. **Document Learnings**:
   - Record the results for each error test, including screenshots and observations about how the API handles invalid inputs.

4. **Extend Your Understanding**:
   - Create **one additional error scenario**. Document the setup and the API’s response.

---

#### **Part 3: Exploring Mock APIs**

**Objective**: Gain practical experience working with a Mock API to simulate real-world scenarios.

**Instructions**:

1. **Setup Mock API**:
   - Access the provided Mock API at `https://mockapi.io`.

2. **Create Custom Data**:
   - Perform the following tasks using the Mock API:
     - **GET**: Retrieve data from `/users`.
     - **POST**: Add a new user to `/users` with the following body:

       ```json
       {
           "name": "Jane Smith",
           "email": "janesmith@example.com"
       }
       ```

     - **DELETE**: Remove a user by ID from `/users/{id}`.

3. **Add Advanced Validations**:
   - Write scripts to validate data in the responses:
     - Ensure the POST response includes the newly created user.
     - Verify the DELETE response returns a success message.

4. **Analyze Mock API Behavior**:
   - Record the response times, status codes, and behavior for each endpoint.
   - Note how the Mock API simulates a real API.

5. **Extend Your Understanding**:
   - Create **one additional test case** targeting the `/users` endpoint.
     - Example: Test for duplicate entries or validate data types in the response (e.g., `email` is a string).

---

### **Reflection Component**

**Objective**: Solidify learning through self-assessment.

1. **Reflection Document**:
   - Answer the following prompts:
     - What did you learn about edge cases and error responses?
     - How did the Mock API help you understand real-world testing scenarios?
     - What challenges did you face, and how did you resolve them?
   - Include examples of insights gained or areas needing further improvement.

---

### **Submission Instructions**

1. **Export and Submit**:
   - Export your Postman collection containing edge case and error response tests.
   - Submit the exported JSON files for your mock API setup.

2. **Provide Documentation**:
   - Create a Google Doc summarizing the assignment:
     - Include screenshots of request responses.
     - Detail findings for edge cases and error responses.
     - Reflect on the use of mock APIs.

3. **Logs**:
   - Save and upload Postman Console logs showing test results and any debugging steps.

---

### **Key Learning Outcomes**

- Understand the importance of testing edge cases and error responses.
- Gain hands-on experience simulating error scenarios.
- Learn how to use and modify mock APIs to simulate server responses.

---

### **Key Interview Questions**

1. Why is it important to test edge cases during API testing?
2. What are some common HTTP error responses, and how do they help identify issues?
3. How can mock APIs be utilized to simulate server behavior during testing?

---

### **Tips for Success**

- Use the Postman Console to debug and analyze request/response details.
- Experiment with different payloads and configurations to expand your understanding of edge cases.
- Reach out to peers or mentors for guidance if you encounter difficulties with mock APIs.

---

### **Next Training**

In **Training 5**, we will focus on automating API tests using Newman and integrating them into CI/CD pipelines for advanced workflows.

