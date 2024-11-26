# Week 3: Training 6 - Introduction to Bug Tracking and Version Control with GitHub (Part 1)

## Objective
Introduce students to bug tracking with Jira and foundational version control concepts using Git and GitHub. By the end of this training, students will:
- Understand how bug tracking tools like Jira are used in QA workflows.
- Learn the basics of Git and GitHub for version control.
- Download and install Git, configure Git for use with GitHub, clone the QA Academy repository, add saved documents from Google Drive, and set up their personal GitHub repository.

---

## Free Online Resources
- [Difference Between Severity and Priority in Testing]()
- [Introduction to Bug Tracking with Jira](https://www.atlassian.com/software/jira/guides)
- [How to use Jira](https://www.youtube.com/watch?v=qi5zLHdOytI)
- [How to work with Bugs in Jira](https://www.youtube.com/watch?v=X-UeAjryCAw)
- [Git Basics](https://git-scm.com/doc)
- [Getting Started with GitHub](https://docs.github.com/en/get-started)

---

## Topics Covered

### 1. Key Features in QA

- **Creating and Managing Bug Reports**:
  - **Summary**: A concise title summarizing the problem.
  - **Description**: A detailed explanation of the issue.
  - **Steps to Reproduce**: Step-by-step instructions to recreate the issue.
  - **Expected Behavior**: How the application should behave.
  - **Actual Behavior**: How the application behaves incorrectly.
  - **Error Details**: Include errors observed (e.g., console errors, API errors).
  - **Accessibility Issues**: Note violations like missing labels or poor contrast.

- **Tracking Defect Statuses**:
  - Open → In Progress → Resolved → Closed.

- **Prioritizing Bugs**:
  - **Severity**: Critical, High, Medium, Low.
  - **Labels**: UI Bug, Accessibility, API Error.
  - **Sprints**: Assign tasks to specific cycles.

### 2. Introduction to Jira for Bug Tracking
Jira is a widely used tool for reporting, prioritizing, and tracking bugs in collaborative environments.

**Setup Instructions**:

- **Sign Up for Jira**:
  - Go to [Jira Free](https://www.atlassian.com/software/jira/try) and create an account.
- **Create a New Project**:
  - Click **Create Project** and select a project type (e.g., Kanban or Scrum).
  - Name the project (e.g., "QA Academy Bug Tracking").

### 3. Setting Up Git and GitHub

#### **3.1 Download and Install Git**
- **Overview**: Git is a version control system used to manage and track changes in source code during software development.
- **Installation Steps**:
  - **Mac**: Git is often pre-installed. You can check if it’s installed by running:
    ```bash
    git --version
    ```
    If not installed, use Homebrew to install Git:
    ```bash
    brew install git
    ```
    Or download it directly from the [Git website](https://git-scm.com/downloads).
  - **Windows**: Download the installer from the [Git website](https://git-scm.com/downloads) and follow the setup wizard instructions.

#### **3.2 Set Up Git and Configure with GitHub**
- **Configure Git** with your personal details:
  - In **Terminal** (Mac) or **Command Prompt** (Windows), run:
    ```bash
    git config --global user.name "Your Name"
    git config --global user.email "your.email@example.com"
    ```
- **Create a GitHub Account** if not done already:
  - Go to [GitHub.com](https://github.com) and **sign up** for a free account.
- **Create a Repository** in GitHub:
  - Click **New** in your GitHub dashboard.
  - **Name** the repository (e.g., "QA-Academy-Portfolio").
  - Add a description (optional) and **initialize with a README**.
  - **Clone the Repository** to your local machine:
    - In GitHub, click on the **<> Code** button and copy the SSH or HTTPS link.
    - In **Terminal** (Mac) or **Command Prompt** (Windows), run:
      ```bash
      git clone <repository-link>
      ```
      Replace `<repository-link>` with the link copied from GitHub.

---

## Practical Assignment

### Part 1: Log a Mock Bug in Jira

1. Navigate to your Jira project.
2. **Log a Mock Bug**:
   - Click **Create Issue** and choose **Bug** as the issue type.
   - Fill in the **Summary**, **Description**, **Steps to Reproduce**, **Expected Behavior**, and **Actual Behavior** fields.
   - Assign a severity level.
   - Save the bug report.

### Part 2: Set Up Git and GitHub

1. **Install Git** following the steps in Section 3.1.
2. **Configure Git** by adding your name and email (Section 3.2).
3. **Create a GitHub Repository** named `QA-Academy-Portfolio`.
4. **Clone the Repository** to your local machine using the command:
   ```bash
   git clone <repository-link>
   ```
5. Verify the repository is cloned successfully.

### Part 3: Add Saved Documents from Google Drive to Your QA Academy Repo

1. **Locate Your Documents**:
   - Download your previous assignments from Google Drive.
   - Save them locally.
2. **Move Files into the QA Academy Repo**:
   - Use the terminal to navigate to the cloned repository:
     ```bash
     cd QA-Academy-Portfolio
     ```
   - **Copy files** into the appropriate folder.

### Part 4: Add Documents to GitHub

1. Add and commit changes to the repository:
   - **Stage all files**:
     ```bash
     git add .
     ```
   - **Commit the changes** with a message:
     ```bash
     git commit -m "Initial commit: Added saved documents"
     ```
2. **Push** changes to GitHub:
   ```bash
   git push origin main
   ```

### Part 5: Write a Personal README

Include:
- A personal introduction (e.g., "I’m learning QA through QA Academy.").
- Program goals (e.g., "To build skills in QA and contribute to high-quality software.").

---

## Submission Instructions

1. **Share Your GitHub Repository Link**:
   - Share the link to your updated repository in the Slack group for feedback.
   - Ensure your files are properly added and committed.

2. **Save Your Progress**:
   - Verify all changes are pushed to your GitHub repository.

---

## Key Interview Questions

1. What is Jira, and how is it used in QA workflows?
2. When logging a bug in Jira, what details should you include to make it clear for others to understand?
3. What are some of the basic Git commands you've learned, and what do they do?
4. What does 'commit' mean in Git, and how is it different from 'push'?
5. What is the purpose of using GitHub along with Git?
6. What makes a good commit message? Can you give an example?

## Tips for Success

- **Practice Using Git**: Get comfortable with basic Git commands like `clone`, `add`, `commit`, and `push`.
- **Document Each Step**: Take screenshots as you work through each step; this can serve as a reference.
- **Ask for Help**: If you encounter any issues, ask questions in Slack—troubleshooting is an important skill.

---

## Next Training
In **Training 7**, we will focus on **branching** and **merging** in Git, along with using **VS Code** for version control. We will also learn how to write effective commit messages.
