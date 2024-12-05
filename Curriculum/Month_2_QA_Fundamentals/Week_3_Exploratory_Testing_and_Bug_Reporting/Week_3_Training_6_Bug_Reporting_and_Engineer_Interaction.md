# Week 3: Training 6 - Bug Reporting Fundamentals

## Objective

By the end of this training, students will:

- Understand how to document bugs effectively, including defining severity and priority.
- Learn to communicate effectively with developers during the bug-fixing process.
- Practice drafting concise, actionable bug reports.

---

## Free Online Resources

Students are encouraged to explore the following resources before this session to gain a foundational understanding of bug reporting:

1. **[Defect/Bug Life Cycle in Software Testing (Guru99)](https://www.guru99.com/defect-life-cycle.html)**  
   Learn about the entire lifecycle of a bug from identification to resolution, with examples.
   
2. **[How to Write a Good Bug Report (Guru99)](https://www.guru99.com/bug-report.html)**  
   A guide to writing concise, informative bug reports with examples.

3. **[How to Write Effective Bug Reports (Atlassian)](https://community.atlassian.com/t5/App-Central-articles/How-to-create-bug-reports-in-Jira-better/ba-p/2425374)**  
   Provides guidance on writing impactful bug reports that facilitate quick understanding and resolution.

### Videos on Bug Reporting

**Tip**: These videos provide a visual walkthrough of the bug reporting process.

- [How to file a bug report](https://www.youtube.com/watch?v=7cDzjS6z5ks)  
- [Common Mistakes in Bug Reporting](https://www.youtube.com/watch?v=e6ta087nxho)  

---

## Topics Covered

### 1. Bug Lifecycle and Severity/Priority

- **Bug Lifecycle**: Discuss the different stages of a bug, from identification to closure.

  - **Stages**: New, Assigned, Open, Fixed, Retested, Closed, Reopened.

- **Severity vs. Priority**:

  - **Severity**: Defines how serious an issue is for the software's functionality.
  - **Priority**: Defines how urgently the issue needs to be fixed.

**Key Insight**: Understanding severity and priority helps in communicating the impact of an issue effectively to stakeholders.

---

### 2. Components of a Good Bug Report

**Key Components**:
- **Title**: Provide a concise summary of the issue.
- **Environment**: Mention the system and platform where the bug was found.
- **Steps to Reproduce**: Detailed, step-by-step instructions to recreate the issue.
- **Expected vs. Actual Result**: Clarify what should have happened and what actually did.
- **Severity and Priority**: Assign values based on impact and urgency.
- **Attachments**: Screenshots, videos, or logs that support your findings.

**Key Insight**: Clear and structured bug reports save time for developers and enhance the efficiency of the QA process.

---

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

---

### 4. Communicating Bugs with Developers

**Communication Tips**:
- **Be Concise**: Keep communication straightforward.
- **Provide Context**: Explain why the bug matters, especially for user experience.
- **Use Templates**: Follow established bug report templates for consistency.
- **Avoid Assumptions**: Stick to the facts and avoid suggesting the cause unless confident.

**Example Scenario**: A QA finds a bug in the checkout process of an e-commerce website. They create a report detailing the steps to reproduce the issue, expected vs. actual behavior, and include a screenshot of the error. The developer needs this context to effectively address the bug.

**Communication Note**: It’s important for QA to answer developer questions promptly and provide additional information or evidence if needed.

---

## Practical Assignment

### Part 1: Writing Bug Reports

- **Objective**: Identify and document bugs in the **QA Practice Demo Environment** ([CHALLENGE - Spot the BUGS!](https://qa-practice.netlify.app/bugs-form)).

- **Task**: Write at least **10 bug reports** using a Google Sheet with the following columns:

  - **Title**
  - **Environment**
  - **Steps to Reproduce**
  - **Expected Result**
  - **Actual Result**
  - **Severity**
  - **Priority**

- **Extra Credit**: Find and report **all 15 bugs** present in the demo environment.

### Part 2: Developer Interaction Simulation

- **Objective**: Use ChatGPT to simulate real developer interactions, where ChatGPT will act as a developer asking questions about your bug reports.
- **Link to Access ChatGPT**: [https://chat.openai.com/](https://chat.openai.com/)

#### Instructions:

1. **Select Three Bug Reports**: Choose **three** of your documented bug reports in Google Sheets for this exercise.

2. **Access ChatGPT**:
   - Go to [https://chat.openai.com/](https://chat.openai.com/).

3. **Use This Prompt in ChatGPT**:
   - *"You are acting as a software developer reviewing bug reports. I will describe a bug report, and you should ask follow-up questions that would help you as a developer to resolve the issue more effectively. Your questions should focus on reproduction steps, expected vs actual results, severity, environment details, and anything else needed to clearly understand the bug."*

4. **Simulate Interaction**: 
   - Provide ChatGPT with a summary of one of your selected bug reports and let it respond with developer-like questions.
   - Answer the questions posed by ChatGPT concisely, just as you would in a real interaction.

5. **Repeat Steps 3 & 4** for the remaining two bug reports.

6. **Record Responses**: Document the questions asked by ChatGPT and your responses in your Google Sheet.

7. **Submit**: 
   - Share your Google Sheet, including the documented bug reports, questions from ChatGPT, and your responses, in the Slack channel for feedback.

---

### Additional Tips for Using ChatGPT Effectively:

- **Be Detailed**: When describing your bug report, include as much information as possible so ChatGPT can ask targeted questions.
- **Practice Realism**: Treat the conversation as if you’re speaking to a real developer—be respectful and clear.

**Key Insight**: Practicing with ChatGPT allows you to refine your communication skills, anticipate developer needs, and ensure your bug reports are as actionable as possible.

---

## Key Learning Outcomes

- Understand the structure and importance of effective bug reports.
- Learn best practices for clear communication with developers regarding bugs.
- Develop the ability to assign appropriate severity and priority to issues.
- Practice writing detailed bug reports that facilitate faster resolutions.

---

## Key Interview Questions

At the end of this training, students should be able to confidently answer the following questions in an interview:

1. **What are the key components of a good bug report?**
2. **How do severity and priority differ, and why are they both important?**
3. **How can you communicate effectively with developers when discussing a bug?**
4. **Why is it important to include detailed reproduction steps in a bug report?**

---

## Tips for Success

- **Be Specific**: Always provide detailed steps and evidence.
- **Anticipate Questions**: Developers may need additional details—be ready to provide them.
- **Be Respectful**: Remember that your goal is to help improve the product, not point fingers.

---

## Preparing for Training 7

In **Training 7**, students will learn how to create a detailed handoff document for developers and stakeholders. This will include how to summarize key findings, create actionable next steps, and provide testing insights to enhance collaboration.