# **Month 4: Training 5 - Advanced Postman Automation with Newman**

### **Objective**

In this training session, students will build on their understanding of Postman and Newman by automating the execution of a larger API collection. They will learn to fork and utilize the Postman Echo Collection, configure Newman to handle advanced scenarios, and document results effectively.

By the end of this session, students will:

- Automate the execution of a complex Postman collection using Newman.
- Customize test scripts within the Postman Echo Collection.
- Analyze and document test run results.

---

### **Free Online Resources**

#### **Mandatory Resources**

1. **[Using Newman CLI](https://learning.postman.com/docs/collections/using-newman-cli/command-line-integration-with-newman/)**  
   - A guide to integrating Newman with Postman collections.

2. **[Mindbowser: API Testing with Postman & Newman](https://www.mindbowser.com/api-testing-postman-newman-methods/)**  
   - Practical insights into API testing with Postman and Newman.

3. **[Postman Newman Tutorial (YouTube)](https://www.youtube.com/watch?v=iS7HPNswv-8&t=78s)**  
   - Video walkthrough of Newman basics and use cases.

4. **[Postman Automation Testing Tutorial](https://www.youtube.com/watch?v=EnrpXlNe2dc)**  
   - Comprehensive guide on Newman and Postman automation testing.

5. **[Running Postman Tests with Newman (YouTube)](https://www.youtube.com/watch?v=SQlwGZj97Y4&t=3s)**  
   - A video tutorial covering Newman setup and execution.

---

#### **Optional Resources**

6. **[Automation Tricks for Newman](https://blog.postman.com/automation-tricks-for-newman/)**  
   - Tips and tricks to enhance automation workflows with Newman.

7. **[Custom Reporters in Newman](https://learning.postman.com/docs/collections/using-newman-cli/newman-custom-reporters/)**  
   - A guide to creating custom reports for Newman runs.

---

### **Topics Covered**

#### **1. Forking and Understanding the Postman Echo Collection**

- **Overview**: The Postman Echo Collection provides a variety of API requests to test functionality, including `GET`, `POST`, `PUT`, and `DELETE` requests.
- **Steps to Fork**:
  1. Open the [Postman Echo Collection](https://learning.postman.com/docs/developer/echo-api/).
  2. Click the **Fork** button.
  3. Select the **QA Academy Workspace**.
  4. Name the fork appropriately (e.g., `QA Academy - Postman Echo Fork`).

#### **2. Configuring Newman for Advanced Collection Runs**

- **Review of Newman CLI**:
  - Understanding basic commands: `newman run <collection-file>`.
  - Adding options such as `--reporters`, `--iteration-data`, and `--environment`.

- **Customizing Test Runs**:
  - Running specific folders or requests within the collection.
  - Validating different responses and status codes.

#### **3. Adding Custom Test Scripts**

- **Examples of Test Scripts**:
  - Validating response status codes:
    ```javascript
    pm.test("Status code is 200", function () {
      pm.response.to.have.status(200);
    });
    ```
  - Checking response headers:
    ```javascript
    pm.test("Content-Type is application/json", function () {
      pm.response.to.have.header("Content-Type", "application/json");
    });
    ```
  - Ensuring response body contains specific data:
    ```javascript
    pm.test("Response contains user data", function () {
      var jsonData = pm.response.json();
      pm.expect(jsonData.user).to.exist;
    });
    ```

---

### **Assignment**

#### **Part 1: Fork the Postman Echo Collection**

1. **Objective**: Gain familiarity with a pre-built collection for Newman automation.

2. **Instructions**:
   - Open the [Postman Echo API Documentation](https://learning.postman.com/docs/developer/echo-api/).
    - Link to the **Echo Collection** can be found under the section titled: **Next Steps**.
   - Fork the collection into your **QA Academy Workspace**.
   - Run a few basic requests in Postman to familiarize yourself with the endpoints and scripts.

#### **Part 2: Customize and Execute the Collection with Newman**

1. **Objective**: Automate the Postman Echo Collection and analyze the results.

2. **Instructions**:
   - **Check Node.js Installation**:
     - Run `node -v` and `npm -v` in Command Prompt (Windows) or Terminal (macOS/Linux).
     - If not installed, download Node.js from [Node.js Official Site](https://nodejs.org).
   - **Install Newman**:
     - Run `npm install -g newman`.
   - **Run the Collection**:
     - Use the command: `newman run <collection-file> --reporters cli,json`.
     - Replace `<collection-file>` with the path to your exported Postman Echo Collection JSON file.

3. **Add Custom Test Scripts**:
   - Write and add test scripts to validate:
     - Response times.
     - Response data integrity.
     - Header validation.

4. **Analyze Results**:
   - Review CLI output for passed/failed tests.
   - Take screenshots of any failures and debug using the Postman Console.

#### **Part 3: Create an Extended Scenario**

1. **Objective**: Demonstrate advanced test creation and execution.

2. **Instructions**:
   - Modify one request in the Echo Collection to include parameters or a unique header.
   - Add assertions to validate:
     - Custom parameter values in the response.
     - Server behavior with additional headers.

3. **Run the Collection**:
   - Use Newman to execute the updated collection.
   - Document results and provide reflections.

---

### **Submission Instructions**

1. **Export and Submit**:
   - Export your updated Postman Echo Collection and submit the JSON file.

2. **Save Newman CLI Logs**:
   - To capture and save CLI logs:
     - **Windows Command Prompt**:
       - Run: `newman run <collection-file> --reporters cli,json > newman-log.txt`
       - This command saves the CLI output to a file named `newman-log.txt` in the current directory.
     - **macOS/Linux Terminal**:
       - Run: `newman run <collection-file> --reporters cli,json > newman-log.txt`
       - The log file will be saved in the directory from which the command is executed.
     - Attach this log file to your submission.

3. **Provide Documentation**:
   - Create a Google Doc summarizing:
     - The steps taken to automate the collection.
     - Test script examples and results.
     - Any challenges faced and how they were resolved.

---

### **Key Learning Outcomes**

- Understand how to automate API testing using Newman.
- Gain hands-on experience executing and customizing Postman collections.
- Learn how to document and analyze automated test results effectively.

---

### **Key Interview Questions**

1. What is Newman, and how is it used in API testing?
2. How do you validate API responses using test scripts in Postman?
3. What are the benefits of automating API tests with Newman?
4. How would you handle debugging test failures in a Newman run?

---

### **Tips for Success**

- Use the Postman Console to debug requests before running them in Newman.
- Experiment with Newman command-line options to explore its full capabilities.
- Take your time reviewing the Postman Echo Collection to understand each endpoint.

---

### **Next Training**

In **Training 6**, we will focus on advanced CI/CD pipelines and integrating Newman runs into automated workflows for scalable API testing.

