# Jenkins CI/CD Practical Test Submission

---

## Part 1: Multiple Choice Questions (MCQs)

---

**1. What is Jenkins mainly used for?**
   
**Answer: B) Continuous Integration and Continuous Delivery** 

**3. Which type of job allows you to define build steps using code in Jenkins?**
   
**Answer: B) Pipeline Project**

**5. Which file is used to define a pipeline in Jenkins?**

**Answer: C) Jenkinsfile**

**4. What is the purpose of a Jenkins Agent (Node)?**

**Answer: B) To execute jobs assigned by the Jenkins controller**

**5. Which plugin is required to connect Jenkins with GitHub?**

**Answer: B) Git Plugin**

**6. What is the purpose of a Webhook in Jenkins CI/CD?**

**Answer: B) To trigger build automatically on code push**

**7. Which command is used inside Jenkins Pipeline to execute shell commands?**

**Answer: C) sh**

**8. What is the purpose of the post block in Jenkins Pipeline?**

**Answer: B) Execute steps after pipeline stages**

**9. What is the use of sshagent in Jenkins Pipeline?**

**Answer: C) Use stored SSH credentials during execution**

**10. What happens if a stage fails in Jenkins Pipeline (by default)?**

**Answer: B) The pipeline stops execution**

---

## Part 2: Practical Test Execution

---

### Task 1: Infrastructure Setup

#### Two Linux servers were provisioned and configured according to the requirements:

Jenkins Server: Installed Java, Jenkins, and required plugins (Git, Pipeline, SSH Agent). Configured SSH credentials to communicate with the target server securely.

Target Server: Installed Nginx, opened port 80, and ensured the webserver was running and accessible.

SSSSSSSSSSSSSSSSSSSSSSSS

---

### Task 2 & Bonus Task: Deployment and Nginx Configuration

#### Both applications were deployed onto the single target server under distinct directory paths:

FoodHub path: /var/www/html/foodhub

ShopEase path: /var/www/html/shopease

Nginx was configured to serve both websites on port 80 without conflicts using path-based routing.

SSSSSSSSSSSSSSSSSS

---

### Task 3: Jenkins Pipeline Jobs

#### Two separate declarative Jenkins Pipeline jobs were created: FoodHub-Pipeline and ShopEase-Pipeline. Each pipeline successfully clones the respective GitHub repository, copies the files to the target server via SSH, restarts Nginx if necessary, and verifies the deployment.

FoodHub Jenkinsfile Snippet:
sssssssssssssssssssssssss

---

ShopEase Jenkinsfile Snippet:
ssssssssssssssssssssssssssss

---

### Task 4: GitHub Webhooks Configuration

#### Webhooks were successfully configured in both GitHub repositories to trigger the Jenkins pipelines automatically upon any new code push.

SSSSSSSSSSSSSSSSSSSSSSSSSSSSSS

---

### Task 5: Application Changes and Automated Deployment

#### To verify the complete CI/CD flow, the required text changes were made to both repositories, committed, and pushed to GitHub. The webhooks successfully triggered the Jenkins jobs, which automatically deployed the new code.

FoodHub Change: Modified text from "Fresh Food Everyday" to "Delicious Food Delivered Fast".
SSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSS

---

ShopEase Change: Modified text from "Welcome to ShopEase" to "Welcome to ShopEase Online Store".
SSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSS

---

### Task 6: Troubleshooting

#### No major issues were encountered during the setup :)
