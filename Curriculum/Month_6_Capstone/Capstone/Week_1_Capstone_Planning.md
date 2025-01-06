# **Week 1: Capstone Planning and Setup**

## **Objective**

Define the scope and objectives of the capstone project by identifying key features to test, establishing measurable goals for each testing type, and planning the deliverables to ensure comprehensive quality assurance coverage.

---

## **Free Online Resources** (Optional)

1. **[How to Write a Test Plan (Software Testing Help)](https://www.softwaretestinghelp.com/how-to-write-test-plan-document-software-testing-training-day3/)**

   - Comprehensive guide on creating professional test plans.

2. **[Exploratory Testing Explained (Ministry of Testing)](https://www.ministryoftesting.com/articles/what-is-exploratory-testing-an-alternative-to-scripted-testing-and-try-to-break-it-testing)**

   - Beginner-friendly tutorial on exploratory testing techniques.

3. **[API Testing Basics (Postman)](https://learning.postman.com/docs/getting-started/introduction/)**

   - Step-by-step introduction to API testing with Postman.

4. **[Performance Testing with Lighthouse (Google Developers)](https://developers.google.com/web/tools/lighthouse)**

   - Detailed guide on using Lighthouse for performance audits.

5. **[Playwright Official Documentation](https://playwright.dev/docs/intro)**

   - Learn how to set up and write UI automation scripts.

6. **Review Prior Resources**:

   - Students are encouraged to revisit the resources provided in earlier months for guidance on:
     - Setting up tools (Month 1).
     - Writing test cases (Month 2).
     - API validation with Postman (Month 3).
     - Creating comprehensive test reports (Months 4 and 5).

---

## **Focus**

1. **Create a Comprehensive Test Plan**:

   - Incorporate multiple testing techniques:
     - Manual testing.
     - Exploratory testing.
     - Accessibility testing.
     - API testing.
     - Performance testing.
     - UI automation testing.
   - Define specific test scenarios for each type of testing.
   - Identify key goals, test coverage, and success criteria.

2. **Define Deliverables and Timelines**:

   - Break the project into manageable milestones:
     - Week 1: Test planning and repository setup.
     - Week 2: Manual, exploratory, and accessibility testing.
     - Week 3: Automation and performance testing.
   - Establish clear deadlines for deliverables.

3. **Set Up the GitHub Repository**:

   Ensure the repository is organized to facilitate collaboration and easy navigation.

   - **Real-World Context**:
     - In a professional setting, this repository would be shared with stakeholders and team members to align on test strategies and progress.
     - Well-documented scripts and a clear structure ensure smooth collaboration.

   - **Team Collaboration Tips**:
     - Use clear naming conventions for files and folders (e.g., `ui_tests` for UI scripts).
     - Add comments to all test scripts to explain their purpose.
     - Maintain a `CHANGELOG.md` to track updates and changes over time.
        - `docs/` folder for test plans and reports.
        - `scripts/` folder for automation scripts.
        - `results/` folder for performance metrics and logs.
     - Create a `README.md` to document the repository structure and usage.

---

## **Step-by-Step Instructions**

To ensure the successful completion of Week 1, follow these detailed steps:

### **1. Define the Project Scope**

Explicitly outline the features and objectives for the capstone project. This section is crucial for establishing a strong foundation.

- Choose a test application (e.g., [The Internet](https://the-internet.herokuapp.com)).
- Identify core features to test:
  - Login functionality: "Ensure login works with valid credentials and fails with invalid ones."
  - Dropdown interactions: "Verify dropdown options are selectable and update the UI correctly."
  - Form validation: "Ensure form inputs display proper error messages for invalid data."
  - Performance benchmarks: "Analyze response times and identify performance bottlenecks."
- List objectives for each testing technique:
  - Example: "Ensure all form inputs display proper error messages for invalid data."

### **2. Draft the Test Plan**

Use the following structure for the test plan:
  1. **Introduction**:
     - Brief overview of the capstone project.
     - Objectives and scope.
  2. **Testing Types**:
     - Manual Testing: Specific user scenarios.
     - Exploratory Testing: Edge cases and undocumented scenarios.
     - Accessibility Testing: Ensuring WCAG compliance.
     - API Testing: Verifying responses and error handling.
     - Performance Testing: Analyzing page load times and response times.
     - UI Automation Testing: Validating UI interactions like dropdowns and forms.
  3. **Test Scenarios**:
     - Provide a clear and detailed description of each scenario, including:
       - The feature being tested (e.g., "Login functionality" or "Form validation").
       - The specific inputs and actions required for the test (e.g., "Enter valid credentials and click submit" or "Enter invalid email format").
       - The expected outcome (e.g., "User is redirected to the dashboard" or "Error message is displayed under the email field").
       - Any edge cases to be considered (e.g., "Empty fields" or "SQL injection attempt").

     **Test Plan Review Checklist**:

        - [ ] Are all test scenarios clearly defined with inputs, actions, and expected outcomes?
        - [ ] Have edge cases and success criteria been considered for each scenario?
        - [ ] Does the plan align with the objectives outlined in the introduction?
        - [ ] Have all team members reviewed the test plan for completeness?


     **Example Test Case**:
     ```plaintext
     Feature: Login Functionality
     Inputs: Username = "user123", Password = "pass123"
     Actions: Navigate to login page, enter credentials, click "Login"
     Expected Outcome: User is redirected to dashboard, no error message displayed.
     Edge Cases: Empty username, SQL injection attempt in password field.
     ```

4. **Success Criteria**:
     - Define clear pass/fail criteria for each test scenario, such as:
       - "The login page must redirect users with valid credentials to the dashboard within 2 seconds."
       - "Error messages must display for all invalid form inputs, with accurate and helpful text."

### **3. Set Up the GitHub Repository**

Ensure the repository is organized to facilitate collaboration and easy navigation.

1. **Create the Repository**:

   - Log in to GitHub.
   - Create a new repository named `Capstone_Project`.
   - Add a description and initialize the repository with a `README.md` file.

2. **Organize Repository Structure**:

   - Add folders:
     ```
     Capstone_Project/
     ├── docs/
     │   ├── test_plan.md
     ├── scripts/
     │   ├── ui_automation_script.js
     ├── results/
     │   ├── performance_report.json
     ```
   - Update the `README.md` with:
     - Repository purpose.
     - Folder descriptions.
     - Instructions for running automation scripts.
     - Include links to reports and scripts as they are completed.

3. **Commit Initial Files**:

   - Draft and add the test plan to the `docs/` folder.
   - Use the following commands to create the folder structure locally:
     ```bash
     mkdir docs scripts results
     touch docs/test_plan.md scripts/ui_automation_script.js results/performance_report.json
     ```
   - Push changes to GitHub:
     ```bash
     git add .
     git commit -m "Initial commit with test plan and folder structure"
     git push origin main
     ```

---

## **Assignment**

Complete the following tasks to demonstrate your understanding of planning and repository setup:

1. **Test Plan**:

   - Create a detailed test plan covering all required testing techniques.
   - Include at least three scenarios for each testing type.

2. **GitHub Repository**:

   - Set up the repository with the specified structure.
   - Add the test plan to the `docs/` folder.
   - Ensure the `README.md` explains the repository purpose and organization.

3. **Submit Work**:

   - Share the link to the GitHub repository in the QA Academy Slack channel.
   - Include a short reflection in your `README.md` on challenges faced during the setup and how they were addressed, e.g., "It was difficult to structure the repository initially, but using a visual outline helped clarify the layout."
   - **Reflection Guiding Questions**:
     - What part of the planning phase was most challenging?
     - How did you approach organizing your repository for clarity and collaboration?
     - What did you learn about defining success criteria for your test scenarios?
     - How confident do you feel applying these skills to a real-world QA project?

   - **Common Mistakes to Avoid**:
     - Missing edge cases or vague success criteria.
     - Unclear folder or file organization in the repository.
     - Overcomplicating test plans with redundant scenarios.
     - Failing to review the test plan for consistency and completeness.

---

## **Key Learning Outcomes**

By the end of this week, you should achieve the following milestones:

- Understand how to scope and plan a comprehensive QA project.
- Gain experience organizing a professional repository for QA deliverables.
- Learn to define clear objectives and timelines for complex projects.

