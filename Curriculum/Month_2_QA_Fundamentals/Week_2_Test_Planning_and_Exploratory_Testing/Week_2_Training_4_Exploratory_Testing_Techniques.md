# Week 3: Training 4 - Exploratory Testing Techniques

## Objective

The purpose of this training is to introduce students to exploratory testing and the mindset required to effectively uncover hidden issues beyond documented test cases. By the end of this session, students will:

- Understand what exploratory testing is and how it differs from scripted testing.
- Learn techniques to explore an application more intuitively.
- Develop skills to identify gaps in existing test coverage.
- Apply exploratory testing techniques to expand the existing OpenCart test cases.

---

## Free Online Resources

Students are encouraged to explore the following resources before this session to gain an understanding of exploratory testing techniques:

- [What is Exploratory Testing (Guru99)](https://www.guru99.com/exploratory-testing.html)  
  An overview of exploratory testing and its key benefits.
- [Exploratory Testing Techniques (Software Testing Help)](https://www.softwaretestinghelp.com/exploratory-testing/)  
  A list of effective techniques to enhance your exploratory testing skills.

### Videos on Exploratory Testing

**Tip**: If you want to adjust the playback speed on YouTube, click on the settings (cog) icon on the video and select your desired speed.

- [Exploratory testing for beginners and why it's important](https://www.youtube.com/watch?v=Pq1Zw7kl2SQ)

---

## Topics Covered

### 1. What is Exploratory Testing?

**Definition**: Exploratory testing is a simultaneous process of test design and test execution that emphasizes learning, discovery, and adaptability.

**Key Insight**: Unlike scripted testing, which relies on predefined test cases, exploratory testing is about understanding the application and dynamically investigating its behavior to find potential defects.

### 2. Differences Between Scripted and Exploratory Testing

**Key Differences**:

- **Scripted Testing**: Follows predefined steps and expected results.
- **Exploratory Testing**: Emphasizes exploring the application without predefined steps to uncover unexpected behavior.

**Key Insight**: Both approaches are complementary. Scripted testing ensures coverage of expected functionality, while exploratory testing captures the unexpected.

### 3. Techniques for Exploratory Testing

- **Session-Based Testing**: Time-boxed sessions with specific goals to focus exploration.
- **Mind Mapping**: Creating a visual representation of the feature or workflow to generate testing ideas.
- **Using Heuristics**: Heuristics are practical techniques to guide your exploration. They help you think from different perspectives to uncover potential issues.
  - **CRISP-DM**: This heuristic helps you consider each aspect of the application from **Context**, **Risk**, **Input**, **State**, and **Platform**. It's especially helpful when determining which scenarios might have the highest impact.
  - **SFDPOT**: This heuristic stands for **Sanity, Functional, Database, Performance, Operations, Tests**. It provides a structured way to think about an application holistically, helping you cover aspects that might otherwise be overlooked.
- **Bug Hunting Sessions**: Focusing specifically on finding issues with a particular feature.

**Key Insight**: These techniques help structure the exploratory process, even though it remains flexible and dynamic.

### Additional Examples of Heuristics

- **CRISP-DM Example**: When testing the registration page in OpenCart, consider each aspect:  
  - **Context**: What is the context of the registration page in the entire user journey?
  - **Risk**: What risks are associated with incorrect registrations?
  - **Input**: Are all fields being validated correctly with different types of input?
  - **State**: Does the page work correctly when in different states (e.g., filled vs. empty)?
  - **Platform**: Does the functionality work consistently across different browsers or devices?

- **SFDPOT Example**: When performing exploratory testing on the login feature:
  - **Sanity**: Does the login process work with correct credentials?
  - **Functional**: Are all user types able to log in as intended?
  - **Database**: Are user details correctly reflected in the database after login?
  - **Performance**: Does the login page load quickly without delays?
  - **Operations**: What happens if the server goes down during the login process?
  - **Tests**: Are there any existing tests that need to be adjusted based on findings?

---

## Practical Exercise: Exploratory Testing for OpenCart

- **Task**: Expand the **registration and login test cases** for OpenCart by using exploratory testing techniques to identify additional test scenarios.
- **Steps to Follow**:
  1. Set a timer for **30 minutes** to perform a focused exploratory testing session on **OpenCart registration**.
  2. **Note down** any unexpected behavior, errors, or usability issues encountered.
  3. Document new test cases or scenarios discovered during exploration.

**Key Insight**: Exploratory testing often leads to the discovery of edge cases or overlooked scenarios that were not covered by the initial test plan.

### 5. Documenting Exploratory Testing

- **Note-Taking Styles**:
  - **Charter**: Define a mission or purpose for your testing session.
  - **Session Notes**: Capture observations, questions, and issues found.
  - **Mind Maps**: Create diagrams to document new areas explored and potential test paths.

**Key Insight**: Documenting your exploratory sessions ensures that findings are reproducible and helps share insights with the team.

---

## Assignment

### Accessing the OpenCart Demo Site

Students will use the following **OpenCart demo site** to conduct the test executions:  
**OpenCart Demo Site**: [https://demo.opencart.com/](https://demo.opencart.com/)

### Part 1: Conduct an Exploratory Testing Session

- **Objective**: Use exploratory testing techniques to expand on the **OpenCart registration and login features**.
- **Instructions**:
  - Set a **30-minute timer** for an exploratory testing session.
  - During the session, explore both the **registration** and **login** functionalities of OpenCart.
  - **Document your observations** in a Google Doc, including any errors, usability issues, or unexpected behaviors.
  - Create **at least three new test cases** based on your findings.

### Part 2: Update Google Sheets with New Test Cases

- **Objective**: Add new exploratory test cases to your existing **Google Sheets** document.
- **Instructions**:
  - Update the **Google Sheets** test case document with the new scenarios identified during your exploratory session.
  - Include columns for **Test Case ID**, **Title**, **Steps**, **Expected Results**, and **Actual Results** (if executed).
  - Mark any issues as **Potential Defects**.

---

## Submission Instructions

- **How to Submit**:
  - Share the **Exploratory Testing Google Doc** in the designated Slack channel.
  - Update your **Google Sheets** document with new test cases and share it for review.
  - Ensure permissions are set to "Anyone with the link can view/comment."

---

## Key Learning Outcomes

- Understand the concept and purpose of exploratory testing.
- Learn techniques to effectively explore an application and identify gaps in testing.
- Practice conducting exploratory sessions and documenting findings.
- Develop a flexible testing mindset to uncover potential defects beyond scripted test cases.

---

## Key Interview Questions

At the end of this training, students should be able to confidently answer the following questions in an interview:

1. What is exploratory testing, and how does it differ from scripted testing?
2. How do you structure an exploratory testing session?
3. What techniques can you use to improve exploratory testing coverage?
4. How would you document the findings from an exploratory testing session?

---

## Tips for Success

- **Stay Curious**: Treat exploratory testing like a puzzle—look for inconsistencies and unexpected behaviors.
- **Focus and Adapt**: Set clear goals for each session but remain adaptable to follow any issues you encounter.
- **Document Thoroughly**: Keep detailed notes of what you test, issues found, and ideas for further exploration.
- **Share Your Findings**: Collaboration can uncover insights you may have missed—share findings with peers for additional feedback.

---

## Next Training

In **Training 5**, we will cover **Introduction to Regression Testing and Automation Candidates**, explaining the purpose of regression testing and introducing identifying automation candidates among test cases.