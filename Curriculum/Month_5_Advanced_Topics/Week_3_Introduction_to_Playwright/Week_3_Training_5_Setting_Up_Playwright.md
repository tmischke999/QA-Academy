# **Training 5: Setting Up and Running Initial Playwright Tests**

## **Objective**
Introduce Playwright by guiding students through the installation and configuration of the framework, running initial tests, and integrating their projects with GitHub. By the end of this training, students will:

- Understand the purpose and key features of Playwright.
- Install and set up Playwright and its prerequisites.
- Execute sample Playwright scripts and interpret their results.
- Push their Playwright projects to GitHub for version control.

---

## **Free Online Resources (Mandatory)**

1. **[TypeScript vs JavaScript (YouTube)](https://www.youtube.com/watch?v=HCXPJmtV47I)**
   - Learn the key differences between TypeScript and JavaScript and why TypeScript is commonly used in Playwright projects.
2. **[Learn TypeScript - Full Course for Beginners (YouTube)](https://www.youtube.com/watch?v=SpwzRDUQ1GI)**
   - A beginner-friendly video that provides a complete introduction to TypeScript for those new to programming or transitioning from JavaScript.
3. **[Playwright Official Documentation](https://playwright.dev/)**
   - Comprehensive guide for setting up and using Playwright, including tutorials for writing tests and advanced configuration options.
   - [Writing Playwright tests](https://playwright.dev/docs/writing-tests)
4. **[GitHub Docs: Creating a Repository](https://docs.github.com/en/get-started/quickstart/create-a-repo)**
   - Step-by-step instructions for creating and managing repositories to organize your Playwright projects.
5. **[What is Playwright? (YouTube)](https://www.youtube.com/watch?v=wGr5rz8WGCE)**
   - Beginner-friendly introduction to Playwright’s features, including an overview of its capabilities for UI automation testing.
6. **[Getting Started with Playwright Testing](https://saucelabs.com/resources/blog/getting-started-with-playwright-testing)**
   - A blog post detailing how to set up and run Playwright tests effectively for both beginners and advanced users.
7. **[Playwright Testing Essentials: A Beginner's Guide](https://betterstack.com/community/guides/testing/playwright-intro/)**
   - A detailed guide for beginners covering the fundamentals of Playwright testing, including installation, writing tests, and debugging.

---

## **Topics Covered**

### **1. Introduction to Playwright**

- **Definition**: Playwright is a powerful open-source automation framework designed for end-to-end testing. It enables testers to perform automated interactions with modern web applications across multiple browsers.

- **Why Choose Playwright?**:

  - **Cross-Browser Testing**: Supports Chromium, Firefox, and WebKit, making it versatile for diverse testing needs.
  - **Parallel Execution**: Allows running multiple tests simultaneously to save time.
  - **Headless Mode**: Speeds up testing by running browsers without a UI.
  - **Rich API**: Provides an extensive library of commands to simulate user interactions like clicking, typing, and navigating.
  - **Automatic Waiting**: Playwright intelligently waits for elements to be ready before performing actions, reducing flaky tests.

- **Key Features**:

  - **Flexible Locators**: Identify and interact with elements using CSS selectors, XPath, or text.
  - **Built-in Reporters**: Generate reports for better test insights.
  - **Screenshot and Video Capabilities**: Capture screenshots or record videos for visual debugging.
  - **Testing on Mobile Devices**: Emulate mobile devices for responsive testing.

- **Use Cases**:

  - Functional and regression testing of web applications.
  - Testing complex workflows involving multiple steps and pages.
  - Simulating user interactions in real-world scenarios.

**Key Insight**: Playwright is ideal for modern QA workflows, offering comprehensive tools to test applications efficiently and effectively.

---

### **2. Setting Up Prerequisites**

#### **Step 1: Check Existing Installations**

Before proceeding, verify if the necessary tools are already installed:

1. **Node.js**:

   - Open the terminal and run:
     ```bash
     node -v
     npm -v
     ```
   - If versions are displayed, Node.js and npm are installed. If not, follow the installation steps below.

2. **VS Code**:

   - Open your applications and search for "Visual Studio Code."
   - If installed, ensure it launches correctly. If not, proceed to installation.

#### **Step 2: Install Missing Tools**

1. **Install Node.js**:

   - Download the LTS version from [Node.js](https://nodejs.org/en/).
   - Follow the installation wizard.
   - Verify the installation:
     ```bash
     node -v
     npm -v
     ```

2. **Install VS Code**:

   - Download from [VS Code](https://code.visualstudio.com/).
   - Complete the installation.

3. **Access Terminal**:

   - **Windows**: Use Command Prompt, PowerShell, or Git Bash.
   - **Mac/Linux**: Open the default terminal application.
   - **VS Code**: Press `Ctrl + ~` (Windows/Linux) or `Cmd + ~` (Mac).

4. **Enable Auto Save in VS Code**:

   - Navigate to **File > Auto Save** in the top menu of VS Code.
   - **Why this is useful**: Auto Save ensures that your changes are saved automatically, reducing the risk of losing unsaved work and maintaining consistency when switching between files or running tests.

---

### **3. Setting Up a New Playwright Project**

#### **Step 1: Cloning Your Repository**

- Open your terminal in **VS Code** by pressing:
  - `Ctrl + ~` (Windows/Linux)
  - `Cmd + ~` (Mac).
- Use the command below in the terminal within the VS Code interface to clone your repository. If you have a folder set up for QA Academy projects, navigate to that folder first using the `cd` command before running the clone command. For example:

```bash
cd path/to/QA-Academy-folder
```

```bash
   git clone <repository-url>
```

#### **Step 2: Initialize Playwright**

1. Navigate to the cloned repository:
   ```bash
   cd Playwright-Project
   ```
2. Initialize Playwright:
   ```bash
   npm init playwright@latest
   ```
3. Follow prompts to configure the project.

#### **Step 3: Verify Installation**

- Ensure the `tests/` folder and `playwright.config.ts` file are created.
- Run a sample test:
  ```bash
  npx playwright test
  ```

---

### **4. Running Sample Playwright Tests**

#### **Step 1: Open VS Code and Navigate to the Test File**

1. Launch **VS Code**.
2. Open the Playwright project folder by selecting **File > Open Folder** and navigating to the cloned repository.
3. Locate the `example.spec.ts` file within the `tests/` folder. This file is a default test script provided by Playwright to demonstrate basic functionality, such as navigating to a webpage and performing simple actions. You can use it to verify that your setup is working correctly.

#### **Step 2: Execute the Default Test Script**

1. Open the integrated terminal in VS Code by pressing:
   - `Ctrl + ~` (Windows/Linux)
   - `Cmd + ~` (Mac).
2. Run the test command:
   ```bash
   npx playwright test
   ```

#### **Step 3: Observe and Analyze the Output**

- **Pass/Fail Results**:
  - The terminal will display whether the test passed or failed.
- **Browser Actions**:
  - A browser window may open, showing the automated interactions.

#### **Step 4: Debugging Tips**

1. Add a pause to observe browser actions in your Playwright script. For example, locate the section in your `example.spec.ts` file where actions like navigation or form interactions occur. Insert the following line after navigating to a page or before an interaction step to pause the script and inspect browser behavior:
   ```typescript
   await page.pause();
   ```
2. Re-run the test and use the Playwright Inspector to examine step-by-step interactions.

---

### **5. Pushing Playwright Projects to GitHub**

1. **Stage and Commit Changes via Terminal in VS Code**:
   - Open the integrated terminal in VS Code by pressing `Ctrl + ~` (Windows/Linux) or `Cmd + ~` (Mac).
   - Use the following commands to stage and commit changes:
     ```bash
     git add .
     git commit -m "Initial Playwright setup"
     ```
2. Push to the main branch:
   ```bash
   git push origin main
   ```
3. Verify the repository on GitHub to ensure all files are uploaded.

---

## **Assignment**

### **Step-by-Step Instructions**

#### **1. Write a Custom Playwright Test**

1. **Create a New Test File**:

   - In your Playwright project folder, navigate to the `tests/` directory.
   - Create a new test file named `custom_test.spec.ts`.

2. **Write a Test Scenario**:

   - Open the `custom_test.spec.ts` file in VS Code.
   - Write a test that navigates to a webpage, performs a simple action (e.g., filling out a form or clicking a button), and verifies the result using assertions. Example:
     ```typescript
     import { test, expect } from '@playwright/test';

     test('Custom Test: Validate Page Title', async ({ page }) => {
         await page.goto('https://example.com');
         const title = await page.title();
         expect(title).toBe('Example Domain');
     });
     ```

3. **Modify the Existing **`example.spec.ts`** File**:

   - Add an additional test case to explore another scenario, such as validating a specific element’s visibility or text content.

#### **2. Execute the Custom Playwright Test**

1. **Run the Test**:

   - Open the integrated terminal in VS Code and execute:
     ```bash
     npx playwright test tests/custom_test.spec.ts
     ```
   - Observe the results and verify that the test passes successfully.

2. **Debug and Refine**:

   - If the test fails, use debugging techniques such as adding `await page.pause()` to observe browser behavior.

#### **3. Screenshots for Playwright Tests**

1. **Add Screenshot Capture to the Test**:

   - Include a line in your test to capture a screenshot upon successful execution:
     ```typescript
     await page.screenshot({ path: 'screenshots/custom_test.png' });
     ```

2. **Save Screenshots in a New Folder**:

   - Create a `screenshots/` folder in your project directory to store all screenshots.

#### **4. Update the README File**

1. **Describe Your Custom Test**:
   - Open the `README.md` file in your project.
   - Add a section explaining the purpose of the custom test, what it validates, and its expected outcome.

#### **5. Push Changes to GitHub**

1. **Stage and Commit Your Work via VS Code Source Control**:

   - Open the **Source Control** tab in VS Code (icon with three branches or press `Ctrl + Shift + G` / `Cmd + Shift + G`).
     - It is the branch icon on your left nav in VS Code. 
   - Enter a commit message in the text box (e.g., "Initial Playwright setup and default test execution").
   - Click the **plus icon** to stage a single change or stage all changes
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

4. **Stage and Commit Your Work**:

   - Use the following commands:
     ```bash
     git add .
     git commit -m "Added custom Playwright test and updated README"
     ```

5. **Push to GitHub**:

   - Push your changes to the main branch:
     ```bash
     git push origin main
     ```

6. **Verify Changes**:

   - Check your GitHub repository to ensure the new test file, screenshots, and updated README are visible.

#### **6. Submit Deliverables**

1. Share your GitHub repository link in the QA Academy Slack channel.

2. Ensure the repository includes:

   - The new `custom_test.spec.ts` file.
   - Screenshots captured during test execution.
   - An updated `README.md` file explaining the custom test.

---

## **Key Learning Outcomes**

- Install and configure Playwright and its prerequisites.
- Execute initial Playwright tests and interpret their results.
- Use GitHub for version control in QA projects.

---

## **Key Interview Questions**

1. What is Playwright, and why is it used in UI automation?
2. How do you set up a Playwright project from scratch?
3. What are the steps to push a project to GitHub?

---

## **Tips for Success**

- Follow the official documentation for troubleshooting setup issues.
- Use version control regularly to save progress.
- Take detailed notes on test execution and outcomes for your reflection.

---

## **Next Training**

In **Training 6**, students will learn how to write and execute basic Playwright tests, focusing on creating custom scripts and debugging test failures.

