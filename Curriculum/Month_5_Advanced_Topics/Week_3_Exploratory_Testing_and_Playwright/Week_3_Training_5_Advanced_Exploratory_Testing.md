 Here is the first draft for **Training 5: Advanced Exploratory Testing and Documentation**:
# **Training 5: Advanced Exploratory Testing and Documentation**

## **Objective**

This training session focuses on advanced exploratory testing techniques, emphasizing heuristic-driven exploration, edge case identification, and structured documentation. By the end of this session, students will:

- Understand the **SFDPOT heuristic** and how to apply it to exploratory testing.
- Develop skills to identify edge cases and document findings effectively.
- Create actionable bug reports based on exploratory testing results.

---

## **Free Online Resources** (Mandatory)

1. **[Exploratory Testing Techniques (Software Testing Help)](https://www.softwaretestinghelp.com/what-is-exploratory-testing/)**  
   - A guide to various exploratory testing techniques to enhance testing skills.

2. **[Getting Started with Session Based Test Management for Exploratory Testing (YouTube)](https://www.youtube.com/watch?v=sGk9uW22NlM)**  
   - Learn about the concept and benefits of session-based exploratory testing.

3. **[Exploratory Testing - Easy, Detailed and with example (YouTube)](https://www.youtube.com/watch?v=tiPBh_0Z6J8)**  
   - Practical explaination of heuristic, session-based, and time-bound exploratory testing.

3. **[How to Write a Bug Report (Guru99)](https://www.guru99.com/how-to-write-a-bug-report.html)**  
   - A step-by-step tutorial on writing effective and actionable bug reports.

---

## **Topics Covered**

### **1. Introduction to Advanced Exploratory Testing**

- **Definition**: Exploratory testing involves simultaneous learning, test design, and execution.  
- **Key Insight**: Advanced techniques focus on structured exploration and identifying hidden defects that escape scripted tests.

---

### **2. Heuristics for Exploratory Testing**

#### **SFDPOT Heuristic**:
- **Structure**: Investigate the application's layout and navigation.
- **Function**: Validate individual features or functionalities.
- **Data**: Test with various input data types and combinations.
- **Platform**: Assess behavior across different platforms, browsers, or devices.
- **Operations**: Simulate operational conditions like server restarts or network disruptions.
- **Time**: Examine behavior under time constraints or extended sessions.

**Example**:
- **Login Feature (SFDPOT)**:
  - **Structure**: Check if the login page layout changes with screen size.
  - **Function**: Verify login with valid and invalid credentials.
  - **Data**: Test with special characters, large inputs, or empty fields.
  - **Platform**: Test on multiple browsers or mobile devices.
  - **Operations**: Simulate server downtime during login.
  - **Time**: Attempt multiple logins in quick succession.

---

### **3. Techniques for Identifying Edge Cases**

- Analyze application workflows for rarely used paths or unexpected inputs.
- Think like a user and anticipate actions outside standard procedures.
- Combine unusual data sets to explore application limits.

---

### **4. Session-Based Exploratory Testing (SBET)**

- **Planning a Session**:
  - Define **charters** or goals for the session (e.g., “Explore the login feature for edge cases”).
  - Allocate a fixed time (e.g., 45 minutes).
- **Executing the Session**:
  - Focus on the charter while remaining flexible to follow discoveries.
  - Record observations, questions, and potential issues.
- **Documenting Results**:
  - Create a concise session report summarizing:
    - Session goals.
    - Observations and findings.
    - Edge cases discovered.

---

### **5. Writing Actionable Bug Reports**

- **Structure of a Bug Report**:
  - **Title**: Clear and descriptive (e.g., “Login button fails on mobile browsers”).
  - **Steps to Reproduce**: Detailed steps to recreate the issue.
  - **Expected Result**: Describe the correct behavior.
  - **Actual Result**: Document the observed issue.
  - **Attachments**: Include screenshots, videos, or logs.
- **Key Insight**: Bug reports must be clear and actionable to help developers resolve issues efficiently.

---

## **Assignment**

### **Objective**

Apply advanced exploratory testing techniques to identify edge cases and document findings.

### **Instructions**

1. **Conduct a Session-Based Exploratory Testing Session**:
   - Use the demo application: [https://the-internet.herokuapp.com](https://the-internet.herokuapp.com).
   - Define a 45-minute session charter (e.g., “Explore the form authentication feature for usability and edge cases”).
   - Focus on identifying edge cases and unexpected behaviors.

2. **Document Your Findings**:
   - Create an **SBET report** that includes:
     - **Session Goals**: Define the focus of your session.
     - **Observations**: Summarize unexpected behaviors or usability issues.
     - **Edge Cases**: Highlight at least two edge cases discovered.

3. **Write Bug Reports**:
   - Write **two detailed bug reports** based on your findings.
   - Include all required components (title, steps to reproduce, expected and actual results, attachments).

4. **Submit Your Work**:
   - Deliverables:
     - **Exploratory Testing Checklist**.
     - **SBET Report**.
     - **Two Bug Reports**.
   - Save files as PDFs and upload them to the QA Academy Slack channel.

---

## **Key Learning Outcomes**

By the end of this training, students will:

- Understand how to use heuristics like SFDPOT for structured exploratory testing.
- Identify and document edge cases effectively.
- Write detailed and actionable bug reports suitable for real-world QA scenarios.

---

## **Key Interview Questions**

1. What is exploratory testing, and how does it differ from scripted testing?
2. How do heuristics like SFDPOT guide exploratory testing?
3. What are the key components of a session-based exploratory testing report?
4. How do you write an actionable bug report?

---

## **Tips for Success**

- **Stay Focused**: Use your session charter to stay on track, but follow interesting discoveries when appropriate.
- **Be Thorough**: Record all observations, even minor ones—they might lead to critical issues.
- **Use Visuals**: Screenshots or videos add clarity to bug reports.
- **Prioritize Findings**: Highlight edge cases with high user impact or likelihood.

---

## **Next Training**

In **Training 6**, students will begin their journey into UI automation by setting up Playwright, configuring their environment in VS Code, and learning best practices for project organization.

