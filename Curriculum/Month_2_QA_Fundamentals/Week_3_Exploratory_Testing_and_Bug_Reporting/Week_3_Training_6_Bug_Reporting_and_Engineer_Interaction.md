# Week 4: Training 6 - Bug Reporting Fundamentals

## Objective

The purpose of this training is to help students understand the essentials of bug reporting, including how to document, communicate, and escalate issues in a way that facilitates timely and effective resolution. By the end of this session, students will:

- Understand the key components of a well-written bug report.
- Learn how to communicate bugs effectively with developers and stakeholders.
- Develop skills to prioritize and escalate issues based on severity and impact.

---

## Free Online Resources

Students are encouraged to explore the following resources before this session to gain a foundational understanding of bug reporting:

- [How to Write a Good Bug Report (Guru99)](https://www.guru99.com/bug-report.html)  
  A guide to writing concise, informative bug reports with examples.
- [Effective Bug Reporting (Software Testing Help)](https://www.softwaretestinghelp.com/bug-reporting/)  
  Tips and best practices for creating actionable bug reports.

### Videos on Bug Reporting

**Tip**: These videos provide a visual walkthrough of the bug reporting process.

- [How to Write a Bug Report](https://www.youtube.com/watch?v=ghi-example)  
- [Common Mistakes in Bug Reporting](https://www.youtube.com/watch?v=jkl-example)  

---

## Topics Covered

### 1. What is a Bug Report?

**Definition**: A bug report is a document that describes an issue observed in the software, providing enough detail to allow developers to reproduce, understand, and fix the issue.

**Key Insight**: A well-crafted bug report improves efficiency by reducing the back-and-forth communication needed to understand and resolve issues.

### 2. Components of a Good Bug Report

**Key Components**:
- **Title**: A concise, descriptive summary of the issue.
- **Description**: Detailed information about the bug, including:
  - **Steps to Reproduce**: Step-by-step actions that led to the issue.
  - **Expected vs. Actual Results**: What should happen versus what actually happened.
  - **Environment Details**: The platform, browser, or device on which the issue was observed.
- **Severity and Priority**: Indicators of the impact and urgency of the bug.
- **Attachments**: Screenshots, videos, or logs that help illustrate the problem.

**Key Insight**: Adding as much relevant detail as possible ensures that the developer can easily reproduce the bug without additional clarification.

### 3. Writing Effective Bug Reports

**Best Practices**:
- **Be Clear and Concise**: Use straightforward language to describe the problem without ambiguity.
- **Use Reproducible Steps**: Clearly describe each step needed to reproduce the bug.
- **Provide Context**: Mention if the bug is part of a larger workflow or if it blocks other tests.
- **Include Severity and Priority**: This helps the team understand the urgency and impact.

**Example Bug Report**:

**Title**: "Login button becomes unresponsive after entering incorrect credentials twice"

**Description**: 
- **Steps to Reproduce**:
  1. Go to the QA Practice Bugs Form.
  2. Enter incorrect credentials.
  3. Click the login button.
  4. Repeat steps 2-3.
- **Expected Result**: Login button should remain responsive to allow users to reattempt.
- **Actual Result**: Login button becomes unresponsive.
- **Environment**: Chrome 90, Windows 10.

**Key Insight**: Well-documented bug reports help save time and avoid misunderstandings between QA and developers.

### 4. Communicating Bugs with Developers

**Communication Tips**:
- **Use a Collaborative Tone**: Approach developers as partners rather than adversaries.
- **Provide Context**: Explain why the bug is important and how it affects the user experience.
- **Be Available for Questions**: Make it easy for developers to reach out for clarification if needed.

**Key Insight**: Effective communication between QA and developers leads to quicker resolutions and better working relationships.

### 5. Bug Severity vs. Priority

**Severity**: How severe the bug is in terms of the application's functionality.
- **Critical**: Major system failure or a key feature is unusable.
- **High**: A significant issue that impacts users but has a workaround.
- **Medium**: A bug that affects functionality but does not prevent users from completing key actions.
- **Low**: Minor issues such as typos or cosmetic inconsistencies.

**Priority**: How urgently the bug needs to be fixed.
- **P1**: Needs immediate attention.
- **P2**: Important but not critical.
- **P3**: Can be scheduled in future releases.

**Key Insight**: Understanding the difference between severity and priority is crucial in ensuring that resources are effectively allocated to fix the most impactful issues first.

---

## Practical Exercise: Writing Bug Reports

### Task: Document Bugs Found in QA Practice Bugs Form

- **Objective**: Identify and document bugs in QA Practice Bugs Form’s **bug submission** features.
- **Steps to Follow**:
  1. Use exploratory testing techniques to find at least **ten bugs** in the registration or login workflows. An extra credit opportunity is available for students who identify all **fifteen** bugs present on the site.
  2. Document the bugs using a Google Doc or Sheets, including all key components (title, description, steps to reproduce, expected vs. actual results, environment, severity, and priority).
  3. Submit your document via the QA Academy Slack channel for feedback.

**Key Insight**: Practice makes perfect. The more you document bugs, the more natural it will become to provide all the necessary information clearly and effectively.

---

## Assignment

### Assignment Instructions

- **Objective**: Create a test suite for the QA Practice Bugs Form, perform exploratory testing to identify ten bugs, and document those bugs in a detailed bug report.
- **Instructions**:
  1. **Create Test Suite**: Develop a comprehensive test suite for the QA Practice Bugs Form covering the main functionalities, such as registration, login, and form submission.
  2. **Exploratory Testing**: Use the QA Practice Bugs Form to find and document at least **ten bugs**. An extra credit opportunity is available for students who identify all **fifteen** bugs present on the site.
  3. **Analyze Test Cases**: Reflect on the exploratory testing process to identify additional test cases that could improve the overall coverage.
  4. **Write Bug Reports**: Document all identified bugs with the key components (title, description, steps to reproduce, expected vs. actual results, environment, severity, priority).
  5. **Deliverable**: Submit your updated test suite and bug reports in the designated Slack channel.

---

## Submission Instructions

- **How to Submit**:
  - Update your **Google Sheets** test case document.
  - Share the updated Google Sheets in the designated Slack channel.
  - Ensure permissions are set to "Anyone with the link can view/comment."

---

## Key Learning Outcomes

- Understand the structure and importance of effective bug reports.
- Learn best practices for clear communication with developers regarding bugs.
- Develop the ability to assign appropriate severity and priority to issues.
- Practice writing detailed bug reports that facilitate faster resolutions.

---

## Key Interview Questions

At the end of this training, students should be able to confidently answer the following questions in an interview:

1. What are the key components of a good bug report?
2. How do you communicate a bug effectively to a developer?
3. What is the difference between severity and priority in bug reporting?
4. Can you provide an example of a bug report you have written in the past?

---

## Tips for Success

- **Be Thorough**: Always provide enough detail to reproduce the bug easily.
- **Be Objective**: Focus on the facts, not assumptions or subjective opinions.
- **Collaborate**: Bug reporting is a team effort—clear communication helps resolve issues faster.

---

## Next Training

In **Training 7**, we will explore **Organizing QA Documentation**, where students will learn how to maintain well-structured QA records and documentation. This includes:
- Best practices for structuring digital folders (e.g., organizing by test phases, reports, and deliverables).
- Using Google Sheets and Docs to systematically track test cases, bug reports, and planning.
- Writing README summaries for GitHub to maintain a clear project overview.