# Week 4: Training 8 - Wrapping Up Tool Setup

## Objective
By the end of this training, students will:
- Ensure that all tools are installed and properly configured.
- Troubleshoot any remaining setup issues.
- Consolidate all work done in Month 1 into a comprehensive GitHub repository.
- Reflect on their learning journey to reinforce key concepts and build confidence.

---

## Topics Covered

### 1. Verifying Tool Setup
- **Checklist for Tool Verification**:
  - Students will use a detailed checklist to ensure all required tools are installed and configured correctly. This checklist includes:
    - [ ] **VS Code**: Verify installation, settings, and extensions required for Git.
    - [ ] **Git and GitHub**: Ensure Git is configured (username and email), and the repository has been cloned successfully.
    - [ ] **Postman**: Install Postman, set up a new workspace, and configure environment variables.
    - [ ] **Browser Developer Tools**: Make sure they know how to access dev tools in Chrome or Firefox.
    - [ ] **Accessibility Testing Tools**: Verify that **NVDA**, **Axe**, **Lighthouse**, **Wave**, **Color Contrast Checker**, and **WAVE** are installed and ready to use.
    - [ ] **Jira**: Ensure that they can create and update issues within their project.
    - [ ] **Git Configuration**: Confirm Git installation and linking to GitHub. 

