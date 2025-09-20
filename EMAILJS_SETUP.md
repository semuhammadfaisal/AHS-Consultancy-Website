# EmailJS Setup Guide

To enable email functionality for the contact form, follow these steps:

## 1. Create EmailJS Account
- Go to https://www.emailjs.com/
- Sign up for a free account
- Verify your email address

## 2. Create Email Service
- In EmailJS dashboard, go to "Email Services"
- Click "Add New Service"
- Choose Gmail (or your preferred email provider)
- Connect your Gmail account (faisalsb0348@gmail.com)
- Note the Service ID

## 3. Create Email Template
- Go to "Email Templates"
- Click "Create New Template"
- Use this template content:

```
Subject: New Contact Form Submission - {{service}}

From: {{from_name}}
Email: {{from_email}}
Phone: {{phone}}
Service Interest: {{service}}

Message:
{{message}}

---
This message was sent from the AHS Consultancy website contact form.
Reply to: {{reply_to}}
```

- Note the Template ID

## 4. Get Public Key
- Go to "Account" > "General"
- Copy your Public Key

## 5. Update JavaScript
In `js/script.js`, replace these placeholders:
- `YOUR_PUBLIC_KEY` with your actual public key
- `YOUR_SERVICE_ID` with your service ID
- `YOUR_TEMPLATE_ID` with your template ID

## Example Configuration:
```javascript
emailjs.init('user_1234567890abcdef'); // Your public key
await emailjs.send('service_gmail', 'template_contact', templateParams);
```

## Fallback Option
If EmailJS fails, the form will automatically open the user's default email client with a pre-filled email to faisalsb0348@gmail.com.

## Testing
1. Fill out the contact form on your website
2. Submit the form
3. Check faisalsb0348@gmail.com for the email
4. Verify all form data is included correctly