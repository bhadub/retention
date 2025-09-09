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
