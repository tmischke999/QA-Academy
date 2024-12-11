# **Month 4: Training 8 - Comprehensive API Testing Project & Month Wrap-Up**

## **Objective**

The purpose of this training is to consolidate all skills learned during Month 4 into a practical, real-world API testing project. Students will:

- Apply manual and automated testing techniques to a mock API scenario.
- Generate a comprehensive test summary report that showcases their skills.
- Reflect on their Month 4 learning journey and prepare for the advanced topics in Month 5.

By the end of this training, students will have portfolio-ready deliverables and a clear understanding of how to transition into the next phase of the QA Academy.

---

## **Free Online Resources** (Mandatory)

1. **[How to Generate Reports Using Postman Tool (GeeksforGeeks)](https://www.geeksforgeeks.org/how-to-generate-reports-using-postman-tool/)**

   - A guide to using Postman and Newman for generating detailed API testing reports.

2. **[Using Postman Environments (Postman Learning Center)](https://learning.postman.com/docs/sending-requests/managing-environments/)**

   - Understand how to set up and manage environments for dynamic testing scenarios.

3. **[Postman CLI Automation with Newman](https://learning.postman.com/docs/running-collections/using-newman-cli/)**

   - Learn how to execute Postman collections using Newman and analyze logs.

4. **[Creating Effective Test Summary Reports](https://www.guru99.com/how-test-reports-predict-the-success-of-your-testing-project.html)**

   - A practical guide to writing professional test summary reports.

---

## **Topics Covered**

### **1. Comprehensive API Testing Project**

- **Test Planning**:

  - Define the scope, endpoints, and methods for testing.
  - Identify dynamic scenarios using environments and variables.

- **Test Execution**:

  - Combine manual and automated testing techniques.
  - Use Postman collections for structured test execution.
  - Run collections using Newman and save logs.

- **Test Analysis**:

  - Review Newman logs for performance metrics and errors.
    - **Example**: Include a snippet of a Newman CLI log:
      ```
      ┌─────────────────────────┬───────────────────┬──────────────┬──────────┐
      │ Item                    │ Request Type      │ Response Time│ Status   │
      ├─────────────────────────┼───────────────────┼──────────────┼──────────┤
      │ Create User             │ POST              │ 123ms        │ Passed   │
      │ Fetch Users             │ GET               │ 98ms         │ Failed   │
      └─────────────────────────┴───────────────────┴──────────────┴──────────┘
      ```
  - Use Google Sheets to create visual aids summarizing test results, such as a pie chart showing pass/fail rates.

- **Documentation**:

  - Create a professional test summary report.
  - Include:
    - Executive Summary
    - Test Scope
    - Key Findings and Metrics
    - Risks and Recommendations
    - Visual Aids
      **Example Visual Aid**: Provide instructions for creating a pie chart in Google Sheets:
    1. Open Google Sheets and input your test data (e.g., pass and fail counts).
    2. Highlight the data and click "Insert > Chart."
    3. Choose "Pie Chart" from the chart editor.
    4. Customize titles and labels for clarity.

### **2. Month 4 Reflection and Wrap-Up**

- **Reflection Document**:

  - Write about key takeaways from Month 4.
  - Highlight challenges faced and how they were overcome.
  - Example: "While working with Newman CLI, I faced difficulty configuring environment variables correctly. After reviewing the Postman documentation and experimenting with the setup, I successfully resolved the issue."
  - Additional Prompts:
    - What tool did you find the most beneficial and why?
    - How did creating visual aids improve your understanding of test results?
    - What is one skill you developed that you feel confident applying in a QA role?
  - Discuss how Month 4 skills apply to real-world QA scenarios.
  - **Guiding Questions**:
    - What were the most challenging aspects of Month 4?
    - Which tools or techniques were the most useful?
    - How will you apply these skills in future QA tasks?

- **Preparation for Month 5**:

  - Preview of advanced topics, including performance testing and exploratory testing techniques.
  - Checklist of tools and concepts to review before starting Month 5.

---

## **Assignment**

### **Part 1: Comprehensive API Testing Project**

**Objective**: Consolidate Month 4 skills into a real-world API testing scenario.

**Instructions**:

1. **Plan**:

   - Use the provided test plan template (linked in resources). You can find the template in the "Free Online Resources" section, or access it directly here: [Test Plan Template Link]. For example, define test objectives, list endpoints such as `GET /users` or `POST /users`, and specify expected outcomes like "Response status: 200, valid JSON response."
   - Define test scope, including:
     - Endpoints (e.g., `GET /users`, `POST /users`).
     - Methods (e.g., GET, POST).
     - Expected outcomes (e.g., status code 200, valid JSON response).
   - Identify edge cases (e.g., invalid user ID in `GET /users/:id`).

2. **Execute**:

   - Write and execute test cases in Postman:
     - Example test: "Validate `GET /users` returns status 200 and non-empty response body."
   - Set up environment variables:
     - Example variable: `baseURL = https://mockapi.example.com`.
   - Run automated tests using Newman and save the generated logs.

3. **Analyze**:

   - Review Newman logs:
     - Example output: Total tests: 10, Passed: 9, Failed: 1.
   - Use Google Sheets to create visual aids:
     - Pie chart: Pass vs. fail rates. For example, use Google Sheets to input pass and fail counts, select the data, and insert a pie chart under "Insert > Chart."
     - Bar graph: Average response times by endpoint. Use Google Sheets to input response times for each endpoint, select the data, and insert a bar chart under "Insert > Chart." Refer to the provided resources for detailed guidance.

4. **Document**:

   - Create a professional test summary report:
     - Include:
       - Executive Summary
       - Test Scope
       - Key Findings and Metrics
       - Risks and Recommendations
       - Visual Aids
     - Use the provided sample report structure as a reference.

5. **Reflect**:

   - Write a reflection document summarizing your Month 4 journey:
     - Key takeaways from the project.
     - Challenges encountered and how they were addressed.
     - Practical applications of the skills learned.

### **Part 2: Submission**

- Follow these steps to submit:
  1. Name your files using the format `YourName_DocumentType_Month4` (e.g., `JaneDoe_TestPlan_Month4.pdf`, `JaneDoe_Reflection_Month4.docx`). Ensure each file clearly corresponds to the required deliverables. (e.g., `JohnDoe_TestSummaryReport_Month4.pdf`).
  2. Compress logs and visuals into a zipped folder named `YourName_VisualsLogs_Month4.zip`.
  3. Share all files in the designated Slack channel.

---

## **Key Learning Outcomes**

- Master the end-to-end API testing process.
- Demonstrate the ability to create professional documentation for QA.
- Develop confidence in analyzing results and identifying actionable insights.
- Prepare for advanced topics and real-world QA challenges.

---

## **Preparing for Month 5**
- [ ] Completed all steps of the comprehensive API testing project.
- [ ] Submitted the following deliverables:
  - Test plan (PDF format).
  - Test summary report (PDF format).
  - Visual aids and Newman logs (zipped folder).
  - Reflection document (Google Doc link).
- [ ] Reviewed Month 4’s mandatory resources and key concepts:
  - JavaScript for test scripts.
  - Postman collections and environment variables.
  - Newman CLI for automated test execution.
  - Visualizing test results with Google Sheets.
- [ ] Practiced documenting risks and recommendations in test summary reports.
- [ ] Prepared portfolio-ready deliverables to showcase during interviews.

### **Preview of Month 5**
- Explore performance testing techniques and tools.
- Begin integrating exploratory testing methodologies.
- Strengthen reporting and documentation skills for larger projects.

---

**Congratulations on Completing Month 4!**

You’ve reached an important milestone in your QA Academy journey. This month, you’ve tackled complex topics like manual and automated API testing, dynamic test scenarios, and professional-level documentation. The deliverables you’ve created showcase not only your technical skills but also your ability to think critically and solve problems.

Take a moment to reflect on how much you’ve accomplished, and know that these skills are directly applicable to real-world QA roles. As you prepare for Month 5, continue building on this strong foundation with confidence and determination.

Congratulations once again on a job well done!

