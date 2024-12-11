# **Month 4: Training 3 - Organizing API Requests and Introduction to Newman**

### **Objective**

This training introduces students to organizing API requests into Postman collections and automating API testing using Newman. By the end of this session, students will:

- Understand the importance of organizing API requests into collections.
- Learn how to create and manage Postman collections.
- Gain hands-on experience running automated tests using Newman.

---

### **Free Online Resources**

1. **[Postman Collections (Postman Learning Center)](https://learning.postman.com/docs/sending-requests/intro-to-collections/)**
   - A detailed guide to creating and managing collections in Postman.

2. **[Postman and Newman Basics (Postman Blog)](https://blog.postman.com/how-to-use-newman-to-run-collections/)**
   - A beginner-friendly overview of Newman and its integration with Postman collections.

3. **[Running Postman Collections with Newman (YouTube)](https://www.youtube.com/watch?v=XGbB9pd9YAc)**
   - A step-by-step tutorial for using Newman.

---

### **Topics Covered**

#### **1. Organizing API Requests into Collections**

- **Overview**:
  - Collections allow users to group related API requests for easier management and testing.
  - Benefits include better organization, reusability, and the ability to run multiple requests in a sequence.

- **Hands-On Practice**:
  - Creating a new collection.
  - Adding requests to a collection.
  - Documenting requests with descriptions and comments.

#### **2. Introduction to Newman**

- **Overview**:
  - Newman is a command-line tool used to run Postman collections in automated workflows.
  - Key advantages include integrating Postman tests into CI/CD pipelines and running tests from the command line.

- **Hands-On Practice**:
  - Installing Newman using Node.js.
  - Running a simple Postman collection with Newman.
  - Understanding Newman output, including test results and logs.

#### **3. Exporting Collections and Environments**

- **Steps to Export**:
  - Navigate to the Postman **Collections** tab, click the three dots ("...") next to a collection, and select **Export**.
  - Repeat for the Postman **Environments** tab to export the `QA Training` environment.

---

### **Assignment**

#### **Part 1: Create and Document a Collection**

**Objective**: Organize API requests into a collection and add documentation for clarity.

1. **Create a Collection**:
   - Name the collection `Month 4 API Testing`.
   - Add the following requests to the collection:
     - A GET request to `https://postman-echo.com/get?test=collection`.
     - A POST request to `https://postman-echo.com/post` with a JSON body:

```json
{
  "key": "value"
}
```

2. **Document the Collection**:
   - Add descriptions to each request explaining their purpose.
   - Include comments about the expected response structure.

---

#### **Part 2: Automate and Run the Collection with Newman**

**Objective**: Execute the collection using Newman and analyze the output.

1. **Check Node.js and npm Installation**:
   - Open Command Prompt (Windows) or Terminal (macOS/Linux).
   - Run the following commands to check if Node.js and npm are installed:

```bash
node -v
npm -v
```
   - If not installed, download and install Node.js from [Node.js Official Website](https://nodejs.org/).

2. **Install Newman**:
   - Run the following command to install Newman globally:

```bash
npm install -g newman
```

3. **Run the Collection**:
   - Navigate to the folder where the collection and environment files are saved.
   - Run the following command:

```bash
newman run <path-to-collection-file> -e <path-to-environment-file>
```

4. **Analyze the Output**:
   - Review the Command Prompt or Terminal output for test results.
   - Note any errors or failed tests and document their possible causes.

*Note*: If you encounter any challenges, consider using tools like ChatGPT to troubleshoot and resolve issues. Paste your error message or question into ChatGPT for assistance.

---

#### **Part 3: Enhance the Collection with Assertions**

**Objective**: Add test scripts to the collection requests to validate responses dynamically.

1. **Add Test Scripts**:
   - **GET Request**:

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

   - **POST Request**:

```javascript
const jsonData = pm.response.json();
pm.test("Key value is correct", function () {
    pm.expect(jsonData.json.key).to.eql("value");
});
```

2. **Run the Enhanced Collection**:
   - Use Newman to run the updated collection.
   - Analyze the output to ensure all assertions pass.

---

### **Submission Instructions**

1. **Export and Submit**:
   - Export the `Month 4 API Testing` collection and the `QA Training` environment.
   - Submit the exported JSON files.

2. **Provide Logs**:
   - Save the Command Prompt or Terminal output from the Newman run and submit it as a text file.

3. **Documentation**:
   - Create a Google Doc summarizing the assignment, including:
     - Screenshots of request responses.
     - Any errors encountered and their resolution.
     - Reflections on using Newman for automation.

---

### **Key Learning Outcomes**

- Organize API requests into collections for efficient testing.
- Understand the basics of automating tests with Newman.
- Use Postman and Newman to validate API responses dynamically.

---

### **Key Interview Questions**

1. What are the benefits of organizing API requests into collections?
2. How does Newman enhance the capabilities of Postman?
3. What steps are involved in running a Postman collection using Newman?

---

### **Tips for Success**

- Double-check your JSON syntax when creating requests and test scripts.
- Use the Postman Console to debug and ensure requests are correctly configured.
- Explore additional Newman features, such as running tests with data files, for extended functionality.

---

### **Next Training**

In **Training 4**, we will dive deeper into handling edge cases and error responses, as well as exploring mock APIs for more advanced testing scenarios.