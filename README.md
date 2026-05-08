# 📞 AI Calling Agent

> An intelligent, automated AI voice calling system powered by Vapi and Node.js. Make smart outbound calls, qualify leads, handle customer interactions, and automate phone-based workflows — all driven by AI.

[![Node.js](https://img.shields.io/badge/Node.js-18+-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)](https://nodejs.org)
[![Vapi](https://img.shields.io/badge/Vapi-AI%20Voice-6C47FF?style=for-the-badge)](https://vapi.ai)
[![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)](https://supabase.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

---

## 🌟 Overview

The **AI Calling Agent** is a production-ready automated voice agent that handles outbound phone calls using conversational AI. Built with Vapi's voice AI platform and Node.js, it enables businesses to automate customer outreach, lead qualification, appointment scheduling, and follow-ups at scale.

This agent is part of the broader [AI Showroom](https://github.com/salikahmed595/ai-showroom-frontend) ecosystem — a suite of AI automation tools built by Salik Ahmed.

---

## ✨ Features

- 📞 **Automated Outbound Calling** — AI-powered calls with natural conversation flow
- 🧠 **Intelligent Responses** — Context-aware dialogue using LLM backends
- 🎙️ **Natural Voice Synthesis** — Human-like speech via Vapi's TTS engine
- 📋 **Lead Qualification** — Automatically screen and qualify prospects
- 🗓️ **Appointment Scheduling** — Book meetings directly during calls
- 💾 **Data Persistence** — Call logs and results stored in Supabase
- 🔒 **Secure Configuration** — Environment-based secrets management
- 📊 **Call Analytics** — Track call outcomes, duration, and conversion rates
- 🔄 **Webhook Integration** — Real-time call events and status updates
- 🌐 **Scalable Architecture** — Handle multiple concurrent calls

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| Node.js 18+ | Runtime environment |
| Vapi AI | Voice AI platform for calls |
| Supabase | Database & real-time backend |
| OpenAI / LLM | Conversation intelligence |
| TypeScript/JavaScript | Application logic |
| Webhooks | Real-time event handling |

---

## 🚀 Getting Started

### Prerequisites

- Node.js 18+
- [Vapi Account](https://vapi.ai) with API key
- [Supabase Account](https://supabase.com) with project URL and API key
- npm or yarn package manager

### Installation

```bash
# Clone the repository
git clone https://github.com/salikahmed595/ai-calling-agent.git
cd ai-calling-agent

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env
# Edit .env with your credentials
```

### Configuration

Create a `.env` file with the following:

```env
# Vapi Configuration
VAPI_API_KEY=your_vapi_api_key
VAPI_PHONE_NUMBER_ID=your_phone_number_id

# Supabase Configuration
SUPABASE_URL=your_supabase_project_url
SUPABASE_SERVICE_KEY=your_supabase_service_key

# AI Model (Optional)
OPENAI_API_KEY=your_openai_api_key

# Agent Settings
AGENT_NAME=AI Assistant
CALL_TIMEOUT=300
MAX_CONCURRENT_CALLS=10
```

> ⚠️ Never commit your `.env` file. It's already in `.gitignore`.

### Running the Agent

```bash
# Development mode
npm run dev

# Production mode
npm start

# Run a test call
npm run test-call
```

---

## 📁 Project Structure

```
ai-calling-agent/
│
├── supabase/                   # Supabase configuration & migrations
│   ├── migrations/
│   └── functions/
│
├── package.json                # Project dependencies
├── package-lock.json           # Lock file
├── .env                        # Environment variables (not committed)
├── .gitignore                  # Git ignore rules
├── Claude.md                   # AI context file
└── README.md                   # Project documentation
```

---

## 🔄 How It Works

```
1. Trigger Call
   └─> Load contact data from Supabase
       └─> Initialize Vapi call session
           └─> AI agent handles conversation
               ├─> Natural language understanding
               ├─> Dynamic response generation
               └─> Data capture & storage
                   └─> Call outcome logged to Supabase
```

### Call Flow

1. **Initiation** — Agent triggers outbound call via Vapi API
2. **Greeting** — AI introduces itself naturally
3. **Conversation** — LLM handles dynamic, context-aware dialogue
4. **Data Collection** — Key information captured during call
5. **Outcome** — Results stored in Supabase for analysis
6. **Follow-up** — Automated actions based on call outcome

---

## 🎯 Use Cases

- 🏠 **Real Estate** — Lead qualification and appointment setting
- 🏥 **Healthcare** — Appointment reminders and patient follow-ups
- 💼 **Sales** — Cold outreach and prospect qualification
- 🛒 **E-commerce** — Order confirmations and customer service
- 📚 **Education** — Enrollment follow-ups and student outreach
- 🏦 **Finance** — Loan inquiry follow-ups and service notifications

---

## 🔗 Related Repositories

| Repository | Description |
|------------|-------------|
| 🌐 [ai-showroom-frontend](https://github.com/salikahmed595/ai-showroom-frontend) | Frontend UI showcasing AI products |
| 🔧 [ai-showroom-backend](https://github.com/salikahmed595/ai-showroom-backend) | Backend API for AI Showroom |
| 🏠 [real-estate-leads-n8n](https://github.com/salikahmed595/real-estate-leads-n8n) | n8n automation for real estate leads |
| 🎓 [AI-Basics](https://github.com/salikahmed595/AI-Basics) | Beginner-friendly AI/ML resources |

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/new-feature`
3. Commit your changes: `git commit -m 'Add new feature'`
4. Push to the branch: `git push origin feature/new-feature`
5. Open a Pull Request

---

## 👤 Author

**Salik Ahmed** — AI Engineer & Automation Architect

> Building intelligent AI products, voice agents & automation systems that transform how businesses operate.

- 🐙 GitHub: [@salikahmed595](https://github.com/salikahmed595)
- 💼 LinkedIn: [salikahmed110](https://linkedin.com/in/salikahmed110)
- 📺 YouTube: [@salikahmed686](https://youtube.com/@salikahmed686)

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

<div align="center">
  <strong>⭐ Star this repo if it helps your AI automation journey!</strong><br/>
  Made with ❤️ and AI by <a href="https://github.com/salikahmed595">Salik Ahmed</a>
</div>
