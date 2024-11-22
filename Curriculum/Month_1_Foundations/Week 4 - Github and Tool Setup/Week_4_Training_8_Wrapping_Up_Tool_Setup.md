# Week 4: Training 8 - Wrapping Up Tool Setup

## Objective
By the end of this training, students will:
- Ensure that all tools are installed and properly configured.
- Troubleshoot any remaining setup issues.
- Consolidate all work done in Month 1 into a comprehensive GitHub repository.
- Reflect on their learning journey to reinforce key concepts and build confidence.

## Topics Covered

### 1. Verifying Tool Setup
- Use a checklist to verify that all tools required in Month 1 are installed correctly and configured.
- Tools: VS Code, Postman, browser developer tools, NVDA, Axe, Lighthouse, Wave, Jira.

### 2. Troubleshooting Common Installation Issues
- Cover common issues that may have occurred during setup.
- Provide solutions and support to ensure everyone is ready for Month 2.

### 3. Preparing for Month 2 with a Checklist
- **Checklist of Essential Skills and Tools Learned in Month 1**:
  - **Tools Setup Verification**:
    - [ ] Installed and configured **VS Code**.
    - [ ] Installed and set up **Postman**.
    - [ ] Installed and familiarized with **Browser Developer Tools**.
    - [ ] Installed **NVDA**, **Axe**, **Lighthouse**, **Wave**, and **Color Contrast Checker** tools.
    - [ ] Created an account and set up **Jira**.
    - [ ] Set up a **GitHub** account, created a repository, and practiced Git commands.
  - **Skill Review**:
    - [ ] Completed a **QA reflection document** on the role of QA in the SDLC.
    - [ ] Created an **SDLC flow diagram** and documented phases.
    - [ ] Written **summaries** on key QA tools and their purpose.
    - [ ] Performed an **accessibility audit** using Lighthouse and documented findings.
    - [ ] Practiced **branching** in GitHub by creating branches and merging them.
    - [ ] Written a **personal README** with your goals and a reflection on Month 1 learning.

- **Outline of What to Expect in Month 2**:
  - **Manual Testing Fundamentals**:
    - Learn how to write **test cases**, focusing on **functional testing**.
    - Understand the different types of testing techniques, like **boundary testing** and **equivalence partitioning**.
    - Practice creating and executing **test cases**.
  - **Bug Reporting**:
    - Learn how to write effective bug reports using **Jira**.
    - Practice documenting issues in a detailed and structured way.
  - **Exploratory Testing**:
    - Understand and practice **exploratory testing** techniques.
  - **Skills Application**:
    - Participants will begin applying the tools they set up in Month 1 to **actual testing scenarios**.
    - Tools like **Jira**, **browser dev tools**, and **Postman** will be incorporated into hands-on testing assignments.

## Final Project for Month 1
Students will submit a comprehensive GitHub repository showcasing everything they've worked on in Month 1. This will demonstrate mastery of foundational QA tools, Git, and GitHub.

### Part 1: Month 1 GitHub Repository Submission

1. **Repository Structure**:
   - Ensure that your GitHub repository is organized and contains:
     - **README**: Write a detailed overview of what you learned in Month 1, including a summary of each week’s focus and your personal goals.
     - **Assignments and Reflections**:
       - **QA Reflection Document**: Your reflection on QA's role in the SDLC.
       - **SDLC Flow Diagram**: Upload the diagram created in Training 2.
       - **Tool Purpose Summaries**: Summaries of the tools you've set up and their purpose.
       - **Accessibility Audit Summary**: Results from the Lighthouse audit exercise.
     - **Branch Structure**:
       - Create at least one additional branch to demonstrate feature work from the month.
       - Example branch name: `feature/month1-final-project`.
     - **Commit History**:
       - Make sure to have clear commit messages that document your progress throughout the month.
       - Use at least 4-5 meaningful commits that reflect the different assignments and tasks you completed.

2. **Final Git Commands to Submit**:
   - **Create a new branch**:
     ```bash
     git checkout -b feature/month1-final-project
     ```
   - **Add all relevant files**:
     ```bash
     git add .
     git commit -m "Add Month 1 final project files and summaries"
     ```
   - **Merge branch into main**:
     ```bash
     git checkout main
     git merge feature/month1-final-project
     ```
   - **Push to GitHub**:
     ```bash
     git push origin main
     ```

