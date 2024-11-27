# Week 3: Training 5 - Introduction to Regression Testing and Automation Candidates

## Objective

The purpose of this training is to explain the role and importance of regression testing in software quality assurance, and to introduce students to identifying automation candidates among existing test cases. By the end of this session, students will:

- Understand what regression testing is and why it is crucial.
- Learn how to identify regression test cases.
- Develop an understanding of which test cases are suitable for automation and why.

---

## Free Online Resources

Students are encouraged to explore the following resources before this session to gain a foundational understanding of regression testing and automation:

- [What is Regression Testing (Guru99)](https://www.guru99.com/regression-testing.html)  
  An introduction to regression testing, why it's important, and how it's performed.
- [Automation Testing Tutorial (Guru99)](https://www.guru99.com/automation-testing.html)  
  An overview of automation testing, focusing on its benefits, tools, and best practices.

### Videos on Regression Testing

**Tip**: These videos provide a visual explanation of regression testing and its application.

- [Regression Testing Explained](https://youtu.be/5A7J5cM2e7c?si=cEernBfNrG6tIvrd&t=33)  
- [How to Decide Which Types of Test Cases to Automate](https://www.youtube.com/watch?v=0-opuGZsHtM)  

---

## Topics Covered

### 1. What is Regression Testing?

**Definition**: Regression testing is a type of software testing that ensures that new code changes do not adversely affect the existing functionalities of an application.

**Key Insight**: Any time new features are added or existing ones are modified, there is a risk that other parts of the software may break. Regression testing helps to mitigate this risk.

**Why is Regression Testing Important?**
- **Stability**: Ensures that the software remains stable after changes.
- **Risk Reduction**: Helps to identify defects that might have been inadvertently introduced due to recent changes.
- **Continuous Quality**: Integral in maintaining software quality throughout the development lifecycle.

**Example**: After implementing a new feature on the **OpenCart registration page**, regression tests ensure that not only the new feature works but also that existing functionality like **login** or **checkout** remains unaffected.

### 2. Identifying Regression Test Cases

**Key Strategies**:
- **High-Risk Areas**: Identify the parts of the application that have high impact or are frequently used.
- **Recently Modified Areas**: Focus on features or components where recent changes have been made.
- **Business-Critical Features**: Include test cases that verify essential workflows for end-users.

**Practical Exercise**:  
Identify existing test cases for OpenCart (registration, login, checkout) that would need to be rerun after each new feature release or major code change.

**Key Insight**: Regression test cases are often a mix of functional and integration tests, ensuring that both individual components and end-to-end workflows remain stable.

### 3. Can Manual Test Cases Be Both Regression and Automated?

**Manual Test Cases as Both Regression and Automation Candidates**:
- **Manual Test Cases for Regression**: Manual test cases can be part of a regression suite, especially when validating areas that are frequently modified or are critical to business operations.
- **Automation Considerations**: Some manual regression test cases are strong candidates for automation if they meet criteria like being repetitive, time-consuming, or stable.
- **Dual Role**: It's possible for a test case to be both manually executed during initial development phases and automated for future regression runs. This allows for comprehensive coverage initially and efficiency over time.

**Key Insight**: Not all regression test cases need to be automated, but automation can significantly enhance efficiency for repetitive and high-impact scenarios.

### 4. Benefits of Automation

  - **Speed**: Automating regression tests allows for faster execution.
  - **Repetition**: Regression tests need to be executed repeatedly, which makes them perfect candidates for automation.
  - **Consistency**: Automation provides consistent results without the variability of manual testing.

**Identifying Candidates for Automation**:
- **Repetitive Tests**: Look for test cases that need to be run frequently (e.g., login functionality across browsers).
- **Data-Driven Tests**: Scenarios involving multiple sets of input data (e.g., different registration forms).
- **Stable Areas**: Features that are unlikely to change often are good automation candidates.

**Key Insight**: Automation helps free up QA testers to focus on exploratory testing and complex scenarios rather than repetitive, time-consuming tests.

---

## Practical Exercise: Reviewing and Marking Test Cases

### Task: Identify Automation Candidates

- **Objective**: Review existing OpenCart test cases for **registration** and **login** and mark those suitable for regression testing and automation.
- **Steps to Follow**:
  1. Review all test cases created so far, including registration, login, and exploratory test cases.
  2. **Mark each test case** for:
     - **Regression**: Whether the test case should be included in regression testing.
     - **Automation Candidate**: Whether the test case is suitable for automation.
  3. Document reasoning for automation selection: Add a comment to each test case explaining why it is or isn’t suitable for automation.

**Key Insight**: Regression testing ensures stability, and automation helps achieve efficiency and consistency in testing large, frequently changing codebases.

---

## Assignment

### Accessing the OpenCart Demo Site

Students will use the following **OpenCart demo site** to conduct the practical exercise:  
**OpenCart Demo Site**: [https://demo.opencart.com/](https://demo.opencart.com/)

### Assignment Instructions

- **Objective**: Mark suitable test cases for **regression testing** and **automation**.
- **Instructions**:
  - **Review**: Go through the test cases created for OpenCart’s registration and login features.
  - **Update Google Sheets**: Mark each test case with:
    - **Regression Suitability**: Yes/No
    - **Automation Candidate**: Yes/No
    - **Reason**: A short explanation for why the test case was marked (e.g., "Frequent usage" or "Stable functionality").
  - **Deliverable**: Submit the updated Google Sheets document via Slack for review.

---

## Submission Instructions

- **How to Submit**:
  - Update your **Google Sheets** test case document.
  - Share the updated Google Sheets in the designated Slack channel.
  - Ensure permissions are set to "Anyone with the link can view/comment."

---

## Key Learning Outcomes

- Understand the concept and purpose of regression testing.
- Learn how to identify which test cases should be part of a regression suite.
- Develop skills in identifying automation candidates among test cases.
- Gain an understanding of the value of automating repetitive, stable, or high-value test cases.

---

## Key Interview Questions

At the end of this training, students should be able to confidently answer the following questions in an interview:

1. What is regression testing, and why is it important?
2. How do you decide which test cases to include in a regression suite?
3. What are the benefits of automating regression tests?
4. How do you determine which test cases are suitable for automation?

---

## Tips for Success

- **Think Risk**: Prioritize test cases based on their potential impact if broken.
- **Stay Practical**: Consider the time and effort required to automate a test case versus the value it adds.
- **Use Real-World Examples**: Practice identifying regression and automation candidates in real-world applications to improve your decision-making skills.

---

## Next Training

In **Training 6**, we will discuss **Bug Reporting Fundamentals**, including how to create detailed, actionable bug reports, and effectively communicate findings with developers to ensure efficient resolution.
