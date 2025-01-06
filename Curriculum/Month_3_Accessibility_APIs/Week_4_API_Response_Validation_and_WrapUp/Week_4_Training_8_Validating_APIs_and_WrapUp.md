# **Month 3 Training 8 - Validating API Responses & Month Wrap-Up**

---

### **Objective**

The purpose of this training is to guide students through understanding and executing **API response validation** using Postman. By the end of this training, students will:

- Understand how to validate API responses using Postman’s built-in test scripts.
- Gain experience using **response validation scripts** to automate and verify their API requests.
- Reflect on Month 3’s journey and document their progress in a **reflection document**.

---

### **Free Online Resources** (Mandatory)

To support your understanding, students must explore the following resources before engaging with the content:

1. **[Testing Responses in Postman (Postman Learning Center)](https://learning.postman.com/docs/writing-scripts/test-scripts/)**  
   This guide will help you understand how to create response validation scripts using Postman, including pre-written snippets.

2. **[JSON Basics (Codecademy)](https://www.codecademy.com/articles/what-is-json)**  
   A refresher on **JSON**, which is commonly used for API response data.

3. **[Postman API Test Automation for Beginners (YouTube)](https://www.youtube.com/watch?v=zp5Jh2FIpF0)**  
   A beginner-friendly video showing how to set up test scripts in Postman for response validation.

---

### **Topics Covered**

#### **1. Introduction to Response Validation**

- **Explanation**: Learn what response validation is, why it’s important, and how it helps ensure the quality of APIs. Response validation is the process of verifying the data returned from an API to ensure it is accurate and meets requirements.
  - **Key Insight**: Response validation helps confirm that the server’s response is as expected and ensures any changes to the server-side don’t introduce bugs in your application.

#### **2. Using Postman Test Scripts**

- **Pre-Built Snippets**: Learn how to use Postman’s pre-built scripts to simplify writing JavaScript tests.
  - Example Snippets Include:
    - **Status Code Check**:  
      ```javascript
      pm.test("Status code is 200", function () {
          pm.response.to.have.status(200);
      });
      ```
      **Explanation**: This script checks if the response status code is 200, indicating a successful GET or POST request.

    - **Response Time Check**:  
      ```javascript
      pm.test("Response time is less than 200ms", function () {
          pm.expect(pm.response.responseTime).to.be.below(200);
      });
      ```
      **Explanation**: Ensures that the response time is less than 200 milliseconds, helping evaluate the speed of the API.

    - **Body Contains String**:  
      ```javascript
      pm.test("Body matches string", function () {
          pm.expect(pm.response.text()).to.include("string_you_want_to_search");
      });
      ```
      **Explanation**: Checks if the response body includes a specific string, useful for validating if certain content is returned.

    - **JSON Key-Value Match**:  
      ```javascript
      pm.test("Your test name", function () {
          var jsonData = pm.response.json();
          pm.expect(jsonData.value).to.eql(100);
      });
      ```
      **Explanation**: Extracts data from the JSON response and verifies that it matches the expected value. Key-value pairs can be compared to a dictionary entry for easy understanding.

    - **Header Check**:  
      ```javascript
      pm.test("Content-Type is present", function () {
          pm.response.to.have.header("Content-Type");
      });
      ```
      **Explanation**: Validates that the Content-Type header is present in the response, ensuring the server specifies the type of returned content.

    - **Successful POST Request Status Codes**:  
      ```javascript
      pm.test("Successful POST request", function () {
          pm.expect(pm.response.code).to.be.oneOf([201, 202]);
      });
      ```
      **Explanation**: Checks if the status code indicates that a resource was successfully created, which is typical for POST requests.

    - **Status Code Name Contains Specific String**:  
      ```javascript
      pm.test("Status code name has string", function () {
          pm.response.to.have.status("Created");
      });
      ```
      **Explanation**: Confirms that the response status message includes a specific string, such as "Created," which can be useful for verifying POST requests.

- **Common Error Codes**: Learn how to test for common **error codes** such as **400 Bad Request**, **401 Unauthorized**, and **500 Internal Server Error**.
  - **Key Insight**: Understanding these error codes helps diagnose issues in requests or server responses, making troubleshooting easier.
  - **Error Code Examples**:
    - **400 Bad Request**: Often caused by incorrect parameters or missing fields.
    - **401 Unauthorized**: Indicates missing or incorrect authentication.
    - **500 Internal Server Error**: Occurs if the server encounters an unexpected condition.

#### **3. Adding and Customizing Response Tests**

- **Practice Exercise**: Practice adding tests to your API requests in Postman:
  1. **Select a Request** from your collection (e.g., a GET or POST request created earlier in Month 3).
  2. Go to the **Scripts** tab in Postman and use the **Snippets** section to add common validation scripts.
  3. Customize one of the scripts by modifying its assertion, such as changing the expected **status code** or **response content**.
  - **Key Insight**: Customizing response tests allows you to ensure the API meets the specific needs of your application.

---

### **Assignment**

#### **Part 1: Using All Pre-Built Snippets to Validate Responses**

- **Objective**: Add validation to previously created requests to ensure their responses meet expectations.
- **Instructions**:
  1. Open the **QA Academy** collection in Postman.
  2. Select the **POST Create User** request from the previous training.
  3. In the **Tests** tab, add the following pre-built snippets:
     - **Status Code is 200**:
       ```javascript
       pm.test("Status code is 200", function () {
           pm.response.to.have.status(200);
       });
       ```
       **Explanation**: Checks that the response status code is 200, indicating a successful GET or POST request.

     - **Response Time is Less Than 200ms**:
       ```javascript
       pm.test("Response time is less than 200ms", function () {
           pm.expect(pm.response.responseTime).to.be.below(200);
       });
       ```
       **Explanation**: Ensures the response time is less than 200 milliseconds to evaluate API performance.

     - **Body Matches String**:
       ```javascript
       pm.test("Body matches string", function () {
           pm.expect(pm.response.text()).to.include("string_you_want_to_search");
       });
       ```
       **Explanation**: Validates that the response body contains a specific string, which is helpful for confirming content.

     - **JSON Key-Value Match**:
       ```javascript
       pm.test("Your test name", function () {
           var jsonData = pm.response.json();
           pm.expect(jsonData.value).to.eql(100);
       });
       ```
       **Explanation**: Extracts data from the JSON response and verifies it matches the expected value.

     - **Content-Type is Present**:
       ```javascript
       pm.test("Content-Type is present", function () {
           pm.response.to.have.header("Content-Type");
       });
       ```
       **Explanation**: Ensures that the `Content-Type` header is present in the response, confirming the data type.

     - **Successful POST Request**:
       ```javascript
       pm.test("Successful POST request", function () {
           pm.expect(pm.response.code).to.be.oneOf([201, 202]);
       });
       ```
       **Explanation**: Confirms that the status code for a POST request indicates success (e.g., resource created).

     - **Status Code Name Contains Specific String**:
       ```javascript
       pm.test("Status code name has string", function () {
           pm.response.to.have.status("Created");
       });
       ```
       **Explanation**: Validates that the response status message contains a specific string, such as "Created."

  4. Send the request and confirm that the tests pass.
  5. Take **screenshots** of your test results and include them in your summary report.

#### **Part 2: Customizing Your Own Test Scripts**

- **Objective**: Practice modifying a pre-built test script to better understand how JavaScript snippets work in Postman.
- **Instructions**:
  1. Choose the **GET Request** created in Training 6.
  2. In the **Tests** tab, modify the **Response Value Matching** snippet to check for a specific value in the response body.
     - Example: Change the value being checked in the snippet to a different expected value.
  3. Execute the request and verify that your custom test passes.
  4. Write a **summary** (at least 1 paragraph) describing what changes you made and why.

#### **Part 3: Month 3 Reflection Document**

- **Objective**: Reflect on your learning journey for Month 3 and document your progress.
- **Instructions**:
  1. Write a **reflection document** that includes:
     - **Key Takeaways**: What did you learn about API testing and validation?
     - **Challenges and Solutions**: What were the biggest challenges, and how did you overcome them?
     - **Practical Applications**: How do you see yourself using these skills in a QA role?
  2. Submit your reflection in a **Google Doc** via the Slack channel.

---

### **Submission Instructions**

**How to Submit**:

1. **Export Your Postman Collection**:
   - Navigate to the **Collections** tab.
   - Find your `QA Academy` collection, click on the three dots (...) next to it, and select **Export**.
   - Save the exported JSON file locally.

2. **Export Your Postman Environments**:
   - Navigate to the **Environments** tab.
   - Click on the three dots (...) next to each environment (`QA` and `Test Server`) and select **Export**.
   - Save each exported JSON file locally.

3. **Share Your Collection, Environments, and Documentation**:
   - Upload the exported JSON files of your `QA Academy` collection and both environments to the designated Slack channel.
   - Attach a **Google Doc** summarizing your POST request results, changes made to the JSON data, and screenshots.

Ensure all sharing settings allow "Anyone with the link" to view and comment as necessary.

---

### **Tips for Success**

- **Use Pre-Built Snippets**: These scripts are designed to help you test without needing deep JavaScript knowledge. Focus on understanding what each snippet does, rather than writing JavaScript from scratch.
- **Test Common Scenarios**: Validate both **success** and **failure** scenarios to ensure your API handles different situations appropriately.
- **Ask Questions**: If you’re unsure about any step or concept, use the Slack channel to collaborate and clarify.

---

### **Key Deliverables for Month 3**

1. **GET and POST API Test Results**:
   - Demonstrate competency in executing GET and POST requests, capturing responses, and analyzing results.

2. **Environment Configuration Proficiency**:
   - Proper setup and usage of multiple environments (`QA` and `Test Server`) with dynamic variables in Postman.

3. **Snippet Implementation and Customization**:
   - Effective application and modification of pre-built test snippets to validate API responses.

4. **Reflection Document**:
   - A detailed reflection summarizing learning and growth during Month 3.

---

### **Preparing for Month 4**

In **Month 4**, we will continue expanding on **API testing**, focusing on more advanced topics like **collections**, **test automation**, and integrating **response validation** into larger testing workflows. Students will also start learning more about **JavaScript**, preparing them to understand the underlying structure of validation scripts used in API testing.

### **Preparing for Month 4 with a Checklist**

- **Checklist of Tools and Concepts**:
   - [ ] Completed Month 3’s assignments and reflections.
   - [ ] **Reviewed JavaScript snippets** used in validation scripts and understand their usage.
   - [ ] **Utilized all free resources** provided in Month 3’s training to build a foundational understanding of JavaScript for API testing.

---

**Congratulations on Completing Month 3!**

You have worked hard to gain a thorough understanding of **API testing**, from GET and POST requests to understanding and validating responses. Your hands-on practice with Postman, JSON, and test scripts has laid a strong foundation for the more advanced topics we'll cover in Month 4. Take pride in what you’ve accomplished, and prepare to build on this knowledge as we advance to more complex testing scenarios.
