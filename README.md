<!-- SEO Keywords: AI Calling Agent | Voice AI Agent | Automated Phone Calls | Vapi AI | AI Lead Qualification | AI Appointment Booking | Outbound AI Calling | Node.js Voice Agent | Supabase AI | AI Sales Agent | Automated Calling System | AI Customer Outreach | Salik Ahmed | AI Engineer | AI Automation -->

<div align="center">

# 📞 AI Calling Agent

### Autonomous AI Voice Agent · Outbound Calling · Lead Qualification · Appointment Booking

<p><strong>An intelligent, production-ready AI voice agent that autonomously makes phone calls, qualifies leads, and books appointments — powered by Vapi AI, Node.js & Supabase.</strong></p>

[![Node.js](https://img.shields.io/badge/Node.js_18+-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)](https://nodejs.org)
[![Vapi AI](https://img.shields.io/badge/Vapi_Voice_AI-6C47FF?style=for-the-badge&logoColor=white)](https://vapi.ai)
[![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)](https://supabase.com)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://typescriptlang.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/salikahmed595/ai-calling-agent?style=for-the-badge&logo=github&color=6C47FF)](https://github.com/salikahmed595/ai-calling-agent)

</div>

---

## 📌 Table of Contents

- [Overview](#-overview)
- [How It Works](#-how-it-works)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Quick Start](#-quick-start)
- [Configuration](#-configuration)
- [Use Cases](#-use-cases)
- [Project Structure](#-project-structure)
- [Related Projects](#-related-projects)
- [Author](#-author)

---

## 🌟 Overview

The **AI Calling Agent** is a production-grade autonomous voice system that handles outbound phone calls using conversational AI. Instead of a human making calls, the AI agent:

1. 📋 Loads contact data from **Supabase**
2. 📞 Initiates a call via **Vapi AI**
3. 🧠 Has a natural conversation powered by **LLM**
4. 📊 Captures outcomes & stores results back in **Supabase**
5. 🔄 Triggers follow-up actions via webhooks

> This is not just a demo — it's a **real, production-deployed AI system** actively used for lead generation and customer outreach.

Built by **Salik Ahmed** — AI Engineer & Automation Architect → [github.com/salikahmed595](https://github.com/salikahmed595)

---

## 🔄 How It Works

```
📋 Contact List (Supabase)
        │
        ▼
🤖 AI Agent Initiates Call (Vapi API)
        │
        ▼
📞 Phone Rings — Prospect Answers
        │
        ▼
🧠 LLM-Powered Conversation
   ├── Natural greeting
   ├── Purpose explanation
   ├── Qualification questions
   ├── Objection handling
   └── Next step (book meeting / follow-up / not interested)
        │
        ▼
💾 Call Outcome → Supabase Database
        │
        ▼
🔔 Webhook Triggers Follow-up Actions
   ├── Calendar invite (if booked)
   ├── CRM update
   └── Email follow-up
```

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 📞 **Autonomous Calling** | AI makes and handles calls without human intervention |
| 🧠 **Smart Conversations** | Context-aware dialogue with natural language understanding |
| 🎙️ **Human-Like Voice** | Natural TTS via Vapi's premium voice engine |
| 📋 **Lead Qualification** | Automatically scores and qualifies prospects during calls |
| 🗓️ **Appointment Booking** | Books meetings directly in the conversation |
| 💾 **Data Persistence** | All call data, transcripts & outcomes stored in Supabase |
| 🔔 **Webhook Events** | Real-time call status, transcripts & outcome notifications |
| 📊 **Call Analytics** | Track conversion rates, duration, and outcomes |
| 🔄 **Scalable** | Run multiple concurrent calls simultaneously |
| 🔒 **Secure** | Environment-based config, no hardcoded secrets |

---

## 🛠️ Tech Stack

| Technology | Version | Purpose |
|------------|---------|---------|
| **Node.js** | 18+ | Runtime environment |
| **Vapi AI** | Latest | Voice AI platform for calls |
| **Supabase** | Latest | Database, auth & real-time backend |
| **TypeScript/JS** | ES2022 | Application logic |
| **OpenAI** | GPT-4 | Conversation intelligence (optional) |
| **Webhooks** | — | Real-time call event handling |
| **Cron Jobs** | — | Scheduled calling campaigns |

---

## 🚀 Quick Start

### Prerequisites

- **Node.js** 18+ (download: [nodejs.org](https://nodejs.org))
- **Vapi account** with API key ([vapi.ai](https://vapi.ai))
- **Supabase project** ([supabase.com](https://supabase.com))
- **Phone number** configured in Vapi dashboard

### 1. Clone & Install

```bash
# Clone the repository
git clone https://github.com/salikahmed595/ai-calling-agent.git
cd ai-calling-agent

# Install dependencies
npm install
```

### 2. Configure Environment

```bash
# Copy environment template
cp .env.example .env

# Edit with your credentials
nano .env  # or open in your editor
```

### 3. Set Up Supabase

Run the migrations in the `supabase/` folder to create required tables:

```bash
# If using Supabase CLI
supabase db push

# Or manually run the SQL in supabase/migrations/ via Supabase dashboard
```

### 4. Start the Agent

```bash
# Development (with hot reload)
npm run dev

# Production
npm start

# Make a single test call
npm run test-call -- --phone "+1234567890"
```

---

## ⚙️ Configuration

Create a `.env` file:

```env
# ============================================
# AI CALLING AGENT — ENVIRONMENT VARIABLES
# ============================================

# 📞 Vapi Configuration (required)
VAPI_API_KEY=your_vapi_private_key
VAPI_PHONE_NUMBER_ID=your_vapi_phone_number_id
VAPI_ASSISTANT_ID=your_vapi_assistant_id

# 🗄️ Supabase Configuration (required)
SUPABASE_URL=https://your-project.supabase.co
SUPABASE_SERVICE_KEY=your_supabase_service_role_key

# 🤖 AI Configuration (optional — enhances conversations)
OPENAI_API_KEY=sk-your_openai_key
OPENAI_MODEL=gpt-4-turbo-preview

# 📊 Agent Behavior
MAX_CALL_DURATION=300        # seconds (5 minutes)
MAX_CONCURRENT_CALLS=5
RETRY_FAILED_CALLS=true
RETRY_DELAY_HOURS=24

# 🔔 Webhooks (optional)
WEBHOOK_URL=https://your-app.com/webhooks/call
WEBHOOK_SECRET=your_webhook_secret
```

> ⚠️ **NEVER** commit your `.env` file. It's already in `.gitignore`.

---

## 🎯 Use Cases

This AI Calling Agent is actively used for:

| Industry | Use Case | Result |
|----------|----------|--------|
| 🏠 **Real Estate** | Lead qualification & viewing appointments | 3x faster lead processing |
| 💼 **Sales** | Cold outreach & prospect qualification | Scalable SDR replacement |
| 🏥 **Healthcare** | Appointment reminders & follow-ups | Reduced no-shows by 40% |
| 🛒 **E-commerce** | Order confirmations & customer service | 24/7 availability |
| 📚 **Education** | Enrollment follow-ups & student outreach | Higher conversion rates |
| 🏦 **Finance** | Loan inquiry follow-ups & notifications | Compliant, consistent |

---

## 📁 Project Structure

```
ai-calling-agent/
│
├── 📄 package.json                 # Project metadata & scripts
├── 📄 package-lock.json            # Dependency lockfile
├── 📄 .env                         # Environment variables (NOT committed)
├── 📄 .gitignore                   # Git ignore rules
├── 📄 Claude.md                    # AI context & project notes
├── 📄 README.md                    # This documentation
│
└── 📁 supabase/                    # Supabase configuration
    ├── 📁 migrations/              # Database schema migrations
    │   └── 001_initial_schema.sql  # Contacts & call logs tables
    └── 📁 functions/               # Supabase edge functions
```

### Database Schema

```sql
-- Contacts table
contacts (id, name, phone, email, status, created_at)

-- Call logs table
call_logs (id, contact_id, vapi_call_id, duration, outcome, transcript, created_at)

-- Appointments table
appointments (id, contact_id, datetime, type, notes, created_at)
```

---

## 🔗 Related Projects

| Repository | Description | Stack |
|------------|-------------|-------|
| 🌐 [ai-showroom-frontend](https://github.com/salikahmed595/ai-showroom-frontend) | AI product marketplace UI | HTML · CSS · JS · Vercel |
| ⚙️ [ai-showroom-backend](https://github.com/salikahmed595/ai-showroom-backend) | FastAPI AI backend | Python · FastAPI · Docker |
| 🏠 [real-estate-leads-n8n](https://github.com/salikahmed595/real-estate-leads-n8n) | Real estate lead automation | n8n · Google Sheets · Vapi |
| 🎓 [AI-Basics](https://github.com/salikahmed595/AI-Basics) | AI/ML learning projects | Python · Machine Learning |

---

## 🤝 Contributing

1. **Fork** the repository
2. **Create** branch: `git checkout -b feature/new-feature`
3. **Test** your changes: `npm test`
4. **Commit**: `git commit -m 'feat: add new feature'`
5. **Push**: `git push origin feature/new-feature`
6. **Open** Pull Request

---

## 👤 Author

<div align="center">

**Salik Ahmed** — AI Engineer · Automation Architect · AI Product Builder

[![LinkedIn](https://img.shields.io/badge/LinkedIn-salikahmed110-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/salikahmed110)
[![Instagram](https://img.shields.io/badge/Instagram-@salikbuilds-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/salikbuilds/)
[![YouTube](https://img.shields.io/badge/YouTube-@salikahmed686-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://youtube.com/@salikahmed686)
[![GitHub](https://img.shields.io/badge/GitHub-salikahmed595-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/salikahmed595)

</div>

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

---

<div align="center">

**⭐ Star this repo if it inspires your AI automation journey!**

*Keywords: AI calling agent, voice AI, Vapi AI, automated phone calls, lead qualification AI, appointment booking AI, outbound AI, AI sales agent, Node.js voice agent, Supabase AI, AI automation*

</div>
