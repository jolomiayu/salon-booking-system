# 💇‍♀️ Karrie Beauty Hub – Serverless Booking System

A real-world serverless booking application built for a salon business using AWS.  
This project demonstrates how to design, secure, and deploy a scalable cloud application with authentication and admin access control.

---

## 🚀 Features

- Public users can book appointments without login  
- Bookings stored securely in DynamoDB  
- Admin-only dashboard to view all bookings  
- Delete bookings functionality (restricted)  
- Authentication using AWS Cognito  
- Protected API routes using JWT authorization  
- Fully serverless architecture (no servers managed)  

---

## 🔐 Security (NEW UPGRADE)

- AWS Cognito authentication for admin access  
- JWT-based authorization via API Gateway  
- Backend validation of user identity (email check)  
- Public booking endpoint remains open for customers  
- Admin endpoints (GET /bookings, DELETE /booking) are protected  

---

## 🌐 Live Demo

Booking Page:  
http://karriebeautyhub-booking.s3-website-eu-west-1.amazonaws.com  

Admin Dashboard (Login Required):  
http://karriebeautyhub-booking.s3-website-eu-west-1.amazonaws.com/admin.html  

---

## ☁️ AWS Services Used

- API Gateway (HTTP API)  
- AWS Lambda (Python backend)  
- DynamoDB (NoSQL database)  
- Cognito (Authentication & Authorization)  
- S3 (Static website hosting)  

---

## ⚙️ Architecture Overview

User → S3 (Frontend) → API Gateway → Lambda → DynamoDB  

Admin → Cognito Login → JWT Token → API Gateway (Protected Routes)  

---

## 📁 Project Structure

index.html          # Public booking page  
admin.html          # Admin dashboard (secured)  
.github/workflows   # CI/CD deployment to S3  

---

## ⚡ API Endpoints

POST   /book       → Public      → Create booking  
GET    /bookings   → Admin only  → Get all bookings  
DELETE /booking    → Admin only  → Delete a booking  

---

## 🧠 What I Learned

- Designing real-world serverless architectures  
- Implementing authentication with AWS Cognito  
- Securing APIs using JWT authorizers  
- Handling CORS and frontend-backend communication  
- Debugging production issues (401, 500 errors, token flow)  
- Structuring scalable cloud applications  
- Connecting frontend authentication to backend security  

---

## ⚙️ DevOps

- CI/CD pipeline using GitHub Actions  
- Automatic deployment to S3 on push  

---

## 👤 Author

Built by Jolomi Anthony Ayu  

---

## 🔥 Future Improvements

- Role-based access (Owner, Manager, Staff)  
- Booking status (Pending / Completed)  
- Notifications (Email/SMS)  
- Custom domain with HTTPS (CloudFront)
