# **Training 6: Setting Up Playwright**

## **Objective**
Introduce students to Playwright by guiding them step-by-step through the installation of prerequisite tools (Node.js, VS Code), verifying existing setups, creating a new GitHub repository, initializing a Playwright project, and running a sample test script.

---

## **Free Online Resources** (Mandatory)
1. **[Playwright Official Documentation](https://playwright.dev/)**  
   - Comprehensive guide to getting started with Playwright.
2. **[GitHub Docs: Creating a Repository](https://docs.github.com/en/get-started/quickstart/create-a-repo)**  
   - Step-by-step instructions for creating and managing GitHub repositories.
3. **[VS Code Beginner Tutorial (YouTube)](https://www.youtube.com/watch?v=WPqXP_kLzpo)**  
   - Beginner-friendly introduction to installing and using Visual Studio Code.
4. **[Installing Node.js (Node.js Official Guide)](https://nodejs.org/en/)**  
   - Instructions for downloading and setting up Node.js.
5. **[Bash Basics for Beginners (freeCodeCamp)](https://www.freecodecamp.org/news/bash-scripting-tutorial-linux-shell-script-and-command-line-for-beginners/)**  
   - Covers essential terminal commands.
6. **[Git Bash Introduction (YouTube)](https://www.youtube.com/watch?v=iGutIN5t9Mo)**  
   - Beginner-friendly tutorial on using Git Bash for Git commands.

---

## **Topics Covered**

### **1. What is Playwright?**
- **Definition**: Playwright is a framework for automating browsers to perform end-to-end testing.
- **Key Insight**: It supports cross-browser testing, robust automation, and efficient debugging.
- **Why Use Playwright?**  
  - Enables testing across Chromium, Firefox, and WebKit.
  - Provides an easy setup for end-to-end testing.

---

### **2. Setting Up Prerequisites**

#### **Step 1: Check for Node.js**
1. Open the command prompt (Windows) or terminal (Mac/Linux).
2. Run the command:
   ```bash
   node -v
   ```
3. If a version appears (e.g., `v16.14.2`), Node.js is installed. If not, proceed to installation.

#### **Step 2: Check for VS Code**
1. Open Start (Windows) or Applications (Mac) and search for “Visual Studio Code.”
2. If not installed, proceed to the installation instructions below.

#### **Step 3: Install Missing Tools**
1. **Install Node.js**:
   - Download the LTS version from the [Node.js website](https://nodejs.org/en/).
   - Follow the installer prompts.
   - Verify installation with `node -v`.
2. **Install VS Code**:
   - Download from the [VS Code website](https://code.visualstudio.com/).
   - Complete the installation and confirm it launches successfully.

#### **Step 4: Introduction to the Terminal**
1. **What is the Terminal (or Bash)?**
   - A command-line interface (CLI) used to interact with your computer by typing commands.
2. **Accessing the Terminal**:
   - **Windows**: Open the Start menu and type `cmd` to open Command Prompt. Alternatively, install Git Bash (covered in prior training).
   - **Mac**: Open Spotlight (`Cmd + Space`) and type `Terminal`.
   - **VS Code**: Press:
     - **Windows/Linux**: `Ctrl + ~`
     - **Mac**: `Cmd + ~`
3. **Basic Commands to Know**:
   - `cd`: Change directory.
   - `ls`: List files.
   - `mkdir`: Create a folder.
   - `pwd`: Show current directory.

---

### **3. Creating a New GitHub Repository**
1. Log into your GitHub account at [github.com](https://github.com).
2. Click the **+** icon in the top-right corner and select **New repository**.
3. Fill in the following details:
   - **Repository name**: `Playwright-Project`.
   - **Description**: Optional.
   - **Initialize with README**: Check this option.
4. Click **Create repository**.
5. Clone the repository locally:
   - Click the **Code** button in your repository.
   - Copy the HTTPS URL.
   - Open the terminal and run:
     ```bash
     git clone <repository-url>
     ```
     Replace `<repository-url>` with your repository’s URL.

---

### **4. Installing and Configuring Playwright**
1. Open the cloned repository folder in VS Code:
   - Use **File > Open Folder** and select the repository folder.
2. Initialize Playwright:
   ```bash
   npm init playwright@latest
   ```
   - Follow the prompts to configure the project, selecting defaults when unsure.
3. Verify setup:
   - Use `ls` to confirm the `tests/` folder and `playwright.config.ts` file were created.

---

### **5. Running a Sample Playwright Test**
1. Locate the default `example.spec.ts` file in the `tests/` folder.
2. Run the sample test:
   ```bash
   npx playwright test
   ```
3. Observe:
   - A browser opens and performs the automated actions from the script.
   - Review the terminal output for test results.

---

## **Assignment**

**Objective:**
Set up a Playwright project and integrate it with GitHub for version control.

**Instructions:**
1. Log in to GitHub and create a repository named `Playwright-Project`.
2. Clone the repository locally and set it up in VS Code.
3. Initialize Playwright in the repository folder.
4. Run the default Playwright test script and take a screenshot of the terminal output showing the test results.
5. Push all changes to your GitHub repository:
   - Stage and commit the files:
     ```bash
     git add .
     git commit -m "Initial setup for Playwright"
     ```
   - Push to GitHub:
     ```bash
     git push origin main
     ```
6. Save the terminal output screenshot as a PNG or JPG file (e.g., `test_results.png`) and place it in a folder named `screenshots/` within your project directory.
7. Stage and commit the screenshot to your repository:
   ```bash
   git add screenshots/test_results.png
   git commit -m "Added screenshot of test results"
   ```
8. Push the changes to your GitHub repository:
   ```bash
   git push origin main
   ```
9. Share your repository link in the QA Academy Slack channel.

---

## **Submission Instructions**
1. Submit the link to your GitHub repository in the QA Academy Slack channel.
2. Ensure the repository includes:
   - Playwright setup files.
   - README file.
   - Screenshot of the test results.

---

## **Key Learning Outcomes**
By the end of this training, students will:
- Create and manage a GitHub repository.
- Set up and configure Playwright in a version-controlled project.
- Execute a sample Playwright test and interpret its output.

---

## **Key Interview Questions**
1. How do you create a new repository on GitHub?
2. What are the steps to set up Playwright in an existing project?
3. How do you push changes to a remote GitHub repository?

---

## **Tips for Success**
- Familiarize yourself with basic terminal commands (`cd`, `ls`, `mkdir`).
- Use the provided resources for guidance and troubleshooting.
- Don’t hesitate to reach out on Slack for clarification or help.

---

## **Next Training**
In **Training 7**, students will learn to write their own Playwright tests, focusing on UI elements, assertions, and debugging techniques.

