# **Month 3 Training 5 - Introduction to APIs and Postman Setup**

### **Objective**

Introduce students to the fundamentals of **APIs** and the use of **Postman** for API testing. By the end of this training, students will:

- Understand what an **API** is and how it enables communication between different software systems.
- Learn the different types of API methods: **GET**, **POST**, **PUT**, and **DELETE**, with a focus on **GET** and **POST**.
- Set up **Postman** as an API testing tool, create a workspace, and perform their first **GET request**.

---

### **Free Online Resources** (Mandatory)

To support your understanding, students must explore the following resources before engaging with the content:

1. **[What is an API? (YouTube)](https://www.youtube.com/watch?v=s7wmiS2mSXY)**
   - This video introduces what APIs are, why they are important, and how they allow different applications to communicate.

2. **[Postman Tutorial for Beginners (Guru99)](https://www.guru99.com/postman-tutorial.html)**
   - A step-by-step tutorial explaining how to install and use Postman, which will help students understand the tool's interface and create their first request.

3. **[HTTP Methods Explained - GET, POST, PUT, DELETE (freeCodeCamp)](https://www.freecodecamp.org/news/http-methods-get-post-put-delete/)**
   - An article detailing the various HTTP methods. Focus on **GET** and **POST** for practice, but gain context on **PUT** and **DELETE** for understanding.

4. **[Postman Quickstart (Postman Learning Center)](https://learning.postman.com/docs/getting-started/quick-start/)**
   - This guide provides a concise overview on setting up Postman and using it for the first time. It will help students with installation and understanding basic features.

---

### **Topics Covered**

#### **1. What is an API?**

- **Explanation**:
  - APIs, or **Application Programming Interfaces**, are a set of rules that allow software applications to communicate with each other. For example, when you use an app to check the weather, the app uses an API to get data from the weather service.
- **Key Insight**: APIs are everywhere—from social media feeds, to weather updates, to booking systems. Understanding how they work helps QA professionals understand how different software systems are integrated.

#### **2. Types of API Requests**

- **GET Requests**:
  - **Purpose**: Used to **retrieve data** from a server.
  - **Example**: When you open a weather app, a GET request is sent to the server to fetch the weather details.
  - **Backend Action**: The server retrieves the requested information from a database and sends it back to the client.

- **POST Requests**:
  - **Purpose**: Used to **send data** to a server, generally to create a new resource.
  - **Example**: Registering a new user on a website involves sending their information (like name, email, password) using a POST request.
  - **Backend Action**: The server takes the information and adds a new entry into the database.

- **Overview of PUT and DELETE**:
  - **PUT**: Used to **update existing data** on a server.
  - **DELETE**: Used to **remove data** from a server.

- **Key Insight**: Even if we don't practice all API types right now, understanding them conceptually is important as they all play a role in web applications' functionality.

#### **3. Introduction to Postman**

- **Postman Interface Overview**:
  - **Overview of Key Areas**:
    - **Collections**:
      - **Description**: Collections are like folders where you store all your related API requests. They help organize multiple API calls, making it easy to manage and reuse different requests.
      - **Example Usage**: You can create a collection for a specific project, like "Weather API Testing," and store all related requests (e.g., for retrieving weather information, creating alerts, etc.).
    - **Environments**:
      - **Description**: Environments in Postman allow you to set variables that can be reused across requests. This is especially useful if you need to switch between different data sets or servers (like development and production).
      - **Example Usage**: For an environment named "QA Server," you might set a variable `baseURL` as `https://api.qaserver.com`. When writing your request URLs, you can refer to this `baseURL` variable instead of typing the full URL each time.
    - **History**:
      - **Description**: The History tab keeps track of every request you’ve made in Postman. This can be very helpful for reviewing past work and reusing requests that you have executed before.
      - **Example Usage**: If you run a request yesterday to test a bug, you can go back into the History tab, locate the request, and rerun it without needing to set it up again.
    - **Requests**:
      - **Description**: This is where you enter the details for an API call, like the method (GET, POST, etc.), the URL, any necessary parameters, headers, or body data.
      - **Example Usage**: A GET request might simply retrieve information like the current weather, whereas a POST request could create a new user profile by sending JSON data to the server.
    - **Variables**:
      - **Description**: Variables can be used within your requests to make them more flexible and reusable. They can store values like URLs, API keys, or parameter values.
      - **Example Usage**: Instead of manually updating an API key in each request, you create a variable called `apiKey`. In your request, use `{{apiKey}}`, which will automatically replace it with the value you set in your environment.
  - **Creating Your First GET Request**:
    1. **Open Postman** and click **New Request**.
    2. Set the **HTTP method** to **GET**.
    3. Enter the following URL: `https://postman-echo.com/get?param1=value1`.
    4. Click **Send** to execute the request.
- **Breaking Down the GET Response**:
  - **Status Code**: Learn about response codes, such as **200 OK** (success) and **404 Not Found** (error).
  - **Headers**: Understand the metadata returned by the server, such as **Content-Type**.
  - **Body**: Analyze the response data returned by the server.

---

### **Assignment**

#### **Part 1: Setting Up Postman and Creating Your First Workspace**

- **Objective**: Set up **Postman** and become familiar with its workspace, which will be used for future assignments.
- **Instructions**:
  - **Note:** If you have already completed this step during Month 1, please verify your setup and make any necessary updates.
    1. **Download** and **install Postman** from the [Postman website](https://www.postman.com/downloads/).
    2. **Create a workspace** named **QA Academy**.
    3. **Verify Workspace Setup**: Ensure that your workspace is set up by creating a test collection in the workspace.

#### **Part 2: Setting Up Environments and Performing a GET Request**

- **Objective**: Execute a **GET request** using **Postman** while switching environments, to understand the process of retrieving data and managing different server settings.
- **Instructions**:

  **1. Set Up the `QA` Environment**:
  - **Create a new environment**:
    1. On the left-hand side of Postman, click **Environments**.
    2. Click the **Create Environment** button.
    3. **Name** the environment as `QA`.
  - **Add Variables**:
    - **Variable Name**: `baseURL`
    - **Initial Value**: `https://postman-echo.com`
    - **Current Value**: `https://postman-echo.com`
    - Click **Save**.

  **2. Set Up the `Test Server` Environment**:
  - **Create a new environment**:
    1. Click **Environments** on the left-hand side.
    2. Click the **Create Environment** button.
    3. **Name** the environment as `Test Server`.
  - **Add Variables**:
    - **Variable Name**: `baseURL`
    - **Initial Value**: `https://jsonplaceholder.typicode.com`
    - **Current Value**: `https://jsonplaceholder.typicode.com`
    - Click **Save**.

  **3. Create Collection and Perform GET Request**:
  - **Create a New Collection**:
    1. Click on **Collections** in the left navigation pane.
    2. Click the **Create Collection** button.
    3. **Name** the collection as `QA Academy`.
  - **Add a GET Request to Your Collection**:
    1. **Create a New Request** in your `QA Academy` collection.
    2. **Name** the request as `GET Request - Echo`.
    3. Set the **method** to **GET**.
    4. Use the following URL: `{{baseURL}}/get?param1=value1`.
    5. **Send the Request** while using the **QA** environment.
    6. Document the following:
       - **Status Code**: Note the returned code (e.g., **200 OK**).
       - **Headers**: Identify key headers such as **Content-Type**.
       - **Body**: Review the JSON response returned.

  **4. Switch to `Test Server` Environment and Execute Again**:
  - **Switch Environments**:
    1. Set the active environment to **Test Server**.
    2. Send the **GET Request** again and observe how the response changes.
  - **Document Your Observations**:
    - Compare the **status code**, **headers**, and **response body** for both environments (`QA` and `Test Server`).
    - Write down any differences you observe, including different data structures or responses.

#### **Submission Instructions**

**How to Submit**:

1. **Export Your Postman Collection**:
   - Navigate to the **Collections** tab.
   - Find your `QA Academy` collection, click on the three dots (...) next to it, and select **Export**.
   - Save the exported JSON file locally.

2. **Export Your Postman Environments**:
   - Navigate to the **Environments** tab.
   - Click on the three dots (...) next to each environment (`QA` and `Test Server`) and select **Export**.
   - Save each exported JSON file locally.

3. **Share the Collection and Environments**:
   - Upload the exported JSON files of your `QA Academy` collection and both environments to the designated Slack channel.
   - Attach a **Google Doc** summarizing your GET request and your observations, including screenshots of your workspace and response.

Ensure all sharing settings allow "Anyone with the link" to view and comment as necessary.

---

### **Key Learning Outcomes**

- Understand what an **API** is and its role in enabling communication between software components.
- Gain familiarity with different **HTTP methods**: GET, POST, PUT, DELETE.
- Successfully use **Postman** to set up a workspace and perform a **GET request**.

---

### **Key Interview Questions**

1. **What is an API**, and why is it important in software testing?
2. Explain the difference between a **GET request** and a **POST request**.
3. **What are the key components** of an API response (e.g., **status code**, **headers**, **response body**)?
4. **What HTTP methods** would you use to update or delete data in an API?

---

### **Tips for Success**

- **Practice in Postman**: Run the GET request multiple times with different parameters to see how the response changes.
- **Understand Each Component**: Pay attention to the **status code** and **response body**—knowing how to interpret these is crucial for a QA tester.
- **Take Your Time**: Getting comfortable with the **Postman interface** and the structure of requests/responses is key to building your foundational skills.

---

### **Next Training**

In **Training 6**, we will explore how to make **GET requests** to different public APIs, including the **Postman Echo API** and **JSONPlaceholder API**. You will learn how to switch between environments, allowing you to work with multiple APIs efficiently. We will delve deeper into understanding **API responses**, including exploring various **status codes**, **headers**, and **response data**. The focus will be on understanding the backend processes and the different components that make up an API response, helping you to confidently analyze and interpret API responses.
