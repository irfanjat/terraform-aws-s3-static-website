# 🌐 Static Website on AWS S3 using Terraform

This project demonstrates how to deploy a **static website on AWS S3** using **Terraform (Infrastructure as Code)**.

The website is built with simple **HTML & CSS** and hosted using **AWS S3 Static Website Hosting**, fully automated via Terraform.

---

---

## 🛠️ Tech Stack
- **AWS S3** – Static website hosting
- **Terraform** – Infrastructure as Code
- **HTML & CSS** – Frontend
- **IAM & S3 Bucket Policy** – Public access control

---

## 📁 Project Structure
proj-Static-Website/
│
├── index.html
├── style.css
├── main.tf
├── variables.tf
├── outputs.tf
├── .gitignore
└── README.md


---

## ⚙️ How It Works
1. Terraform provisions an S3 bucket
2. Static website hosting is enabled
3. Public read access is configured using a bucket policy
4. HTML & CSS files are uploaded with correct `Content-Type`
5. Website is accessible via S3 website endpoint

---

## 🧠 Key Learnings
- Automating cloud infrastructure using Terraform
- Debugging S3 static website issues (Content-Type & metadata)
- Understanding the difference between S3 object URLs and website endpoints
- Writing clean, reusable IaC configurations

---

## 🧪 How to Deploy Locally

```bash
terraform init
terraform validate
terraform plan
terraform apply
