# **Week 3: Capstone Execution (Part 2)**

## **Objective**

Finalize the capstone project with automation and performance testing.

---

## **Free Online Resources** (Optional)

1. **[Playwright Official Documentation](https://playwright.dev/docs/intro)**

   - Guide on writing and executing UI automation scripts.

2. **[Postman API Testing Guide](https://learning.postman.com/docs/getting-started/introduction/)**

   - Comprehensive resource for writing and testing API scripts.

3. **[Lighthouse Performance Audits (Google Developers)](https://developers.google.com/web/tools/lighthouse)**

   - Step-by-step guide for running and interpreting performance audits.

4. **Review Prior Resources**:

   - Students are encouraged to revisit resources from:
     - **Month 4**: API testing techniques and Postman collections.
     - **Month 5**: Writing Playwright scripts and performance testing insights.

---

## **Focus**

1. **Write and Execute API Automation Scripts**:

   - **Purpose**: Automate key API tests to validate functionality, error handling, and performance, ensuring consistent results across environments.

   - **Key Goals**:
     - Verify response codes, headers, and payloads.
     - Validate error handling for edge cases and invalid inputs.
     - Ensure APIs meet performance benchmarks.

   - **Tools and Techniques**:
     - Use Postman for scripting and testing API endpoints:
       - Write tests to validate status codes and response payloads.
       - Use pre-request and test scripts for advanced validation.
     - Example:
       ```javascript
       pm.test("Validate user details endpoint returns correct response", function () {
                pm.response.to.have.status(200);
                const jsonData = pm.response.json();
                pm.expect(jsonData).to.have.property('userId');
                pm.expect(jsonData.userId).to.equal(123);
            });
            const jsonData = pm.response.json();
            pm.expect(jsonData).to.have.property('userId');
            pm.expect(jsonData.userId).to.equal(123);
        });
       ```
   - **Document Expectations**:
     - Save test results, including response payloads and logs.
     - Take screenshots for errors or failed validations.

   - **Output**:
     - Comprehensive API test results with key metrics, validations, and identified issues.
     - Example:
       ```javascript
       pm.test("Validating user details endpoint", function () {
            pm.response.to.have.status(200);
            const jsonData = pm.response.json();
            pm.expect(jsonData).to.have.property('userId');
            pm.expect(jsonData.userId).to.equal(123);
        });
            });
       ```
   - Document test results, including screenshots and logs.

2. **Write and Execute UI Automation Scripts**:

   - **Purpose**: Automate critical user flows to ensure consistent and reliable functionality across different environments.

   - **Key Goals**:
     - Validate essential workflows such as login, form submissions, and dropdown interactions.
     - Identify and document UI inconsistencies or failures during execution.

   - **Tools and Techniques**:
     - Use Playwright to write and execute scripts for automated UI tests.
       - Example: Automate dropdown interaction:
         ```javascript
         test("Validate dropdown functionality allows valid selections", async ({ page }) => {
            await page.goto("https://the-internet.herokuapp.com/dropdown");
            await page.selectOption("#dropdown", "2");
            const selectedOption = await page.locator("#dropdown option:checked").textContent();
            expect(selectedOption).toBe("Option 2");
            });
                await page.selectOption("#dropdown", "2");
                const selectedOption = await page.locator("#dropdown option:checked").textContent();
                expect(selectedOption).toBe("Option 2");
            });
         ```

        - Example: Automate form submission:
         ```javascript
         test("Verify form submission", async ({ page }) => {
             await page.goto("https://the-internet.herokuapp.com/login");
             await page.fill("#username", "invalid_user");
             await page.fill("#password", "wrong_password");
             await page.click("button[type='submit']");
             await expect(page.locator("#flash")).toContainText("Your username is invalid!");
         });
         ```
   - **Document Expectations**:
     - Save screenshots for failed tests and debugging logs.
     - Create a list of pass/fail outcomes with a summary of key findings.

   - **Output**:
     - Comprehensive UI automation results with documented workflows, issues, and resolutions.

3. **Perform Performance Audits**:

   - **Purpose**: Evaluate the responsiveness, stability, and overall performance of the application using real-world metrics.

   - **Key Metrics to Analyze**:
     - **Page Load Times**: Measure how quickly the application renders for users.
     - **Largest Contentful Paint (LCP)**: Identify the time taken to render the largest visible element on the page.
     - **Time to Interactive (TTI)**: Determine how long it takes for the application to become fully interactive.
     - **Cumulative Layout Shift (CLS)**: Evaluate unexpected layout shifts during loading.

   - **Tools and Techniques**:
     - Use Lighthouse in Chrome DevTools:
       - Navigate to the "Performance" tab and run a detailed audit.
       - Save the report as a PDF.
       - Document key findings and generate insights for improvement.
     - Consider running tests on different network speeds (e.g., 3G, 4G) to simulate real-world scenarios.

   - **Report Expectations**:
     - Summary of metrics with detailed explanations of each.
     - Visual aids (charts or screenshots) to highlight significant findings.
     - Recommendations for improving performance, such as:
       - Compressing images.
       - Minimizing JavaScript execution.
       - Using browser caching effectively.

   - Example Report Sections:
     - **Metrics Summary**: Provide an overview of the audit results with key insights.
     - **Critical Issues**: Highlight areas that significantly impact user experience.
     - **Recommendations**: List prioritized actions to improve performance..

4. **Compile Results into a Test Summary Report**:

   - Combine findings from automation and performance testing into a single professional-grade report.
   - Include:
     - Executive Summary.
     - Detailed Results:
       - API Test Results.
       - UI Automation Test Results.
       - Performance Metrics.
     - Recommendations:
       - Prioritized list of fixes based on severity and impact.
   - Format the report with visual aids such as charts and tables.

---

## **Step-by-Step Instructions**

### **1. Execute Automation Scripts**

- Use the test plan from Week 1 to guide your automation testing.
- Write and execute API and UI automation scripts for the key scenarios identified.
- Document results for each script:
  - Pass/fail outcomes.
  - Issues encountered and steps taken to debug.

### **2. Perform Performance Audits**

1. **Run Lighthouse Audits**:

   - Open Chrome DevTools > Lighthouse tab.
   - Select "Performance" and run the audit.
   - Save the report as a PDF.

2. **Analyze Results**:

   - Highlight key metrics like Speed Index, LCP, and TTI.
   - Identify high-impact issues and list recommended improvements.

### **3. Compile Results into a Professional Report**

- Structure your report as follows:
  1. **Executive Summary**:
     - Overview of testing objectives and outcomes.
  2. **API Test Results**:
     - Summary of automated test cases and outcomes.
  3. **UI Automation Test Results**:
     - Results from Playwright scripts, including screenshots.
  4. **Performance Metrics**:
     - Key metrics and issues identified from Lighthouse audits.
  5. **Recommendations**:
     - Actionable suggestions to improve quality, prioritized by severity.

### **4. Bug Tracking and Collaboration**

- Document any bugs identified during automation and performance testing using a structured approach:
  - Use tools like Google Sheets or defect tracking tools (e.g., Trello, Jira) if available.
  - Include the following fields in your bug log:
    - **Bug ID**: Unique identifier for each bug.
    - **Summary**: A brief description of the bug.
    - **Steps to Reproduce**: Detailed instructions to recreate the bug.
    - **Expected vs. Actual Results**: Clear comparison of what should happen vs. what actually occurred.
    - **Severity**: Critical, High, Medium, or Low.
    - **Status**: Open, In Progress, Closed.
    - **Assignee**: The person responsible for addressing the bug.
  - Example Bug Log:
    ```plaintext

        | **Bug ID** | **Summary**                  | **Steps to Reproduce**                        | **Expected Result**      | **Actual Result**         | **Severity** | **Status**  |
        |------------|------------------------------|-----------------------------------------------|--------------------------|---------------------------|--------------|-------------|
        | 001        | Error message not displayed | Navigate to login page, enter invalid credentials | Error message displayed | No error message displayed | High         | Open        |
    ```

- Structure your report as follows:
  1. **Executive Summary**:
     - Overview of testing objectives and outcomes.
  2. **API Test Results**:
     - Summary of automated test cases and outcomes.
  3. **UI Automation Test Results**:
     - Results from Playwright scripts, including screenshots.
  4. **Performance Metrics**:
     - Key metrics and issues identified from Lighthouse audits.
  5. **Recommendations**:
     - Actionable suggestions to improve quality, prioritized by severity.

---

## **Assignment**

**Real-World Context**:
- These deliverables (e.g., test summary report, automation scripts) mimic real-world tasks for QA professionals.
- The test summary report and supporting artifacts are designed to:
  - Provide developers with actionable insights.
  - Help stakeholders understand the application's quality.
  - Serve as a reference for team discussions and decision-making.

**Portfolio Readiness**:
- Prepare your GitHub repository to showcase your work professionally:
  - Include clear documentation in the `README.md`.
  - Add comments to all scripts to explain their purpose.
  - Use descriptive commit messages to highlight your workflow.
- Be prepared to discuss your approach and findings during interviews.

1. **Automation Testing**:

   - Write and execute API and UI automation scripts.
   - Document results in the `docs/` folder of your repository.

2. **Performance Audits**:

   - Run Lighthouse performance audits.
   - Save the report and document findings in the `docs/` folder.

3. **Test Summary Report**:

   - Compile all results into a single professional-grade report.
   - Include visual aids like charts and tables for clarity.

4. **Submit Work**:

   - Share the link to your GitHub repository in the QA Academy Slack channel.
   - Ensure the repository includes:
     - API and UI automation scripts in the `scripts/` folder.
     - Performance report in the `results/` folder.
     - Test summary report in the `docs/` folder.
   - Include a reflection in your `README.md` addressing:
   - What challenges did you face in automation testing?
   - How did performance testing highlight opportunities for improvement?
   - What did you learn about combining multiple testing techniques?
   - How would you prioritize bugs or issues identified during testing?
   - How do you plan to showcase this project in a professional portfolio?
   - How would you communicate findings effectively to developers or stakeholders?
---

## **Key Learning Outcomes**

- Gain hands-on experience with API and UI automation testing.
- Analyze performance metrics to identify and address critical issues.
- Create a professional-grade test summary report.
- Enhance skills in integrating and documenting multiple testing techniques.

