# Week 3: Training 5 - Accessibility Tools Overview

---

## Objective

Introduce students to the tools and techniques used for accessibility testing. By the end of this training, students will:

- Understand the importance of accessibility testing in QA workflows.
- Gain familiarity with popular accessibility tools and their purposes.
- Download, set up, and perform a comprehensive accessibility audit using multiple tools.

---

## Free Online Resources

To support your understanding and use of accessibility tools:

- [How Accessibility Testing Impacts QA](https://www.youtube.com/watch?v=EwqYxTj0lbA)
- [NVDA User Guide](https://www.nvaccess.org/documentation/)
- [Getting Started with Axe](https://www.deque.com/axe/)
- [Lighthouse Accessibility Overview](https://developers.google.com/web/tools/lighthouse/)
- [Wave Tool Guide](https://wave.webaim.org/help)
- [WebAIM Color Contrast Basics](https://webaim.org/resources/contrastchecker/)
- [Keyboard Accessibility Guide (W3C)](https://www.w3.org/WAI/test-evaluate/preliminary/#keyboard)
- [Reflow and Zoom Requirements (W3C)](https://www.w3.org/WAI/WCAG21/quickref/?showtechniques=142#resize-content)

---

## Topics Covered
**Note:** If you want to adjust the playback speed on YouTube, click on the settings (cog) icon on the video and select your desired speed.

### 1. NVDA (NonVisual Desktop Access)
- **Purpose:**
  A free, open-source screen reader for Windows that allows users to test how visually impaired individuals interact with web content.

  - **User Guide:** [NVDA User Guide](https://www.nvaccess.org/documentation/)
  - **YouTube Video:** [NVDA Introduction](https://www.youtube.com/watch?v=-L00rrNNaGs)

  **How to Download and Set Up:**
  - Visit [NVDA Download Page](https://www.nvaccess.org/download/).
  - Follow the installation instructions to set up NVDA on your Windows device.

---

### 2. Axe (Browser Extension)
- **Purpose:**
  A browser extension for detecting accessibility issues in web applications.

  - **User Guide:** [Getting Started with Axe](https://www.deque.com/axe/)
  - **YouTube Video:** [Introduction to Axe](https://www.youtube.com/watch?v=iRGB40c_YJc)

  **How to Download and Set Up:**
  - Visit [Axe Extension for Chrome](https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd).
  - Click 'Add to Chrome' to install the extension.

---

### 3. Lighthouse (Chrome DevTools)
- **Purpose:**
  A built-in tool in Chrome used to audit web performance, SEO, and accessibility.

  - **User Guide:** [Lighthouse Accessibility Overview](https://developers.google.com/web/tools/lighthouse/)
  - **YouTube Video:** [Lighthouse Tutorial](https://www.youtube.com/watch?v=K419UlgZ_b0)

  **How to Access and Set Up:**
  - Open Google Chrome and navigate to any webpage.
  - Right-click on the page and select 'Inspect'.
  - Click on the 'Lighthouse' tab to perform an audit.

---

### 4. Wave (Web Accessibility Evaluation Tool)
- **Purpose:**
  A tool for visually identifying accessibility issues directly on the webpage.

  - **User Guide:** [Wave Tool Guide](https://wave.webaim.org/help)
  - **YouTube Video:** [Wave Tool Overview](https://www.youtube.com/watch?v=EGJmNyPuKJo)

  **How to Access and Set Up:**
  - Visit [Wave Tool Page](https://wave.webaim.org/).
  - You can use the online version by entering a webpage URL or add the Wave extension to your browser.

---

### 5. Color Contrast Checkers (WebAIM)
- **Purpose:**
  Verifies that text and background colors meet WCAG contrast ratio guidelines.

  - **User Guide:** [WebAIM Color Contrast Basics](https://webaim.org/resources/contrastchecker/)
  - **YouTube Video:** [Color Contrast Accessibility](https://www.youtube.com/watch?v=T1UoZZ45beQ)

  **How to Access:**
  - Visit [WebAIM Color Contrast Checker](https://webaim.org/resources/contrastchecker/).
  - Use this tool to test color combinations for accessibility compliance.

---

### 6. Mobile Screen Readers: TalkBack (Android) and VoiceOver (iOS)
- **Purpose:**
  Built-in tools on Android and iOS devices for testing accessibility on mobile applications.

  **How to Set Up:**
  - **TalkBack (Android):** Go to Settings > Accessibility > TalkBack and enable it to test how users interact with your app.
  - **VoiceOver (iOS):** Go to Settings > Accessibility > VoiceOver and enable it to test how users interact with your app.

---

### 7. Keyboard Navigation Testing
- **Purpose:**
  To ensure all functionalities are accessible via keyboard only, without requiring a mouse.

  - **User Guide:** [Keyboard Accessibility Guide (W3C)](https://www.w3.org/WAI/test-evaluate/preliminary/#keyboard)
  - **YouTube Video:** [Keyboard Navigation Tutorial](https://www.youtube.com/watch?v=uO8NJqAtMLM)

  **How to Perform:**
  - Use the Tab key to navigate through elements on a webpage and verify that all interactive elements are reachable and usable.

---

### 8. Reflow Testing
- **Purpose:**
  To verify that content remains usable and readable when resized or zoomed, ensuring it conforms to WCAG reflow guidelines.

  - **User Guide:** [Reflow and Zoom Requirements (W3C)](https://www.w3.org/WAI/WCAG21/quickref/?showtechniques=142#resize-content)
  - **YouTube Videos:** [Reflow Testing Basics](https://www.youtube.com/watch?v=3NlmMmb1ka4) & [Advanced Reflow Techniques](https://www.youtube.com/watch?v=o-QorhbXEMI)

  **How to Perform:**
  - Adjust the browser window size or use the browser zoom feature to check that content reflows properly without horizontal scrolling.

---

## Assignment: Perform a Comprehensive Accessibility Audit

### Task

Perform a comprehensive accessibility audit using the tools introduced in this training.

### Prepare for the Audit

Follow the setup instructions to ensure the following tools are installed and ready for use:

- **NVDA** for screen reader testing.
- **Axe** for detecting accessibility issues.
- **Wave** for visualizing accessibility problems.
- **Lighthouse** for a detailed accessibility report.
- **Color Contrast Checkers (WebAIM)** for verifying color contrast.
- **Keyboard Navigation Testing** for assessing keyboard accessibility.
- **Reflow Testing** to verify content reflows properly without horizontal scrolling.

Additionally, watch the suggested YouTube tutorials to understand the basic features and navigation of each tool.

**Reminder:** If you want to adjust the playback speed on YouTube, click on the settings (cog) icon on the video and select your desired speed.

### Choose a Sample Webpage
Select a publicly available webpage (e.g., a news site, blog, or personal webpage).

### Conduct the Audit

1. Use **Color Contrast Checkers (WebAIM)** to verify that text and background colors meet WCAG contrast ratio guidelines.
2. Use **Keyboard Navigation Testing** to navigate through the webpage using only the keyboard and ensure all elements are accessible.
3. Use **Reflow Testing** to verify that content remains usable and readable when resized or zoomed, without horizontal scrolling.
4. Use **Lighthouse** to perform an accessibility audit.
5. Test the page with **NVDA** to assess screen reader compatibility.
6. Analyze the page with **Axe** for specific issues and recommendations.
7. Use **Wave** to visually identify missing alt text, contrast issues, or improper form labels.

### Write a Summary Report

Include the following:
- Key findings from each tool used, highlighting unique insights from each.
- Key findings from each tool, highlighting unique insights from each.
- An evaluation of how the tools complement one another in identifying accessibility issues.
- Recommendations for improving the page’s accessibility.

### Submission Instructions
- Save your summary report in Google Docs.
- Title your document: "Week 3 Training 5 - Comprehensive Accessibility Audit Report".
- Share your Google Doc via the Slack group or email it to the instructor for feedback.
- Save your document for future use. You will learn how to upload it to GitHub in the next lesson.

---

## Key Interview Questions

By the end of this training, students should be able to answer:
1. What is the purpose of accessibility testing?
2. How do tools like NVDA, Axe, and Lighthouse assist in identifying accessibility issues?
3. What are WCAG guidelines, and why are they important in accessibility testing?
4. How do you perform keyboard navigation testing and why is it important?
5. What is reflow testing, and what does it verify?

---

## Tips for Success

- Take notes on how each tool works during the session, including setup steps.
- Watch the provided YouTube tutorials to familiarize yourself with the tool interfaces and common testing workflows.
- Explore additional features of the tools to enhance your understanding.
- Use the free resources to supplement your learning.

---

## Next Training

In **Training 6**, we will introduce bug tracking and version control with tools like Jira and GitHub.
