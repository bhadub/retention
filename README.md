# retention
This n8n workflow automates customer engagement emails for users based on different engagement scenarios to minimize churn.

It allows users to monitor the customer product usage and customized the reach out using n8n automation and AI to  craft personalized, empathetic emails and updates a Supabase database to track outreach status automatically.

## Main goals:

- Re-engage users showing early signs of disengagement.

- Send tailored emails according to customer behavior.

- Update workflow status in Supabase for tracking and reporting.

## ⚙️ How It Works

1. Product Usage Dashboard
- a dashboard allows the user to monitor the customer product usage
- select the customers based on the usage scenario (e.g. low usage of particular feature(s))
- ability to reach out the selected custoemrs within the dashboard
2. Trigger
- Receives webhook events with customer data (Webhook node).
- Split & Process Customers
- Split Out node separates multiple customer entries.
- Loop Over Items node processes each customer individually.
3. AI Email Generation
- AI Agent + OpenAI Chat Model generate personalized email content.
- Parse AI Output formats the AI output into subject and body ready for sending.
4. Email Sending & Tracking
- Send a message node sends emails via Gmail.
- Update a row updates the Supabase database with email status.
- Wait node controls the workflow loop timing.
## 🛠️ Tech Stack

**Automation Platforms**  
![n8n](https://img.shields.io/badge/n8n-EA4C89?style=for-the-badge&logo=n8n&logoColor=white)  

**AI / NLP**  
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)  

**Databases & Storage**  
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)  

**Email / APIs**  
![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white)  

**Languages & Tools**  
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)  
## 🔐 Setup Instructions

1. Clone this repo:  
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
2. Copy .env.example to .env and add your own API keys:
   ``` bash
   cp .env.example .env
3. Import the workflow JSON from workflows/workflow.json into n8n.
4. Test the workflow with a sample webhook payload.

