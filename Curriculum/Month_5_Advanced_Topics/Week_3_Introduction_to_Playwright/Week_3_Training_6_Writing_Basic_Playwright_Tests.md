# **Training 6: Writing and Structuring Basic Playwright Tests**

## **Objective**

Provide students with a structured approach to testing with Playwright. This training will teach how to write and structure Playwright tests effectively, what to test, what not to test, and best practices for organizing test files and debugging. By the end of this training, students will:

- Understand how to write basic Playwright tests.
- Learn best practices for structuring test folders and files.
- Identify appropriate test cases for automation.
- Gain foundational debugging skills in Playwright.

---

## **Free Online Resources (Mandatory)**

1. **[Playwright Official Documentation](https://playwright.dev/docs/intro)**
   - A comprehensive guide for writing and organizing Playwright tests.
   - [Writing Playwright Tests](https://playwright.dev/docs/writing-tests)
2. **[Best Practices for Playwright](https://playwright.dev/docs/best-practices)**
   - Best practices for structuring test folders and files.
3. **[Debugging Tests with Playwright](https://playwright.dev/docs/debug)**
   - A guide to using Playwright's debugging tools effectively.
4. **[The Internet - Test Application](https://the-internet.herokuapp.com)**
   - A demo application to practice various test scenarios.
5. **[Playwright Assertions Guide](https://playwright.dev/docs/assertions)**
   - Detailed documentation on using assertions in Playwright.
6. **[How to Organize Your Test Project (YouTube)](https://www.youtube.com/watch?v=2E-h-cdHjEQ)**
   - A video tutorial on structuring a Playwright project.

---

## **Topics Covered**

### **1. Writing Basic Playwright Tests**

#### **Step 1: Key Components of a Playwright Test**

- **Test Description**: Use meaningful names for test cases.
- **Page Navigation**: Ensure the page is fully loaded before performing actions.
- **Assertions**: Verify outcomes using clear and specific assertions.

#### **Step 2: Writing Simple Tests**

- Start with simple functionality like navigation and text validation:
  ```typescript
  import { test, expect } from '@playwright/test';

  test('Verify Example Page Title', async ({ page }) => {
      await page.goto('https://example.com');
      const title = await page.title();
      expect(title).toBe('Example Domain');
  });
  ```

#### **Step 3: Adding More Assertions**

- Validate element visibility and content:
  ```typescript
  const header = await page.locator('h1');
  await expect(header).toBeVisible();
  const paragraph = await page.locator('p');
  await expect(paragraph).toContainText('Example Domain');
  ```

---

### **2. Structuring Playwright Test Projects**

#### **Step 1: Folder Organization**

1. Use a clear and consistent structure:

   ```
   tests/
     ├── login/
     │   ├── valid_login.spec.ts
     │   └── invalid_login.spec.ts
     ├── navigation/
     │   └── homepage_navigation.spec.ts
     └── utils/
         └── helpers.ts
   ```

2. **Best Practices**:

   - Group tests by functionality or feature.
   - Use a `utils/` folder for reusable code (e.g., helper functions).

#### **Step 2: Configuration File**

1. Update `playwright.config.ts` for organization and performance:
   ```typescript
   import { defineConfig } from '@playwright/test';

   export default defineConfig({
       testDir: './tests',
       retries: 1,
       use: {
           headless: true,
           baseURL: 'https://example.com',
           actionTimeout: 10000,
           viewport: { width: 1280, height: 720 },
       },
   });
   ```

---

### **3. What to Test and What Not to Test**

#### **Step 1: What to Test**

1. **Critical User Flows**:

   - Login workflows (both valid and invalid credentials).
   - Checkout processes for e-commerce platforms.
   - Form submissions (e.g., contact forms or sign-ups).

2. **Repetitive and High-Risk Areas**:

   - Regression testing: Ensuring recent code changes haven’t introduced new bugs.
   - Critical application workflows that must function reliably.

3. **Cross-Browser and Device Compatibility**:

   - Tests to ensure functionality across different browsers (e.g., Chrome, Firefox, Safari).
   - Testing responsiveness on desktop, tablet, and mobile devices.

4. **Performance-Impacting Features**:

   - Validating loading times for key pages or interactions.
   - Ensuring large datasets are processed or rendered correctly.

#### **Step 2: What Not to Test**

1. **Non-Deterministic Behavior**:

   - Animations or transitions that are difficult to verify programmatically.
   - Randomized content (e.g., advertisements).

2. **Visual and Aesthetic Changes**:

   - Exact pixel-perfect alignments (best handled by visual regression tools).
   - Testing colors or font changes unless tied to accessibility.

3. **Rapidly Changing Features**:

   - Elements undergoing frequent UI updates.
   - Experimental features that are still in early development.

4. **Low-Risk Areas**:

   - Static pages with no user interaction.
   - Rarely used edge-case scenarios unless critical to functionality.

**Key Insight**: Focus on high-impact, stable areas where automated testing will provide the most value, and leave aesthetic or experimental testing for manual or specialized tools.

---

### **4. Debugging Playwright Tests**

#### **Step 1: Debugging Tools**

1. **Inspector Mode**:

   - Run tests in debug mode to open the Playwright Inspector and step through each action interactively:
     ```bash
     npx playwright test --debug
     ```
   - The Inspector allows you to pause, step over actions, and view logs for each step in real-time.

2. **Pause for Inspection**:

   - Insert pauses into your test script to interact with the page manually:
     ```typescript
     await page.pause();
     ```
   - Useful for visually verifying the page state at a specific point in the test.

3. **Capture Screenshots for Failing Tests**:

   - Use screenshots to understand failures visually:
     ```typescript
     await page.screenshot({ path: 'error.png' });
     ```
   - Save all failure screenshots in a dedicated folder (e.g., `screenshots/`) for organized debugging.

#### **Step 2: Using Trace Viewer**

1. **Enable Tracing**:

   - Enable trace recording to capture the entire test execution:
     ```typescript
     await context.tracing.start({ snapshots: true, screenshots: true });
     await page.goto('https://example.com');
     await context.tracing.stop({ path: 'trace.zip' });
     ```
   - The trace file provides detailed insights into all actions, including element locators, network requests, and timing data.

2. **Review Traces**:

   - Open the trace file using the Playwright Trace Viewer:
     ```bash
     npx playwright show-trace trace.zip
     ```
   - Inspect each step in the test, view screenshots, and analyze logs for failures.

#### **Step 3: Leveraging Logs and Debugging Outputs**

1. **Console Logs**:

   - Add `console.log` statements to track variable values or actions:
     ```typescript
     console.log('Current URL:', await page.url());
     ```
   - Review terminal output during test execution for additional context.

2. **Network and Request Logs**:

   - Monitor network requests to ensure proper API calls and responses:
     ```typescript
     page.on('response', response => console.log(`Response: ${response.url()} -> ${response.status()}`));
     ```

3. **Playwright Debug Mode with VS Code**:

   - Use VS Code’s built-in debugger with Playwright by configuring a `launch.json` file. This allows breakpoint-based debugging for seamless troubleshooting.

#### **Step 4: Common Debugging Scenarios**

1. **Element Not Found**:

   - Check if the selector is correct by inspecting the DOM.
   - Use Playwright’s `page.locator()` to validate the element’s visibility or existence:
     ```typescript
     await expect(page.locator('selector')).toBeVisible();
     ```

2. **Timeout Errors**:

   - Increase the timeout for actions to account for slower network or rendering times:
     ```typescript
     await page.waitForSelector('selector', { timeout: 10000 });
     ```

3. **Flaky Tests**:

   - Use retries to re-run failing tests automatically:
     ```typescript
     test('Flaky Test', async ({ page }) => {
         await page.goto('https://example.com');
         // Add retry logic
     }, { retries: 2 });
     ```

**Key Insight**: Debugging is an iterative process. Combine tools like Inspector, logs, and trace viewer to pinpoint issues efficiently.

---

## **Assignment**

### **Step-by-Step Instructions**

#### **Step 1: Setting Up the Project**

1. **Prepare Folder Structure**:
   - Navigate to your project folder.
   - Create a new folder `tests/login` to store test scripts.
2. **Add New Test Files**:
   - Create two files inside `tests/login/`:
     - `valid_login.spec.ts`
     - `invalid_login.spec.ts`

#### **Step 2: Writing Tests**

1. **Create Tests for Common Scenarios**:

   - Write tests for the following scenarios using the [The Internet - Test Application](https://the-internet.herokuapp.com):
     - **Valid Login Test**:
       - Test the Basic Auth functionality at [Login Page](https://the-internet.herokuapp.com/login) to validate proper credentials are required to access a secured page. Test successful login using valid credentials (`tomsmith` and `SuperSecretPassword!`).
     - **Invalid Login Test**:
       - Test invalid login attempts at [Login Page](https://the-internet.herokuapp.com/login) by entering incorrect username and password combinations to ensure proper error messages are displayed. Test invalid login by entering incorrect username and password combinations.
     - **Dropdown Interaction Test**:
       - Test the Dropdown functionality at [Dropdown Page](https://the-internet.herokuapp.com/dropdown) by selecting `Option 1` and ensuring the selected value displays correctly.
       - Validate dropdown menu selection by selecting `Option 1` and ensuring it displays correctly.
     - **Checkbox Selection Test**:
       - Test the Checkbox functionality at [Checkbox Page](https://the-internet.herokuapp.com/checkboxes) by selecting and unselecting each checkbox and validating their states. Test checking and unchecking both checkboxes and validate their state.
     - **Add/Remove Elements Test**:
       - Test the Add/Remove Elements functionality at [Dynamic Controls Page](https://the-internet.herokuapp.com/dynamic_controls) by adding an element, validating their presence, and then removing them to ensure proper functionality. Add additional tests for enable/disabling elements and validate their presence.
     - **Hover Test**:
       - Test the Hover functionality at [Hover Page](https://the-internet.herokuapp.com/hovers) by hovering over each image and ensuring the additional information is displayed correctly. over images on the Hover page and ensure additional information is displayed.

2. **Write Valid Login Test**:

   - Open `valid_login.spec.ts` in VS Code.
   - Add the following test to validate successful login:
     ```typescript
     import { test, expect } from '@playwright/test';

     test('Valid Login', async ({ page }) => {
         await page.goto('https://the-internet.herokuapp.com/login');
         await page.fill('#username', 'tomsmith');
         await page.fill('#password', 'SuperSecretPassword!');
         await page.click('button[type="submit"]');
         await expect(page.locator('#flash')).toContainText('You logged into a secure area!');
     });
     ```

3. **Write Invalid Login Test**:

   - Open `invalid_login.spec.ts` in VS Code.
   - Add the following test to validate error messages for invalid credentials:
     ```typescript
     import { test, expect } from '@playwright/test';

     test('Invalid Login', async ({ page }) => {
         await page.goto('https://the-internet.herokuapp.com/login');
         await page.fill('#username', 'invalidUser');
         await page.fill('#password', 'wrongPassword');
         await page.click('button[type="submit"]');
         await expect(page.locator('#flash')).toContainText('Your username is invalid!');
     });
     ```

#### **Step 3: Writing Remaining Tests**

1. **Write Additional Test Cases for Common Scenarios**:

   - Using the provided links to [The Internet - Test Application](https://the-internet.herokuapp.com), create and implement the following tests:
     - **Dropdown Interaction Test**:
       - Validate the functionality of the dropdown menu.
       - Example: Select `Option 1` and ensure the correct value displays.
     - **Checkbox Selection Test**:
       - Test checking and unchecking both checkboxes.
       - Validate their states to ensure correct functionality.
     - **Add/Remove Elements Test**:
       - Add an element and validate their presence.Remove element and ensure proper functionality.
       - Enable an element and validate proper functionality.Disable element and ensure functionality.
     - **Hover Test**:
       - Hover over images on the Hover page and validate that additional information is displayed.

2. **Structure and Save Tests**:

   - Store each test in its respective feature folder under `tests/` (e.g., `tests/dropdown`, `tests/checkbox`, etc.).
   - Include descriptive comments explaining the purpose of each step.

3. **Run and Validate All Tests**:

   - Execute each test script individually to ensure they function as expected:
     ```bash
     npx playwright test tests/<folder>/<test_file>.spec.ts
     ```

#### **Step 4: Debugging and Refining**

1. **Run Tests in Debug Mode**:
   - Use the Playwright Inspector to debug your tests:
     ```bash
     npx playwright test --debug
     ```
2. **Capture Screenshots for Failures**:
   - Update your test to take screenshots for failing steps:
     ```typescript
     if (!(await page.locator('#flash').isVisible())) {
         await page.screenshot({ path: 'screenshots/error.png' });
     }
     ```
3. **Inspect Logs and Fix Issues**:
   - Add `console.log` to track the execution of your tests.
   - Use the trace viewer if needed to identify specific issues.

#### **Step 5: Push Changes to GitHub**

1. **Stage and Commit Your Work via VS Code Source Control**:

   - Open the **Source Control** tab in VS Code (icon with three branches or press `Ctrl + Shift + G` / `Cmd + Shift + G`).
     - It is the branch icon on your left nav in VS Code.
   - Enter a commit message in the text box (e.g., "Initial Playwright setup and default test execution").
   - Click the **plus icon** to stage a single change or stage all changes.
   - Click the **checkmark icon** or **Commit button** to commit your changes.

2. **Push Your Changes via VS Code**:

   - After committing, click the **Sync Changes button** in the Source Control tab.
   - Verify that your changes are pushed to your GitHub repository.

3. **Stage, Commit, and Push via Command Line** (alternative):

   - Use the following commands in the terminal:
     ```bash
     git add .
     git commit -m "Initial Playwright setup and default test execution"
     git push origin main
     ```

4. **Verify Changes**:

   - Check your GitHub repository to ensure the new test file, screenshots, and updated README are visible.

#### **Step 6: Submit Deliverables**

1. **Review Repository**:
   - Ensure all test scripts and folders are properly structured.
   - Verify that screenshots are saved in the appropriate folder.
2. **Share Link**:
   - Post your GitHub repository link in the QA Academy Slack channel for feedback.

---

## **Key Learning Outcomes**

- Write structured and meaningful Playwright tests.
- Organize test projects effectively.
- Debug and troubleshoot Playwright tests using built-in tools.
- Differentiate between test cases suitable for automation and those better suited for manual testing.

---

## **Key Interview Questions**

1. How do you structure test folders and files in a Playwright project?
2. What are the best practices for writing Playwright tests?
3. How do you debug a failing Playwright test?
4. What types of test scenarios should not be automated?

---

## **Tips for Success**

- Focus on structuring tests for readability and maintainability.
- Use comments to document the purpose of each test.
- Test incrementally and debug often to identify issues early.
- Regularly commit changes to GitHub for version control.

---

## **Next Training**

In **Training 7**, students will learn to create reusable test components, integrate test data files for dynamic testing, and configure basic cross-browser setups.

