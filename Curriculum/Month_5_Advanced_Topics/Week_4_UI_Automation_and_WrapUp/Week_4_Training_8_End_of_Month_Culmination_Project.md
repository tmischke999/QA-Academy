# **Month 5: Training 8 - Comprehensive Testing Project & Month Wrap-Up**

## **Objective**

Consolidate all skills learned during Month 5 into a practical project encompassing performance testing, exploratory testing, and UI automation using Playwright. Students will:

- Combine multiple testing techniques into a cohesive testing strategy.
- Produce portfolio-ready deliverables, including test results, scripts, and reports.
- Reflect on their Month 5 learning journey and prepare for the capstone project in Month 6.

By the end of this training, students will have confidence in applying advanced QA techniques and producing professional documentation.

---

## **Free Online Resources** (Mandatory)

1. **[Playwright Official Documentation](https://playwright.dev/docs/intro)**
   - Comprehensive guide for using Playwright.
2. **[How to Use Lighthouse for Performance Testing (Google Developers)](https://developers.google.com/web/tools/lighthouse)**
   - Step-by-step guide to running Lighthouse for performance audits.
3. **[Exploratory Testing Guide (Software Testing Help)](https://www.softwaretestinghelp.com/what-is-exploratory-testing/)**
   - Insights into exploratory testing techniques and documentation.
4. **[Google Sheets Beginner Tutorial (YouTube)](https://www.youtube.com/watch?v=G93P4DxryVE)**
   - Learn how to create charts and tables in Google Sheets for visualizing test results.

---

## **Topics Covered**

### **1. Comprehensive Testing Project**

#### **Step 1: Test Planning**
- **Define Scope and Objectives**:
  - Choose a website or application for testing (e.g., [The Internet](https://the-internet.herokuapp.com)).
  - Identify key areas for testing:
    - Performance (e.g., page load speed, response times).
    - Exploratory (e.g., edge cases in form inputs).
    - UI Automation (e.g., validating button clicks, dropdown selections).

- **Prepare Test Scenarios**:
  - Example scenarios:
    - Performance: Measure the page load time for the login page.
    - Exploratory: Test invalid inputs in the login form.
    - UI Automation: Verify the dropdown menu updates correctly.

#### **Step 2: Test Execution**

1. **Performance Testing with Lighthouse**:
   - Open Chrome DevTools (Right-click > Inspect > "Lighthouse" tab).
   - Run an audit for performance metrics (e.g., First Contentful Paint, Speed Index).
   - Save the results as a PDF report.

2. **Exploratory Testing**:
   - Use the login form on [The Internet](https://the-internet.herokuapp.com/login):
     - Input invalid credentials and note the error messages.
     - Attempt multiple failed logins to check for account lockout.
   - Document findings in a checklist:
     - Example: "Entering a blank username shows 'Username is required' error."

3. **UI Automation with Playwright**:
   - Write and execute tests for dropdown functionality:
     ```typescript
     test('Dropdown option selection', async ({ page }) => {
         await page.goto('https://the-internet.herokuapp.com/dropdown');
         await page.selectOption('#dropdown', '1');
         const selectedOption = await page.locator('#dropdown option:checked').textContent();
         expect(selectedOption).toBe('Option 1');
     });
     ```
   - Ensure scripts are functional and results are logged.

#### **Step 3: Test Analysis**

1. **Review Results**:
   - Analyze Lighthouse scores for key metrics.
   - Reflect on exploratory testing findings and identify edge cases.
   - Review Playwright test logs and screenshots for errors.

2. **Create Visual Aids in Google Sheets**:
   - Create a pie chart showing performance scores (e.g., Excellent, Good, Needs Improvement).
   - Use bar charts to display response times for different pages.

#### **Step 4: Documentation**

1. **Create a Professional Test Summary Report**:
   - **Include**:
     - Executive Summary
     - Test Objectives
     - Key Findings (Performance, Exploratory, Automation)
     - Risks and Recommendations
     - Visual Aids

2. **Structure the Report**:
   - Use headings, bullet points, and charts for clarity.
   - Example: "Performance testing revealed a slow Speed Index of 4.2 seconds on the login page. Recommendation: Optimize image sizes and use lazy loading."

---

### **2. Month 5 Reflection and Wrap-Up**

#### **Reflection Document**

Write a reflection document summarizing:
- Key takeaways from Month 5.
- Challenges faced and how they were overcome.
- Practical applications of the skills learned.

**Guiding Questions**:
- What testing technique did you find most valuable?
- How did you approach debugging automation scripts?
- How confident do you feel applying these skills in a real-world QA role?

#### **Preparation for Month 6**

- **Checklist**:
  - [ ] Ensure all project deliverables are completed and submitted.
  - [ ] Review Playwright documentation for advanced scripting techniques.
  - [ ] Prepare for capstone project planning and execution.

- **Preview**:
  - Focus on capstone project development and career preparation.
  - Mock interviews and resume reviews.

---

## **Assignment**

### **Part 1: Comprehensive Testing Project**

1. **Plan**:
   - Create a test plan detailing performance, exploratory, and UI automation scenarios.
2. **Execute**:
   - Perform performance audits, exploratory tests, and UI automation scripts.
3. **Analyze**:
   - Summarize findings in visual aids (e.g., charts, tables).
4. **Document**:
   - Write a professional test summary report.

### **Part 2: Submission**

- Submit the following by sharing your GitHub repository link in the designated Slack channel. Ensure your repository includes:
  - Test plan (PDF format).
  - Test summary report (PDF format).
  - Visual aids and automation logs (zipped folder).
  - Reflection document (Google Doc link).
  - Playwright automation scripts, committed to the repository.

#### **Steps for Adding PDFs to the Repository**

1. **Save Deliverables Locally**:
   - Save all required files (e.g., test plan, summary report) as PDFs.

2. **Organize Files**:
   - Create a folder in your repository (e.g., `docs/`) to store all PDFs and other documents.

3. **Add Files to the Repository**:
   - Move the PDF files into the `docs/` folder.

4. **Stage and Commit the Files**:
   - Use the following commands to add the files to your repository:
     ```bash
     git add docs/
     git commit -m "Added documentation PDFs"
     ```

5. **Push Changes to GitHub**:
   - Push the updates to the repository:
     ```bash
     git push origin main
     ```

---

## **Key Learning Outcomes**

- Integrate performance, exploratory, and UI automation testing into a cohesive strategy.
- Produce professional, portfolio-ready deliverables.
- Reflect on progress and prepare for capstone challenges.

---

## **Preparing for Month 6**

- **Checklist**:
  - [ ] Ensure all project deliverables are completed and submitted.
  - [ ] Review Playwright documentation for advanced scripting techniques.
  - [ ] Reflect on Month 5 accomplishments and challenges.
  - [ ] Prepare for capstone project planning and execution.

- **Preview of Month 6**:
  - Focus on capstone project development, showcasing a comprehensive test plan, and applying all skills learned throughout the QA Academy.
  - Career preparation activities, including resume building and mock interviews.

---

## **Congratulations on Completing Month 5!**

You’ve reached another significant milestone in your QA Academy journey. This month, you successfully combined performance, exploratory, and UI automation testing into a cohesive project. You’ve also demonstrated the ability to produce professional, portfolio-ready deliverables that showcase your expertise.

Take a moment to reflect on how far you’ve come and how these skills align with real-world QA practices. As you prepare for Month 6, approach the capstone project with confidence, knowing you’ve built a strong foundation. Great work on reaching this milestone, and keep striving toward your QA goals!

