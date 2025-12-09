# 🎧 AI Call Transcription & MoM Data Extraction Workflow (n8n)

This repository contains an automated **n8n workflow** that processes call recordings end-to-end:  
Google Drive upload → AI transcription → MoM (Minutes of Meeting) extraction → Google Sheets logging.

The workflow is designed for sales teams, client servicing, and meeting documentation where detailed structured data is required.

---

## 🚀 Workflow Overview

This workflow automatically:

1. Detects new audio files uploaded to a Google Drive folder.
2. Downloads and transcribes the recording using OpenAI/Gemini.
3. Sends the transcript to an LLM for structured MoM extraction.
4. Generates fields such as objectives, key discussion points, decisions, risks, opportunities, and more.
5. Merges all extracted values into a single structured JSON.
6. Appends the final MoM output into Google Sheets using predefined columns.

---

## 🗂️ Workflow Components

- **Google Drive Trigger** – Fires when a new audio file is uploaded.
- **Download File** – Retrieves the recording.
- **AI Transcription Node** – Converts audio to text.
- **LLM Extraction Node** – Extracts detailed MoM insights.
- **Structured Output Parser** – Ensures clean formatting for Sheets.
- **Merge Node** – Combines client + meeting insights.
- **Google Sheets Node** – Appends a new row with all MoM data.

---

## 📊 Google Sheets Output Columns

The workflow automatically fills the following Google Sheet columns:

| Column Name |
|-------------|
| person |
| mom_objective_of_call |
| mom_key_discussion_points |
| mom_decisions_taken |
| mom_action_items |
| mom_next_steps_timeline |
| red_flags |
| potential_opportunities |
| qualification_score |
| deal_probability |
| risk_factors |
| buying_triggers |
| salesperson_performance |
| next_steps_recommendations |
| follow_up_email_subject |
| follow_up_email_body |

Each field is generated or enhanced by the AI model based on the call transcript.

---

## ✨ Features

- End-to-end MoM automation  
- AI-based extraction of objectives, decisions, risks, red flags, opportunities, and more  
- Auto-generation of follow-up email subject + body  
- Supports OpenAI / Gemini  
- Zero manual data entry  
- Ideal for sales, client success, and internal team calls  

---

## 📦 Requirements

- n8n (self-hosted or cloud)
- Google Drive API credentials
- Google Sheets API credentials
- OpenAI or Gemini API key
- Audio recordings (MP3/WAV/M4A)

---

## ▶️ Setup

1. Import the workflow JSON into n8n.
2. Configure credentials:
   - Google Drive
   - Google Sheets
   - LLM provider (OpenAI/Gemini)
3. Update your Drive Folder ID in the trigger.
4. Map workflow fields to your Google Sheet columns listed above.
5. Upload an audio file to verify end-to-end automation.

---

## 🔧 Optional Enhancements

- Auto-generate PDF MoM summaries
- Send follow-up email automatically
- Push MoM to CRM systems
- Add sentiment or intent analysis
- Store transcripts in a central database

---

## 📜 License

Open-source under the **MIT License**.

---

