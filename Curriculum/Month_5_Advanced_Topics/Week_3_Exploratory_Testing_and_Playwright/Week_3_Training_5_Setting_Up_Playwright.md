# **Training 5: Setting Up and Running Initial Playwright Tests**

## **Objective**

Introduce Playwright by guiding students through the installation and configuration of the framework, running initial tests, and integrating their projects with GitHub. By the end of this training, students will:

- Understand the purpose and key features of Playwright.
- Install and set up Playwright and its prerequisites.
- Execute sample Playwright scripts and interpret their results.
- Push their Playwright projects to GitHub for version control.

---

## **Free Online Resources (Mandatory)**

1. **[Playwright Official Documentation](https://playwright.dev/)**  
   - Comprehensive guide to getting started with Playwright.
2. **[GitHub Docs: Creating a Repository](https://docs.github.com/en/get-started/quickstart/create-a-repo)**  
   - Instructions for creating and managing GitHub repositories.
3. **[Installing Node.js (Node.js Official Guide)](https://nodejs.org/en/)**  
   - Steps for downloading and setting up Node.js.
4. **[What is Playwright? (YouTube)](https://www.youtube.com/watch?v=wGr5rz8WGCE)**  
   - Beginner-friendly video introducing Playwright's features and demos.

---

## **Topics Covered**

### **1. Introduction to Playwright**
- **Definition**: Playwright is a framework for end-to-end testing, enabling automated browser interactions.
- **Key Features**:
  - Cross-browser testing for Chromium, Firefox, and WebKit.
  - Supports parallel and headless execution.
  - Easy debugging with built-in tools.

**Key Insight**: Playwright is ideal for modern web applications, offering robust automation capabilities for QA professionals.

---

### **2. Setting Up Prerequisites**

#### **Step 1: Install Node.js**
1. Download the LTS version from [Node.js](https://nodejs.org/en/).
2. Follow the installation wizard.
3. Verify the installation:
   ```bash
   node -v
   npm -v
   ```

#### **Step 2: Install VS Code**
1. Download from [VS Code](https://code.visualstudio.com/).
2. Complete the installation.

#### **Step 3: Access Terminal**
- **Windows**: Use Command Prompt, PowerShell, or Git Bash.
- **Mac/Linux**: Open the default terminal application.
- **VS Code**: Press `Ctrl + ~` (Windows/Linux) or `Cmd + ~` (Mac).

---

### **3. Setting Up a New Playwright Project**

#### **Step 1: Create a GitHub Repository**
1. Log into [GitHub](https://github.com).
2. Click the **+** icon and select **New repository**.
3. Name it `Playwright-Project` and initialize it with a README.
4. Clone the repository:
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
1. Locate the `example.spec.ts` file in the `tests/` folder.
2. Execute the default test script:
   ```bash
   npx playwright test
   ```
3. Observe the terminal output:
   - **Pass/Fail Results**: Displays the success or failure of tests.
   - **Browser Actions**: Visual feedback from test execution.

4. Debug if necessary:
   - Add `await page.pause()` to observe interactions in real-time.

---

### **5. Pushing Playwright Projects to GitHub**
1. Stage and commit changes:
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

1. **Set Up a Playwright Project**:
   - Complete the installation and initialization steps.
   - Execute the default Playwright test script.

2. **Push Your Work to GitHub**:
   - Commit and push all project files.

3. **Submit Deliverables**:
   - Share your GitHub repository link in the QA Academy Slack channel.
   - Ensure the repository includes:
     - Playwright setup files.
     - A README file summarizing the project.
     - Logs/screenshots of the initial test resultGs.

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

