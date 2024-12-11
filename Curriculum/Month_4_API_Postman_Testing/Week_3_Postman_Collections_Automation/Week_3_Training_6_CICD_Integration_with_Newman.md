 # **Month 4: Training 6 - CI/CD Integration with Newman**

## **Objective**

In this training session, students will learn how to integrate their automated API tests with Continuous Integration/Continuous Deployment (CI/CD) pipelines using GitHub Actions. By the end of this session, students will:

- Understand the basics of CI/CD pipelines.
- Create and configure GitHub Actions workflows to automate Newman runs.
- Troubleshoot and debug CI/CD pipeline issues.

---

## **Free Online Resources**

### **Mandatory Resources**

1. **[Using Newman CLI](https://learning.postman.com/docs/collections/using-newman-cli/command-line-integration-with-newman/)**  
   - A guide to integrating Newman with Postman collections.

2. **[CI/CD Integrations with Postman](https://learning.postman.com/docs/integrations/ci-integrations/)**  
   - Postman’s official documentation on CI/CD integrations.

3. **[Driving Pipeline Automation with Newman and Postman API](https://www.postman.com/postman-galaxy/driving-pipeline-automation-with-newman-and-postman-api/)**  
   - Insights into pipeline automation with Newman and the Postman API.

4. **[YouTube: Postman CI/CD Pipeline with GitHub Actions](https://www.youtube.com/watch?v=ZlTzOIv88o8)**  
   - A video tutorial on setting up GitHub Actions for Newman collections.

5. **[TechTarget: CI/CD Pipelines Explained](https://www.techtarget.com/searchsoftwarequality/CI-CD-pipelines-explained-Everything-you-need-to-know)**  
   - Comprehensive overview of CI/CD pipelines, their components, and benefits.

---

## **Topics Covered**

### **1. Overview of CI/CD Pipelines**
- **Explanation**: CI/CD pipelines automate the process of integrating and deploying code changes.
- **Key Components**:
  - Continuous Integration: Automatically tests and integrates code changes.
  - Continuous Deployment: Automatically deploys the tested code to production or staging environments.
- **Benefits**: Faster deployment cycles, fewer errors, and improved collaboration.

### **2. Introduction to GitHub Actions**
- **Overview**: GitHub Actions enables automation of workflows directly within GitHub repositories.
- **Key Features**:
  - Pre-built actions for common tasks.
  - Support for custom workflows.
  - Integration with popular tools like Newman.
- **Structure of a Workflow File**:
  - `name`: Workflow name.
  - `on`: Trigger events (e.g., `push`, `pull_request`).
  - `jobs`: Steps to execute.

### **3. Setting Up a CI/CD Pipeline with Newman**
- **Preparation**:
  - Ensure Node.js and Newman are installed locally for testing.
  - Use the forked Postman Echo Collection.
- **Workflow Creation**:
  - Create a `.github/workflows` directory.
  - Write a YAML file to define the workflow steps:
    ```yaml
    name: Newman Collection Run
    on:
      push:
        branches:
          - main
    jobs:
      run-newman:
        runs-on: ubuntu-latest
        steps:
          - name: Checkout code
            uses: actions/checkout@v2
          - name: Set up Node.js
            uses: actions/setup-node@v3
            with:
              node-version: '16'
          - name: Install Newman
            run: npm install -g newman
          - name: Run Postman Collection
            run: newman run postman-echo-collection.json
    ```

### **4. Troubleshooting and Debugging CI/CD Pipelines**
- **Common Issues**:
  - Missing dependencies (e.g., Node.js).
  - Incorrect file paths or syntax errors in YAML files.
  - Failing tests in Newman runs.
- **Troubleshooting Tools**:
  - Use the `--verbose` Newman flag for detailed logs.
  - Enable GitHub Actions log output for debugging.
- **Tips for Success**:
  - Test workflows locally before committing to GitHub.
  - Use descriptive commit messages to track changes.

---

## **Assignment**

### **Part 1: Automating Newman in GitHub Actions**

1. **Objective**: Simulate a basic CI/CD pipeline by automating the execution of your Postman Echo Collection in GitHub Actions.

2. **Instructions**:
   - **Set Up Your Repository**:
     1. Log in to GitHub and create a new repository:
        - Click on your profile picture (top-right corner) > Your repositories > New.
        - Name your repository (e.g., `newman-automation`) and set it to Public or Private.
        - Click **Create repository**.
     2. Clone the repository to your local machine:
        - Copy the repository URL (e.g., `https://github.com/username/newman-automation.git`).
        - Open your Command Prompt or Terminal and run:
          ```bash
          git clone <repository-url>
          ```
        - Navigate into the repository folder:
          ```bash
          cd newman-automation
          ```
     3. Add your Postman Echo Collection JSON file to the repository:
        - Save your collection as `postman-echo-collection.json` in the repository folder.

   - **Create the `.github/workflows` Directory**:
     1. Inside your repository folder, create the `.github` directory:
        ```bash
        mkdir -p .github/workflows
        ```
     2. Navigate to the `workflows` directory:
        ```bash
        cd .github/workflows
        ```
     3. Create the workflow file:
        ```bash
        touch newman.yml
        ```
     4. Open the `newman.yml` file in a text editor (e.g., Notepad or VS Code) and paste the following YAML content:
        ```yaml
        name: Newman Collection Run
        on:
          push:
            branches:
              - main
        jobs:
          run-newman:
            runs-on: ubuntu-latest
            steps:
              - name: Checkout code
                uses: actions/checkout@v2
              - name: Set up Node.js
                uses: actions/setup-node@v3
                with:
                  node-version: '16'
              - name: Install Newman
                run: npm install -g newman
              - name: Run Postman Collection
                run: newman run postman-echo-collection.json
        ```

   - **Push Your Changes**:
     1. Save the `newman.yml` file and navigate back to the root of your repository:
        ```bash
        cd ../../
        ```
     2. Add all files to Git:
        ```bash
        git add .
        ```
     3. Commit your changes:
        ```bash
        git commit -m "Add GitHub Actions workflow for Newman"
        ```
     4. Push your changes to GitHub:
        ```bash
        git push origin main
        ```

   - **Observe Workflow Execution**:
     1. Go to your GitHub repository page.
     2. Click on the **Actions** tab to view your workflow's progress.
     3. Monitor the logs for successful execution and any potential errors.

### **Part 2: Enhancing the Collection with Custom Test Scripts**

1. **Objective**: Add additional test scripts to your Postman Echo Collection.

2. **Instructions**:
   - Open Postman and navigate to your forked Postman Echo Collection.
   - Select a request (e.g., `GET /get`) and click on the **Tests** tab.
   - Add the following tests:
     - **Status Code Check**:
       ```javascript
       pm.test("Status code is 200", function () {
           pm.response.to.have.status(200);
       });
       ```
     - **Header Validation**:
       ```javascript
       pm.test("Content-Type is application/json", function () {
           pm.response.to.have.header("Content-Type", "application/json");
       });
       ```
     - **Response Time Check**:
       ```javascript
       pm.test("Response time is less than 300ms", function () {
           pm.expect(pm.response.responseTime).to.be.below(300);
       });
       ```
   - Save your changes and export the collection:
     - Click on the three dots next to the collection name > Export.
     - Save the file as `postman-echo-collection-updated.json`.

   - **Run the Updated Collection in GitHub Actions**:
     1. Replace the `postman-echo-collection.json` in your repository with `postman-echo-collection-updated.json`.
     2. Commit and push the changes:
        ```bash
        git add .
        git commit -m "Update Postman Echo Collection with custom scripts"
        git push origin main
        ```
     3. Monitor the new workflow run in the **Actions** tab.

### **Part 3: Debugging Newman Runs**

1. **Objective**: Learn to troubleshoot and debug failed Newman runs.

2. **Instructions**:
   - **Introduce an Intentional Error**:
     - Modify one request in the collection to produce an error (e.g., change the endpoint URL to `/invalid-endpoint`).
   - **Run in Newman Locally**:
     - Execute the collection locally using verbose mode:
       ```bash
       newman run postman-echo-collection-updated.json --verbose
       ```
     - Review the detailed output for the source of the failure.
   - **Debug and Fix the Issue**:
     - Revert the intentional error and re-run the collection.

---

## **Submission Instructions**

1. Submit the following:
   - Updated Postman Echo Collection JSON file.
   - YAML workflow file for GitHub Actions.
   - CLI logs showing successful and failed runs.
   - A Google Doc summarizing:
     - Steps taken to automate the collection.
     - Challenges faced and how you resolved them.
     - Reflections on CI/CD pipeline integration.

---

## **Key Learning Outcomes**

- Understand the basics of CI/CD pipelines.
- Gain hands-on experience integrating Newman into GitHub Actions workflows.
- Learn effective debugging and troubleshooting techniques for automated testing.

---

## **Key Interview Questions**

1. What is CI/CD, and why is it important in modern software development?
2. How does Newman integrate into a CI/CD pipeline?
3. What are the key components of a GitHub Actions workflow?
4. How do you troubleshoot common errors in CI/CD pipelines?

---

## **Tips for Success**

- Take time to understand each component of the GitHub Actions workflow file.
- Use the Postman Console and Newman flags to debug effectively.
- Practice modifying and re-running workflows to solidify your understanding.

---

## **Next Training**

In **Training 7**, we will explore creating comprehensive API test summary reports and reflect on the progress made in API testing, laying the groundwork for Month 5’s advanced topics.
