# Task 3 - Infrastructure as Code (IaC) with Terraform and Docker (Local)

## 📌 Objective

Use *Terraform* to provision and manage infrastructure locally by deploying an *Nginx container* using *Docker*, without relying on any cloud provider.

---

## 📁 Project Structure

task-3-iac-with-terraform/ ├── main.tf              # Terraform configuration ├── terraform.tfstate    # Terraform state file (auto-generated after apply) ├── .terraform/          # Terraform plugin files (auto-generated) └── README.md            # Project documentation

---

## ⚙ Tools Used

- [Terraform](https://www.terraform.io/) – Infrastructure as Code
- [Docker](https://www.docker.com/) – Containerization
- [Nginx](https://hub.docker.com/_/nginx) – Web Server image
- Local Windows/Linux machine (no cloud)

---

## 🚀 Steps to Run the Project

### 1. 📁 Clone the Repository (or create your working folder)

```bash
git clone https://github.com/yourusername/task-3-iac-with-terraform.git
cd task-3-iac-with-terraform

2. 📄 Create main.tf

Paste the following code in your main.tf file:

terraform {
  required_providers {
    docker = {
      source  = "kreuzwerker/docker"
      version = "~> 3.0.2"
    }
  }
}

provider "docker" {}

resource "docker_image" "nginx_image" {
  name         = "nginx:latest"
  keep_locally = false
}

resource "docker_container" "nginx_container" {
  name  = "nginx_container"
  image = docker_image.nginx_image.latest

  ports {
    internal = 80
    external = 8081
  }
}


---

3. 🛠 Initialize Terraform

terraform init

4. ✅ Validate the Configuration

terraform validate

5. 📦 Apply Configuration

terraform apply

Type yes when prompted.


---

🌐 Verify

Open your browser and go to:

http://localhost:8081

You should see the Nginx Welcome Page.


---

🧹 (Optional) Destroy the Container

To stop and delete the container and image:

terraform destroy


---

📌 Notes

This project is fully local. No cloud or remote infrastructure is used.

Ensure Docker Desktop is running before executing Terraform.

Change external port in main.tf if 8081 is already in use.



---

## 📸 Screenshots

### ✅ Terraform Init


<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/b04b0c30-e867-4336-9c3a-f69a25bd65fc" />
<img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/3fb98962-aa1a-4dc5-8a4c-ba907d42946d" />
<img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/a303a5e7-c855-42f1-87bb-ef146a61224a" />
<img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/4eda37cf-e641-464e-9174-6ad281a0391f" />
<img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/14a1470f-0d01-40a8-bd57-7af782ca84d1" />

<img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/50383768-91c0-4eb4-84b5-ae03625f4a04" />
<img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/5b20b696-0cf9-4e86-832d-05b1a7110cf8" />
<img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/8047bd9b-53ea-4482-adfb-79d747754d82" />
<img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/942680f5-2d01-494e-ab94-32d7274eb189" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/83f345cf-c7f8-428d-b9f7-3b0a8aa7aaac" />

<img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/bd5bdde2-1a79-48c1-97e0-17d2081698a1" />

<img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/7c483aa4-91b4-4290-8194-2a2fb069cdf0" /><img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/13f01d40-d806-4ed0-8697-29f4805ae427" />
![Terraform Init](./screenshots/screenshot1.png)

### ✅ Terraform Validate
![Terraform Validate](./screenshots/Screenshot2.png)

### ✅ Terraform Plan
![Terraform Plan](./screenshots/Screenshot 3.png)

### ✅ Terraform Apply - Part 1
![Terraform Apply 1](./screenshots/Screenshot 4.png)

### ✅ Terraform Apply - Part 2
![Terraform Apply 2](./screenshots/screenshot 5.png)

### 🌐 Nginx Running in Browser
![Nginx Output](./screenshots/Screenshot 6.png)
###✅Terraform destroy part 1
![Terraform  destroy(./screenshots/screenshot7.png)
###✅Terraform destroy part 2
![Terraform  destroy(./screenshots/Screenshot8.png)
