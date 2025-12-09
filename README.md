# n8n-call-transcription-workflow
An automated n8n workflow that detects new audio files in Google Drive, transcribes them using AI, extracts structured client and meeting details via LLMs, merges the outputs, and logs everything into Google Sheets. Ideal for automating sales calls, meeting notes, and CRM data entry.

# 🎧 AI Call Transcription & Data Extraction Workflow (n8n)

This repository contains an automated **n8n workflow** that processes call recordings end-to-end:  
from Google Drive upload → AI transcription → structured client & meeting data extraction → Google Sheets logging.

---

## 🚀 Workflow Overview

This workflow automatically:

1. Detects new audio files uploaded to a Google Drive folder.
2. Downloads and transcribes the recording using OpenAI/Gemini.
3. Sends the transcript to an LLM for structured extraction.
4. Separates extracted information into **Client Details** and **Meeting Details**.
5. Merges both outputs into a single structured object.
6. Appends the final data into a Google Sheet.

---

## 🗂️ Workflow Components

- **Google Drive Trigger** – Starts the workflow when a file is created.
- **Download File** – Fetches the audio file for processing.
- **Transcribe Recording** – Converts audio to text using AI.
- **LLM Chain (OpenAI/Gemini)** – Extracts key fields like:
  - Client name
  - Email / Phone
  - Requirements
  - Meeting summary
  - Action items
- **Client Details Node** – Holds structured client-specific outputs.
- **Meeting Details Node** – Holds meeting insights and summary.
- **Structured Output Parser** – Ensures clean JSON formatting.
- **Merge Node** – Combines all extracted data.
- **Google Sheets Node** – Adds a new row containing the finalized details.

---

## ✨ Features

- Fully automated audio → text → structured insights → Sheets
- Supports OpenAI, Gemini, or any n8n-compatible LLM
- No manual data entry required
- Perfect for:
  - Sales calls
  - Customer support analysis
  - Meeting documentation
  - CRM data automation
- Easy to extend with notifications, CRMs, PDFs, etc.

---

## 📦 Requirements

- n8n (self-hosted or cloud)
- Google Drive API credentials
- Google Sheets API credentials
- OpenAI or Google Gemini API key
- Audio files in MP3/WAV/M4A format

---

## ▶️ Setup

1. Import the workflow JSON into your n8n instance.
2. Configure:
   - Google Drive authentication
   - Google Sheets authentication
   - LLM API key (OpenAI/Gemini)
3. Set your Google Drive folder ID in the trigger node.
4. Map your Google Sheet columns to the workflow fields.
5. Upload a test audio file to confirm the automation.

---

## 📊 Example Output (Google Sheets)

| Client Name | Email | Phone | Requirements | Meeting Summary | Action Items | Date |
|-------------|-------|--------|--------------|------------------|--------------|------|
| John Doe | john@example.com | 9876543210 | Product inquiry | Discussed pricing & features | Send proposal | 2025-01-01 |

---

## 🔧 Optional Enhancements

- Auto-generate PDF summaries
- Send follow-up emails or WhatsApp messages
- Push data to CRM (HubSpot, Zoho, Salesforce)
- Add sentiment analysis or keyword tagging
- Store transcripts in a database

---

## 📜 License

This project is open-source under the **MIT License**.

---

## 📩 Support

For enhancements or additional workflows, feel free to raise a request or open an issue.
