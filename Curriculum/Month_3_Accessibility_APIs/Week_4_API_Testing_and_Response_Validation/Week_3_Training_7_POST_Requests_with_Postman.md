# **Month 3 Training 7 - Making POST Requests with Postman**

### **Objective**

In this training, students will explore how to send data to an API using **POST requests** in **Postman**. By the end of this training, students will:

- Understand the concept of **POST requests** and how they differ from **GET requests**.
- Be able to create and execute **POST requests** in Postman to submit data to an API.
- Learn about the structure of a **POST request**, including **headers**, **body**, and **JSON data**.

---

### **Free Online Resources** (Mandatory)

To support your understanding, students must explore the following resources before engaging with the content:

1. **[POST Request using Postman Tutorial (ToolsQA)](https://toolsqa.com/postman/post-request-in-postman/)**
   - This tutorial provides a step-by-step guide on creating and executing a POST request using Postman, helping you understand the process thoroughly.

2. **[What is a POST Request? (Postman Learning Center)](https://learning.postman.com/docs/sending-requests/create-requests/parameters/)**
   - This guide provides an overview of what a POST request is and how it can be used to send data to a server.

3. **[Learn JSON Basics (Codecademy)](https://www.codecademy.com/articles/what-is-json)**
   - This resource provides an introduction to **JSON** (JavaScript Object Notation), which is used for formatting the data we send in POST requests. Understanding JSON will help you interact effectively with APIs.

4. **[Creating a POST Request in Postman (YouTube)](https://www.youtube.com/watch?v=qyYAOty_bDs)**
   - A beginner-friendly video guide showing how to create a POST request in Postman, including setting up headers and body content.

---

### **Topics Covered**

#### **1. POST Requests Explained**

- **GET vs POST**: **GET requests** retrieve data from a server without modifying it, while **POST requests** send data to the server to create or update resources. In real-world applications, **GET** is often used for actions like displaying user profiles or product listings, whereas **POST** is used for actions such as registering users or submitting forms.
  - **Example Scenarios**:
    - **GET**: Viewing a list of available products on an e-commerce site.
    - **POST**: Placing an order or creating a user profile.
  - **Key Insight**: Understanding when to use GET or POST is crucial for interacting effectively with APIs and ensuring data integrity.

- **Explanation**: A **POST request** is used to **send data** to a server, such as creating a new user or submitting a form. Unlike **GET requests**, which only retrieve data, **POST requests** modify data on the server.
  - **Key Insight**: POST requests are essential for actions that require sending information, like user registrations or data submissions.

#### **2. Structure of a POST Request**

- **Headers**: Learn about important headers such as **Content-Type**, which tells the server what kind of data you are sending (e.g., **JSON**). To understand headers, think of them like the address label on a package—it tells the server exactly what's inside and how to handle it. Without the right label, the server won't know how to process the information, which could lead to errors or confusion.
  - **Key Insight**: Correctly setting headers ensures the server can interpret your data accurately. Headers are critical for successful communication between the client and server, and incorrect headers can lead to data being misinterpreted or rejected.

- **Body**: Understand how to use the **Body** section in Postman to format the data you send. We will use **JSON format** to represent our data.
  - **Key Insight**: The body of a POST request contains the data you want to send, and using JSON allows it to be well-structured and machine-readable.

- **JSON Overview**: A brief introduction to **JSON syntax**—students will learn how JSON represents data as **key-value pairs**, similar to a dictionary.
  - **Example**: `{ "name": "John Doe", "email": "john.doe@example.com" }`
  - **Key Insight**: JSON is a lightweight format that is easy for both humans and machines to understand. It is widely used in APIs for sending structured data.

- **Additional JSON Information**: JSON data is composed of **key-value pairs**, where the key is a string that represents the name of a property, and the value can be a string, number, boolean, array, or even another JSON object. JSON is commonly used because it is easy to read and write, making it ideal for transmitting data between clients and servers.

  - **Simple Example**:
    ```json
    {
      "firstName": "Jane",
      "lastName": "Doe",
      "age": 30,
      "isStudent": false
    }
    ```
  - This format helps structure the data in a consistent way, which is necessary when interacting with different APIs.

#### **3. Creating and Executing POST Requests in Postman**

- **Step-by-Step Guidance**: Students will learn how to create a **POST request** in Postman, including:
  - Setting the **method** to **POST**.
  - Specifying the **URL** for the API endpoint.
  - Adding **headers** to inform the server of the type of data being sent.
  - Using the **Body** section to format the data in **JSON**.
  - **Key Insight**: Understanding the different components of a POST request will allow you to interact with APIs that require data submissions effectively.

---

### **Assignment**

#### **Part 1: Creating and Executing a POST Request in Postman**

- **Explanation**: When making a POST request, it is essential to specify the **Content-Type** as `application/json`. This tells the server the format of the data you are sending, ensuring that it knows how to interpret the data properly.

- **Objective**: Send data to an API using a **POST request** and analyze the server's response.
- **Instructions**:
  1. **Create a new request** in your `QA Academy` collection and name it **POST Create User**.
  2. **Set the Method Type** to **POST**.
  3. **Select the `Test Server` Environment** in Postman to ensure you are sending requests to the correct server.
  4. **URL**: `{{baseURL}}/posts`.
  5. **Headers**: Add a **Content-Type** header with the value `application/json`. This header specifies the format of the data being sent, ensuring the server knows how to interpret it. For example, 'Content-Type: application/json' is used when sending data in JSON format, which is critical for effective communication between the client and the server.
  6. **Body**: Select **raw** and **JSON** as the body type, and enter the following JSON:
     ```json
     {
       "title": "My New Post",
       "body": "This is a post created via a POST request.",
       "userId": 1
     }
     ```
  7. **Send the Request** and analyze the response.
     - **Status Code**: Note the status code (e.g., **201 Created**) that indicates the successful creation of a resource.
     - **Headers**: Review the response headers, such as **Content-Type** and **Location**.
     - **Response Body**: Understand the returned data, which may include an **ID** for the newly created resource.
  8. Document your findings, including a **screenshot** of your POST request and the server response.

#### **Part 2: Creating Your Own JSON Data**

- **Objective**: Practice writing **JSON** to better understand its flexibility and adaptability.
- **Instructions**:
  1. Modify the **Body** of your **POST Create User** request to create a different type of post. Change the **title** and **body** fields to something else of your choice.
  2. Try adding a new field to your JSON, such as **"category": "Learning"** or **"tags": ["API", "Postman"]**, to see how additional data can be included.
  3. **Send the modified POST request** and verify that the server successfully processes your data.
  4. Write a short summary (at least 1-2 paragraphs) on how you structured your JSON, what changes you made compared to the original example, and any additional fields you added.

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
   - Attach a **Google Doc** summarizing your POST request results, changes made to the JSON data, and screenshots.

Ensure all sharing settings allow "Anyone with the link" to view and comment as necessary.

---

### **Key Learning Outcomes**

- Understand the concept and use cases of **POST requests** for sending data to an API.
- Learn to create and execute **POST requests** using **JSON** data in Postman.
- Develop a basic understanding of **JSON syntax** and how to structure data effectively for API interactions.

---

### **Key Interview Questions**

1. **What is a POST request**, and how is it different from a GET request?
2. **How do you structure the body** of a POST request in Postman?
3. **What is JSON**, and why is it commonly used in APIs?
4. **What are the key components** of a POST request that you need to configure in Postman?

---

### **Tips for Success**

- **Practice Writing JSON**: The more comfortable you become with JSON, the easier it will be to work with APIs.
- **Use Pre-Built Snippets**: Postman has snippets that help create headers or JSON data—use these tools to make setting up requests easier. Remember, these snippets are designed to make your tasks simpler and to help you quickly set up correct configurations without writing JavaScript from scratch.
- **Read the API Documentation Carefully**: Understanding what the API expects will help you correctly configure your requests and prevent errors.

---

### **Next Training**

In **Training 8**, we will learn how to **validate API responses** by using Postman’s **built-in test scripts**. These scripts are written in **JavaScript**, but don’t worry—we’ll be using **pre-built snippets** to make it easy to validate that your responses are correct. You’ll learn to automate validation checks, such as ensuring a **status code** is 200 or that the **data returned** matches what you expect.

