# 🔐 Secure Media Hosting Platform on AWS

## 📌 Project Overview
This project demonstrates how to securely host and serve media files using AWS services.

Media files are stored in a **private S3 bucket**, and access is provided securely through an EC2 web server using an IAM role. This ensures that sensitive data is not exposed publicly.

---

## 🎯 Objective
- Launch EC2 instance with restricted access
- Create a private S3 bucket
- Upload media files to S3
- Securely serve media via EC2 web server using IAM role

---

## 🛠️ Technologies & Services Used
- AWS EC2 (Elastic Compute Cloud)
- Amazon S3 (Private Bucket)
- IAM Role (Secure Access)
- Apache Web Server (httpd)
- AWS CLI
- Linux

---
## 🏗️ Architecture Diagram
User → EC2 (Web Server) → IAM Role → Private S3 Bucket → Media Files


---

## 🔄 Workflow

1. Launch EC2 instance
2. Install Apache web server (httpd)
3. Create a private S3 bucket
4. Block all public access to S3
5. Upload media files to S3
6. Create IAM role with S3 access
7. Attach IAM role to EC2 instance
8. Install AWS CLI on EC2
9. Copy media files from S3 to web directory
10. Access media using EC2 public IP

---Step 3: Create Private S3 Bucket
Go to S3 service
Create bucket
Enable Block Public Access
🔹 Step 4: Upload Media Files
Upload images/videos to S3 bucket
🔹 Step 5: Create IAM Role
Create role with S3 access policy
Attach role to EC2 instance
🔹 Step 6: Install AWS CLI
sudo yum install aws-cli -y
🔹 Step 7: Copy Media Files from S3
aws s3 cp s3://your-bucket-name/ /var/www/html/ --recursive
🔹 Step 8: Access Media
Open browser:
http://<EC2-Public-IP>/image.jpg


EC2 Instance Setup
Apache Installation
Private S3 Bucket
Uploaded Media Files
IAM Role Configuration
Media Output in Browser
✅ Key Features
Secure media storage
Private S3 bucket (no public access)
IAM-based authentication
Controlled media access via EC2
📈 Benefits
Improved security
No credential exposure
Cost-effective solution
Easy to implement
🚀 Future Enhancements
Use CloudFront CDN for faster delivery
Add HTTPS using SSL certificate
Implement user authentication
Automate deployment using scripts


👨‍💻 Author

Harshavardhan
BCA Student | Aspiring Cloud & DevOps Engineer



