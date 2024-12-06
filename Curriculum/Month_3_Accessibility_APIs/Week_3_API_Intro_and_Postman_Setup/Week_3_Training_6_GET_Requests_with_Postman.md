# **Month 3 Training 6 - Making GET Requests with Postman**

### **Objective**

In this training, students will expand their understanding of **GET requests** and how to interact with multiple **public APIs** using **Postman**. By the end of this training, students will:

- Be able to make **GET requests** to different **public APIs**, including **Postman Echo API** and **JSONPlaceholder API**.
- Understand how to **switch environments** in Postman to work with multiple APIs effectively.
- Be able to analyze and interpret different components of an **API response** (e.g., **status codes**, **headers**, **response body**).

---

### **Free Online Resources** (Mandatory)

To support your understanding, students must explore the following resources before engaging with the content:

1. **[What is HTTP? Protocol Overview for Beginners (freeCodeCamp)](https://www.freecodecamp.org/news/what-is-http/)**
   - This article provides a detailed overview of HTTP.

2. **[Learn HTTP Methods like GET, POST, and DELETE – a Handbook with Code Examples (freeCodeCamp)](https://www.freecodecamp.org/news/learn-http-methods-like-get-post-and-delete-a-handbook-with-code-examples/)**
   - This handbook explains the different **HTTP methods**—including **GET**, **POST**, and **DELETE**—with practical examples. It's helpful for understanding how these methods are used in API communication, providing essential context for the API testing you’ll perform in this training.

3. **[Learn HTTP Status Codes In 10 Minutes (YouTube)](https://www.youtube.com/watch?v=wJa5CTIFj7U)**
   - This guide provides a quick overview of HTTP status codes.

3. **[Working with GET Requests in Postman (Postman Learning Center)](https://learning.postman.com/docs/sending-requests/requests/#making-your-first-get-request)**
   - This guide provides a step-by-step approach to making your first GET request using Postman and understanding how the response is structured.

4. **[Using JSONPlaceholder for API Practice (JSONPlaceholder)](https://jsonplaceholder.typicode.com/guide/)**
   - A beginner-friendly introduction to **JSONPlaceholder**, an open-source fake API used for practice. Learn how to use this API for making test requests.

---

### **Topics Covered**

#### **1. GET Requests and Public APIs**

- **Explanation**: A **GET request** is used to **retrieve data** from a server. When using a public API like **Postman Echo** or **JSONPlaceholder**, you can fetch specific information provided by the service.
  - **Key Insight**: Understanding GET requests will help you interact with external data sources, which is crucial for many QA and testing tasks.

#### **2. Understanding API Responses**

- **Status Codes**: Learn about **status codes** such as **200 OK**, **404 Not Found**, and others that help indicate whether a request was successful.
  - **Key Insight**: Status codes are the first indicator of whether your request succeeded and if any errors occurred.

- **Headers**: Review the metadata associated with an API response, such as **Content-Type**, which specifies the format of the returned data.
  - **Key Insight**: Headers provide important information about how the data can be processed.

- **Response Body**: Understand how to read the response body, which usually contains data returned by the server, often formatted as **JSON**.
  - **Key Insight**: The response body contains the data you requested, and understanding its format is crucial for validating the accuracy of your GET request.

#### **3. Switching Between Environments in Postman**

- **Explanation**: Learn how to create different **environments** in Postman (e.g., **QA** and **Test Server** environments). This helps you test API requests with different servers or data sets without manually updating each URL.
  - **Step-by-Step Guidance**: Students will set up two environments, `QA` and `Test Server`, and will practice switching between them to run GET requests.
  - **Key Insight**: Mastering environments makes your API testing more efficient and less prone to human error.

---

### **Assignment**

#### **Part 1: Making GET Requests to Postman Echo and JSONPlaceholder APIs**

- **Objective**: Understand how to make **GET requests** to multiple public APIs, and analyze the response details.
- **Instructions**:
  1. **Use Postman** to make a **GET request** to the **Postman Echo API** using the `QA` environment created in Training 5.
     - URL: `{{baseURL}}/get?param1=value1`
     - **Analyze the Response**: Write down the **status code**, **headers**, and **body**. Take note of the `param1` value returned in the response.
  2. **Switch to the `Test Server` Environment** and make a **GET request** to the **JSONPlaceholder API**.
     - URL: `{{baseURL}}/posts/1`
     - **Analyze the Response**: Note the **status code**, **headers**, and **response body**.

#### **Part 2: Comparing Responses from Different APIs**

- **Objective**: Learn to compare responses from different environments and identify how API structure and responses differ.
- **Instructions**:
  1. Compare the **status codes**, **headers**, and **response body** from the **Postman Echo** and **JSONPlaceholder** APIs.
  2. Write a short summary (at least 2-3 paragraphs) describing the differences in the response formats, data structures, and any insights you gain regarding the purpose of each API.

#### **Part 3: Practice Using the History Tab**

- **Objective**: Understand how the **History tab** can help track your work and reuse previous requests.
- **Instructions**:
  1. Review your **History** tab and locate both GET requests you made.
  2. Re-run each request directly from the History tab and confirm that you receive the same responses as earlier.
  3. Document your findings and screenshots in a **Google Doc**.

---

### **Submission Instructions**

**How to Submit**:

1. **Export Your Postman Collection**:
   - Navigate to the **Collections** tab.
   - Find your `QA Academy` collection, click on the three dots (...) next to it, and select **Export**.
   - Save the exported JSON file locally.

2. **Export Your Postman Environments**:
   - Navigate to the **Environments** tab.
   - Click on the three dots (...) next to each environment (`QA` and `Test Server`) and select **Export**.
   - Save each exported JSON file locally.

3. **Share the Collection, Environments, and Documentation**:
   - Upload the exported JSON files of your `QA Academy` collection and both environments to the designated Slack channel.
   - Attach a **Google Doc** summarizing your GET request results, comparisons, and screenshots.

Ensure all sharing settings allow "Anyone with the link" to view and comment as necessary.

---

### **Key Learning Outcomes**

- Gain hands-on experience making **GET requests** to multiple public APIs.
- Understand how to **switch environments** in Postman and why it is beneficial.
- Learn to analyze API responses, including **status codes**, **headers**, and **response data**.

---

### **Key Interview Questions**

1. **What is a GET request**, and how is it used in API testing?
2. **How can you switch environments** in Postman, and why is this feature useful?
3. **What are the different components** of an API response, and why are they important for testing?
4. What are some **common status codes** you encounter during GET requests, and what do they indicate?

---

### **Tips for Success**

- **Practice Switching Environments**: The more comfortable you become with changing environments, the more efficiently you can manage your testing setups.
- **Observe Differences**: Pay attention to the differences between responses from different APIs. This will help you understand how various systems behave and what you should expect during testing.
- **Use History Effectively**: Knowing how to leverage the **History tab** will save you time and effort, especially when repeating tests or verifying previous results.

---

### **Next Training**

In **Training 7**, we will begin exploring how to make **POST requests** with Postman. You will learn to send data to an API, understand how to structure a **POST request**, and practice sending information to create new resources.

