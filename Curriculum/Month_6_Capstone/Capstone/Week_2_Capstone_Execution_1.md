# **Week 2: Capstone Execution (Part 1)**

## **Objective**

Begin executing the capstone project by applying manual, exploratory, and accessibility testing techniques to uncover usability issues, validate WCAG compliance, and identify gaps in test coverage. This phase emphasizes hands-on testing to produce actionable findings and improve application quality.

---

## **Free Online Resources** (Optional)

1. **[Exploratory Testing Explained (Ministry of Testing)](https://www.ministryoftesting.com/articles/what-is-exploratory-testing-an-alternative-to-scripted-testing-and-try-to-break-it-testing)**

   - Beginner-friendly tutorial on exploratory testing techniques.

2. **[Accessibility Testing with Axe (Deque)](https://www.deque.com/axe/)**

   - Guide on using Axe to identify and resolve accessibility issues.

3. **[Lighthouse Accessibility Audits (Google Developers)](https://developers.google.com/web/tools/lighthouse)**

   - Instructions for running accessibility audits with Lighthouse.

4. **[NVDA Screen Reader Guide (WebAIM)](https://webaim.org/articles/nvda/)**

   - Detailed guide on using NVDA for screen reader compatibility testing.

5. **Review Prior Resources**:

   - Students are encouraged to revisit earlier materials on:
     - Writing test cases (Month 2).
     - Comprehensive test reports (Month 4).

---

## **Focus**

1. **Execute Manual Test Cases**:

   - Perform the manual test cases created in Week 1 for core features:
     - Login functionality.
     - Dropdown interactions.
     - Form validation.
   - Record results for each test case:
     - Pass/fail outcomes.
     - Any issues encountered, with details like steps to reproduce and screenshots.

2. **Perform Exploratory Testing**:

   - Identify potential gaps in test coverage by exploring:
     - Edge cases and unexpected user behaviors.
     - Scenarios not covered by existing test cases.
   - Use exploratory testing techniques such as:
     - Session-based testing: Time-boxed testing with clear objectives.
     - Heuristics-based testing: Using guidelines like SFDPOT (Structure, Function, Data, Platform, Operations, Time).

3. **Conduct Accessibility Audits**:

   - Use tools like Axe, Lighthouse, and NVDA to test for:
     - WCAG compliance.
     - Keyboard navigation.
     - Screen reader compatibility.
   - Document findings for each tool:
     - Example: "Axe identified missing ARIA labels on form inputs."
     - Example: "NVDA did not announce error messages for invalid form inputs."

4. **Document Findings and Recommendations**:

   - Summarize manual and exploratory testing results:
     - List key findings, such as uncovered edge cases or usability issues.
     - Provide screenshots or logs where applicable.
   - Create an accessibility testing report:
     - Use a structured format including issue descriptions, severity, and recommendations.

---

## **Step-by-Step Instructions**

### **1. Execute Your Manual Test Cases**

- Use the manual test cases created in Week 1 for core features:
  - Login functionality.
  - Dropdown interactions.
  - Form validation.
- Document outcomes for each test case:
  - Pass/fail results.
  - Any issues encountered, including steps to reproduce and screenshots.

### **2. Execute Your Exploratory Testing Plan**

- Use the exploratory testing objectives and scenarios defined in your Week 1 capstone planning document.

- Follow the planned time limits for each session (e.g., 30 minutes).

- Document outcomes for each scenario:

  - Scenarios tested.
  - Observations and issues encountered.
  - Suggested improvements or additional test cases to explore.

### **3. Conduct Accessibility Audits**

1. **Run Axe Audits**:

   - Install the Axe browser extension.
   - Navigate to the chosen application (e.g., [The Internet](https://the-internet.herokuapp.com)).
   - Run an audit by clicking the "Analyze" button.
   - Document identified issues:
     - Missing labels, low contrast, or ARIA violations.

2. **Use Lighthouse for Accessibility**:

   - Open Chrome DevTools > Lighthouse tab.
   - Select "Accessibility" and run the audit.
   - Save the report as a PDF and note key metrics such as contrast issues or missing labels.

3. **Test with NVDA**:

   - Enable NVDA and navigate the application.
   - Test critical paths (e.g., logging in, submitting forms) while listening for screen reader feedback.
   - Note any issues with announcements, focus order, or error message accessibility.

### **4. Document Your Findings**

1. **Bug Reporting Skills**:

   - Write clear and actionable bug reports using the following format:
     | Field                  | Example                                          |
     | ---------------------- | ------------------------------------------------ |
     | **Title**              | Error message not displayed for invalid password |
     | **Steps to Reproduce** | 1. Navigate to the login page.                   |

2. Enter a valid username and an invalid password.

3. Click the "Login" button. |
   \| **Expected Result** | An error message should display.             |
   \| **Actual Result**   | No error message displayed.                  |
   \| **Severity**        | High                                         |
   \| **Priority**        | Medium                                       |
   \| **Supporting Evidence** | Include screenshots or logs.               |

4. **Defect Tracking**:

   - Use defect tracking tools like Jira or Trello if available.
   - Alternatively, create a simple bug log in Google Sheets with the following columns:
     - Bug ID
     - Title
     - Steps to Reproduce
     - Status (Open, In Progress, Closed)
     - Assigned to
     - Supporting Evidence

5. **Real-World Examples**:

   - Exploratory Testing: Test login functionality for brute force attempts to ensure security.
   - Accessibility Testing: Verify WCAG compliance for high-traffic e-commerce websites to ensure usability for all users.

6. **Exploratory Testing Report**:

   - Use a structured format:
     - Feature tested.
     - Scenarios explored.
     - Observations and outcomes.
     - Recommendations.
   - Example:
     ```plaintext
     Feature: Login Functionality
     Scenario: Enter invalid credentials with special characters.
     Observation: The application displayed a generic error message.
     Recommendation: Provide specific feedback for invalid inputs.
     ```

7. **Accessibility Testing Report**:

   - Include a summary of findings for each tool used (Axe, Lighthouse, NVDA).
   - Document each issue with:
     - Description.
     - Severity (e.g., critical, moderate, minor).
     - Recommendation for improvement.
   - Example:
     ```plaintext
     Tool: Axe
     Issue: Missing ARIA labels on form inputs.
     Severity: Critical
     Recommendation: Add ARIA labels to all required fields.
     ```

---

## **Assignment**

Complete the following tasks to demonstrate your understanding of manual, exploratory, and accessibility testing:

1. **Manual Testing**:

   - Execute the manual test cases created in Week 1.
   - Document pass/fail outcomes and any issues encountered.

2. **Exploratory Testing**:

   - Perform at least two exploratory testing sessions on your chosen application.
   - Document findings in an exploratory testing report.

3. **Accessibility Testing**:

   - Run accessibility audits using Axe, Lighthouse, and NVDA.
   - Document findings in an accessibility testing report.

4. **Submit Work**:

   - Share the link to your GitHub repository in the QA Academy Slack channel.
   - Ensure the repository includes:
     - Exploratory testing report in the `docs/` folder.
     - Accessibility testing report in the `docs/` folder.
     - Bug log or examples of bug reports.
   - Include a reflection in your `README.md` addressing:
     - What challenges did you face executing the manual test cases?
     - How did exploratory testing complement the manual test cases?
     - What were the most critical findings from your accessibility audits?
     - How did writing and organizing bug reports improve your QA process?

5. **Common Mistakes to Avoid**:

   - Missing edge cases or vague success criteria.
   - Unclear bug descriptions or insufficient evidence.
   - Failing to document accessibility testing steps and results.
   - Not using a structured approach for exploratory testing.

---

## **Key Learning Outcomes**

- Understand how to identify gaps in test coverage through exploratory testing.
- Perform comprehensive accessibility audits using multiple tools.
- Write actionable bug reports and maintain an organized defect log.
- Gain insight into how manual, exploratory, and accessibility testing align with real-world QA scenarios.
- Develop communication skills for writing reports, collaborating with stakeholders, and documenting findings effectively.

