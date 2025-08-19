# AWS Beginner Project: Personal Website

This is a **beginner-friendly AWS project** that demonstrates how to host a static personal website using Amazon Web Services (AWS).  

It is designed for beginners learning **cloud computing** and wanting hands-on experience with **S3, IAM, CloudFront, and Route 53**.

---

## Project Overview

- **Project Name:** Personal Website on AWS  
- **Purpose:** Learn how to deploy a static website on AWS  
- **Skills Learned:** AWS S3, CloudFront, IAM, HTML, CSS, JavaScript  

---

## Project Structure

---

## Deployment on AWS S3

1. **Create an S3 Bucket**  
   - Log in to AWS → **S3** → **Create Bucket**  
   - Give it a unique name and select your region  

2. **Enable Static Website Hosting**  
   - Go to **Properties** → **Static website hosting**  
   - Set `index.html` as the **Index document**  

3. **Upload Files**  
   - Upload all files from this repository to your bucket  

4. **Set Bucket Policy to Public**  
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::YOUR_BUCKET_NAME/*"
    }
  ]
}
