# Task 3 - Infrastructure as Code (IaC) with Terraform and Docker (Local)

## 📌 Objective

Use *Terraform* to provision and manage infrastructure locally by deploying an *Nginx container* using *Docker*, without relying on any cloud provider.

--

## 📁 Project Structure

task-3-iac-with-terraform/ ├── main.tf              # Terraform configuration ├── terraform.tfstate    # Terraform state file (auto-generated after apply) ├── .terraform/          # Terraform plugin files (auto-generated) └── README.md            # Project documentation

---

## ⚙ Tools I Used

- [Terraform](https://www.terraform.io/) – Infrastructure as Code
- [Docker](https://www.docker.com/) – Containerization
- [Nginx](https://hub.docker.com/_/nginx) – Web Server image
- Local Windows/Linux machine (no cloud)

---

#### 📸 Screenshots


### ✅ terraform init
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/f858b4ca1b34eb8d23771ec5b3d57c61fae180ae/screenshot1.png)
### ✅ Tterraform validate
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/2709c2bee5d7e0b4e61a1a3e8d2d18403de53a81/screenshot2.png)
# ## ✅ Tterraform plan 
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/eee5b925558109f5bed83a896421e4bd07bd422f/screenshot3.png)
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/cd50b140335c56b8f4dbe86de5d42d5f84e79ae2/screenshot4.png)
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/071c33c58b3940892d01071891c92cec4b2488e0/screenshot5.png)
###  🌐 Nginx Running in Browser
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/7f8af1854a8ba0f6647139c6362a73a20070f9cb/screenshot6.png)
## ✅ Tterraform destroy
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/d3e64a281cda37a0a23847ad5a019ff13e2f7cea/screenshot7.png)
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/b8816dbfd50ade1d1cdb09f9b04196ad3d7c838c/screenshot8.png)
📌 Notes
commands :
terraform init
terraform validate
terraform plan
terraform apply
terraform  destroy
