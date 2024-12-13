# **Training 1: Introduction to Performance Testing**

## **Objective**

Introduce students to the fundamentals of performance testing, focusing on understanding key performance metrics and using Lighthouse to evaluate a web application's performance. By the end of this session, students will be able to:

- Understand what performance testing is and why it’s important.
- Identify key performance metrics such as response time, throughput, and error rates.
- Perform a basic performance audit using Lighthouse.

---

## **Free Online Resources** (Mandatory)

1. **[What is Performance Testing? (Guru99)](https://www.guru99.com/performance-testing.html)**
   - A beginner-friendly introduction to performance testing, including its types and objectives.

2. **[How to Use Lighthouse for Performance Testing (Google Developers)](https://developers.google.com/web/tools/lighthouse/)**
   - Step-by-step guide to using Lighthouse for evaluating website performance.

3. **[What Is Google Lighthouse and How to Use It? (YouTube)](https://www.youtube.com/watch?v=VyaHwvPWuZU)**
   - A short video explaining Lighthouse.

4. **[Crash Course: How To Analyze A Google Lighthouse Report 2021 | Actionable Website Speed Insights (YouTube)](https://www.youtube.com/watch?v=_Y7g_1vuQkY)**
   - A video walkthrough on analyzing Lighthouse reports and implementing actionable insights.

---

## **Topics Covered**

### **1. What is Performance Testing?**

- **Explanation**: Performance testing evaluates how well a system performs under a specific workload.
  - Key goals: Ensure the system is fast, scalable, and stable.
  - **Example**: An e-commerce website experiencing slow load times during a holiday sale can benefit from performance testing to identify and resolve bottlenecks.
- **Key Insight**: Performance testing helps identify bottlenecks and optimize the user experience.

### **2. Key Performance Metrics**

- **Explanation**:
  - **Response Time**: Time taken for a system to respond to a request.
    - **Example**: A fast response time is typically under 200ms for a web application.
  - **Throughput**: Number of requests handled per unit time.
    - **Example**: A system handling 1000 requests per second during peak traffic.
  - **Error Rates**: Percentage of failed requests during testing.
    - **Example**: An acceptable error rate for a production system is less than 1%.
- **Key Insight**: Understanding these metrics is critical for diagnosing performance issues.

### **3. Using Lighthouse for Performance Testing**

- **Explanation**:
  - Lighthouse is an open-source tool that provides performance insights for web applications.
  - Key metrics analyzed: Performance score, Time to Interactive, Speed Index.
    - **Performance Score**: A numerical representation of the page's overall performance. Scores above 90 are excellent, 50-89 indicate room for improvement, and below 50 require significant optimization.
    - **Time to Interactive**: The time it takes for the page to become fully interactive. An ideal time to interactive is less than 5 seconds on mobile.
    - **Speed Index**: Measures how quickly content is visually displayed during load.
  - **Example**: A Lighthouse report showing a performance score of 70 indicates room for improvement in areas like image optimization or JavaScript execution.
- **Key Insight**: Lighthouse generates actionable recommendations to improve performance.

---

## **Assignment**

### **Objective**

Perform a performance audit on a demo application using Lighthouse and document findings in a simplified performance report.

### **Instructions**

1. **Set Up Lighthouse**:
   - Open Google Chrome and navigate to the demo application: [https://the-internet.herokuapp.com](https://the-internet.herokuapp.com).
   - Access Lighthouse by following these steps:
     - Right-click anywhere on the demo application webpage and select “Inspect.”
     - In the Developer Tools panel, select the “Lighthouse” tab.
     - Click on “Generate Report” in the Lighthouse panel.

2. **Configure the Audit**:
   - Under “Categories,” select only the “Performance” checkbox.
   - Choose “Device” as “Mobile” for testing mobile performance.
   - Click “Run Audit” to start the performance analysis.

3. **Run and Save the Audit**:
   - Wait for the Lighthouse audit to complete.
   - Save the report by clicking “Download Report” and choosing the PDF format.
   - Save the file with your name, e.g., `JohnDoe_LighthouseReport.pdf`.

4. **Document Your Findings**:

   ### Performance Audit Summary
   **Performance Score**: [Insert Score Here]  
   **Time to Interactive**: [Insert Value Here]  
   **Speed Index**: [Insert Value Here]  
   **Recommendations**:  
   1. [Actionable Recommendation 1]  
   2. [Actionable Recommendation 2]  
   3. [Actionable Recommendation 3]  
   **Observations**:  
   - The Performance Score suggests [Insert Observation Here].  
   - The most critical recommendations are [Insert Critical Recommendations Here].

   - Fill in the provided performance report template with:
     - **Performance Score**: Record the score from the Lighthouse report.
     - **Key Metrics**: Document the “Time to Interactive” and “Speed Index” values.
     - **Recommendations**: Summarize actionable improvements suggested by Lighthouse (e.g., optimizing images, reducing JavaScript payloads).
     - **Observations**: Write 2–3 sentences interpreting what the metrics indicate about the web application's performance. Reflect on questions such as:
       - What does the Performance Score suggest about the application’s overall health?
       - Which recommendations are the most critical for improving the score?

5. **Submit Your Work**:
   - Save the completed report as `YourName_PerformanceReport.pdf`.
   - Upload both the Lighthouse PDF and the completed performance report to the QA Academy Slack channel.
   - Ensure sharing permissions are set to “Anyone with the link can view.”

---

## **Submission Instructions**

1. Save the Lighthouse report and completed performance report as PDFs.
2. Share the files in the QA Academy Slack channel.
3. Ensure sharing permissions are set to “Anyone with the link can view.”

---

## **Key Learning Outcomes**

By the end of this training, students will:

- Understand the purpose of performance testing.
- Identify and interpret key performance metrics.
- Conduct a basic performance audit using Lighthouse.

---

## **Key Interview Questions**

1. What is the purpose of performance testing?
2. What are the three key metrics in performance testing?
3. How does Lighthouse help in evaluating web performance?

---

## **Tips for Success**

- Follow the step-by-step instructions in the Lighthouse guide to avoid errors.
- Double-check that you selected only the “Performance” category in Lighthouse and saved your report correctly as a PDF to avoid needing to re-run the audit.
- Focus on understanding the meaning of each metric reported by Lighthouse.
- Use the Slack channel to ask questions if you encounter any issues.
- Pay close attention to the actionable recommendations in the Lighthouse report; these insights can improve real-world web applications.

---

## **Next Training**

In **Training 2**, we will focus on analyzing and interpreting performance results to identify bottlenecks and suggest optimizations.

