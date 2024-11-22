# Week 3: Training 6 - Introduction to Bug Tracking and Version Control with GitHub (Part 1)

## Objective
Introduce students to bug tracking with Jira and foundational version control concepts using GitHub. By the end of this training, students will:
- Understand how bug tracking tools like Jira are used in QA workflows.
- Learn the basics of Git and GitHub for version control.
- Clone the QA Academy repository, add saved documents from Google Drive, and set up their personal GitHub repository.

## Topics Covered

### 1. Introduction to Jira for Bug Tracking
Jira is a widely used tool for reporting, prioritizing, and tracking bugs in collaborative environments.

**Key Features in QA:**
- **Creating and Managing Bug Reports:**
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

**Instructions**:
- Sign up for Jira at [Jira Free](https://www.atlassian.com/software/jira/try).
- Review this guide: [How to Use Jira for Bug Tracking](https://www.atlassian.com/software/jira/guides).

### 2. Setting Up a GitHub Account and Repository
GitHub enables version control and collaboration.

**Steps to Get Started**:
1. **Sign Up for GitHub**:
   - Navigate to [GitHub](https://github.com/) and create a free account.
2. **Create a New Repository**:
   - **Name**: `QA-Academy-Portfolio`.
   - Add a description (e.g., "Personal QA training repository").
   - Initialize with a README file.

### 3. Basic Git Commands

**Clone**: Download a repository to your local machine.
```bash
git clone https://github.com/tmischke999/QA-Academy/
```

**Add and Commit**: Stage changes and save them locally.
```bash
git add .
git commit -m "Add saved documents to personal repo"
```

**Push**: Upload changes to GitHub.
```bash
git push origin main
```

**Pull**: Fetch updates from GitHub.
```bash
git pull origin main
```

## Assignment

### Part 1: Clone the QA Academy Repository
1. Open a terminal or command prompt and run:
   ```bash
   git clone https://github.com/tmischke999/QA-Academy/
   ```
2. Verify the repository is cloned successfully.

### Part 2: Add Saved Documents from Google Drive to Your QA Academy Repo
1. **Locate Your Documents**:
   - Download your previous assignments from Google Drive.
   - Save them locally.
2. **Move Files into QA Academy Repo**:
   ```bash
   cd QA-Academy
   ```
   Copy files into the appropriate folder.

### Part 3: Add Documents to Personal Repository
1. Navigate to your personal GitHub repository folder:
   ```bash
   cd [your-repo-name]
   ```
2. Add and commit changes:
   ```bash
   git add .
   git commit -m "Initial commit: Added saved documents"
   git push origin main
   ```

### Part 4: Write a Personal README
Include:
- A personal introduction (e.g., "I’m learning QA through QA Academy.").
- Program goals (e.g., "To build skills in QA and contribute to high-quality software.").

## Submission Instructions
1. Share your GitHub repository link in the Slack group for feedback.
2. Verify the README includes your personal introduction and program goals.
3. Save the repository link for future use in upcoming sessions.

## Free Online Resources
- [Git Basics](https://git-scm.com/doc)
- [Getting Started with GitHub](https://docs.github.com/en/get-started)
- [Introduction to Bug Tracking with Jira](https://www.atlassian.com/software/jira/guides)

## Key Interview Questions
1. What is Jira’s purpose in QA workflows?
2. How do Git commands like clone, commit, push, and pull work?
3. Why is version control important in QA?

## Tips for Success
- Organize files logically in GitHub.
- Practice Git commands for confidence.
- Follow best practices for commit messages.

## Next Training
In **Training 7**, we will explore GitHub branches, managing files, and writing effective commit messages.

