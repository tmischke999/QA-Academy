# **Month 4: Training 7 - API Test Summary Reports**

## **Objective**

This training session will guide students in creating comprehensive API test summary reports. These reports will consolidate the results of automated tests, manual tests, and CI/CD pipeline executions, ensuring students understand how to effectively communicate testing outcomes. By the end of this session, students will:

- Understand the structure and purpose of a test summary report.
- Learn to analyze and document test results.
- Gain skills in presenting testing outcomes to technical and non-technical stakeholders.

---

## **Free Online Resources**

### **Mandatory Resources**

1. **[How to Write a Test Summary Report (Guru99)](https://www.guru99.com/how-test-reports-predict-the-success-of-your-testing-project.html)**

   - A step-by-step guide to writing effective test summary reports.

2. **[Test Reporting Best Practices (Software Testing Help)](https://www.softwaretestinghelp.com/test-summary-report-template-download-sample/)**

   - Practical tips for summarizing test results effectively.

3. **[How to Generate Reports Using Postman Tool (GeeksforGeeks)](https://www.geeksforgeeks.org/how-to-generate-reports-using-postman-tool/)**

   - A detailed guide on using Postman and Newman for generating API testing reports.

---

## **Topics Covered**

### **Key Elements of an API Testing Report**

1. **Executive Summary**:

   - **Project Overview**: Briefly describe the project and the APIs being tested.
   - **Testing Scope**: Outline the specific API endpoints and functionalities covered in the testing.
   - **Overall Test Status**: Summarize the overall test results, highlighting pass/fail rates and major issues found.

2. **Test Environment Details**:

   - **API Server URL**: The base URL of the API under test.
   - **Authentication Method**: How authentication is handled (e.g., API key, OAuth).
   - **Test Data**: Specify the data used for testing (sample data, test cases).
   - **Testing Tools**: Mention the tools used for API testing (e.g., Postman, Rest Assured).

3. **Test Cases and Results**:

   - **Test Case ID**: Unique identifier for each test case.
   - **API Endpoint**: The URL of the API endpoint being tested.
   - **HTTP Method**: The request method (GET, POST, PUT, DELETE).
   - **Request Parameters**: Details of the input data sent in the request.
   - **Expected Response**: The anticipated response format and status code.
   - **Actual Response**: The actual response received from the API.
   - **Test Result**: Pass/Fail status, with detailed error messages if applicable.

4. **Performance Metrics**:

   - **Response Time**: Average response time for each API call.
   - **Throughput**: Number of requests processed per unit of time.
   - **Latency**: Time taken for the first response to be received.
   - **Error Rate**: Percentage of failed API calls.

5. **Key Findings and Insights**:

   - **Major Issues**: Highlight the most critical issues encountered during testing (e.g., invalid responses, authentication errors).
   - **Areas of Improvement**: Suggest specific actions to address identified problems.
   - **Positive Observations**: Mention any positive aspects of the API behavior.

6. **Recommendations**:

   - **Prioritization**: Suggest which issues should be addressed first based on severity and impact.
   - **Further Testing**: Recommend additional test scenarios or performance testing if needed.
   - **Documentation Updates**: Highlight any necessary updates to API documentation based on testing results.

---

### **1. Importance of Test Summary Reports**

- **Purpose**: Communicate the outcomes of testing activities to stakeholders.
- **Key Components**:
  - Executive Summary
  - Test Scope
  - Test Coverage Summary
  - Key Findings
  - Risks and Recommendations

**Example Scenario:** Imagine testing a new API for a payment processing system. A test summary report might include an executive summary stating that "All critical payment endpoints were successfully validated, with 95% passing test cases. One critical bug was identified in the refund endpoint, which caused unexpected errors when handling specific edge cases." Key findings could detail the number of passed/failed tests, response time metrics, and specific bugs encountered.

**Relatable Context:** Think of the test summary report as a "QA storybook" that tells the journey of your testing. It translates technical data into actionable insights for stakeholders, such as developers fixing bugs or managers deciding on deployment readiness.

### **2. Structuring an API Test Summary Report**

- **Executive Summary**:

  - Brief overview of testing objectives and results.
  - Highlight critical issues and their resolutions.

- **Test Scope and Coverage**:

  - Details about the APIs tested (e.g., endpoints, methods).
  - Overview of manual and automated tests conducted.

- **Key Findings**:

  - Summary of passed and failed test cases.
  - Metrics such as response times, status codes, and error rates.

**Sample Key Findings Section:**

- **Total Test Cases Executed**: 50
- **Passed**: 45
- **Failed**: 5
- **Average Response Time**: 250ms
- **Error Rate**: 10%
- **Critical Issues Identified**: One endpoint returned a 500 error when processing specific input data.

This format helps summarize testing results concisely and highlights actionable insights for stakeholders.

- **Risks and Recommendations**:
  - Identify potential risks (e.g., untested edge cases).
  - Propose next steps or mitigation strategies.

### **3. Tools and Visual Aids for Test Reporting**

- **Data Visualization**:

  - Use tools like Google Sheets to create charts summarizing test results.
    - **Step-by-step guide**:
      - Open Google Sheets and enter test data (e.g., pass/fail rates).
      - Highlight data and select "Insert" > "Chart."
      - Choose a chart type such as pie chart or bar graph.
      - Customize titles and labels for clarity.
  - Examples: pie charts for pass/fail rates, bar graphs for response times.

- **Log Analysis**:

  - **Using Newman CLI**:
    - Run the command `newman run <collection_name.json>` to execute the Postman collection.
    - Add the `--reporters` option to save logs in HTML or JSON format.
    - Example: `newman run <collection_name.json> --reporters cli,html`.
  - Review Newman CLI logs to identify patterns or anomalies.
  - Highlight critical failures and successful tests.

---

## **Assignment**

### **Part 1: Create a Test Summary Report**

**Objective**: Document the outcomes of your API tests and CI/CD pipeline runs.

**Instructions**:

1. **Executive Summary**:

   - Write a brief overview of the testing objectives and outcomes.
   - Highlight critical issues identified and their resolutions.

2. **Test Scope and Coverage**:

   - List the APIs tested, including endpoints and HTTP methods.
   - Mention the tools used (e.g., Postman, Newman, GitHub Actions).
   - Describe the types of tests conducted (manual, automated, etc.).

3. **Key Findings**:

   - Summarize the test results, including:
     - Total number of test cases executed.
     - Number of passed/failed test cases.
     - Average response times and error rates.
   - Calculate metrics using Google Sheets formulas, such as `=AVERAGE()` for response times.

4. **Visual Aids**:

   - Create at least one chart summarizing test results (e.g., pass/fail rates).
   - Include screenshots of Newman run outputs showing successful and failed tests.

5. **Risks and Recommendations**:

   - Identify untested scenarios or potential risks.
   - Propose next steps or improvements to the testing process.

6. **Review a Sample Report**:

   - Use the sample test summary report shared in Slack as a reference.

### **Part 2: Self-Reflection Document**

**Objective**: Reflect on your progress and identify areas for improvement.

**Instructions**:

1. Write a reflection covering:

   - Key skills acquired during Month 4.
   - Challenges faced and how you overcame them.
   - Goals for Month 5.

2. Submit the reflection as a Google Doc via Slack, ensuring clarity and conciseness.

---

### **Submission Instructions**

1. Submit the following:

   - Test summary report in PDF format.
   - Visual aids and screenshots in a single zipped folder.
   - Self-reflection document in Google Docs.

2. Share all deliverables via Slack, ensuring sharing permissions are set to "Anyone with the link can comment."

---

## **Key Learning Outcomes**

- Master the structure and components of a professional test summary report.
- Develop skills in analyzing test results and identifying risks.
- Gain experience in creating actionable recommendations based on testing outcomes.

---

## **Key Interview Questions**

1. What is the purpose of a test summary report?
2. How do you structure an effective test summary report?
3. What metrics are most useful for summarizing API test results?
4. How would you present key findings to non-technical stakeholders?

---

## **Tips for Success**

- **Be Concise**: Focus on critical findings and actionable insights.
- **Use Visuals**: Simplify complex data with clear charts and graphs.
  - **Using Google Sheets**: Enter test data in rows and columns, highlight it, and select "Insert > Chart" to create a visual representation like pie charts or bar graphs. Customize labels and titles to make your charts clear and professional.
- **Practice**: Review sample reports to understand best practices.
- **Collaborate**: Share drafts with peers for feedback in Slack.
- **Troubleshoot**: Refer to the troubleshooting guide for Newman CLI issues.

---

## **Next Training**

In **Training 8**, we will conclude Month 4 with a comprehensive project that consolidates all the skills learned in API testing. Students will:

- Apply manual and automated testing techniques to a practical API testing scenario.
- Generate detailed test summary reports, including key findings and performance metrics.
- Reflect on the integration of tools like Postman, Newman, and Google Sheets in their workflows.

This session will serve as a capstone for Month 4, preparing students to transition smoothly into Month 5.

