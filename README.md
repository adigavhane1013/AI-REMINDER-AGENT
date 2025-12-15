# AI Reminder Agent

AI Reminder Agent is an automation workflow built using n8n, Google Gemini, and Google Calendar.
It converts natural language reminder requests into scheduled Google Calendar events automatically.

This project demonstrates practical use of LLMs in workflow automation.

---

## What This Project Does

- Accepts reminder requests in natural language
- Extracts reminder details using an LLM:
  - Title
  - Date
  - Time
- Resolves relative dates such as today, tomorrow, and next Friday
- Automatically creates Google Calendar events
- Handles timezone-aware scheduling (Asia/Kolkata)

---

## Example

**User input:**

> Remind me to submit the assignment tomorrow at 6 PM

**Result:**

> A Google Calendar event is created for tomorrow at 6:00 PM with the correct title and timezone.

---

## Tech Stack

- n8n (workflow automation)
- Google Gemini (LLM for information extraction)
- Google Calendar API
- JavaScript (n8n Code node)

---

## Workflow Overview

1. A chat trigger receives the user message
2. Google Gemini extracts structured reminder data in JSON format
3. A JavaScript code node validates the data and builds timestamps
4. A Google Calendar node creates the event

---

## How to Use

1. Open n8n
2. Import the workflow JSON file into n8n
3. Configure credentials:
   - Google Gemini API
   - Google Calendar OAuth
4. Activate the workflow
5. Send a chat message with a reminder request

---

## Key Features

- Natural language reminder creation
- Relative date handling
- Automatic calendar scheduling
- Clean, modular workflow design
- Real-world automation use case

---

## Limitations

- No conflict detection for overlapping events
- Single-user configuration
- No external notification system

---

## Future Improvements

- Conflict detection and rescheduling
- Multi-user support
- Notifications via email or messaging platforms
- Logging and monitoring

---

## Author

Aditya Gavhane  
Final-year B.Tech student (AI & Analytics)  
Focused on AI automation, LLM systems, and workflow engineering


