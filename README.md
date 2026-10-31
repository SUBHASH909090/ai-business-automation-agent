# AI Business Automation Agent

An automated workflow built with **n8n** and **Google Gemini** that processes incoming customer requests, extracts structured intent, logs records to Google Sheets, and sends automated email confirmations via Gmail.

---

## 📌 Features

- **Automated Request Processing:** Ingests incoming customer inquiries automatically.
- **AI-Powered Structured Extraction:** Uses Google Gemini to analyze unstructured message text and extract customer details, intent, and priority into clean JSON format.
- **Centralized Data Logging:** Automatically appends extracted request data into Google Sheets.
- **Notification & Confirmation:** Dispatches real-time confirmation emails to the customer via Gmail.

---

## 🛠️ Tech Stack

- **Orchestration:** n8n
- **LLM / AI:** Google Gemini API
- **Integrations:** Google Sheets, Gmail API
- **Data Format:** JSON, REST APIs

---

## ⚙️ Workflow Architecture

1. **Trigger:** Receives customer request via Webhook or incoming form trigger.
2. **AI Processing:** Gemini node processes the message prompt and returns structured JSON (Name, Email, Query Type, Summary, Urgency).
3. **Database Action:** Google Sheets node creates a new row with the structured fields.
4. **Email Dispatch:** Gmail node sends a personalized acknowledgement email to the client.

---

## 🚀 Setup & Installation

1. Clone or download this repository.
2. Open your self-hosted or cloud **n8n** instance.
3. Import the workflow JSON file (`workflow.json`).
4. Configure required credentials:
   - **Google Gemini API Key**
   - **Google Sheets OAuth2 / Service Account**
   - **Gmail OAuth2 Credentials**
5. Activate the workflow.
