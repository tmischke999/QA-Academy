# **Month 4: Training 1: Intro to JavaScript for QA**

### **Objective**

JavaScript is a versatile and essential programming language for QA professionals, especially when writing test scripts in tools like Postman. This training focuses on building foundational JavaScript knowledge and understanding JSON, a commonly used data format in API testing.

---

### **Free Online Resources**

1. **[MDN Web Docs: JavaScript Basics](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps)** – A detailed guide to understanding JavaScript fundamentals.
2. **[Learn JavaScript for Free (Codecademy)](https://www.codecademy.com/learn/introduction-to-javascript)** – Beginner-friendly JavaScript lessons.
3. **[freeCodeCamp JavaScript Basics](https://www.freecodecamp.org/learn)** (Optional) – A comprehensive JavaScript course. Students are advised to focus on the following sections:
    - **Core JavaScript Fundamentals**:
        - Variables and Assignment Operators
        - Basic Arithmetic
        - Strings
        - Arrays
        - Functions
    - **Control Structures (Optional)**:
        - Conditionals and Loops
    - **JSON-Related Concepts**:
        - Objects and Data Extraction
    - Spend no more than 2–3 hours, focusing on hands-on practice for QA-related concepts.

---

### **Topics Covered**

#### **JavaScript Basics**

- **Variables**: Introduction to `var`, `let`, and `const`. Include examples like storing your name, age, and favorite QA tools.
- **Data Types**: Strings, numbers, arrays, and objects. Example: Create an array of numbers and access specific elements.
- **Control Structures**: Using `if/else`, `switch`, and loops (`for`, `while`). Example: Use a loop to check if numbers in an array are even or odd.

#### **JSON Syntax**

- Understanding key-value pairs and nested objects. Compare JSON to a dictionary with a key as a word and the value as its definition.
- Writing and parsing JSON with simple examples like extracting values from a JSON object.

#### **Hands-On Examples**

- Declaring variables and performing simple calculations.
- Writing loops to iterate over an array of data and printing results.
- Parsing JSON responses to extract specific values.

#### **Postman Integration**

- Review the Postman interface, focusing on the **Tests** tab.
- Demonstrate how to add and execute test scripts in Postman.
- Walk through an example of using the Postman Console to debug scripts.

---

### **Assignment**

#### **Part 1: JavaScript Basics**

**What to Do:**

1. Declare three variables using `var`, `let`, and `const`:

```javascript
var userName = "John";
let userAge = 25;
const favoriteTools = ["Postman", "Jira", "VS Code"];
```

2. Write an `if/else` statement to check if a number is even or odd:

```javascript
let number = 4;
if (number % 2 === 0) {
    console.log(`${number} is even`);
} else {
    console.log(`${number} is odd`);
}
```

3. Create an array of numbers and loop through it using a `for` loop, logging each number and whether it's even or odd:

```javascript
const numbers = [1, 2, 3, 4, 5];
for (let i = 0; i < numbers.length; i++) {
    if (numbers[i] % 2 === 0) {
        console.log(`${numbers[i]} is even`);
    } else {
        console.log(`${numbers[i]} is odd`);
    }
}
```

**Where to Write the Code:**

- Use an online code editor such as [JSFiddle](https://jsfiddle.net) or [CodePen](https://codepen.io).
- Alternatively, use a local text editor like VS Code. Take a screenshot of your output or save the code in a .txt or .js file for submission.

#### **Part 2: JSON and Postman Test Scripts**

**What to Do:**

1. Use the Postman Echo API to send a GET request to `https://postman-echo.com/get?name=QA`.
2. Add the following test script under the **Tests** tab:

**Parse the JSON response:**

```javascript
const jsonData = pm.response.json();
console.log(jsonData.args.name);
```

**Validate that `args.name` equals "QA":**

```javascript
pm.test("Name is QA", function () {
    pm.expect(jsonData.args.name).to.eql("QA");
});
```

**Add two new parameters to the URL query (age and role) and modify the test script to validate them:**

```javascript
pm.test("Age is 30 and Role is Tester", function () {
    pm.expect(jsonData.args.age).to.eql("30");
    pm.expect(jsonData.args.role).to.eql("Tester");
});
```

3. Use the Postman Console to debug and confirm the output.

**Where to Write the Script:**

- Navigate to the Collections tab in Postman, ensure your QA Academy collection is selected, and create a new request for the GET operation.
- Add your test script under the **Tests** tab.

**Detailed Steps:**

- Open Postman and create a new request in the QA Academy collection.
- Add parameters `name=QA`, `age=30`, and `role=Tester` to the request URL.
- Add the provided JavaScript snippets under the **Tests** tab.
- Execute the request and review results in the Postman Console.

---

### **Submission Instructions**

1. **JavaScript Basics:**
    - Save your exercises in a Google Doc with clear section headings for each task.
    - Include screenshots of the output from your chosen code editor (e.g., JSFiddle, CodePen, or VS Code).

2. **Postman Collection:**
    - Export your Postman collection:
        - Go to the **Collections** tab in Postman.
        - Find your `QA Academy` collection, click on the three dots (...), and select **Export**.
        - Save the JSON file locally.

3. **Postman Environment:**
    - Export your Postman environment:
        - Navigate to the **Environments** tab.
        - Find the environment you used (e.g., `QA` or `Test Server`), click the three dots (...), and select **Export**.
        - Save the JSON file locally.

4. **Screenshots:**
    - Capture screenshots of the following:
        - **API request and response** in Postman.
        - **Postman Console logs** showing the results of your test scripts.

5. **Final Submission:**
    - Upload the following files to the designated Slack channel:
        - Google Doc with JavaScript exercises.
        - Exported JSON files for the Postman collection and environment.
        - Screenshots of the Postman request, response, and Console logs.
    - Ensure all shared files and links have "Anyone with the link can view/comment" permissions.

---

### **Key Learning Outcomes**

- Understand JavaScript fundamentals, including variables, control structures, and JSON.
- Apply JavaScript in QA scenarios to validate API responses and automate basic checks.
- Gain hands-on experience with Postman test scripts.

---

### **Key Interview Questions**

1. What are the differences between `var`, `let`, and `const` in JavaScript?
2. How would you explain the structure of a JSON object to a non-technical person?
3. How can JavaScript be used in Postman for validating API responses?

---

### **Tips for Success**

- Break down each JavaScript topic into small, manageable sections and practice frequently.
- Use the free resources listed above to strengthen your understanding.
- Don’t hesitate to revisit concepts or ask questions if something isn’t clear.

---

### **Next Training**

In **Training 2**, we will dive deeper into using JavaScript specifically within Postman, exploring test scripts, variables, and handling dynamic data in API testing.

