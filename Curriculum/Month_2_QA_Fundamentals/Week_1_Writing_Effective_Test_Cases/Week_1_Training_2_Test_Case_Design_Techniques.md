# Week 1: Training 2 - Introduction to Test Case Design Techniques

## Objective
The goal of this training is to introduce students to foundational test case design techniques that will help optimize test coverage. By the end of this training, students will:

- Understand the purpose of test case design techniques.
- Learn how to use **Equivalence Partitioning (EP)** and **Boundary Value Analysis (BVA)** to enhance test cases.
- Apply EP and BVA to extend the test cases they developed in **Training 1**.

---

## Free Online Resources
To supplement this training, students are encouraged to explore the following resources before the session:

1. [Equivalence Partitioning and Boundary Value Analysis (Guru99)](https://www.guru99.com/equivalence-partitioning-boundary-value-analysis.html)
   - A beginner-friendly overview of EP and BVA, including examples.

2. [Software Testing Fundamentals - Test Design Techniques (SoftwareTestingHelp)](https://www.softwaretestinghelp.com/test-design-techniques-in-software-engineering/)
   - A detailed explanation of various test design techniques, including EP and BVA.

---

## Topics Covered

### 1. Test Case Design Techniques Overview

- **Why Use Test Case Design Techniques?**
  - Test case design techniques help create efficient and effective test cases that reduce redundancy and maximize test coverage with minimal effort.

### 2. Equivalence Partitioning (EP)

- **Definition**: EP is a technique that divides the input data of an application into partitions of equivalent data from which test cases can be derived.
- **How It Helps**: It reduces the number of test cases while ensuring comprehensive coverage by grouping similar types of input.
- **Examples**:
  - For a field that accepts **age**, partitions could be:
    - Negative values (e.g., -1)
    - Valid values (e.g., 18 - 65)
    - Values exceeding the limit (e.g., 100+)

**Key Insight**: By grouping similar inputs, EP ensures that we have adequate test coverage without being redundant.

### 3. Boundary Value Analysis (BVA)

- **Definition**: BVA focuses on testing the boundaries between partitions since these are often where defects are most likely to occur.
- **How It Helps**: It ensures that boundary conditions are verified thoroughly, including values just inside, on, and just outside the limits.
- **Examples**:
  - If the age field accepts values between **18 and 65**:
    - Test at boundaries like **17, 18, 65, 66**.

**Key Insight**: Boundary values are often where mistakes happen, so by focusing on these, we can catch issues that might not be obvious with more standard values.

### 4. Applying EP and BVA to Registration Test Cases

- Students will revisit the test cases they wrote for the **OpenCart registration form**.
- They will:
  - Identify equivalence classes for each input field.
  - Define boundary values for fields such as age, passwords, and numeric inputs (e.g., phone number).

**Key Insight**: Enhancing existing test cases with EP and BVA helps ensure that you are testing all critical inputs efficiently and thoroughly.

---

## Assignment
### **Accessing the OpenCart Demo Site**
- Students will use the following **OpenCart demo site** to practice writing test cases:
  - **OpenCart Demo Site**: [https://demo.opencart.com/](https://demo.opencart.com/)
  
### Part 1: Enhance Registration Test Cases

- **Objective**: Using **Equivalence Partitioning (EP)** and **Boundary Value Analysis (BVA)**, enhance the test cases previously written for the OpenCart registration feature.
- **Instructions**:
  - Review each input field in the registration form and apply EP and BVA to identify key partitions and boundaries.
  - Update the test case sheet in Google Sheets to include new test cases derived from these techniques.
- **Scenarios to Cover**:
  - **First Name Field**: Use BVA to test minimum and maximum character limits.
  - **Last Name Field**: Use BVA to test minimum and maximum character limits.
  - **Email Field**: Use EP to classify valid vs. invalid formats.
  - **Password Field**: Use BVA to test minimum and maximum character limits.

### Part 2: Create Login Test Cases for OpenCart

- **Objective**: Expand on the OpenCart scenarios by creating new test cases for the **login feature** using EP and BVA.
- **Instructions**:
  - Identify key input fields for the login form (e.g., email, password).
  - Apply **Equivalence Partitioning** to determine valid and invalid inputs for these fields.
  - Use **Boundary Value Analysis** to explore edge cases, such as minimum/maximum password length.
- **Scenarios to Cover**:
  - **Valid Login**: Correct email and password.
  - **Invalid Scenarios**: Incorrect email format, incorrect password, empty fields, etc.
  - **Boundary Conditions**: Email & Password length at its minimum and maximum limits.

**Template Update**: Ensure that each test case is updated to indicate:
- **Design Technique** used (e.g., EP or BVA).
- **Enhanced Expected Results** based on new partitions and boundary conditions.

---

## Submission Instructions

- **How to Submit**:
  - Update the existing Google Sheets document used for the registration form.
  - Add new sections or rows for the **login test cases** along with enhanced registration test cases.
  - Share the updated Google Sheet link in the designated Slack channel for review.

---

## Key Learning Outcomes

- Understand how to use Equivalence Partitioning and Boundary Value Analysis to improve test coverage.
- Be able to extend test cases using systematic techniques that focus on critical inputs.
- Gain experience in optimizing test cases for comprehensive coverage with minimal redundancy.

---

## Key Interview Questions

At the end of this training, students should be able to confidently answer the following questions in an interview:

1. What are Equivalence Partitioning and Boundary Value Analysis?
2. How do Equivalence Partitioning and BVA help improve test case design?
3. How would you apply EP and BVA to a registration form?
4. Why is it important to identify boundary conditions in testing?

---

## Tips for Success

- **Review Existing Test Cases**: Go over the test cases created in Training 1 and see how EP and BVA could add value.
- **Practice Identifying Partitions**: Think about how data inputs can be categorized and how each group could lead to different outcomes.
- **Focus on Boundaries**: Remember that defects are often found at the boundaries—testing at these points can often reveal issues that wouldn’t be apparent otherwise.

---

## Next Training

In **Training 3**, we will explore **Test Planning and Execution Fundamentals**. Be ready to take your test cases into practical execution, learning how to use testing cycles effectively and ensuring quality standards are met.

---
