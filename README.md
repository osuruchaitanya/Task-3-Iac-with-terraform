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
## 📸 Screenshots
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/ab81f78c41d975f7a84af168977580889eb6796f/screenshot1.png)
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/87711a492bd6f86dcf6b4b2d372e69901cc912ba/screenshot2.png)
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/20503ea3c86ca04a5852a7238e9105789daf28ca/screenshot3.png)
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/ee5c5d759f06a8321e5edb7d1be46839e7411762/screenshot4.png)
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/b121103412fe6e58faadb270585ba956be18171c/screenshot5.png)
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/0e2958a14312bea30d10fce566868a6d5acabf42/screenshot6.png)
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/75ed6b579e486ffd1c126345a7ae1ebb18aadbaf/screenshot7.png)
![image alt](https://github.com/osuruchaitanya/Task-3-Iac-with-terraform/blob/352524d8f59d821a4002b55edbb7e09caa1eb3ea/screenshot8.png)
