# **Month 3: Training 2 - Screen Reader & Keyboard Navigation Testing**

### **Objective**

In this training, students will gain hands-on experience with **screen reader compatibility** and **keyboard navigation testing**. By the end of this session, students will:

- Understand the role of **screen readers** in web accessibility.
- Learn how to conduct accessibility tests using a **screen reader**.
- Understand the importance of **keyboard navigation** in ensuring website accessibility for all users.
- Gain practical skills in navigating and assessing websites using only a keyboard.

---

### **Free Online Resources** (Mandatory)  

To supplement this training, students must explore the following resources to build foundational knowledge:

1. **[Using NVDA to Evaluate Web Accessibility (WebAIM)](https://webaim.org/articles/nvda/)**  
   - This resource provides an introduction to screen readers, explaining their function and how users with visual impairments rely on them to interact with digital content.

2. **[Introduction to Screen Readers (Deque)](https://www.youtube.com/watch?v=y0m7VEHoXMI)**  
   - A guide to using NVDA, a free screen reader for Windows, to perform accessibility tests.

3. **[NVDA 2024.4.1 User Guide](https://www.nvaccess.org/files/nvda/documentation/userGuide.html)**  
   - NVDA User Guide.

4. **[Keyboard Accessibility Guide (W3C)](https://www.w3.org/WAI/test-evaluate/preliminary/#keyboard)**  
   - A guide to conducting keyboard accessibility testing to ensure that all website functionalities are accessible without a mouse.

---

### **Topics Covered**

#### **1. Introduction to Screen Readers**
- **Explanation**: Screen readers are assistive technology tools that convert digital text into speech, allowing visually impaired users to interact with web content.
- **Key Insight**: Understanding how screen readers interpret and announce webpage elements helps developers create content that is accessible for all users, particularly those with visual impairments.

#### **2. Setting Up and Using NVDA**
- **Explanation**: NVDA (NonVisual Desktop Access) is a free, open-source screen reader for Windows that allows testers to evaluate how accessible a website is for visually impaired users.
  - **Step-by-Step Setup**: Download and install NVDA from [NVDA Download Page](https://www.nvaccess.org/download/). Follow the installation instructions to set up NVDA on your device.
  - **Practice Exercise**: Practice basic navigation with NVDA, including reading through headings, paragraphs, and forms.

#### **3. Keyboard Navigation Testing**
- **Explanation**: Keyboard navigation is an essential aspect of accessibility testing, ensuring that users who cannot use a mouse can still fully interact with web content.
  - **Key Techniques**: Using the **Tab** key to navigate between focusable elements, checking for logical tab order, and ensuring that all interactive elements are accessible.
  - **Key Insight**: All interactive elements should be operable via keyboard alone to comply with accessibility standards and to provide a positive experience for users with motor impairments.

#### **4. Common Issues and Fixes for Screen Reader and Keyboard Navigation**
- **Explanation**: Students will learn about the most common issues affecting screen reader compatibility and keyboard navigation, such as missing ARIA labels, improper use of headings, and inaccessible forms.
  - **Key Insight**: Proper labeling and logical structure significantly impact the experience of users relying on assistive technologies.

---

### **Assignment**

#### **Part 1: Understand Screen Reader Testing**
- **Objective**: Learn how screen readers like NVDA interact with websites and identify potential accessibility issues.
- **Instructions**:
  1. Visit the [Accessibility Tool Audit](https://alphagov.github.io/accessibility-tool-audit/test-cases.html).
  2. Focus on the **"Screen Reader Behavior"** examples, such as:
     - Missing or incorrect ARIA labels.
     - Non-descriptive link text (e.g., "Click here").
  3. Write a short explanation (2-3 sentences) of why these issues affect screen reader users and how they violate accessibility standards.

#### **Part 2: Practice Testing with NVDA**
- **Objective**: Understand common accessibility barriers and test how screen readers handle these scenarios.
- **Instructions**:
  1. Visit the [Accessibility Tool Audit](https://alphagov.github.io/accessibility-tool-audit/test-cases.html).
  2. Focus on the following examples:
     - **Non-Descriptive Links**: Links with generic text like "Click here" or "Read more."
     - **Missing or Incorrect ARIA Labels**: Form elements or buttons missing ARIA roles or attributes.
     - **Empty or Missing Alternative Text**: Images lacking alt text or with meaningless alt text.
     - **Empty Paragraphs**: HTML elements with unnecessary or empty paragraph tags.
     - **Color Contrast Issues**: Text with low contrast against its background, impacting readability.
  3. Use NVDA to simulate these issues:
     - Review the examples on the **Accessibility Tool Audit** site.
     - Test how NVDA interacts with similar elements on any available website or sandbox environment.
  4. Document findings for **two issues**, including:
     - What issue did you identify from the Accessibility Tool Audit?
     - Why is it a problem for screen reader users?
     - Which WCAG principle does it violate?
     - What recommendation would you provide?

#### **Part 3: Write Bug Reports**
- **Objective**: Practice documenting screen reader accessibility issues.
- **Instructions**:
  1. Choose **two issues** from your findings in **Part 2**.
  2. Write a bug report for each issue using this format:
     ```plaintext
     Title: [Describe the issue concisely]
     Steps to Reproduce:
       1. Open the test case on the Accessibility Tool Audit website.
       2. [Describe the exact interaction that caused the issue].
     Expected Result: [Describe what the screen reader should announce].
     Actual Result: [Describe what the screen reader actually announced].
     WCAG Reference: [Provide the relevant WCAG guideline, e.g., Perceivable - Name, Role, Value (4.1.2)].
     Recommendation: [Suggest a fix for the issue].
     ```
     - Example:
       ```plaintext
       Title: Screen reader does not announce dropdown options
       Steps to Reproduce:
         1. Navigate to the "Missing ARIA Labels" example on the Accessibility Tool Audit website.
         2. Use NVDA to navigate through the example dropdown options.
       Expected Result: NVDA should announce each dropdown option's text.
       Actual Result: NVDA does not announce any options.
       WCAG Reference: Perceivable - Name, Role, Value (4.1.2).
       Recommendation: Add ARIA roles and labels to each dropdown option.
       ```

#### **Submission Instructions**
- Submit all work in a **Google Doc**:
  1. Include your summary from **Part 1**.
  2. Document your findings from **Part 2**.
  3. Add your bug reports for **Part 3**.
- Share the Google Doc link in the designated Slack channel.

---

### **Key Learning Outcomes**
- Gain a hands-on understanding of how screen readers are used to access web content.
- Learn the importance of keyboard navigation and how to identify issues affecting keyboard-only users.
- Develop skills in identifying accessibility issues and suggesting appropriate fixes.

---

### **Key Interview Questions**
1. What are screen readers, and why are they important for web accessibility?
2. How do you test a website for screen reader compatibility?
3. What are the key elements to check when conducting keyboard navigation testing?
4. Why is logical tab order important for accessibility?

---

### **Tips for Success**
- **Take Your Time**: Navigating a website with a screen reader can be challenging at first. Take your time to understand how NVDA works.
- **Document Thoroughly**: Keep notes on your experience, especially challenges. This will be useful for the assignment and future accessibility testing.
- **Engage with Peers**: Share your findings on Slack and learn from your peers' experiences.

---

### **Next Training**
In **Training 3**, we will continue to build on accessibility concepts by exploring **ARIA roles** and **more advanced screen reader testing techniques** to enhance your understanding of accessible development.

