# AI Chatbot

A simple and clean AI chatbot web application built with Flask and powered by Claude (Anthropic). Supports file uploads including PDF, Word, PowerPoint, Excel, and images.

---

## Features

- Chat with Claude AI in a clean light-mode interface
- Upload and analyze files:
  - PDF documents
  - Word files (.docx)
  - PowerPoint presentations (.pptx)
  - Excel spreadsheets (.xlsx, .xls)
  - Images (PNG, JPG, GIF, WEBP)
- Typing indicator while AI is responding
- Clear chat button to reset conversation
- Timestamps on every message
- Plain text responses — no markdown symbols

---

## Project Structure

```
chatbot/
├── app.py               # Flask backend
├── requirements.txt     # Python dependencies
├── .env                 # Your API key (not uploaded)
└── templates/
    └── index.html       # Frontend UI
```

---

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/chatbot.git
cd chatbot
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Add Your API Key

Create a `.env` file in the project folder:

```
ANTHROPIC_API_KEY=your_api_key_here
```

Get your API key from: [console.anthropic.com](https://console.anthropic.com)

### 4. Run the App

```bash
python app.py
```

Open your browser and go to: `http://localhost:5000`

---

## How to Use

- Type a message and press **Enter** to send
- Press **Shift+Enter** to add a new line
- Click the **📎 attach button** to upload a file
- Ask questions about the uploaded file
- Click **Clear Chat** to start a new conversation

---

## Tech Stack

- **Backend:** Python, Flask
- **AI Model:** Claude (claude-opus-4-6) by Anthropic
- **File Support:** python-docx, python-pptx, openpyxl
- **Frontend:** HTML, CSS, JavaScript (no frameworks)

---

## Notes

- Never upload your `.env` file to GitHub — it contains your private API key
- The conversation history is stored in the browser only — it resets on page refresh
- File content is sent to the AI once per upload — follow-up questions use the AI's previous response as context
