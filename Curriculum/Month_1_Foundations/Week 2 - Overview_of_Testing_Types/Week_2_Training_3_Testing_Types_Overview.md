# Week 2: Training 3 - Testing Types Overview

## Objective
Introduce students to the different types of testing commonly used in QA. By the end of this training, students will:
- Understand the basics of manual testing, accessibility testing, and API testing.
- Gain foundational knowledge of WCAG guidelines, HTTP methods, and API testing best practices.
- Be able to identify the use cases and importance of each testing type in QA workflows.

---

## Free Online Resources
To support your research and learning, students are encouraged to explore the following resources before diving into the topics:
1. [Manual Testing Basics (Guru99)](https://www.guru99.com/manual-testing.html)  
   - An overview of manual testing, its processes, benefits, and limitations.
2. [Introduction to WCAG Guidelines (W3C)](https://www.w3.org/WAI/standards-guidelines/wcag/)  
   - Official guidelines for making web content accessible, covering the key principles of accessibility.
3. [What is API Testing? (Postman)](https://www.postman.com/api-platform/api-testing/)  
   - A detailed guide on API testing, including its types, significance in an API-first world, best practices, and how to use tools like Postman for effective testing.

---

## Topics Covered

### 1. What is Manual Testing?
Manual testing involves testing software manually to ensure it behaves as expected.
- **Key Characteristics:**
  - Performed without the use of automation tools.
  - Focused on identifying defects from the user’s perspective.
  - Includes activities such as exploratory testing, test case execution, and reporting issues.
- **Benefits:**
  - Helps identify usability and design issues.
  - Allows for detailed exploratory testing where automation is not feasible.
- **Limitations:**
  - Time-consuming and prone to human error.
  - Not suitable for repetitive tasks or large datasets.

**Key Insight:** Manual testing is crucial for assessing usability and the overall user experience, especially during the initial stages of development.

---

### 2. Introduction to Accessibility Testing and WCAG Basics
Accessibility testing ensures that software is usable by individuals with disabilities, in compliance with guidelines such as WCAG (Web Content Accessibility Guidelines).
- **Key Concepts:**
  - **WCAG Guidelines:** Provide standards for making web content accessible, based on the principles of being Perceivable, Operable, Understandable, and Robust (POUR).
  - **Testing Methods:**
    - **Keyboard Navigation Testing:** Verifying that all functionalities are accessible via keyboard.
    - **Screen Reader Testing:** Ensuring compatibility with screen readers like NVDA.
    - **Contrast Testing:** Checking for sufficient color contrast between text and background.
- **Importance:**
  - Ensures equal access for all users, regardless of ability.
  - Improves usability and reduces legal risks related to accessibility compliance.

**Key Insight:** Accessibility testing helps ensure inclusivity and can enhance the overall usability of the software for all users.

---

### 3. Overview of API Testing: Types and Best Practices
API testing focuses on verifying the communication between different software systems.
- **Key Concepts:**
  - **What is an API?**
    - An Application Programming Interface (API) allows different software systems to communicate by sending requests and receiving responses.
  - **API Testing Types:**
    - **Contract Testing:** Ensures that the API adheres to its defined contract, which specifies the expected inputs and outputs.
    - **Unit Testing:** Verifies that individual API endpoints return the correct response to given requests.
    - **End-to-End Testing:** Validates complete workflows involving multiple endpoints to ensure seamless user journeys.
    - **Load Testing:** Confirms that the API can handle expected peak traffic loads without failing.
    - **Security Testing:** Identifies vulnerabilities such as unauthorized access or data breaches within the API.
  - **Best Practices for API Testing:**
    - **Shift Left Testing:** Conduct API tests early in the development cycle to catch issues before they reach production.
    - **Automate Tests:** Use tools like Postman to automate repetitive tests, ensuring consistent quality checks.
    - **Monitor APIs in Production:** Utilize API monitoring alongside testing to ensure ongoing reliability and performance.

**Key Insight:** API testing is critical in an API-first development model, helping ensure APIs remain reliable, secure, and high-performing throughout the lifecycle.

---

## Assignment

### Task: Research and Summarize a Testing Type
- Choose one of the following testing types to research:
  - Manual Testing
  - Accessibility Testing
  - API Testing
- Write a short summary (1–2 paragraphs) in Google Docs. Your summary should include:
  - A brief explanation of the testing type.
  - Its benefits and limitations.
  - An example of how it might be used in a QA process.
  - For API Testing: Include a specific type of API test (e.g., Contract Testing, Load Testing) and its purpose.

### Submission Instructions:
1. Open Google Docs and create a new document.
2. Title your document: **"Week 2 Training 3 - [Testing Type] Summary"**.
3. Complete the summary based on your research.
4. **Submitting Your Work:**
   - **Option 1 (Preferred):**  
     - Share your completed Google Doc with the instructor by using the provided email address.  
     - Alternatively, share the Google Doc link directly in the Slack group for feedback (ensure the sharing permissions allow "Anyone with the link" to view or comment).  
   - **Option 2 (Optional):**  
     - Save the Google Doc in your Drive for future use.  
     - You will learn how to upload it to GitHub in Week 3.

### Notes:
- If sharing in Slack, copy the document link (File > Share > Copy link) and post it in the designated Slack channel (e.g., `#qa-academy`) with a message like:  
  *"Here is my completed Testing Type Summary for Training 3: [Your Name]. Please review!"*

---

## Key Interview Questions
By the end of this training, students should be able to confidently answer the following questions in an interview:
1. What is manual testing, and when is it used?
2. What are the core principles of accessibility testing?
4. How does accessibility testing benefit the overall user experience?
5. What are the different types of API testing, and what is the purpose of each type?

---

## Tips for Success
- Focus on understanding the unique role of each testing type in QA workflows.
- Use the free resources to supplement your knowledge and include specific examples in your summary.
- Keep your summary concise and clear, with practical use cases where possible.
- Keep a **log of interview questions** you encounter during this course to help you prepare for interviews.

---

## Next Training
In **Training 4**, we will explore key QA tools, including text editors, Postman for API testing, and browser developer tools.
