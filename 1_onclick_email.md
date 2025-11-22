# 📧 On-Click Email Workflow (n8n)

This document explains how to create a simple **On-Click Email Workflow** using **n8n**.  
The workflow sends an email automatically when a user clicks a button or triggers an action in your application.

---

## 🚀 Overview

This workflow performs:

1. Receive data via a **Webhook**
2. Extract user information (email, name, message)
3. Send an email using Gmail / SMTP / SendGrid
4. Return a success response

This is ideal for contact buttons, “email me info”, notifications, etc.

---

## 🛠 Requirements

- n8n running locally or on a server  
- Email credentials (Gmail, SMTP, etc.)  
- Ability to send a POST request from your application  

---

## 🔗 Workflow Steps

### **1. Webhook Node**

- **HTTP Method:** POST  
- **Path:** `send-email`  
- Your app should send JSON like:

```json
{
  "email": "user@example.com",
  "name": "John Doe",
  "message": "Hello, please contact me!"
}
