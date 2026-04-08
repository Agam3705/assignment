# 🏓 AWS Cloud Pong Pro
### Enterprise-Grade Static Hosting on Amazon S3

## 📋 Project Overview
This project demonstrates the deployment of a high-performance, responsive web application using **Amazon S3 Static Website Hosting**. Moving beyond a simple static page, I developed a "Cyberpunk-themed" Pong game featuring a dashboard-style interface that remains fully functional within a serverless cloud environment.

## 🚀 Live Demo
> **Live Website:** 

---

## 🛠️ Key Features
* **Serverless Infrastructure:** Hosted entirely on an **AWS S3 Bucket** (Free Tier).
* **Responsive Dashboard:** A "Viewport-Aware" UI that automatically scales to fit any screen size without scrolling.
* **Custom Game Engine:**
    * **Neural Link Speed:** Adjustable player paddle sensitivity.
    * **AI Intelligence Core:** Variable difficulty logic for the automated opponent.
    * **Kinetic Energy:** Real-time ball velocity control.
    * **Match Management:** Custom "Match Point" settings with a persistent high-score UI.
* **Visual Aesthetics:** Cyberpunk-inspired design featuring neon glow effects and a "Single-Screen" dashboard layout.

---

## 🏗️ Technical Architecture



1.  **Storage:** Amazon S3 (Standard Storage Class).
2.  **Hosting:** S3 Static Website Hosting enabled.
3.  **Security:** IAM Bucket Policy configured for `s3:GetObject` permission for public access.
4.  **Frontend:** HTML5 Canvas, CSS3 (Flexbox/Viewport Units), and Vanilla JavaScript.

---

## 📖 Deployment Steps

### 1. S3 Configuration
* Created a globally unique bucket.
* Disabled "Block all public access" to allow website traffic.
* Enabled **Static Website Hosting** under the Properties tab.

### 2. Permissions & Policy
Applied the following JSON Bucket Policy to ensure the website is accessible to the public:

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::pong-game-agam/*"
        }
    ]
}
