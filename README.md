# Task 3 - Infrastructure as Code (IaC) with Terraform and Docker (Local)

## 📌 Objective

Use *Terraform* to provision and manage infrastructure locally by deploying an *Nginx container* using *Docker*, without relying on any cloud provider.

--
## ⚙ Tools I Used

- [Terraform](https://www.terraform.io/) – Infrastructure as Code
- [Docker](https://www.docker.com/) – Containerization
- [Nginx](https://hub.docker.com/_/nginx) – Web Server image
- Local Windows/Linux machine (no cloud)


##  WHAT  I  DID

In this project (Task 3 - IaC with Terraform), I implemented a complete end-to-end infrastructure automation workflow using *Terraform*. Here's a breakdown of what I accomplished:

- ✅ *Initialized a new GitHub repository* named Task-3-Iac-with-terraform to store all project files and documentation.
- ✅ **Created a main.tf Terraform configuration file** to provision an Nginx server on a local virtual machine or compatible infrastructure.
- ✅ *Used core Terraform commands* to manage the infrastructure lifecycle:
  - terraform init to initialize the working directory
  - terraform validate to validate syntax and structure
  - terraform plan to preview changes before deployment
  - terraform apply to provision the Nginx server
  - terraform destroy to decommission the infrastructure
- ✅ *Captured screenshots* of each step (init, validate, plan, apply, Nginx verification, and destroy) to visually document the process.
- ✅ *Uploaded all 8 screenshots* to the repository and ensured they are displayed properly in the README.md.
- ✅ *Verified Nginx server accessibility* by accessing it through a web browser after successful deployment.
- ✅ **Wrote a detailed README.md file** explaining the project, tools used, step-by-step actions, and results, with properly embedded screenshots.

This project reflects the core concepts of *Infrastructure as Code*, automation, version control, and documentation — all implemented using a single Terraform file and GitHub.
 
---
# 📁 Project Structure
Task-3-Iac-with-terraform/
│
├── main.tf                
├── README.md              
├──  8 screenshots
---

#### 📸 Screenshots


### ✅ terraform init
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/f858b4ca1b34eb8d23771ec5b3d57c61fae180ae/screenshot1.png)
### ✅ terraform validate
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/2709c2bee5d7e0b4e61a1a3e8d2d18403de53a81/screenshot2.png)
# ## ✅ terraform plan 
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/eee5b925558109f5bed83a896421e4bd07bd422f/screenshot3.png)
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/cd50b140335c56b8f4dbe86de5d42d5f84e79ae2/screenshot4.png)
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/071c33c58b3940892d01071891c92cec4b2488e0/screenshot5.png)
## terraform apply
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/ae8d722d0f22699c9caf6d6703e8ec45825ed827/screenshot6a.png)
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/0c2c9799aa9c074c09a3d0190da6761348e94a24/screenshot6b.png)

###  🌐 Nginx Running in Browser
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/7f8af1854a8ba0f6647139c6362a73a20070f9cb/screenshot6.png)
## ✅ terraform destroy
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/d3e64a281cda37a0a23847ad5a019ff13e2f7cea/screenshot7.png)
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/b8816dbfd50ade1d1cdb09f9b04196ad3d7c838c/screenshot8.png)


 ## 🔧 Terraform Commands Used
''''bash
terraform init
terraform validate
terraform plan
terraform apply
terraform  destroy## # 🚀 Task 3: Terraform Project – Nginx Deployment

This project demonstrates how to use *Terraform* to deploy an *Nginx server* using Infrastructure as Code (IaC).  
It includes the full Terraform workflow with screenshots.

---
---

## 🔧 Terraform Commands Used

 ```bash

- terraform init  
  → Initializes the working directory and downloads required provider plugins.

- terraform validate  
  → Checks whether the configuration syntax is valid and internally consistent.

- terraform plan  
  → Creates an execution plan, showing what actions Terraform will take before making any changes.

- terraform apply  
  → Applies the changes required to reach the desired infrastructure state as defined in main.tf.

- terraform destroy  
  → Safely removes all resources created by Terraform and cleans up the environment.
