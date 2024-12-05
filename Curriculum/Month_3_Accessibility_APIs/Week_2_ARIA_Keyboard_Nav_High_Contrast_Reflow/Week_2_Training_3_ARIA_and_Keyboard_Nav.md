# **Month 3 Training 3 - ARIA Roles, Screen Reader, and Keyboard Navigation Usage**

---

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

#### **Part 1: Implement ARIA Roles**
- **Objective**: Apply ARIA roles to improve the accessibility of a sample HTML document.
- **Instructions**:
  1. **Download the sample HTML file** provided in the Slack channel.
  2. **Add ARIA roles** where appropriate to enhance the accessibility of the document (e.g., add `role="button"` to interactive elements that lack semantic tags).
  3. **Test your implementation** using NVDA to ensure that the roles are correctly recognized.
- **Specific Task**: Submit your modified HTML file along with a short write-up explaining the ARIA roles you added and why.

#### **Part 2: ARIA and Keyboard Navigation Testing with Screen Readers**
- **Objective**: Evaluate the effectiveness of ARIA roles and keyboard navigation by navigating a webpage with a screen reader.
- **Instructions**:
  1. **Choose a public website** that uses ARIA roles (e.g., an e-commerce site with dynamic content).
  2. **Use NVDA** to navigate through the page, focusing on how ARIA roles are announced and how well the keyboard navigation works.
  3. Identify any areas where ARIA roles improve accessibility and any where they might be used incorrectly.
  4. Document the **keyboard navigation flow** to identify focus issues or traps.
- **Specific Task**: Document at least three instances where ARIA roles enhanced accessibility and one instance of incorrect usage, along with suggestions for improvement. Additionally, report any keyboard navigation issues found and how they could be resolved.

---

### **Submission Instructions**
- **How to Submit**: Upload your modified HTML file and Google Doc write-up to the designated Slack channel. Ensure sharing settings allow "Anyone with the link" to view.

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
