# 🔐 Secure DevOps Pipeline Configuration and Vulnerability Report
## Internship Task 4 – DevSecOps Implementation

---

## 📌 Objective

The objective of this task is to design and implement a Secure DevOps (DevSecOps) pipeline using GitHub Actions and SonarCloud to automatically analyze source code and identify security vulnerabilities during the Continuous Integration process.

This task demonstrates how security practices can be integrated into DevOps workflows to ensure safe and reliable software delivery.

---

## 🧠 Introduction

Modern software development requires both speed and security. Traditional development models perform security testing after development, which increases risks and delays deployment.

DevSecOps integrates security directly into the CI/CD pipeline so that vulnerabilities are detected automatically whenever code is pushed to the repository.

This approach enables:

• Continuous security monitoring  
• Automated vulnerability detection  
• Early risk mitigation  
• Secure application lifecycle management  

---

## 🛠 Tools and Technologies Used

• GitHub Repository – Source code management  
• GitHub Actions – CI/CD pipeline automation  
• SonarCloud – Static code analysis & vulnerability scanning  
• Python – Sample application  
• YAML – Pipeline configuration language  

---

## ⚙️ Pipeline Configuration

The pipeline is configured using GitHub Actions workflow files stored inside:

.github/workflows/ci.yml

The workflow automatically executes when code is pushed to the repository branch.

### Pipeline Flow

Developer pushes code
        ↓
GitHub detects repository change
        ↓
GitHub Actions workflow triggered
        ↓
Project dependencies installed
        ↓
SonarCloud security scan executed
        ↓
Code quality and vulnerability analysis
        ↓
Quality Gate evaluation
        ↓
Pipeline success or failure

---

## 📂 Project Directory Structure

Intern_task4/

│
├── app.py
├── requirements.txt
├── sonar-project.properties
├── README.md
└── .github
    └── workflows
        └── ci.yml

---

## 🚀 Implementation Process

### Step 1 — Repository Setup

A GitHub repository was created to host the project files.  
Git was initialized locally and connected to the remote repository.

Commands used:

git init
git add .
git commit -m "Initial commit"
git push origin master

---

### Step 2 — Sample Application Creation

A simple Python application was developed for security analysis testing.

Example code:

print("Hello Secure DevOps")
password = "12345"

The hardcoded password was intentionally added to simulate a vulnerability.

---

### Step 3 — SonarCloud Configuration

1. Logged into SonarCloud using GitHub account.
2. Imported the repository into SonarCloud.
3. Generated authentication token.
4. Added token to GitHub repository secrets.

Secret Name:

SONAR_TOKEN

---

### Step 4 — CI/CD Workflow Creation

A workflow file named ci.yml was created inside:

.github/workflows/

The pipeline performs:

• Code checkout  
• Environment setup  
• Dependency installation  
• SonarCloud scanning  

---

### Step 5 — Automatic Pipeline Execution

Whenever code is pushed:

git push

GitHub Actions automatically runs the pipeline and sends the project for security analysis.

---

## 🔎 Identified Vulnerabilities Report

During analysis, SonarCloud identified security issues in the project.

### Vulnerability Detected

Issue Type: Security Hotspot  
Description: Hardcoded credential detected  
Severity: Medium  
File Location: app.py  

### Risk Explanation

Hardcoding passwords inside source code exposes sensitive information and allows unauthorized access if the repository becomes public or compromised.

---

## 🛠 Vulnerability Remediation

The vulnerability was resolved by replacing hardcoded credentials with environment variables.

### Insecure Code

password = "12345"

### Secure Code

import os
password = os.getenv("APP_PASSWORD")

This prevents credentials from being stored directly in source code.

---

## ✅ Quality Gate Evaluation

SonarCloud Quality Gate verifies whether the project meets defined security and quality standards.

Initial Scan Result: FAILED  
After Fix Implementation: PASSED

The pipeline ensures deployment proceeds only when quality conditions are satisfied.

---

## 📊 Secure DevOps Benefits Achieved

• Automated security scanning  
• Continuous code inspection  
• Early vulnerability detection  
• Improved software reliability  
• Secure CI/CD implementation  

---

## 🎯 Learning Outcomes

Through this task, the following concepts were learned:

• CI/CD pipeline automation  
• DevSecOps principles  
• Static Application Security Testing (SAST)  
• GitHub Actions workflow configuration  
• SonarCloud integration  
• Secure coding practices  

---

## ✅ Conclusion

This task successfully demonstrates the implementation of Secure DevOps practices by integrating security analysis within a CI/CD pipeline.

By automating vulnerability detection using SonarCloud and GitHub Actions, the development workflow becomes more secure, efficient, and reliable.

DevSecOps ensures that security is treated as a continuous process rather than a final step in software development.

---

## 👨‍💻 Author

DevOps Internship Submission  
Secure DevOps Pipeline Implementation