### Part 2: Reflection Document
Write a **Reflection Document** and include the following:
- **Key Takeaways**: Summarize the key concepts and skills acquired during Month 1. This can include any challenges you faced and what you found most rewarding.
- **Challenges and Solutions**: What were some of the challenges you faced in learning these tools and processes? How did you overcome them?
- **Applications in QA**: Reflect on how the tools and concepts you learned could be applied in real QA environments.

**Submit this reflection document** by adding it to your repository and pushing it as a separate commit:
```bash
git add reflection_month1.txt
git commit -m "Add Month 1 reflection document"
git push origin main
```

## Submission Instructions
1. **GitHub Repository Link**:
   - Share your GitHub repository link in the Slack group for final Month 1 feedback.
   - Make sure your repository contains the README, assignments, the branch structure, and the reflection document.

2. **Repository Requirements**:
   - Your **README** should summarize your Month 1 experience.
   - All files from previous assignments should be neatly organized.
   - Use **branching** to demonstrate your knowledge of Git and document your work.

## Free Online Resources for Troubleshooting
- **GitHub Troubleshooting Guide**: [GitHub Help](https://docs.github.com/en/github/getting-started-with-github)
- **Common Issues with Git**: [Atlassian Git Troubleshooting](https://www.atlassian.com/git/tutorials/troubleshooting-git)
- **Accessibility Testing Tools Resources**: [WebAIM Resources](https://webaim.org/resources/)

## Key Interview Questions
By the end of this training, students should be able to confidently answer:
1. What tools did you set up and use during Month 1, and what is their purpose?
2. What is the importance of version control in QA?
3. How does accessibility testing contribute to software quality?

## Tips for Success
- **Take Your Time**: Use this session to wrap up any tools or assignments you may still need to complete.
- **Use the Checklist**: The checklist provided will help ensure you are ready for Month 2.
- **Ask Questions**: If you face issues, the Slack group is available for support and questions.

## Key Deliverables for Month 1
1. **All Tools Installed and Configured**:
   - VS Code, Postman, browser developer tools, NVDA, Axe, Lighthouse, Wave, and Jira.
2. **GitHub Repository Created with Key Documents**:
   - **README**: Summary of Month 1.
   - **Assignments and Reflections**: All key documents completed during the month.
   - **Branch Structure and Commit History**.

## Preparing for Month 2

- **Outline of What to Expect in Month 2**:
  - **Manual Testing Fundamentals**:
    - Learn how to write **test cases**, focusing on **functional testing**.
    - Understand the different types of testing techniques, like **boundary testing**, **equivalence partitioning**, and **decision table testing**.
    - Practice creating and executing **test cases** with real-world scenarios.
  - **Bug Reporting**:
    - Learn how to write effective bug reports using **Jira**.
    - Practice documenting issues in a detailed and structured way, including steps to reproduce, expected vs actual behavior, severity, and priority.
  - **Exploratory Testing**:
    - Understand and practice **exploratory testing** techniques.
    - Learn how to identify gaps in testing by using exploratory methods to discover unexpected behaviors.
  - **Skills Application**:
    - Participants will begin applying the tools they set up in Month 1 to **actual testing scenarios**.
    - Tools like **Jira**, **browser dev tools**, and **Postman** will be incorporated into hands-on testing assignments.

  - **Key Goals for Month 2**:
    - By the end of Month 2, students should feel comfortable creating **comprehensive test cases** for a given requirement, documenting **bug reports** effectively, and performing **exploratory testing** to assess software quality.
    - The foundational skills from Month 1 will help students document and organize their work effectively, ensuring they are fully prepared to handle manual testing activities.

  - **Additional Preparation Tips for Month 2**:
    - **Practice Writing Test Cases**: Consider using real-world scenarios to practice writing functional test cases.
    - **Familiarize Yourself with Jira**: Revisit Jira tutorials or any provided resources to feel comfortable navigating the tool for bug tracking.
    - **Explore Additional Resources**: Use supplementary online resources to strengthen understanding of manual testing techniques and best practices.
