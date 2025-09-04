# 💸 Demo: My First AI Agent in n8n

This project is a **Payment Reminder Roaster Agent** built in [n8n](https://n8n.io).  
It uses AI (Google Gemini + LangChain integration) to automatically send **funny, savage, Hinglish-style payment reminders** to friends/customers.  

---

## 🚀 Features
- 🤖 **AI Agent with Personality** – Witty, savage, and funny roast-style reminders.  
- 📧 **Automated Email Sending** – Sends reminders via SMTP.  
- 🧠 **Memory Support** – Uses conversational memory for context handling.  
- 🔗 **LangChain + Google Gemini** – Intelligent response generation.  
- 🔔 **Chat Trigger** – Starts workflow when a chat message is received.  

---

## 📂 Workflow Overview

The workflow consists of the following main nodes:

1. **When Chat Message Received** – Triggers the workflow.  
2. **Agent** – Defines the witty Hinglish roasting rules and JSON summary format.  
3. **Google Gemini Chat Model** – Generates subject and body content.  
4. **Simple Memory** – Keeps track of session context.  
5. **paymentReminder (Email Send Tool)** – Sends the actual reminder email.  
6. **Sticky Note** – Instructional note for debugging/starting point.  

---

## 🛠️ Tech Stack
- [n8n](https://n8n.io) – Workflow automation  
- [LangChain](https://www.langchain.com) – AI orchestration  
- [Google Gemini](https://ai.google) – Language model for generating reminders  
- **SMTP** – Email sending  

---

## 📜 Reminder Rules
The Agent follows these rules strictly:
1. Always call the tool:  
   ```js
   paymentReminder(customerEmail, subject, message)
