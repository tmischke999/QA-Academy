# **Month 3 Training 4 - High Contrast and Reflow Testing**

### **Objective**

In this training, students will learn the principles and techniques behind **high contrast** and **reflow testing** to ensure web content is accessible to users with visual impairments or those relying on screen magnifiers. By the end of the training, students will:

- Understand the importance of **high contrast** for users with low vision.
- Learn how to perform **high contrast testing** to evaluate the accessibility of a webpage.
- Gain familiarity with **reflow testing** to ensure content remains usable and functional at different zoom levels or screen sizes.
- Be able to identify and report issues related to contrast, resizing, and usability.

---

### **Free Online Resources** (Mandatory)

To support this training, students must explore the following resources before engaging with the content:

1. **[How to Use High Contrast Mode (Microsoft Support)](https://support.microsoft.com/en-us/windows/turn-high-contrast-mode-on-or-off-in-windows-909e9d89-a0f9-a3a9-b993-7a6dcee85025#:~\:text=Select%20the%20Start%20button%2C%20then,like%20links%20and%20button%20text.)**

   - This resource provides step-by-step guidance on enabling high contrast mode on Windows, allowing students to simulate the experience of users with visual impairments.

2. **[A Guide to Windows High Contrast Mode (Smashing Magazine)](https://www.smashingmagazine.com/2022/06/guide-windows-high-contrast-mode/)**

   - A comprehensive guide on using Windows High Contrast Mode, exploring its practical uses and best practices for ensuring accessibility compliance.

3. **[Understanding Reflow (W3C)](https://www.w3.org/WAI/WCAG21/Understanding/reflow.html)**

   - Provides insights into conducting a comprehensive reflow audit, including reflow testing techniques.

4. **[Accessibility testing: zooming in (YouTube)](https://youtu.be/tj7j54T9FLc?si=H1hemOChf9YJzxf5)**

   - A video demonstration showing how to use reflow testing on a sample webpage, providing practical examples of what to look for.

5. **[What is Windows High Contrast Mode? (YouTube)](https://www.youtube.com/watch?v=7fsu8Wulqc4)**

   - A video demonstration showing how to use high contrast testing on a sample webpage, providing practical examples of what to look for.

---

### **Topics Covered**

#### **1. High Contrast Testing**

- **Explanation**: High contrast testing involves using color contrast settings to ensure that text and other key elements are easily readable for users with low vision.
  - **Why It Matters**: Proper color contrast is critical for users with low vision, allowing them to differentiate between elements without strain.
  - **Key Insight**: Testing websites in high contrast mode helps uncover issues that might make content unreadable or inaccessible to some users.

#### **2. Reflow Testing**

- **Explanation**: Reflow testing ensures that web content remains usable and properly formatted when resized or viewed at high zoom levels, such as 200% or more. This is important for users relying on screen magnifiers or smaller device screens.
  - **Step-by-Step Practice**: Students will use the browser's zoom settings to evaluate whether all elements of the page reflow correctly, without horizontal scrolling.
  - **Key Insight**: Ensuring content can reflow properly improves usability for users on different devices, including those with visual impairments.

#### **3. Common Accessibility Issues Related to Contrast and Reflow**

- **Explanation**: Discuss common problems that arise during high contrast and reflow testing, such as missing focus indicators, overlapping text, and elements that become hidden or unusable when zoomed in.
  - **Examples**: Examples of good and bad implementations will be reviewed to help students identify issues during their own testing.

---

### **Assignment**

#### **Part 1: Understand High Contrast and Reflow Issues**
- **Objective**: Learn how high contrast and reflow issues impact accessibility.
- **Instructions**:
  1. Visit the [Accessibility Tool Audit](https://alphagov.github.io/accessibility-tool-audit/test-cases.html).
  2. Focus on the following examples:
     - **Color Contrast Issues**: Understand how low contrast ratios affect readability.
     - **Reflow Problems**: Explore issues where content does not adapt correctly to small or zoomed screens.
  3. Write a short explanation (2-3 sentences) for each issue, describing:
     - Why it is a problem for users with low vision or on mobile devices.
     - Which WCAG principle is violated.

#### **Part 2: Practice Testing High Contrast and Reflow**
- **Objective**: Use examples from the **Accessibility Tool Audit** to understand how high contrast and reflow issues manifest in real-world scenarios.
- **Instructions**:
  1. **Review Specific Examples from the Accessibility Tool Audit**:
     - Visit the [Accessibility Tool Audit](https://alphagov.github.io/accessibility-tool-audit/test-cases.html).
     - Focus on these examples:
       - **Typography - Very Small Text Found**: Understand the challenges of small text sizes for readability.
       - **Typography - Poor Contrast**: Explore examples of insufficient text contrast against backgrounds.
       - **Content Reflow - Content Overflows Viewport**: Learn how content fails to adapt on zoomed or small screens.
  2. **Test High Contrast and Reflow Scenarios**:
     - **Test 1: Poor Contrast**:
       - Use the example of poor contrast from the Accessibility Tool Audit.
       - Verify contrast ratios using a tool like [Contrast Checker](https://webaim.org/resources/contrastchecker/).
     - **Test 2: Reflow Problems**:
       - Follow the example of content overflow from the Accessibility Tool Audit.
       - Simulate zooming to 200% or resizing the browser to a small screen.
  3. **Document Your Findings**:
     - For each test, write down:
       - The specific example you reviewed from the **Accessibility Tool Audit**.
       - What issue did you identify?
       - Why is it a problem for users with visual impairments or on small screens?
       - Which WCAG principle does it violate?
       - A recommendation for fixing the issue.

#### **Part 3: Write Bug Reports**
- **Objective**: Practice documenting high contrast and reflow issues.
- **Instructions**:
  1. Choose **two issues** from your findings in **Part 2**.
  2. Write a bug report for each issue using this format:
     ```plaintext
     Title: [Describe the issue concisely]
     Steps to Reproduce:
       1. Open the test case or page with the issue.
       2. [Describe the exact interaction that caused the issue].
     Expected Result: [Describe what should happen].
     Actual Result: [Describe what happens instead].
     WCAG Reference: [Provide the relevant WCAG guideline, e.g., Perceivable - Contrast Minimum (1.4.3)].
     Recommendation: [Suggest a fix for the issue].
     ```
     - Example:
       ```plaintext
       Title: Text has insufficient contrast against background
       Steps to Reproduce:
         1. Navigate to the homepage.
         2. Identify the text in the footer section.
       Expected Result: Text should have a contrast ratio of at least 4.5:1.
       Actual Result: Text has a contrast ratio of 2.8:1, making it hard to read.
       WCAG Reference: Perceivable - Contrast Minimum (1.4.3).
       Recommendation: Adjust text and background colors to achieve a 4.5:1 contrast ratio.
       ```

#### **Submission Instructions**
- Submit all work in a **Google Doc**:
  1. Include your summary from **Part 1**.
  2. Add your bug reports for **Part 3**.
  3. Document your findings from **Part 2**.
- Share the Google Doc link in the designated Slack channel.

---

### **Key Learning Outcomes**

- Gain a strong understanding of **high contrast** and **reflow** testing techniques.
- Develop the ability to assess **web content accessibility** for users with low vision or those needing screen magnification.
- Identify common **accessibility issues** related to contrast and reflow and provide constructive solutions.

---

### **Key Interview Questions**

1. What is the purpose of high contrast testing, and how does it help users with visual impairments?
2. How would you conduct reflow testing, and why is it important for accessibility?
3. Can you describe some common issues that arise during high contrast or reflow testing?
4. What tools or browser settings would you use to perform high contrast and reflow testing?

---

### **Tips for Success**

- **Experiment with Different Websites**: Practice high contrast and reflow testing on different types of websites to see a variety of issues.
- **Take Detailed Notes**: Write down the issues you encounter, why they are problems, and how they can be addressed. This will help in your reports and during interviews.
- **Understand User Perspectives**: Keep in mind how these accessibility issues might impact a user’s ability to access content comfortably and effectively.

---

### **Next Training**

In **Training 5**, we will begin our introduction to **API Testing**. Students will learn what APIs are, how they function, and why testing them is crucial for maintaining software quality.