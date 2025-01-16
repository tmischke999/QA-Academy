# **Training 7: Advanced Playwright Techniques**

## **Objective**
Expand on foundational Playwright knowledge by introducing advanced techniques. Students will learn how to create reusable test components, use test data files for dynamic testing, and configure cross-browser test executions. By the end of this training, students will:

- Understand how to modularize and reuse test components.
- Integrate JSON or CSV files for data-driven testing.
- Set up and execute tests across multiple browsers.

---

## **Free Online Resources (Mandatory)**

1. **[Playwright Official Documentation](https://playwright.dev/docs/intro)**
   - Comprehensive guide for advanced features of Playwright.
   - [Reusable Components](https://playwright.dev/docs/test-advanced/).
2. **[Data-Driven Testing with Playwright](https://playwright.dev/docs/test-parameterize)**
   - A guide to implementing parameterized and data-driven tests.
3. **[Cross-Browser Testing in Playwright](https://playwright.dev/docs/browsers)**
   - Official documentation for configuring and running cross-browser tests.
4. **[How to Use JSON in JavaScript](https://www.w3schools.com/js/js_json_intro.asp)**
   - A beginner-friendly tutorial for understanding JSON data.
5. **[Using CSV Files in Node.js](https://www.geeksforgeeks.org/how-to-read-and-write-csv-files-using-node-js/)**
   - A practical guide for working with CSV files in Node.js.

---

## **Topics Covered**

### **1. Reusable Test Components and Modularization**

#### **Step 1: Why Modularize Tests?**
- **Improves Maintainability**: Makes test scripts easier to update.
- **Reduces Redundancy**: Avoids duplicating code for similar test steps.

#### **Step 2: Creating Reusable Components**
1. **Example: Form Filling Utility**:
   - Create a helper function for repetitive form-filling actions:
     ```typescript
     export async function fillLoginForm(page, username, password) {
         await page.fill('#username', username);
         await page.fill('#password', password);
         await page.click('button[type="submit"]');
     }
     ```
2. **Organize Reusable Code**:
   - Save helper functions in a `utils/` folder (e.g., `tests/utils/helpers.ts`).
   - Import and use these helpers in your tests:
     ```typescript
     import { fillLoginForm } from '../utils/helpers';

     test('Login Test with Helper', async ({ page }) => {
         await page.goto('https://the-internet.herokuapp.com/login');
         await fillLoginForm(page, 'tomsmith', 'SuperSecretPassword!');
         await expect(page.locator('#flash')).toContainText('You logged into a secure area!');
     });
     ```

---

### **2. Data-Driven Testing with JSON and CSV**

#### **Step 1: Why Use Test Data Files?**
- **Scalability**: Test multiple scenarios with minimal changes to the script.
- **Flexibility**: Centralize data management for better test organization.

#### **Step 2: Implementing Data-Driven Tests**
1. **Using JSON Data**:
   - Create a `data.json` file:
     ```json
     [
         { "username": "tomsmith", "password": "SuperSecretPassword!", "expected": "You logged into a secure area!" },
         { "username": "invalidUser", "password": "wrongPassword", "expected": "Your username is invalid!" }
     ]
     ```
   - Write a parameterized test to use this data:
     ```typescript
     import testData from './data.json';

     test.describe('Data-Driven Login Tests', () => {
         for (const data of testData) {
             test(`Login Test for ${data.username}`, async ({ page }) => {
                 await page.goto('https://the-internet.herokuapp.com/login');
                 await page.fill('#username', data.username);
                 await page.fill('#password', data.password);
                 await page.click('button[type="submit"]');
                 await expect(page.locator('#flash')).toContainText(data.expected);
             });
         }
     });
     ```

2. **Using CSV Data**:
   - Install a library to parse CSV files (e.g., `csv-parser`):
     ```bash
     npm install csv-parser
     ```
   - Create a `data.csv` file:
     ```csv
     username,password,expected
     tomsmith,SuperSecretPassword!,You logged into a secure area!
     invalidUser,wrongPassword,Your username is invalid!
     ```
   - Read and use this data in a test:
     ```typescript
     import fs from 'fs';
     import csv from 'csv-parser';

     test.describe('CSV Data-Driven Login Tests', () => {
         const results = [];

         beforeAll(async () => {
             fs.createReadStream('./data.csv')
                 .pipe(csv())
                 .on('data', (row) => results.push(row));
         });

         test('Run Tests', async ({ page }) => {
             for (const data of results) {
                 await page.goto('https://the-internet.herokuapp.com/login');
                 await page.fill('#username', data.username);
                 await page.fill('#password', data.password);
                 await page.click('button[type="submit"]');
                 await expect(page.locator('#flash')).toContainText(data.expected);
             }
         });
     });
     ```

---

### **3. Cross-Browser Testing**

#### **Step 1: Setting Up Cross-Browser Configuration**
1. Update `playwright.config.ts`:
   ```typescript
   import { defineConfig } from '@playwright/test';

   export default defineConfig({
       projects: [
           { name: 'Chromium', use: { browserName: 'chromium' } },
           { name: 'Firefox', use: { browserName: 'firefox' } },
           { name: 'WebKit', use: { browserName: 'webkit' } },
       ],
   });
   ```

2. Execute Tests Across Browsers:
   ```bash
   npx playwright test --project=Chromium
   npx playwright test --project=Firefox
   npx playwright test --project=WebKit
   ```

#### **Step 2: Writing Cross-Browser Tests**
- Ensure tests are compatible across all supported browsers.
- Use browser-specific conditions if necessary:
  ```typescript
  test('Browser-Specific Test', async ({ browserName, page }) => {
      if (browserName === 'firefox') {
          console.log('Running on Firefox');
      }
      await page.goto('https://example.com');
  });
  ```

---

## **Assignment**

### **Step-by-Step Instructions**

1. **Create Reusable Components**:
   - Write a utility function for form filling and save it in a `utils/` folder.
   - Use this function in at least one test case.

2. **Implement Data-Driven Tests**:
   - Create a `data.json` or `data.csv` file with login scenarios.
   - Write parameterized tests to use this data.

3. **Run Cross-Browser Tests**:
   - Update `playwright.config.ts` to enable cross-browser testing.
   - Execute tests on Chromium, Firefox, and WebKit.

4. **Push Changes to GitHub**:
   - Commit your work and push to GitHub.
   - Share your repository link in the QA Academy Slack channel.

---

## **Key Learning Outcomes**

- Modularize Playwright test code for better maintainability.
- Execute data-driven tests using JSON or CSV files.
- Configure and run cross-browser tests in Playwright.

---

## **Key Interview Questions**

1. How do you create reusable test components in Playwright?
2. What are the benefits of data-driven testing, and how can you implement it?
3. How do you configure Playwright for cross-browser execution?
4. What challenges might arise in cross-browser testing, and how do you address them?

---

## **Tips for Success**

- Focus on creating clean and modular test scripts.
- Use Playwright’s debugging tools if tests fail across browsers.
- Keep test data organized and up to date for easier maintenance.
- Commit changes frequently to track progress effectively.

---

## **Next Training**
In **Training 8**, students will consolidate their Playwright skills by creating a comprehensive test suite, including performance tests, exploratory tests, and reusable components for a mock application.