### 2. Setting Up Postman 
- **Download and Install Postman**:
  1. **Visit [Postman’s website](https://www.postman.com/downloads/)**.
  2. **Download** the appropriate version for your system (Windows or Mac).
  3. **Install** and open Postman.
  4. **Create an Account**: Sign up with your email to save your workspace.

---

## Practical Assignment

### Part 1:
Students will submit a comprehensive GitHub repository showcasing everything they've worked on in Month 1. This will demonstrate mastery of foundational QA tools, Git, and GitHub.

#### **Repository Structure**
- **Detailed Organization Guidelines**:
  1. **Root Directory**:
     - **README.md**: Provide an overview of what was covered during Month 1. Include summaries of each training week and your learning journey.
  2. **Directories**:
     - **Assignments**: Create a directory named `assignments/` where each file (QA reflection, SDLC diagram, etc.) is stored logically.
     - **Accessibility Audits**: Create a folder called `accessibility_audits/` for all reports related to accessibility exercises.
     - **Branches**: Ensure a separate branch for final submissions (`feature/month1-final-project`) to demonstrate feature work.
  3. **Commit History**:
     - **Commit Messages**: Write clear and descriptive messages like:
       - "Add SDLC flow diagram created in Training 2"
       - "Initial accessibility audit using Lighthouse"

#### **Final Git Commands to Submit**:
- **Create a new branch**:
```bash
git checkout -b feature/month1-final-project
```

- **Add all relevant files**:
```bash
git add .
git commit -m "Add Month 1 final project files and summaries"
```
- **Merge branch into main**:
```bash
git checkout main
git merge feature/month1-final-project
```
- **Push to GitHub**:
```bash
git push origin main
```

  
### Part 2: Setting Up Postman Environment and Practical Assignment
Students will create a Postman environment and complete an API request setup to gain practical experience.

#### **Environment and API Request Practical Assignment**

1. **Review Postman tutorial** - [Variables and Environments](https://learning.postman.com/docs/sending-requests/variables/variables-intro/)

2. **Create Workspace**:
   - **Create a new workspace** in Postman named `QA Academy`:
     1. **Select Workspaces** from the top navigation.
     2. Click on **Create Workspace**.
     3. The setup should default to **Blank Workspace**. Click **Next**.
        - Note: You can check out the other workspace options later.
     4. In the **Name** field, type `QA Academy`.
     5. Under **Who can access your workspace?**, keep it set to **Personal**, then click **Create**.

   - **Review Available Workspaces**:
     1. Select **Workspaces** from the top navigation.
     2. Ensure that two workspaces are available:
        - `QA Academy`
        - `My Workspace` (default)

3. **Create Environment and Variables**:
   - **Select Environment from the Left Navigation**:
     1. On the left-hand side of Postman, click **Environments**.
     2. Click the **Create Environment** link located in the environment panel.

   - **Add Environment Details**:
     1. **Name**: Enter `QA` for the environment name.

   - **Add Variables**:
     1. Under the new `QA` environment, enter the following information:
        - **Variable Name**: Enter `baseURL`.
        - **Initial Value**: Enter `https://postman-echo.com`.
        - **Current Value**: Enter `https://postman-echo.com`.
     2. Click **Save**.
        - This variable will be used to store the base URL for your API requests.

   - **Review Available Environments**:
     1. In the **Environment** panel, ensure that two environments are available:
        - `Globals` (default)
        - `QA`

4. **Create Collection**:
   - **Create a new collection** in Postman named `QA Academy`:
     1. Select **Collections** from the left navigation.
     2. Click the **Create Collection** button located in the environment panel. 
     3. **Name**: Enter `QA Academy` for the collection name.

5. **Perform a Basic API Request using Postman Echo**:
   - We will use Postman's [Postman Echo](https://www.postman-echo.com/get) as a practice API to understand how requests work.
     1. **Create a New Request** in the `QA Academy` collection.
        - Click on the **Add a request** link within your collection.
        - **Name**: Enter `GET Postman Echo` for the request name.
     2. **Set the Method Type**:
        - Click on the dropdown to the left of the URL field.
        - Select **GET** as the method type.
     3. **Set Up the Request URL**:
        - In the **URL field**, enter `{{baseURL}}`.
        - This uses the variable you created for the base URL, which makes the request flexible and reusable.
        - Tip: Hover over the variable to see the value.
     4. **Add Parameters**:
        - Click on the **Params** tab.
        - Add a parameter called `sampleKey` with a value of `sampleValue`.
        - Note how the URL value updates.
     5. **Send the Request**:
        - Click the **Send** button to make the request.
     6. **View the Response**:
        - Observe the response in the **Body** tab.
        - Notice how the parameters you added appear in the response.
     7. **Add Documentation**:
        - Click on the Documentation icon in the right navigation to add a short description.
        - Explain that this is a practice GET request to understand how the Postman Echo API returns data.
     8. **Save the Request**:
        - Save the request in a collection named `QA Academy Practice Requests` for future reference.

### Export Postman Workspace and Environment

**Export Environment**:
- Click **Environment** in the left navigation of Postman.
- Click the ellipsis next to your `QA` environment.
- Select **Export** from the dropdown menu.  
- Save the JSON file.

**Export Collection**:
- Click **Collections** in the left navigation of Postman.
- Click the ellipsis next to your `QA Academy` environment.
- Select **Export** from the dropdown menu.  
- Save the JSON file.

**Submit**:
- Upload both JSON files (environment and collection) to the Slack channel for review and feedback.


### **Part 3: Reflection Document**
- **Key Takeaways**: Summarize the key skills acquired.
- **Challenges and Solutions**: Reflect on challenges and how they were overcome.
- **Applications in QA**: Describe how these tools and concepts will be useful in a QA role.

**Submit this reflection document** as a separate commit:
```bash
git add reflection_month1.txt
git commit -m "Add Month 1 reflection document"
git push origin main
```

---

## Key Interview Questions
By the end of this training, students should be able to confidently answer:
1. **What tools did you set up and use during Month 1, and what is their purpose?**
2. **What is the importance of version control in QA?**
3. **How does accessibility testing contribute to software quality?**
4. **What common issues did you face during tool setup, and how did you solve them?**
5. **Explain how Git branching is used to manage changes effectively in a project.**

---

## Tips for Success
- **Use the Checklist**: Make sure every item is checked off before moving to Month 2.
- **Ask Questions**: If any tools are still unclear, ask for help now to avoid challenges later.
- **Practice in Postman**: Start familiarizing yourself with the interface and making simple requests to prepare for API testing next month.
- **Collaborate with Peers**: Compare GitHub repository structures and ask peers for feedback to ensure your submissions are well-organized.

---

## Key Deliverables for Month 1
1. **All Tools Installed and Configured**:
   - VS Code, Postman, browser developer tools, NVDA, Axe, Lighthouse, Wave, Color Contrast Checker, WAVE, Git, and Jira.
2. **GitHub Repository Created with Key Documents**:
   - **README** summarizing Month 1.
   - **Assignments and Reflections** organized clearly.
   - **Branch Structure** showing Git and GitHub knowledge.

---

## Preparing for Month 2

- **Outline of What to Expect in Month 2**:
  - **Manual Testing Fundamentals**:
    - Learn how to write **test cases**, focusing on **functional testing**.
    - Understand the different types of testing techniques, like **boundary testing**, **equivalence partitioning**, and **decision table testing**.
    - Practice creating and executing **test cases** with real-world scenarios.
  - **Bug Reporting**:
    - Learn how to write effective bug reports using **Jira**.
    - Practice documenting issues in a detailed and structured way, including steps to reproduce, expected vs actual behavior, severity, and priority.
  - **Exploratory Testing**:
    - Understand and practice **exploratory testing** techniques.
    - Learn how to identify gaps in testing by using exploratory methods to discover unexpected behaviors.
  - **Skills Application**:
    - Participants will begin applying the tools they set up in Month 1 to **actual testing scenarios**.
    - Tools like **Jira**, **browser dev tools**, and **Postman** will be incorporated into hands-on testing assignments.

### Preparing for Month 2 with a Checklist
- **Checklist of Essential Skills and Tools Learned in Month 1**:
  - **Tools Setup Verification**:
    - [ ] Installed and configured **VS Code** and **Git**.
    - [ ] Installed **Postman** and configured the workspace.
    - [ ] Verified browser **developer tools** functionality.
    - [ ] Installed and set up **NVDA**, **Axe**, **Lighthouse**, **Wave**, **Color Contrast Checker**, and **WAVE**.
    - [ ] Set up and tested **Jira**.
    - [ ] Created a **GitHub** repository, practiced basic Git commands, and verified branch setup.

  - **Skill Review**:
    - [ ] Completed a **QA reflection document** about the QA role.
    - [ ] Created an **SDLC flow diagram**.
    - [ ] Written **summaries** of QA tools and their uses.
    - [ ] Performed an **accessibility audit** using Lighthouse.
    - [ ] Practiced **branching** in GitHub by creating and merging branches.
    - [ ] Written a **personal README** with Month 1 reflections.
    - [ ] Logged a **mock bug** in Jira with appropriate details.
    - [ ] Created and exported a **Postman workspace and environment**.
    - [ ] Completed a **basic API request** using Postman Echo.
    - [ ] Uploaded all assignments and reflections into the **GitHub repository** with correct directory structure.
    - [ ] Practiced **committing and merging** changes in GitHub, including creating a feature branch and merging it back into the main branch.