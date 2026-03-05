\# AI Inbox Manager


An automated email triage system built with n8n and a local LLM (Ollama). It monitors your Gmail inbox, classifies every incoming email using AI, and routes it intelligently — logging everything to Google Sheets, drafting replies for action-required emails, sending Telegram alerts for urgent messages, and extracting invoice data to a dedicated finance tracker.

~What it does



\-Classifies emails into categories: spam, important, newsletter, invoice, action required, notification, personal, other

\-Summarizes each email in one sentence

\-Analyzes sentiment: urgent, positive, neutral, negative

\-Detects invoices and extracts amount, currency, and due date

\-Drafts replies automatically for emails that need a response

\-Sends Telegram notifications for urgent emails

\-Logs everything to Google Sheets for tracking and analytics

## SET UP


Create a spreadsheet with two sheets:

Sheet "AI\_Inbox" — columns:

Date | From | Subject | Category | Summary | Sentiment | Confidence | Action Needed | Is Invoice | Suggested Reply

Sheet "Finances" — columns:

Date | From | Subject | Amount | Currency | Due Date

~Import



\-Download the workflow JSON file

\-In n8n: Ctrl+Shift+I → select the JSON file

\-Connect your credentials (Gmail, Google Sheets, Telegram, Ollama)

\-Update the Google Sheets node with your spreadsheet ID and sheet names

\-Update the Telegram node with your bot token and chat\_id

\-Activate the workflow

