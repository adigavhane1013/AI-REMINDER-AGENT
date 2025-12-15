# AI Reminder Agent

An AI-powered reminder scheduling agent built using n8n, Google Gemini, and Google Calendar.  
The system converts natural language messages into structured reminders and automatically creates calendar events.

This project demonstrates how LLMs can be used in real-world workflow automation instead of toy demos.

---

## What This Project Does

- Accepts reminder requests in natural language
- Extracts reminder details using an LLM:
  - Title
  - Date
  - Time
- Resolves relative dates like:
  - today
  - tomorrow
  - next Friday
- Automatically creates events in Google Calendar
- Handles timezone-aware scheduling (Asia/Kolkata)

Example input:
> Remind me to submit the report tomorrow at 5 PM

Output:
- A Google Calendar event is created with the correct date and time

---

## Tech Stack

- n8n (workflow automation)
- Google Gemini (LLM for information extraction)
- Google Calendar API
- JavaScript (n8n Code node)
- JSON-based workflow configuration

---

## Workflow Overview

1. Chat trigger receives the user message
2. Google Gemini extracts structured reminder details in JSON format
3. JavaScript code node:
   - Validates extracted data
   - Builds start and end timestamps
4. Google Calendar node creates the calendar event

---

## How to Use

1. Open n8n
2. Import the workflow file:
3. Configure credentials:
- Google Gemini API
- Google Calendar OAuth
4. Activate the workflow
5. Send a chat message with a reminder request

---

## Key Features

- Natural language reminder creation
- Relative date handling
- Automatic Google Calendar scheduling
- Clean and modular workflow design
- Practical LLM usage in automation

---

## Future Improvements

- Conflict detection for overlapping events
- Automatic rescheduling
- Multi-user support
- Notifications via email or messaging apps
- Logging and error monitoring

---

## Author

Aditya Gavhane  
Final-year B.Tech (AI & Analytics) student  
Focused on AI automation, LLM systems, and workflow engineering

