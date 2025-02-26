# 🌐 Personal-Portfolio-Website

This project showcases my skills, projects, and experiences in **Cloud Security &amp; Cloud Computing**. It is fully deployed on AWS using **S3, CloudFront, Route 53, and ACM** for high availability, security, and performance.

The portfolio is hosted on AWS with the following architecture :

- **Amazon S3** – Stores the static website files (HTML, CSS, JavaScript).
- **AWS CloudFront** – Distributes the content globally with low latency.
- **AWS Route 53** – Manages the custom domain and DNS records.
- **AWS Certificate Manager (ACM)** – Provides SSL/TLS for secure HTTPS traffic.


## 🔗 Live Demo

👉 **[Shar1ff.me](https://shar1ff.me)**

## 📸 Architecture Diagram

> **

## 🛠️ Tech Stack

- **Frontend**: HTML, CSS, JavaScript  
- **Hosting & CDN**: AWS S3, AWS CloudFront  
- **Domain & Security**: AWS Route 53, AWS ACM

## 🔧 Setup & Deployment

Follow these steps to set up and deploy the portfolio:

### 1️⃣ Upload Files to S3
- Create an **S3 bucket** and enable **Static Website Hosting**.
- Upload your website files (`index.html`, `style.css`, `scripts.js`, etc.).
- Set the bucket **public access policy** or use CloudFront for security.

### 2️⃣ Configure CloudFront
- Create a **CloudFront distribution** and set the S3 bucket as the origin.
- Enable **Redirect HTTP to HTTPS** under **Viewer Protocol Policy**.
- Enable **HTTPS (SSL/TLS)** using ACM.
- Configure caching and invalidations as needed.

### 3️⃣ Set Up Route 53
- Register a domain or use an existing one.
- Create an **A Record (Alias)** pointing to CloudFront.

### 4️⃣ Secure with ACM
- Request a **SSL certificate** in AWS Certificate Manager.
- Attach the certificate to the CloudFront distribution.

### 5️⃣ Test & Deploy 🚀
- Wait for CloudFront propagation.
- Open your custom domain and verify everything is working.

## 🔒 Security Configurations  

✅ **S3 Public Access Blocked:** The S3 bucket does not allow public access.  
✅ **CloudFront as the Only Access Point:** The S3 bucket has an **Origin Access Control (OAC)** policy allowing only CloudFront to serve content.  
✅ **HTTP to HTTPS Redirection:** CloudFront is configured to redirect all HTTP requests to HTTPS.  
✅ **ACM SSL Certificate:** Ensures encrypted communication via HTTPS. 

