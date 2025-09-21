# Student Mentor AI Chatbot

A chatbot application that provides personalized academic mentoring for Riya using Google Gemini AI with local storage for chat history.

## Features

- **Single Student Focus**: Pre-configured with Riya's profile
- **Google Gemini Integration**: Uses environment variable for API key
- **Local Storage**: Chat history and API key stored locally
- **Clean Chat UI**: Modern interface with typing indicators
- **Student Profile Display**: Shows academic performance and preferences
- **Responsive Design**: Works on all devices

## Student Profile

**Riya** 💃
- **Schedule**: School 8 AM–2 PM, Dance 5–6 PM, Homework 7–9 PM
- **Academic Performance**: Math: 92%, Science: 78%, English: 85%, History: 65%
- **Interests**: Dancing, reading novels, cricket
- **Learning Preferences**: Group study, interactive learning apps
- **Challenges**: Long lectures, rote memorization
- **Description**: Active student who enjoys creative expression. History is her weakest subject.

## Setup Instructions

### Prerequisites

- Node.js 18+ installed
- Google Gemini API key from [Google AI Studio](https://aistudio.google.com/app/apikey)

### 1. Configure Environment Variables

1. Get your Gemini API key from [Google AI Studio](https://aistudio.google.com/app/apikey)
2. Add your API key to the `.env` file:
   ```
   VITE_GEMINI_API_KEY=your_actual_api_key_here
   ```

### 2. Install Dependencies

```bash
npm install
```

### 3. Start Development

```bash
npm run dev
```

## How It Works

1. **API Key Setup**: Gemini API key is loaded from environment variables
2. **Student Context**: App displays Riya's profile information
3. **Query Processing**: User types questions about studies
4. **AI Processing**: Gemini AI processes queries with student context and mentor system prompt
5. **Personalized Response**: AI provides tailored advice based on Riya's profile
6. **Local Storage**: Chat history is automatically saved and restored

## System Prompt

The AI mentor uses this system prompt:

> "You are a personalized student mentor chatbot. You know about the student's schedule, marks, hobbies, likes, dislikes, and personal description. Always ground your responses in the retrieved student data. If the data does not include something, give polite general advice. Be supportive, encouraging, and practical."

## Example Interactions

**User**: "How should I plan my weekend?"

**AI Response**: "Hi Riya! Based on your schedule and interests, I'd suggest balancing your weekend between catching up on History (your weakest subject at 65%) and enjoying your hobbies. Since you prefer interactive learning over long lectures, try using educational apps or group study sessions for History review. You could also incorporate some cricket or reading time as rewards after study sessions. Don't forget to keep up with your dance practice since it's such an important part of your routine!"

## Tech Stack

- **Frontend**: React, TypeScript, Tailwind CSS, Lucide React
- **AI**: Google Gemini 1.5 Flash (direct API calls)
- **Storage**: Browser localStorage
- **Build Tool**: Vite

## Features

- ✅ Single student profile (Riya)
- ✅ Google Gemini API integration
- ✅ Environment variable configuration
- ✅ Local storage for chat history
- ✅ Responsive chat interface
- ✅ Student profile display
- ✅ Typing indicators and loading states
- ✅ Clear chat functionality

## Development Notes

- No backend required - runs entirely in the browser
- API key is loaded from environment variables
- Chat history persists between sessions
- Direct Gemini API calls from frontend
- Student data is embedded in the application code