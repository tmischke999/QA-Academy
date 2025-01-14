# **Month 3: Training 1 - Introduction to WCAG Guidelines**

### **Objective**

In this training, students will be introduced to the fundamentals of **accessibility testing**, focusing specifically on **WCAG guidelines**. By the end of this session, students will:

- Understand the purpose and importance of **WCAG** in making websites accessible.
- Learn about the **four key principles** of WCAG.
- Gain practical experience in evaluating websites using WCAG guidelines.

---

### **Free Online Resources**  

To supplement this training, students should explore the following resources before diving into the topics:

1. **[Introduction to WCAG (WebAIM)](https://webaim.org/intro/)**  
   - An overview of WCAG and its importance in web accessibility.

2. **[WCAG Quick Reference (W3C)](https://www.w3.org/WAI/WCAG21/quickref/)**  
   - A detailed reference for the WCAG 2.1 guidelines.

3. **[How to Perform a Web Accessibility Audit](https://www.freecodecamp.org/news/how-to-perform-a-web-accessibility-audit/)**  
   - Learn how to conduct a WCAG audit on websites using accessibility tools.

4. **[Web Content Accessibility Guidelines (WCAG 2.1) Crash Course (YouTube)](https://www.youtube.com/watch?v=NEK3aMPs1Us)**  
   - A brief video introduction to WCAG and its practical application.

---

### **Topics Covered**

#### **1. What is WCAG?**
- **Explanation**: WCAG (Web Content Accessibility Guidelines) are a set of guidelines created to ensure websites are accessible to people with disabilities, covering visual, auditory, cognitive, and navigational needs.
- **Key Insight**: The WCAG guidelines are crucial for developing websites that are accessible to a wide range of users, including people with visual impairments, hearing disabilities, or cognitive challenges.

#### **2. The Four Principles of WCAG**
- **Perceivable**: Content must be presented in ways that users can perceive, including providing text alternatives for non-text content, like images, videos, or audio.
  - **Example**: Images without alt text are not perceivable by screen readers for visually impaired users.
- **Operable**: User interface components must be operable by a variety of input methods, such as keyboard navigation. This ensures that all users can interact with a website.
  - **Example**: Websites must be navigable using a keyboard alone, without relying on a mouse.
- **Understandable**: Information and operation must be understandable to all users, including predictable page behavior, simple language, and error identification.
  - **Example**: If a form contains an error, the error message should be clear and explain how to fix it.
- **Robust**: Content must be robust enough to work with current and future technologies, ensuring compatibility with a wide range of devices and user agents.
  - **Example**: A site should work properly on both mobile phones and desktop browsers.

#### **3. Practical Applications of WCAG**
- **Explanation**: Students will review real-world examples of WCAG implementation, understanding how web developers can meet these guidelines to ensure accessibility for all users.
- **Key Insight**: By implementing WCAG principles, developers create more inclusive digital experiences, helping to bridge accessibility gaps for people with disabilities.

---

### **Assignment**

#### **Part 1: Understand WCAG Guidelines**
- **Objective**: Learn about common accessibility issues and their impact on users.
- **Instructions**:
  1. Visit the [Accessibility Tool Audit](https://alphagov.github.io/accessibility-tool-audit/test-cases.html).
  2. Navigate to the **"Content Identified by Location"** section.
  3. Read the examples provided, focusing on:
     - How content is described only by its position (e.g., "Click the button on the left").
     - Why this creates challenges for screen reader users.
  4. Write a short explanation (2-3 sentences) of what the issue is and why it violates accessibility standards.

#### **Part 2: Write Bug Reports**
- **Objective**: Practice documenting accessibility issues.
- **Instructions**:
  1. Choose **two issues** from the **Accessibility Tool Audit** examples.
     - Suggested sections: **Empty Paragraphs**, **Missing ARIA Labels**, or **Text Size**.
  2. For each issue:
     - Write a bug report using the following format:
       ```plaintext
       Title: [Describe the issue concisely]
       Steps to Reproduce:
         1. Go to [specific page/section].
         2. Identify [specific element causing the issue].
       Expected Result: [Describe what should happen if the issue did not exist.]
       Actual Result: [Describe what happens currently.]
       WCAG Reference: [Provide the exact WCAG guideline, e.g., Perceivable - Text Alternatives (1.1.1)]
       Recommendation: [Suggest a fix for the issue, e.g., Add appropriate alt text.]
       ```
     - Example:
       ```plaintext
       Title: Button not accessible to screen readers
       Steps to Reproduce:
         1. Navigate to the homepage.
         2. Tab to the "Learn More" button.
       Expected Result: Screen readers announce the button text as "Learn More."
       Actual Result: The button is announced as "Button."
       WCAG Reference: Operable - Name, Role, Value (4.1.2)
       Recommendation: Add an ARIA label to the button describing its function.
       ```

#### **Part 3: Execute a Sample Accessibility Test**
- **Objective**: Conduct a hands-on accessibility audit.
- **Instructions**:
  1. Use the website [The Internet](https://the-internet.herokuapp.com).
  2. Test the **login page** for the following:
     - Missing alt text on images.
     - Keyboard navigation issues.
     - Text contrast problems.
  3. Document findings for **one issue**:
     - What did you test?
     - What issue did you find?
     - Which WCAG principle was violated?
     - What recommendation would you provide?

#### **Submission Instructions**
- Submit all work in a **Google Doc**:
  1. Include your summary from **Part 1**.
  2. Add your bug reports for **Part 2**.
  3. Document your test findings for **Part 3**.
- Share the Google Doc link in the designated Slack channel.

---

### **Key Learning Outcomes**
- Understand the purpose and structure of WCAG guidelines.
- Learn how to evaluate websites using WCAG principles.
- Develop skills in identifying accessibility issues and providing remediation recommendations.

---

### **Key Interview Questions**
1. What is WCAG, and why is it important for web development?
2. What are the four principles of WCAG, and how do they contribute to accessibility?
3. How can you identify and address common accessibility issues on a website?
4. Why is it important for content to be operable using a keyboard?

---

### **Tips for Success**
- **Take Notes**: Document each WCAG principle and its application in detail. This will help reinforce your understanding.
- **Practice**: Use different websites for practice to improve your ability to identify accessibility issues.
- **Seek Feedback**: Engage in discussions on Slack to get feedback on your accessibility audit findings.

---

### **Next Training**
In **Training 2**, we will dive deeper into **screen reader compatibility** and **keyboard navigation testing**, giving you hands-on experience with the NVDA screen reader and other essential tools for accessibility testing.

