# n8n-call-transcription-workflow
An automated n8n workflow that detects new audio files in Google Drive, transcribes them using AI, extracts structured client and meeting details via LLMs, merges the outputs, and logs everything into Google Sheets. Ideal for automating sales calls, meeting notes, and CRM data entry.

📼 AI Call Transcription & Data Extraction Workflow (n8n)

This repository contains an automated n8n workflow that converts uploaded call recordings into structured client and meeting details using AI, then saves the results directly to Google Sheets. It streamlines sales calls, meeting documentation, and CRM data entry with zero manual effort.

🚀 Workflow Summary

The workflow automatically:

Detects new audio files uploaded to a Google Drive folder.

Downloads and transcribes the recording using OpenAI/Gemini.

Sends the transcript to an LLM for structured extraction.

Separates and formats Client Details and Meeting Details.

Merges all extracted fields into a single output.

Appends the final data into a Google Sheets log or CRM sheet.

🗂️ Workflow Components

Google Drive Trigger – Starts the workflow when a file is added.

Download File – Retrieves the audio file.

Transcription Node – Converts speech to text using AI.

LLM Chain – Extracts important fields like name, email, needs, summary, and action items.

Client Details Node – Captures structured client information.

Meeting Details Node – Captures summary, discussion points, follow-ups, etc.

Merge Node – Combines client & meeting data.

Google Sheets Node – Saves the final structured record.

🧠 Features

End-to-end automation from upload → transcription → structured output → Sheets

Supports OpenAI, Gemini, and custom LLMs

Highly customizable field mapping

Works with any CRM-friendly Google Sheet

Reduces manual note-taking and data entry

Ideal for sales, support, and meeting workflows

📦 Requirements

n8n self-hosted or cloud

Google Drive API credentials

Google Sheets API credentials

OpenAI or Gemini API key

Audio files in MP3/WAV/M4A format

▶️ Setup Instructions

Import the provided workflow JSON into n8n.

Configure API credentials for Google and your LLM provider.

Set your Google Drive folder ID in the trigger node.

Map fields to your Google Sheet column names.

Upload an audio file to test the workflow.

📊 Output Example

After processing, a new row is added to Google Sheets containing:

Client Name

Contact Information

Requirements / Intent

Meeting Summary

Action Items

Date & Time

Any additional fields you configure

🔧 Customization Ideas

Generate a PDF summary

Send follow-up emails automatically

Push data to HubSpot, Zoho, or Salesforce

Add sentiment analysis

Auto-tag calls by topic or priority

📝 License

This project is open-source and free to use under the MIT License.
