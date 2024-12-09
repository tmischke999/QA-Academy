# **Month 4: Training 2 - Advanced JavaScript in Postman**

### **Objective**

This training builds on the JavaScript fundamentals covered in Training 1, focusing on using JavaScript in Postman. By the end of this session, students will:

- Understand how to create and use variables dynamically in Postman.
- Write and debug basic test scripts using JavaScript in Postman.
- Learn how to handle dynamic data using Postman variables.

---

### **Free Online Resources**

1. **[Using Variables in Postman (Postman Learning Center)](https://learning.postman.com/docs/sending-requests/variables/)**

   - A comprehensive guide to understanding Postman variables and their usage.

2. **[Postman Scripting with JavaScript (Postman YouTube)](https://www.youtube.com/watch?v=FyUvHbVm3mE)**

   - Learn how to write and use JavaScript scripts in Postman.

3. **[Debugging JavaScript in Postman](https://blog.postman.com/debugging-javascript-in-postman-scripts/)**

   - Practical tips on using the Postman Console for debugging JavaScript scripts.

4. **[Understanding Nested JSON in JavaScript (FreeCodeCamp)](https://www.freecodecamp.org/news/understanding-nested-json/)**

   - Explains how to navigate and manipulate nested JSON objects.

---

### **Topics Covered**

#### **1. Dynamic Variables in Postman**

- **Overview**: Explanation of Postman variables and how they can make tests dynamic and reusable.
- **Types of Variables**:
  - **Global Variables**: Accessible across all requests.
  - **Environment Variables**: Specific to a selected environment.
  - **Collection Variables**: Local to a collection.
  - **Local Variables**: Scoped to a single request.
- **Practical Examples**:
  - Using variables in request parameters.
  - Setting variables in scripts.
  - Updating variables dynamically during test execution.

#### **2. Writing Postman Test Scripts**

- **Key Concepts**:
  - Using `pm.*` methods in Postman.
  - Writing assertions for response validation.
- **Hands-On Examples**:
  - Validating response status codes.
  - Checking response body content.
  - Verifying headers and other metadata.
  - Navigating and validating nested JSON objects.

#### **3. Using the Postman Console**

- **Overview**: Introduction to the Postman Console for debugging scripts.
- **Practical Demonstration**:
  - Viewing request and response logs.
  - Debugging JavaScript errors in test scripts.
  - Using the console to print dynamic variable values.

---

### **Assignment**

#### **Part 1: Using Dynamic Variables**

**Objective**: Learn to use dynamic variables in Postman requests and tests.

1. **Setup Variables**:
   - Create an environment named `QA Training`.
   - Add the following variables:
     - `baseURL` with value `https://postman-echo.com`.
     - `userName` with value `StudentQA`.

2. **Create a Request**:
   - Use the `baseURL` variable to send a GET request to `{{baseURL}}/get?name={{userName}}`.

3. **Test Script**:
   - Validate that the `name` parameter in the response equals `StudentQA`:

```javascript
const jsonData = pm.response.json();
pm.test("Name parameter is correct", function () {
    pm.expect(jsonData.args.name).to.eql(pm.environment.get("userName"));
});
```

4. **Dynamic Updates**:
   - Add a script to update the `userName` variable dynamically:

```javascript
pm.environment.set("userName", "UpdatedQA");
```
   - Send the request again and validate the updated value.

---

#### **Part 2: Writing Advanced Test Scripts**

**Objective**: Practice writing more advanced JavaScript test scripts in Postman.

1. **Create a New Request**:
   - Send a POST request to `{{baseURL}}/post` with the following JSON body:

```json
{
  "age": 25,
  "role": "Tester"
}
```

2. **Add Test Scripts**:
   - Validate that the response includes the correct age and role:

```javascript
const jsonData = pm.response.json();
pm.test("Age is correct", function () {
    pm.expect(jsonData.json.age).to.eql(25);
});
pm.test("Role is correct", function () {
    pm.expect(jsonData.json.role).to.eql("Tester");
});
```

3. **Add Dynamic Variables**:
   - Store the response data as variables:

```javascript
pm.environment.set("responseAge", jsonData.json.age);
pm.environment.set("responseRole", jsonData.json.role);
```

---

#### **Part 3: Advanced Assertions and Validation**

**Objective**: Write custom scripts to validate API responses using JavaScript.

1. **Validate Response Time**:
   - Add the following test script to any request:

```javascript
pm.test("Response time is less than 500ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(500);
});
```

2. **Check Response Structure**:
   - Validate that a response contains all expected fields:

```javascript
const jsonData = pm.response.json();
pm.test("Response has required fields", function () {
    pm.expect(jsonData).to.have.all.keys("id", "name", "age", "role");
});
```

3. **Conditional Logic in Tests**:
   - Write a script that only validates certain fields based on conditions:

```javascript
if (pm.response.json().role === "Tester") {
    pm.test("Role is Tester", function () {
        pm.expect(pm.response.json().role).to.eql("Tester");
    });
} else {
    pm.test("Role is not Tester", function () {
        pm.expect(pm.response.json().role).to.not.eql("Tester");
    });
}
```

---

### **Submission Instructions**

1. **Export Postman Collection**:
   - Navigate to the **Collections** tab in Postman.
   - Find your `QA Academy` collection, click the three dots (...), and select **Export**.

2. **Export Postman Environment**:
   - Navigate to the **Environments** tab.
   - Find the `QA Training` environment, click the three dots (...), and select **Export**.

3. **Submit the Following**:
   - Exported JSON files for the Postman collection and environment.
   - Screenshots of the following:
     - Requests and responses.
     - Console logs showing script execution.

---

### **Key Learning Outcomes**

- Understand and utilize dynamic variables in Postman.
- Write and debug JavaScript test scripts in Postman.
- Use the Postman Console effectively for debugging.
- Validate nested JSON structures using assertions.

---

### **Key Interview Questions**

1. What are the different types of variables in Postman, and how are they used?
2. How can you validate API responses using JavaScript in Postman?
3. What is the Postman Console, and why is it useful?
4. How can you handle dynamic data in Postman requests and tests?

---

### **Tips for Success**

- Practice using variables in different parts of your requests to reinforce learning.
- Debug scripts frequently using the Postman Console to understand errors.
- Explore how to navigate nested JSON objects effectively for deeper validation.
- Use the free resources provided to deepen your understanding of Postman scripting.

---

### **Next Training**

In **Training 3**, we will focus on organizing API requests into Postman collections and automating tests using Newman for streamlined testing workflows.

