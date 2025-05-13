# Email Outreach Automation in n8n

## Overview

This project automates the email outreach process using **n8n**, an open-source workflow automation tool. The system integrates with **Google Sheets**, uses **SMTP** for sending emails, and incorporates personalized **PDF attachments** for each lead. Additionally, the workflow includes robust **error handling** and **follow-up logic** to ensure efficient and reliable outreach.

## Features

- **Automated Email Outreach:** Sends cold emails and follow-up messages to leads based on a scheduled trigger.
- **Google Sheets Integration:** Fetches lead data and configuration settings from Google Sheets.
- **Personalized PDF Attachments:** Dynamically generates and attaches personalized PDFs for each lead.
- **Error Handling:** Automatically retries failed messages up to 3 times and logs errors for monitoring.
- **Follow-Up Logic:** Sends follow-up emails based on predefined intervals and tracks the status in Google Sheets.

## Workflow Overview

1. **Trigger:** The workflow is triggered either on a scheduled basis (daily/hourly) or manually.
2. **Read Settings:** Configuration values are pulled from a Google Sheets Settings Sheet, including links to cold message templates and follow-ups.
3. **Fetch Leads:** Retrieves lead data from Google Sheets and filters out leads that are marked as “Completed.”
4. **Send Cold Email:** Composes and sends personalized cold emails to each lead using SMTP.
5. **Follow-Up Logic:** After a waiting period, the system checks previous messages sent and sends follow-up emails as needed.
6. **PDF Attachment:** A personalized PDF is dynamically created and attached to the cold email for each lead.
7. **Logging & Updates:** Updates lead status in Google Sheets, logging each message ID and the status of the outreach process.
8. **Error Handling:** Automatically retries failed email sends, with a maximum of 3 attempts. If all attempts fail, the lead is marked as “Failed.”

## Setup

### Prerequisites

- **n8n Account**: You need an n8n account to run the workflows.
- **Google Sheets**: Set up Google Sheets with lead data and configuration values (cold message template, follow-up emails).
- **SMTP Configuration**: Have SMTP credentials available for sending emails.
- **Google Docs API**: If using Google Docs for message templates, configure Google Docs API.

### Installation

1. Download the json file and import the file in new workflow 
 
