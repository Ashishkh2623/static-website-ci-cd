# 🚀 CI/CD Pipeline for Static Website Deployment

This project showcases a CI/CD pipeline that deploys a static website automatically using GitHub Actions and an AWS EC2 instance.  
Every update pushed to GitHub is deployed to the EC2 server running Apache.

---

## 🧠 Project Description

The goal of this project is to demonstrate continuous integration and continuous deployment for a static website.  
The website is hosted on an AWS EC2 instance, and the deployment process is automated using GitHub Actions.

---

## ✨ Key Features

- 📄 Static website built with HTML and CSS
- ☁️ Deployed on AWS EC2
- 🌐 Apache used as the web server
- 🔁 Automated deployment with GitHub Actions
- 🔐 Secure deployment using SSH
- ❌ No manual intervention required after setup

---

## 🛠️ Technologies Used

### Frontend
- HTML
- CSS

### CI/CD Tools
- GitHub
- GitHub Actions

### Cloud Infrastructure
- AWS EC2 (Ubuntu)
- Apache Web Server

---

## 📁 Directory Structure

static-website-ci-cd/
├── index.html
├── style.css
├── README.md
└── .github/
    └── workflows/
        └── deploy.yml

---

## 🌐 Application URL

The deployed website can be accessed using the EC2 public IP:

http://<EC2_PUBLIC_IP>

---

## 🛠️ Installation & Setup

### Requirements
- Ubuntu-based EC2 instance
- Apache Web Server
- GitHub account
- SSH access to the server

---

## 🔹 Step 1: Clone the GitHub Repository

git clone https://github.com/Ashishkh2623/static-website-ci-cd.git

---

## 🔹 Step 2: Apache Installation on EC2

sudo apt update  
sudo apt install apache2 -y  
sudo systemctl start apache2  
sudo systemctl enable apache2  

Apache document root:  
/var/www/html

---

## 🔹 Step 3: GitHub Actions CI/CD Pipeline

On every push to the `main` branch, GitHub Actions:
- Establishes an SSH connection to the EC2 instance
- Deploys website files to the Apache directory
- Restarts the Apache service

Workflow file path:  
.github/workflows/deploy.yml

---

## 🔐 GitHub Secrets Used

The following secrets are configured in GitHub Actions:

- EC2_HOST – EC2 public IP address
- EC2_USER – ubuntu
- EC2_SSH_KEY – SSH private key

---

## 🔁 CI/CD Process Flow

GitHub Commit → GitHub Actions → EC2 Server → Apache → Website Live

---

## 🧪 CI/CD Execution Steps

1. Code is pushed to GitHub
2. GitHub Actions workflow starts automatically
3. Workflow connects to EC2 using SSH
4. Files are copied to the web server directory
5. Apache reloads the updated website

---

## 📌 Current Project Status

- Static website developed ✅
- Source code managed with GitHub ✅
- EC2 server configured ✅
- Manual deployment verified ✅
- CI/CD automation implemented ✅

---


---

## 🚀 Possible Improvements

- Enable HTTPS with SSL certificates
- Use Nginx instead of Apache
- Implement rollback mechanism
- Add monitoring and logging

---

## 👨‍💻 Author

Ashish

---

## 📄 License

This project is licensed under the MIT License.
