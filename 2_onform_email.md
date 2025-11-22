# 📝 On-Form Submission Workflow (n8n)

This documentation explains how to create an **On-Form Submission Workflow** using **n8n**.  
The workflow sends collected form data to your email, database, CRM, or any other service as soon as a user submits a form.

---

## 🚀 Overview

This workflow:

1. Accepts data from a **form submission** via a Webhook  
2. Processes and validates the submitted fields  
3. Sends an email or saves the data  
4. Returns a success response to the form

Works with any frontend form:

- HTML / JavaScript
- React / Next.js
- Vue
- PHP forms
- WordPress custom forms
- Mobile apps

---

## 🛠 Requirements

- Running n8n instance (local or server)
- Email credentials (SMTP, Gmail, SendGrid, etc.)
- A frontend form capable of making a POST request

---

## 🔗 Workflow Steps

### **1. Webhook Node**

- **HTTP Method:** POST  
- **Path:** `submit-form`  

Your form should send JSON like:

```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "message": "Hello, I need support!"
}
