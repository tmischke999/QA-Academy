# Week 2: Training 4 - Comprehensive Exploratory Testing

## Objective

This training introduces and builds foundational skills in exploratory testing, progressing into advanced techniques and documentation practices. By the end of this session, students will:

- Understand what exploratory testing is and its importance in QA workflows.
- Learn techniques and heuristics to structure exploratory testing.
- Develop skills to identify gaps in test coverage and uncover edge cases.
- Master documentation practices for session-based exploratory testing (SBET) and actionable bug reports.

---

## Free Online Resources (Mandatory)

1. [What is Exploratory Testing (Guru99)](https://www.guru99.com/exploratory-testing.html)
   - An overview of exploratory testing and its benefits.
2. [Exploratory Testing Techniques (Software Testing Help)](https://www.softwaretestinghelp.com/exploratory-testing/)
   - Techniques to enhance exploratory testing.
3. [Getting Started with Session-Based Test Management for Exploratory Testing (YouTube)](https://www.youtube.com/watch?v=sGk9uW22NlM)
   - A practical introduction to SBET.
4. [How to Write a Bug Report (Guru99)](https://www.guru99.com/how-to-write-a-bug-report.html)
   - A guide to creating effective bug reports.

---

## Topics Covered

### 1. What is Exploratory Testing?
- **Definition**: A process of simultaneous test design and execution, emphasizing learning, discovery, and adaptability.
- **Comparison with Scripted Testing**:
  - Scripted Testing: Predefined steps and expected outcomes.
  - Exploratory Testing: Dynamic, focused on investigating unexpected behaviors.

---

### 2. Heuristics for Exploratory Testing
#### SFDPOT Heuristic:
- **Structure**: Analyze layout and navigation.
- **Function**: Test specific features or workflows.
- **Data**: Explore inputs and combinations.
- **Platform**: Test across devices and browsers.
- **Operations**: Simulate real-world conditions (e.g., server outages).
- **Time**: Check time-sensitive behaviors.

#### CRISP-DM Heuristic:
- **Context, Risk, Input, State, Platform**: A structured way to examine test scenarios.

---

### 3. Techniques for Exploratory Testing
- **Session-Based Testing**: Time-boxed sessions with specific charters (e.g., "Test login feature for usability and edge cases").
- **Mind Mapping**: Visual representation of features to uncover new testing ideas.
- **Bug Hunting Sessions**: Dedicated time to find defects in a specific area.

---

### 4. Identifying Edge Cases
- Analyze workflows for rare paths or unexpected inputs.
- Combine unusual data sets to test boundaries of the system.

---

### 5. Documenting Exploratory Testing
#### SBET Report Components:
- **Session Charter**: Goal of the session.
- **Observations**: Unexpected behaviors or issues found.
- **Edge Cases**: Highlight unusual but impactful scenarios.

#### Writing Actionable Bug Reports:
- **Key Elements**:
  - **Title**: Concise and descriptive.
  - **Steps to Reproduce**: Detailed instructions.
  - **Expected Result**: Correct behavior.
  - **Actual Result**: Observed behavior.
  - **Attachments**: Include evidence (screenshots, videos, logs).

---

## Assignment

### Part 1: Conduct an Exploratory Testing Session
1. Access the demo application: [https://demo.opencart.com/](https://demo.opencart.com/).
2. Define a 30-minute session charter (e.g., "Explore the registration feature for usability and edge cases").
3. Document observations and potential issues.

### Part 2: Write Bug Reports
1. Select two key issues found during your session.
2. Write detailed bug reports including all key elements.
3. Save reports in Google Docs and share via Slack.

### Part 3: Update Test Cases
1. Create or update three test cases based on your findings.
2. Include:
   - Test Case ID
   - Title
   - Steps
   - Expected Results
   - Actual Results (if executed)
3. Submit updates in your shared Google Sheets test case document.

---

## Submission Instructions
- Share your **SBET Report** and **Bug Reports** via Slack.
- Update your Google Sheets document with new test cases.
- Ensure all submissions are clear and accessible.

---

## Key Learning Outcomes
- Understand exploratory testing and its techniques.
- Use heuristics to structure exploratory testing sessions.
- Document findings effectively using SBET and bug reports.
- Identify edge cases and create new test cases.

---

## Key Interview Questions
1. What is exploratory testing, and how does it differ from scripted testing?
2. How do heuristics like SFDPOT guide exploratory testing?
3. What are the components of an SBET report?
4. How do you write an actionable bug report?

---

## Tips for Success
- **Stay Curious**: Treat testing like a puzzle.
- **Focus**: Stick to your session charter but follow unexpected discoveries.
- **Be Thorough**: Record all findings, even minor observations.
- **Collaborate**: Share findings with peers for additional insights.

---

## Next Training
In **Training 5**, we will cover **Introduction to Regression Testing and Automation Candidates**, focusing on the importance of regression testing and identifying test cases for automation.

