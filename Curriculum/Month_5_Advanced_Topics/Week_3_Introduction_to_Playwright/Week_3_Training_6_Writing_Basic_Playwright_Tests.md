 # **Training 6: Writing Basic Playwright Tests**

## **Objective**

Teach students how to write and execute basic Playwright tests, including interacting with UI elements, validating outcomes using assertions, and debugging tests. This session will also introduce best practices for deciding when to create automated test cases versus using manual testing.

---

## **Free Online Resources** (Mandatory)

1. **[Playwright Official Documentation](https://playwright.dev/docs/intro)**
   - Comprehensive guide for writing and executing Playwright tests.
2. **[The Internet - Test Application](https://the-internet.herokuapp.com)**
   - A demo web application for practicing test scenarios.
3. **[What is Playwright? (YouTube)](https://www.youtube.com/watch?v=wGr5rz8WGCE)**
   - Beginner-friendly video on Playwright introduction tutorial, features & demo.
4. **[Introduction to Playwright for End-to-End Testing with Debbie O'Brien | JS Drops (YouTube)](https://www.youtube.com/watch?v=lCb9JoZFpHI)**
   - Learn how to get started with Playwright using the VS Code extension and easily generate tests with Playwright`s test generator.

---

## **Topics Covered**

### **1. Writing Basic Playwright Tests**

#### **Step 1: Setting Up a New Test File**

1. Open your Playwright project in VS Code.
2. Navigate to the `tests/` folder. This is where all test files are stored.
3. Create a new test file named `test-site.spec.ts`. This file will contain the custom tests you write.

#### **Step 2: Writing and Understanding Tests**

Let’s break down the process of writing basic Playwright tests step by step:

1. **Import Playwright**:

   ```typescript
   import { test, expect } from '@playwright/test';
   ```

   - `test`: Defines a test case with a name and its steps.
   - `expect`: Provides assertions to validate application behavior.

2. **Write a Valid Login Test**:

   ```typescript
   test('Login with valid credentials', async ({ page }) => {
       await page.goto('https://the-internet.herokuapp.com/login');
       await page.fill('#username', 'tomsmith');
       await page.fill('#password', 'SuperSecretPassword!');
       await page.click('button[type="submit"]');
       await expect(page.locator('#flash')).toContainText('You logged into a secure area!');
   });
   ```

   - **What it does**:
     - Navigates to the login page.
     - Inputs valid credentials.
     - Submits the form and checks for a success message.

3. **Write an Invalid Login Test**:

   ```typescript
   test('Login with invalid credentials', async ({ page }) => {
       await page.goto('https://the-internet.herokuapp.com/login');
       await page.fill('#username', 'invaliduser');
       await page.fill('#password', 'wrongpassword');
       await page.click('button[type="submit"]');
       await expect(page.locator('#flash')).toContainText('Your username is invalid!');
   });
   ```

   - **What it does**:
     - Navigates to the login page.
     - Inputs invalid credentials.
     - Submits the form and verifies an error message.

4. **Run the Tests**:

   - Open the terminal in VS Code (`Ctrl + ~` or `Cmd + ~`).
   - Execute the command:
     ```bash
     npx playwright test
     ```
   - Review the output for:
     - **Pass/Fail Results**: Indicates which tests succeeded or failed.
     - **Error Messages**: Details of any issues encountered.
     - **Summary**: Total tests run and their statuses.

---

### **2. When to Create Automated Test Cases**

1. **Scenarios for Automation**:

   - Repetitive tests: Useful for tasks that need frequent execution (e.g., login validation).
   - High-risk areas: Tests for critical application workflows.
   - Large datasets: Tests that involve multiple input variations.
   - Cross-browser compatibility: Ensuring functionality across multiple browsers.

2. **Scenarios for Manual Testing**:

   - Exploratory testing: When the focus is on discovering new issues.
   - Visual testing: Validating UI alignment or design consistency.
   - One-off scenarios: Features that don’t require repeated testing.

---

### **3. Debugging and Reporting**

#### **Debugging Tools**

1. **Scenario for Debugging**: Imagine a test fails because the "Login with valid credentials" test does not find the success message `You logged into a secure area!`. Here’s how to debug it step by step:

   - Add a `page.pause()` command right after navigating to the login page to observe what the browser is doing:
     ```typescript
     test('Debugging login failure', async ({ page }) => {
         await page.goto('https://the-internet.herokuapp.com/login');
         await page.pause();
         await page.fill('#username', 'tomsmith');
         await page.fill('#password', 'SuperSecretPassword!');
         await page.click('button[type="submit"]');
         await expect(page.locator('#flash')).toContainText('You logged into a secure area!');
     });
     ```
   - When the test runs, use the Playwright inspector to confirm that the page is loading correctly, fields are being filled, and the button is clicked.
   - Check if the success message element is present or if the locator `#flash` needs adjustment.

2. **Run Tests in Debug Mode**:

   - Use the `--debug` flag to launch the Playwright Inspector:
     ```bash
     npx playwright test --debug
     ```
   - Step through each action in the test, observing behavior and identifying where it deviates from expectations.

3. **Inspect Logs**:

   - Review logs in the terminal to find specific errors or unhandled exceptions.

#### **Reporting Test Results**

1. **Capture Screenshots for Failures**:

   - Add a screenshot command for failed tests:
     ```typescript
     await page.screenshot({ path: 'error-screenshot.png' });
     ```
   - Save screenshots in a `screenshots/` folder for review.

2. **Log Observations**:

   - Use `console.log` to print intermediate steps or variable values for additional insights during test execution.

3. **Push Results to GitHub**:

   - Ensure all screenshots and debug files are committed to the repository for reference.

---

## **Assignment**

**Objective:**
Write and execute Playwright tests on [The Internet](https://the-internet.herokuapp.com) to validate login functionality and dropdown interactions.

**Instructions:**

1. **Create and Write Tests:**
   - Create a new test file named `test-site.spec.ts` in the `tests/` folder.
   - Write two tests:
     - Test 1: Validate successful and failed logins on the Login page.
       - Use assertions to verify the success message "You logged into a secure area!" for valid credentials and the error message "Your username is invalid!" for invalid credentials.
     - Test 2: Interact with the Dropdown page.
       - Select options from the dropdown menu and use assertions to confirm that the selected option is displayed on the page.
       - Example: Verify that selecting "Option 1" updates the dropdown value correctly.
2. **Run the Tests:**
   - Execute the tests using:
     ```bash
     npx playwright test
     ```
   - Debug failing tests using `--debug` or `page.pause()`.
3. **Capture Results:**
   - Take a screenshot of the terminal output for successful tests.
   - Save screenshots for failed tests (if any) in a `screenshots/` folder.
4. **Organize Your Test Scripts:**
   - Use clear and descriptive test names for each test.
   - Group related tests into logical blocks to make the script easier to read and maintain.
   - Add comments explaining the purpose of each step in the test.
5. **Push Changes to GitHub:**
   - Add and commit your test scripts and screenshots:
     ```bash
     git add .
     git commit -m "Added Playwright tests for login and dropdown"
     git push origin main
     ```
6. **Submit Your Work:**
   - Share your GitHub repository link in the QA Academy Slack channel.

---

## **Submission Instructions**

1. Submit the link to your GitHub repository in the QA Academy Slack channel.
2. Ensure the repository includes:
   - Test scripts.
   - Screenshots of results.
   - A README file summarizing the tests performed.

---

## **Key Learning Outcomes**

By the end of this training, students will:

- Write and execute Playwright tests for basic web interactions.
- Debug and troubleshoot failing tests.
- Determine when to automate versus use manual testing.

---

## **Key Interview Questions**

1. How do you write a Playwright test to interact with UI elements?
2. What are assertions, and why are they important in testing?
3. When should you automate a test case versus performing it manually?
4. How can you debug failing Playwright tests effectively?

---

## **Tips for Success**

- Start simple: Focus on one functionality per test.
- Use Playwright’s debugging tools to identify issues step-by-step.
- Push changes to GitHub frequently to track your progress.

---

## **Next Training**

In **Training 8**, students will consolidate skills by combining test case creation, performance testing, and exploratory testing into a comprehensive project.

