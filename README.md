# 🌐 Static Website on AWS S3 using Terraform.

> Deploy a static website on AWS S3 fully automated with Terraform (Infrastructure as Code)

---

## 📌 Overview

This project demonstrates how to deploy a **static website on AWS S3** using **Terraform**. The website is built with simple **HTML & CSS** and hosted using **AWS S3 Static Website Hosting** — the entire infrastructure is provisioned and managed through Terraform, eliminating any manual setup.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| **AWS S3** | Static website hosting |
| **Terraform** | Infrastructure as Code (IaC) |
| **HTML & CSS** | Frontend |
| **IAM & S3 Bucket Policy** | Public access control |

---

## 📁 Project Structure

```
proj-Static-Website/
│
├── index.html          # Main webpage
├── style.css           # Stylesheet
├── main.tf             # Core Terraform configuration
├── variables.tf        # Input variables
├── outputs.tf          # Output values (e.g., website URL)
├── .gitignore          # Files to ignore in version control
└── README.md           # Project documentation
```

---

## ⚙️ How It Works

```
Terraform → S3 Bucket Created → Static Hosting Enabled → Bucket Policy Applied → Files Uploaded → Website Live
```

1. **Terraform** provisions an S3 bucket on AWS
2. **Static website hosting** is enabled on the bucket
3. **Public read access** is configured using an S3 bucket policy
4. **HTML & CSS files** are uploaded with the correct `Content-Type` metadata
5. **Website** becomes accessible via the S3 static website endpoint

---

## 🚀 How to Deploy

### Prerequisites

- [ ] AWS CLI installed and configured (`aws configure`)
- [ ] Terraform installed (`terraform -v`)
- [ ] AWS account with S3 permissions

### Steps

**1. Clone the Repository**

```bash
git clone https://github.com/irfanjat/proj-Static-Website.git
cd proj-Static-Website
```

**2. Initialize Terraform**

```bash
terraform init
```

**3. Validate Configuration**

```bash
terraform validate
```

**4. Preview the Plan**

```bash
terraform plan
```

**5. Deploy the Infrastructure**

```bash
terraform apply
```

> Type `yes` when prompted to confirm.

**6. Access Your Website**

After apply completes, Terraform will output the S3 website endpoint:

```
website_url = "http://<your-bucket-name>.s3-website-<region>.amazonaws.com"
```

Open that URL in your browser — your site is live! 🎉

---

## 🧹 Tear Down

To destroy all resources and avoid AWS charges:

```bash
terraform destroy
```

---

## 🧠 Key Learnings

- Automating cloud infrastructure provisioning using Terraform
- Debugging S3 static website issues related to `Content-Type` & metadata
- Understanding the difference between **S3 object URLs** and **S3 website endpoints**
- Writing clean, reusable Infrastructure as Code configurations
- Configuring **IAM bucket policies** for controlled public access

---

## 🌐 Live Demo

| Item | Value |
|------|-------|
| Website URL | `http://<bucket-name>.s3-website-<region>.amazonaws.com` |
| Hosting | AWS S3 Static Website Hosting |
| Provisioned via | Terraform |

---

## 🤝 Contributing

1. Fork this repository
2. Create your feature branch (`git checkout -b feature/my-feature`)
3. Commit your changes (`git commit -m 'Add my feature'`)
4. Push to the branch (`git push origin feature/my-feature`)
5. Open a Pull Request

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

<p align="center">Made with ❤️ by <a href="https://github.com/irfanjat">irfanjat</a></p>
