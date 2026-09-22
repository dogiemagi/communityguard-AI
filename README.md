# CommunityGuard AI - Intelligent Community Decision Intelligence Platform

 **AI-Powered Emergency Response, Healthcare Access & Public Safety**

 **Live Application:** [https://communityguard-ai-production.up.railway.app/](https://communityguard-ai-production.up.railway.app/)

[![Live Demo](https://img.shields.io/badge/Live%20Demo-CommunityGuard%20AI-06b6d4?style=for-the-badge&logo=railway&logoColor=white)](https://communityguard-ai-production.up.railway.app/)
[![Hackathon](https://img.shields.io/badge/Google%20GenAI%20Academy-Cohort%202-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://cloud.google.com/)


## Overview

**CommunityGuard AI** is a Gemini-powered **Decision Intelligence Platform** built for the **Google GenAI Academy Cohort 2 Hackathon** under the problem statement:

> **"AI for Better Living and Smarter Communities"**

The platform helps **citizens, community health workers, and local administrators** make faster and more informed decisions during emergencies and everyday community health situations.

Unlike a traditional chatbot, CommunityGuard AI combines conversational Generative AI with **location awareness, emergency response intelligence, healthcare triage, community alerts, and structured decision support**.

The system is designed to provide calm, actionable, and structured responses while supporting **English, Hindi, and Hinglish** interactions.


## Core Feature Matrix

### 1. Emergency Response Intelligence

- Provides instant step-by-step emergency action checklists.
- Generates **Golden Hour** response plans for critical situations.
- Provides simulated nearby hospital and ambulance information.
- Supports one-tap SMS alerts to configured emergency contacts.
- Provides structured guidance based on the emergency scenario.

### 2. Healthcare Access Navigator

- AI-powered symptom triage.
- Categorizes situations into:
  - Emergency
  - Urgent
  - Non-Urgent
- Recommends appropriate levels of care.
- Provides general healthcare access guidance.
- Supports information about government healthcare schemes.

### 3. Community Decision Intelligence

- Generates structured decision-support reports.
- Helps administrators and NGOs understand community-level situations.
- Provides resource allocation insights.
- Converts conversational input into actionable recommendations.
- Supports community health and safety decision-making.

### 4. Live Location Intelligence

- Automatically detects the user's current location using browser geolocation.
- Supports manual location selection.
- Uses reverse geocoding to identify the location.
- Provides location-aware emergency and healthcare assistance.
- Surfaces simulated nearby emergency resources.

### 5. Live Situation Hub

The platform includes a real-time community information sidebar containing:

-  Nearby hospitals
-  Air Quality Index (AQI)
-  Heat alerts
-  Emergency alerts
-  Health alerts
-  Environmental alerts

Users can filter community alerts based on their category.

### 6. Multilingual AI Assistant

- Supports **English and Hindi**.
- Understands **Hinglish**.
- Responds according to the language used by the user.
- Designed for natural conversational interaction.
- Maintains context during multi-turn conversations.

### 7. Conversational Decision Assistant

- Natural-language conversational interface.
- Maintains conversation history during a session.
- Supports follow-up questions.
- Provides structured and actionable responses.
- AI behavior is controlled through an engineered system prompt.

### 8. Mobile-Friendly Emergency Experience

- Responsive interface for mobile and desktop.
- Haptic feedback support.
- Native sharing capabilities.
- SMS integration for emergency communication.
- Quick-action cards for common emergency scenarios.

## AI Architecture

```text
                    ┌─────────────────────┐
                    │      User Input     │
                    │  Text / Emergency   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │  React Frontend     │
                    │  TypeScript + Vite  │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Express Backend   │
                    │     Node.js         │
                    └──────────┬──────────┘
                               │
                 ┌─────────────┴─────────────┐
                 │                           │
                 ▼                           ▼
       ┌──────────────────┐       ┌──────────────────┐
       │ Location Service │       │ Community Data   │
       │ Geolocation      │       │ Alerts / AQI     │
       │ Reverse Geocode  │       │ Heat / Health    │
       └────────┬─────────┘       └────────┬─────────┘
                │                          │
                └────────────┬─────────────┘
                             │
                             ▼
                    ┌─────────────────────┐
                    │   Gemini AI Layer   │
                    │  Decision Support   │
                    │  Symptom Triage     │
                    │  Emergency Guidance │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Structured Response │
                    │ + Recommendations   │
                    └─────────────────────┘
```


## Technology Stack

| Layer | Technology |
|---|---|
| Frontend | React 19 |
| Language | TypeScript |
| Build Tool | Vite |
| Styling | Tailwind CSS v4 |
| Backend | Express.js |
| Runtime | Node.js |
| AI | Google Gemini API |
| AI SDK | `@google/genai` |
| Markdown | react-markdown |
| Markdown Extensions | remark-gfm |
| Icons | lucide-react |
| Geolocation | Browser Geolocation API |
| Communication | SMS / Native Share Integration |
| Deployment | Railway |


## Project Structure

```text
communityguard-ai/
│
├── server.ts
│   └── Express server + Gemini API integration
│
├── src/
│   │
│   ├── App.tsx
│   │   └── Core application state and logic
│   │
│   ├── components/
│   │   ├── Header.tsx
│   │   │   └── Location, emergency contact and sharing
│   │   │
│   │   ├── ChatArea.tsx
│   │   │   └── AI chat interface and quick actions
│   │   │
│   │   ├── Sidebar.tsx
│   │   │   └── Live Situation Hub
│   │   │
│   │   └── EmergencyContactModal.tsx
│   │       └── Emergency contact configuration
│   │
│   ├── data/
│   │   └── constants.ts
│   │       └── Quick actions and mock alert data
│   │
│   ├── types/
│   │   └── index.ts
│   │       └── Shared TypeScript types
│   │
│   └── utils/
│       └── index.ts
│           └── Helper utilities
│
├── index.html
├── package.json
└── README.md
```


# Local Development Setup

## 1. Requirements

- Node.js 18+
- npm
- Google Gemini API Key

## 2. Clone the Repository

```bash
git clone https://github.com/pradeep1330/communityguard-ai.git
cd communityguard-ai
```

## 3. Install Dependencies

```bash
npm install
```

## 4. Configure Environment Variables

Create a `.env.local` file in the project root:

```env
GEMINI_API_KEY="your_gemini_api_key_here"
```

Replace the placeholder with your Google Gemini API key.

## 5. Run the Application

```bash
npm run dev
```

The application will be available at:

```text
http://localhost:3000
```


# Deployment

CommunityGuard AI is deployed as a web application using **Railway**.

### Live Application

**[https://communityguard-ai-production.up.railway.app/](https://communityguard-ai-production.up.railway.app/)**

### Deployment Steps

1. Push the project to GitHub.
2. Create a new project in Railway.
3. Connect the GitHub repository.
4. Configure the `GEMINI_API_KEY` environment variable.
5. Railway installs the project dependencies.
6. Railway builds and starts the application.
7. The deployed application becomes available through the Railway-generated URL.


# AI Safety & Domain Control

CommunityGuard AI uses an engineered system prompt to keep the AI focused on the application's intended domains:

- Emergency response
- Healthcare access
- Community safety
- Public health
- Environmental alerts
- Administrative decision support

The AI is designed to provide structured and actionable responses while avoiding unnecessary conversational drift.


# Location Intelligence

The application supports location-aware assistance through browser-based geolocation.

```text
User
  │
  ▼
Browser Geolocation
  │
  ▼
Latitude + Longitude
  │
  ▼
Reverse Geocoding
  │
  ▼
Current Location
  │
  ▼
Location-Aware AI Assistance
```

For the hackathon prototype, hospital, ambulance, and environmental information displayed in the interface may use **simulated data** for demonstration purposes.

# Language Support

CommunityGuard AI is designed to support:

| Language | Support |
|---|---|
| English | ✅ |
| Hindi | ✅ |
| Hinglish | ✅ |

The assistant adapts its response language based on the user's interaction.


# Disclaimer

CommunityGuard AI provides **AI-generated informational guidance** and is intended for demonstration and educational purposes.

It is **not a substitute for professional medical advice, diagnosis, or treatment**.

For real emergencies in India, contact the appropriate emergency services, including **112/108 as applicable**.

Hospital, ambulance, environmental, and community alert information in this prototype may be simulated and should not be relied upon as real-time emergency information.



# Hackathon

Built for:

**Google GenAI Academy APAC Edition – Cohort 2 Hackathon**

**Problem Statement:**  
*AI for Better Living and Smarter Communities*

The project explores how Generative AI can be combined with location intelligence and community-level information to support faster decision-making during emergencies and healthcare situations.


# Team

### Pradeep Pankaj
**Project Lead / Developer**

GitHub: [https://github.com/pradeep1330](https://github.com/pradeep1330)

### Mageshwari M
**Team Member / Developer**


# License

This project was developed for the **Google GenAI Academy Cohort 2 Hackathon** and is intended primarily for educational and demonstration purposes.

<div align="center">

###  CommunityGuard AI

**AI for safer, smarter and more connected communities.**

Built with using **Google Gemini + React + TypeScript + Express.js**

</div>
