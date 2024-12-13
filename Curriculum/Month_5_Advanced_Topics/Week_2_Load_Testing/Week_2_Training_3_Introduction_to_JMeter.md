# **Training 3: Introduction to JMeter and Load Testing**

## **Objective**

This training introduces students to the fundamentals of load testing using JMeter. Students will learn how to create simple test plans, execute tests with a small number of virtual users, and analyze metrics such as response times, throughput, and error rates. By the end of this session, students will:

- Understand the purpose of load testing and its distinction from performance testing.
- Set up and execute a simple JMeter test.
- Analyze key load testing metrics and document findings effectively.

---

## **Free Online Resources** (Mandatory)

1. **[What is Load Testing? (Guru99)](https://www.guru99.com/load-testing.html)**

   - Overview of load testing concepts and their importance.

2. **[JMeter User Manual (Apache)](https://jmeter.apache.org/usermanual/index.html)**

   - Official guide to JMeter, covering installation, interface, and basic usage.

3. **[How to Do Load Testing (BlazeMeter)](https://www.blazemeter.com/blog/how-to-do-load-testing)**

   - Beginner-friendly tutorial on creating and running load tests.

4. **[JMeter Beginner Tutorial (YouTube)](https://www.youtube.com/watch?v=1tJGRWABpW0)**

   - Step-by-step video tutorial for setting up and executing JMeter tests.

---

## **Topics Covered**

### **1. What is Load Testing?**

- **Definition**: Load testing evaluates a system’s performance under expected and peak user loads.

- **Importance**: Ensures the application can handle multiple users simultaneously without degradation in performance.

- **Impact on User Experience**: By simulating real-world user loads, load testing helps identify bottlenecks that could lead to slow response times or application crashes. These issues, if left unresolved, can result in poor user experiences, such as:

  - Increased wait times leading to user frustration.
  - Failed transactions in e-commerce platforms causing loss of sales.
  - Inaccessible features during peak usage, reducing overall satisfaction.
  - Ensuring smooth performance during high-traffic events, such as sales or promotions.

- **Comparison with Performance Testing**:

  - Performance testing focuses on overall system behavior, while load testing simulates user loads to identify bottlenecks.

### **2. Introduction to JMeter**

- **Overview**: JMeter is a popular open-source tool for load testing applications.

- **Interface Basics**:

  - **Test Plan**: The root element for organizing test components. For example, think of a Test Plan as a blueprint for your load test, where you define all the test elements.
  - **Thread Group**: Defines the number of users and the test duration. For instance, if you want to simulate five users accessing a website over a 10-second period, you configure this in the Thread Group settings.
  - **HTTP Sampler**: Configures the requests sent to the application. For example, you can use the HTTP Sampler to test logging into a website by specifying the login endpoint and providing required parameters like username and password.

### **3. Setting Up a Simple Test**

- **Demo Application**: Use `https://the-internet.herokuapp.com/` as the test target.
- **Steps**:
  - Create a new Test Plan.
  - Add a Thread Group with five virtual users.
  - Configure an HTTP Request Sampler to test a specific endpoint (e.g., `/login`).

### **4. Running a Test**

- Execute the test and monitor real-time progress in JMeter’s listeners (e.g., Summary Report, Graph Results).

- Save results for analysis.

- **Guidance on Interpreting CSV Data**:

  - **Average Response Time**: Indicates how long it takes for a server to respond to a request. Look for spikes that might indicate bottlenecks.
  - **Throughput**: Represents the number of requests handled per second. Higher throughput generally indicates better performance.
  - **Error Rate**: Shows the percentage of failed requests. Ideally, this should be 0%; investigate further if it is high.
  - Open the CSV file in a spreadsheet tool like Excel or Google Sheets to organize and analyze the data effectively. Use filters to sort by response times or error codes for a deeper understanding of potential issues.

### **5. Key Metrics to Analyze**

- **Response Time**: Average time taken to process requests.
- **Throughput**: Number of requests processed per second.
- **Error Rate**: Percentage of failed requests.

---

## **Assignment**

### **Objective**

Set up and execute a simple load test using JMeter, analyze the results, and document findings in a report.

### **Instructions**

1. **Install JMeter**:

   - Download JMeter from [Apache JMeter](https://jmeter.apache.org/download_jmeter.cgi).
   - Follow the installation steps in the **JMeter User Manual** linked in the resources.
   - Verify the installation by opening the JMeter GUI.

2. **Set Up a Test Plan**:

   - Open JMeter and create a new Test Plan:
     1. Right-click on the Test Plan node in the left pane.
     2. Select **Add > Threads (Users) > Thread Group**.
   - Configure the Thread Group:
     - Number of Threads (users): **5**.
     - Ramp-Up Period (in seconds): **10** (this means users will be added one by one over 10 seconds).
     - Loop Count: **1** (each user will execute the test once).
   - Add an HTTP Request Sampler:
     1. Right-click on the Thread Group.
     2. Select **Add > Sampler > HTTP Request**.
     - Set the **Server Name** to `the-internet.herokuapp.com`.
     - Set the **Path** to `/login`.
     - Choose an appropriate HTTP method (e.g., GET or POST).

3. **Run the Test**:

   - Save your Test Plan by clicking **File > Save**.
   - Click the green **Start** button in the toolbar to execute the test.
   - Open the **View Results Tree** or **Summary Report** listener to monitor the test as it runs.

4. **Analyze Results**:

   - Focus on the following metrics in the **Summary Report** listener:
     - **Average Response Time**: Time taken to process requests.
     - **Throughput**: Number of requests processed per second.
     - **Error Rate**: Percentage of requests that failed.
   - Save the results by right-clicking the listener and choosing **Save Table Data as CSV**.

5. **Document Findings**

- Create a performance report with the following sections:
  - **Test Setup**: Describe the Test Plan configuration (e.g., 5 users, 10-second ramp-up, 1 loop).
  - **Key Metrics**: Include average response time, throughput, and error rate.
  - **Observations**: Highlight significant findings (e.g., slow response times or high error rates).
  - **Recommendations**: Provide at least two actionable suggestions to improve performance.

**Example Performance Report:**

**Test Setup:**

- Number of Users: 5
- Ramp-Up Period: 10 seconds
- Loop Count: 1
- Target Application: `https://the-internet.herokuapp.com/login`

**Key Metrics:**

- Average Response Time: 350 ms
- Throughput: 25 requests/second
- Error Rate: 0%

**Observations:**

- The response time is acceptable under the simulated load but could be optimized for larger user bases.
- Throughput indicates the system handles requests efficiently within the tested limits.

**Recommendations:**

1. Optimize database queries to further reduce response times.

2. Perform additional tests with increased user loads to assess scalability.:

   - Create a performance report with the following sections:
     - **Test Setup**: Describe the Test Plan configuration (e.g., 5 users, 10-second ramp-up, 1 loop).
     - **Key Metrics**: Include average response time, throughput, and error rate.
     - **Observations**: Highlight significant findings (e.g., slow response times or high error rates).
     - **Recommendations**: Provide at least two actionable suggestions to improve performance.

3. **Submit Work**:

   - Save your report as `YourName_JMeterReport.pdf`.
   - Upload the report and test results file to the QA Academy Slack channel.
   - Ensure the sharing permissions allow the mentor to view your files.

---

### **Additional Notes**

- Use the resources provided in the **Free Online Resources** section if you encounter challenges.
- If you experience connectivity issues with the demo application, double-check the server name and path configuration in the HTTP Request Sampler.
- Reach out on the QA Academy Slack channel for support.

---

## **Submission Instructions**

1. Save your JMeter test results and report as instructed.
2. Upload the report to the QA Academy Slack channel.
3. Verify sharing permissions to allow access.

---

## **Key Learning Outcomes**

By the end of this training, students will:

- Understand the purpose and basic concepts of load testing.
- Gain hands-on experience with JMeter for setting up and running tests.
- Analyze load testing results and provide actionable recommendations.

---

## **Key Interview Questions**

1. What is load testing, and how does it differ from performance testing?
2. What are the key metrics you analyze in a JMeter test report?
3. How would you explain the significance of throughput and error rates to a non-technical stakeholder?

---

## **Tips for Success**

- Double-check all settings in JMeter before running tests to avoid errors.
- Focus on understanding the metrics rather than just completing the test.
- Use the provided resources for troubleshooting and additional guidance.
- Ask questions in the QA Academy Slack channel if you encounter challenges.

---

## **Next Training**

In **Training 4**, we will focus on analyzing load testing results in greater depth. Students will learn to interpret JMeter reports, identify performance bottlenecks, and document insights effectively, aligning with the Month 5 itinerary.

