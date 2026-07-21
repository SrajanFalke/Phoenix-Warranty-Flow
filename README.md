# Postman API Automation Integration with Github Actions #

This repository is a demonstration for POC for integrating Postman tests with GitHub Actions. The tests are written in Postman and are executed on the VM with the help of Newman and **newman-reporter-htmlextra**.
GitHub Actions will trigger the project execution on every push to the **main** branch. You can also execute the project manually using **workflow_dispatch**. The project runs on a scheduled time with the help of a **cron job**.
The HTML report is archived and kept in the **Artifacts** section for the team to download. Along with that, the team can view the report directly from the GitHub Pages URL:[https://srajanfalke.github.io/Phoenix-Warranty-Flow/]

The latest report is mailed to the team members using **Gmail SMTP**.

## About Me
Hi, my name is **Srajan Falke**. I am a **QA Automation Engineer** with expertise in **Manual Testing**, **API Testing**, and **UI Automation**.
My skill set includes:

- Manual Testing (Functional, Regression, Smoke, Sanity, Accessibility & API Testing)
- UI Automation using **Selenium WebDriver** and **Java**
- API Automation using **Postman** and **Rest Assured**
- Test Framework Development with **TestNG**, **Maven**, **Log4j**, and **Extent Reports**
- CI/CD Integration using **GitHub Actions** and **Jenkins**
- Version Control using **Git** and **GitHub**

I am passionate about building reliable test automation frameworks, improving software quality, and continuously learning modern automation tools and technologies.
You can connect with me on **LinkedIn**:

🔗 https://www.linkedin.com/in/srajan-phalke/

## Testing Coverage

1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data-Driven Testing with CSV
5. Schema Validation
6. Secrets Management with GitHub Secrets

---

## Tech Stack

1. Postman
2. Node.js 22.x
3. Newman
4. newman-reporter-htmlextra
5. GitHub Actions
6. Gmail SMTP
7. GitHub Pages
8. CSV for Data-Driven Testing
9. AWS EC2 Instance for Self-Hosted GitHub Runner.

## Github Pages
You can directly view the latest Postman test report on GitHub Pages:

**GitHub Pages:**  
https://github.com/SrajanFalke/Phoenix-Warranty-Flow

## Project Structure

```text
Phoenix-Inwarranty-Flow
├── Inwarranty-flow Collection.postman_collection.json   # Collection File
├── QA.postman_environment.json                          # Environment File
└── testdata.csv                                         # Test Data File
```

## How to Run the Project

You can run the project on your local system by following these steps:

1. Clone the repository to your local machine:
   ```
   https://github.com/SrajanFalke/Phoenix-Warranty-Flow
  ---
  
2. Install **Node.js** and **npm** from:
   ```
   https://nodejs.org/en
   ```
3. Install Newman globally:
   ```bash
   npm install -g newman
   ```
4. Install the Newman HTML Extra Reporter:
   ```bash
   npm install -g newman-reporter-htmlextra
   ```
5. Execute the Newman command:

   ```bash
   newman run "Inwarranty-flow Collection.postman_collection.json" \
     -e QA.postman_environment.json \
     -d testdata.csv \
     -r cli,htmlextra \
     --reporter-htmlextra-export ./newman/index.html
   ```

---

## HTML Report

The HTML report will be generated inside the **newman** folder.
)
![Postman Report](https://github.com/SrajanFalke/Phoenix-Warranty-Flow/blob/static-content/Newman%20report%20ss.png)
