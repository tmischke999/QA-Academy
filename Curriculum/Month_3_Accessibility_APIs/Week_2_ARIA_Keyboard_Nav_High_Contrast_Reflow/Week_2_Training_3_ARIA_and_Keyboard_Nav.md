# **Month 3 Training 3 - ARIA Roles, Screen Reader, and Keyboard Navigation Usage**

### **Objective**

In this training, students will gain an understanding of **ARIA roles** and how they enhance web accessibility for assistive technologies. By the end of this session, students will:

- Understand the role of **ARIA (Accessible Rich Internet Applications)** in improving web accessibility.
- Learn how to use **ARIA attributes** effectively to bridge accessibility gaps.
- Gain hands-on experience using **screen readers** to test ARIA attributes and understand their impact on the user experience.
- Learn how to conduct **keyboard navigation testing** to ensure accessible interaction for users who do not rely on a mouse.

---

### **Free Online Resources** (Mandatory)  

To supplement this training, students must explore the following resources to build foundational knowledge:

1. **[WAI-ARIA Overview (W3C)](https://www.w3.org/WAI/standards-guidelines/aria/)**  
   - This resource provides an overview of WAI-ARIA, explaining its purpose and how it helps make dynamic web content and applications more accessible to users with disabilities.

2. **[How to Use ARIA Roles (MDN Web Docs)](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles)**  
   - A detailed guide on different ARIA roles, how they should be used, and the best practices to ensure proper implementation.

3. **[How to Perform a Web Accessibility Audit (freeCodeCamp)](https://www.freecodecamp.org/news/how-to-perform-a-web-accessibility-audit/)**  
   - This article provides practical examples of how to implement ARIA to improve the accessibility of various web components.

4. **[Keyboard Accessibility Guide (W3C)](https://www.w3.org/WAI/test-evaluate/preliminary/#keyboard)**  
   - This guide explains how to ensure that web content is accessible to users who rely solely on the keyboard, providing key strategies and best practices for effective keyboard navigation testing.

---

### **Topics Covered**

#### **1. Introduction to ARIA Roles**
- **Explanation**: ARIA roles are attributes that define the purpose of elements on a webpage, especially dynamic content that native HTML may not describe well.
- **Key Insight**: Using ARIA roles helps assistive technologies better interpret and communicate the purpose of interactive elements to users with disabilities.

#### **2. Common ARIA Roles and Their Applications**
- **Explanation**: Explore commonly used ARIA roles, such as `button`, `alert`, `dialog`, and `navigation`, and understand how they enhance interaction for screen reader users.
  - **Examples**: Practical scenarios where ARIA roles are crucial for accessibility, such as custom dropdown menus and modal dialogs.

#### **3. Testing ARIA with Screen Readers**
- **Explanation**: Students will learn how to use screen readers, such as **NVDA**, to test the implementation of ARIA roles and attributes.
  - **Step-by-Step Practice**: Use NVDA to navigate through an ARIA-enhanced sample webpage, focusing on how roles and attributes are announced.
- **Key Insight**: Proper testing ensures that ARIA roles are correctly implemented and improve the user experience rather than cause confusion.

#### **4. Keyboard Navigation Testing**
- **Explanation**: Keyboard navigation testing ensures that all functionalities on a webpage are accessible through the keyboard, without requiring a mouse. This includes verifying that focus moves logically through interactive elements and that no focus traps exist.
  - **Step-by-Step Practice**: Use the `Tab` key to navigate through an ARIA-enhanced sample webpage and observe how focus moves between interactive elements.
- **Key Insight**: Ensuring proper keyboard navigation is crucial for users with mobility impairments who cannot use a mouse.

#### **5. Best Practices for Using ARIA**
- **Explanation**: While ARIA can greatly enhance accessibility, improper use can hinder it. This topic covers best practices for applying ARIA without negatively impacting usability.
  - **Key Insight**: ARIA should be used to enhance, not replace, semantic HTML. Understanding the appropriate use of ARIA ensures better accessibility outcomes.

---

### **Assignment**

#### **Part 1: Understand ARIA and Keyboard Navigation Issues**
- **Objective**: Learn about common ARIA-related issues and barriers to keyboard navigation.
- **Instructions**:
  1. Visit the [Accessibility Tool Audit](https://alphagov.github.io/accessibility-tool-audit/test-cases.html).
  2. Focus on these examples:
     - **Missing ARIA Labels**: Understand how missing or incorrect ARIA roles affect accessibility.
     - **Keyboard Navigation Failures**: Explore examples where interactive elements (e.g., buttons or links) are not accessible using a keyboard.
  3. Write a short explanation (2-3 sentences) for each issue, describing:
     - Why it is a problem for users relying on ARIA and keyboard navigation.
     - Which WCAG principle is violated.

#### **Part 2: Practice ARIA and Keyboard Testing**
- **Objective**: Conduct hands-on testing to identify ARIA and keyboard navigation issues.
- **Instructions**:
  1. **Review the Accessibility Tool Audit**:
     - Visit the [Accessibility Tool Audit](https://alphagov.github.io/accessibility-tool-audit/test-cases.html).
     - Focus on these examples:
       - **Missing ARIA Labels**: Learn why ARIA labels are critical for screen reader users.
       - **Keyboard Navigation Failures**: Explore examples where interactive elements are inaccessible via keyboard.
  2. **Set Up Testing Environment**:
     - Install a browser extension for inspecting ARIA roles (e.g., [Chrome Accessibility Developer Tools](https://chrome.google.com/webstore/detail/accessibility-developer-to/)).
     - Familiarize yourself with using the **Tab** key to navigate web pages.
  3. **Perform the Following Tests**:
     - **Test 1: Missing ARIA Labels**:
       - Identify a button or interactive element that lacks an ARIA role or label.
       - Use your ARIA inspection tool to confirm the absence of ARIA attributes.
       - Note what happens when a screen reader encounters this element.
     - **Test 2: Keyboard Navigation Failures**:
       - Focus on testing dropdowns, modals, or buttons.
       - Attempt to navigate these elements using the **Tab** key only.
       - Identify any elements that cannot be accessed or lose focus unexpectedly.
  4. **Document Your Findings**:
     - For each test, write down:
       - The issue you identified.
       - Why it is a problem for users.
       - Which WCAG principle is violated.
       - A recommendation for fixing the issue.

  **Example Documentation for Part 2**

    ```plaintext
      Test: Missing ARIA Labels
      Issue: A button has no ARIA role or label.
      Why it’s a problem: Screen readers cannot announce the purpose of the button.
      WCAG Principle: Perceivable - Name, Role, Value (4.1.2).
      Recommendation: Add an ARIA role of “button” and a label describing the button’s function.
      
      Test: Keyboard Navigation Failures
      Issue: The dropdown menu cannot be accessed using the Tab key.
      Why it’s a problem: Keyboard-only users cannot select options in the dropdown.
      WCAG Principle: Operable - Keyboard Accessible (2.1.1).
      Recommendation: Add keyboard focus support to all dropdown options.
    ```

#### **Part 3: Write Bug Reports**
- **Objective**: Practice documenting ARIA and keyboard navigation issues.
- **Instructions**:
  1. Choose **two issues** from your findings in **Part 2**.
  2. Write a bug report for each issue using this format:
     ```plaintext
     Title: [Describe the issue concisely]
     Steps to Reproduce:
       1. Open [specific page or example from the Accessibility Tool Audit].
       2. [Describe the exact interaction that caused the issue].
     Expected Result: [Describe what should happen].
     Actual Result: [Describe what happens instead].
     WCAG Reference: [Provide the relevant WCAG guideline, e.g., Operable - Keyboard Accessible (2.1.1)].
     Recommendation: [Suggest a fix for the issue].
     ```
     - Example:
       ```plaintext
       Title: Keyboard navigation skips modal dialog
       Steps to Reproduce:
         1. Open the modal dialog example on the Accessibility Tool Audit website.
         2. Use the Tab key to navigate through the modal.
       Expected Result: All interactive elements within the modal are focusable using the keyboard.
       Actual Result: Keyboard navigation skips some buttons inside the modal.
       WCAG Reference: Operable - Keyboard Accessible (2.1.1).
       Recommendation: Ensure all interactive elements within the modal have proper focus management.
       ```

#### **Submission Instructions**
- Submit all work in a **Google Doc**:
  1. Include your summary from **Part 1**.
  2. Add your bug reports for **Part 3**.
  3. Document your findings from **Part 2**.
- Share the Google Doc link in the designated Slack channel.

---

### **Key Learning Outcomes**
- Understand the purpose and application of ARIA roles in web accessibility.
- Develop skills in implementing and testing ARIA roles to enhance the experience for screen reader users.
- Conduct keyboard navigation testing to ensure all elements are accessible without a mouse.
- Identify common pitfalls in ARIA usage and understand how to avoid them.

---

### **Key Interview Questions**
1. What are ARIA roles, and how do they contribute to web accessibility?
2. Can you provide examples of when to use ARIA roles in a web application?
3. How would you test the effectiveness of ARIA roles using a screen reader?
4. How would you conduct keyboard navigation testing, and why is it important for accessibility?
5. What are some best practices for implementing ARIA roles without harming accessibility?

---

### **Tips for Success**
- **Practice Makes Perfect**: Experiment with different ARIA roles to see how they impact screen reader output.
- **Stick to Semantic HTML**: Use ARIA to enhance elements when native HTML is insufficient, not as a replacement for semantic tags.
- **Peer Review**: Share your modified HTML document with a peer to get feedback on ARIA implementation.

---

### **Next Training**
In **Training 4**, we will explore **High Contrast and Reflow Testing** to ensure that web content is accessible for users with visual impairments and those relying on screen magnifiers or zoom functionality.

