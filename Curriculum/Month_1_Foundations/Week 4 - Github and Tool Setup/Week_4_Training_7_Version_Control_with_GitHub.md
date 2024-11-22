# Week 4: Training 7 - Version Control with GitHub (Part 2)

## Objective
By the end of this training, students will:
- Learn how to create and manage branches in GitHub.
- Understand the importance of writing effective commit messages.
- Practice creating branches, adding files, and merging changes into the main branch.

## Topics Covered

### 1. Creating Branches in GitHub
- What is a branch?
- Why are branches important in version control?
- Practical steps to create a new branch.

### 2. Managing Files in GitHub
- How to add files to a branch.
- Making changes and committing them to the branch.
- Understanding when to merge changes back into the main branch.

### 3. Writing Effective Commit Messages
- What makes a good commit message?
- Guidelines for writing meaningful commit messages.

## Learning Resources

### Free Online Tutorials to Get Started
1. **GitHub Learning Lab: Introduction to GitHub**
   - Link: [GitHub Learning Lab - Introduction to GitHub](https://lab.github.com/githubtraining/introduction-to-github)
   - Description: This interactive lab walks you through branching, creating files, and merging changes.

2. **Atlassian Git Tutorial - Branching**
   - Link: [Atlassian Git Tutorial - Branching](https://www.atlassian.com/git/tutorials/using-branches)
   - Description: This tutorial explains branching in detail and covers the basics of Git commands for managing branches.

3. **FreeCodeCamp Git & GitHub**
   - Link: [FreeCodeCamp Git Tutorial](https://www.freecodecamp.org/news/git-and-github-for-beginners/)
   - Description: This beginner-friendly guide covers branching, merging, and best practices for effective version control.

## Practical Assignment

### Part 1: Complete the GitHub Learning Lab Module
1. **Start with the GitHub Learning Lab module**:
   - Navigate to the [GitHub Learning Lab - Introduction to GitHub](https://lab.github.com/githubtraining/introduction-to-github).
   - Complete the module on branching, following the steps to create and manage branches.
   - This module will walk you through the entire process interactively.

### Part 2: Practice Branching, Adding Files, and Merging
After completing the GitHub Learning Lab module, follow these steps to practice in your **QA Academy repository**:

1. **Create a New Branch**
   - Open a terminal or command prompt.
   - Navigate to your local QA Academy repository.
     ```bash
     cd QA-Academy
     ```
   - Create a new branch for your practice:
     ```bash
     git checkout -b feature/practice-branch
     ```
     - **Note**: The name `feature/practice-branch` is an example. You can use any meaningful branch name, like `training-week4`.

2. **Add a New File to the Branch**
   - Create a new file in the repository. For example, create a simple text file named `branch_practice.txt`.
     ```bash
     echo "This is my practice file for branching." > branch_practice.txt
     ```
   - Stage the file for commit:
     ```bash
     git add branch_practice.txt
     ```
   - Commit the new file with a descriptive message:
     ```bash
     git commit -m "Add practice file for branching exercise"
     ```

3. **Merge the Branch Back into Main**
   - Switch back to the `main` branch:
     ```bash
     git checkout main
     ```
   - Merge your `feature/practice-branch` into the `main` branch:
     ```bash
     git merge feature/practice-branch
     ```
   - Push your changes to GitHub:
     ```bash
     git push origin main
     ```

4. **Delete the Branch (Optional)**
   - Once your changes are merged, you can delete the branch locally:
     ```bash
     git branch -d feature/practice-branch
     ```
   - And remotely (on GitHub):
     ```bash
     git push origin --delete feature/practice-branch
     ```

### Part 3: Write a Commit Message Guideline
Write a short document titled **"Commit Message Guidelines"**. This should include:
- **Why good commit messages matter**.
- **Examples** of good commit messages (e.g., "Add tests for new login feature").
- **Guidelines** for writing commit messages, such as:
  - Start with a verb (e.g., "Add," "Fix," "Update").
  - Keep it concise but informative.
  - Reference an issue or ticket if applicable.

Save this document in your local repository and commit it with a message like:
```bash
git add commit_guidelines.txt
git commit -m "Add commit message guideline document"
git push origin main
```

## Submission Instructions
1. **Share Your GitHub Repository Link**:
   - Share the link to your updated repository in the Slack group for feedback.
   - Make sure your new file (`branch_practice.txt`) and commit message guidelines (`commit_guidelines.txt`) are present.

2. **Save Your Progress**:
   - Ensure all your changes are pushed to your personal GitHub repository.
   - Save the link to your repository as you'll use it in future exercises.

## Free Online Resources for Further Learning
- [Pro Git Book - Chapter on Branching](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell)
- [GitHub Guide on Writing Commit Messages](https://github.com/erlang/otp/wiki/Writing-good-commit-messages)

## Key Interview Questions
By the end of this training, students should be able to answer:
1. What is a Git branch, and why is it useful?
2. How do you create and merge a branch in Git?
3. What makes a good commit message?

## Tips for Success
- **Practice Branching**: Don’t hesitate to create multiple branches for practice. The more comfortable you are with branches, the easier collaboration becomes.
- **Write Detailed Commit Messages**: Use the guidelines you’ve written to make your commit messages more effective.
- **Ask Questions in Slack**: If you face issues, share them in Slack. Learning from challenges is part of the process.

## Next Training
In **Training 8**, we will wrap up tool setup and ensure everyone is comfortable with the tools we've introduced. We will troubleshoot common issues, and prepare for Month 2, which dives deeper into manual testing fundamentals.
