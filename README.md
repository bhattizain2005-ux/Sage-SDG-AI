[README.md](https://github.com/user-attachments/files/28457373/README.md)
# 🌿 Sage SDG AI

> **Your human-like guide for learning, well-being, and clean water action.**

[![Live Demo](https://img.shields.io/badge/Live%20Demo-cloud--sparkle--ninja.lovable.app-EF233C?style=for-the-badge&logo=vercel&logoColor=white)](https://cloud-sparkle-ninja.lovable.app/)
[![GitHub](https://img.shields.io/badge/GitHub-Sage--SDG--AI-0B0B0F?style=for-the-badge&logo=github&logoColor=white)](https://github.com/bhattizain2005-ux/Sage-SDG-AI)
[![Next.js](https://img.shields.io/badge/Next.js-14-black?style=for-the-badge&logo=next.js)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-CSS-38BDF8?style=for-the-badge&logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)

---

## 📌 Overview

**Sage SDG AI** is a full-stack, safety-first AI mega-agent platform aligned with the United Nations Sustainable Development Goals. It combines three specialized AI modules into one unified, human-like assistant — helping users learn, reflect on their well-being, and navigate clean water safety concerns.

The platform originated as **AquaHealth AI** — a water safety awareness agent — and has since been expanded into a comprehensive SDG platform. The water module now lives on as **AquaLife Mode**, the original foundation of this project.

---

## 🌍 SDG Alignment

| Mode | SDG | Focus |
|------|-----|-------|
| 📚 Learn Mode | SDG 4 — Quality Education | AI tutoring, study plans, quizzes, progress tracking |
| 🧠 MindCare Mode | SDG 3 — Good Health & Well-being | Reflection, breathing exercises, well-being guidance |
| 💧 AquaLife Mode | SDG 6 + SDG 3 | Water risk awareness, symptom urgency, complaint reporting |

---

## ✨ Features

### 📚 Learn Mode — Quality Education AI
- AI tutor-style topic explanations
- Personalized study plans
- Auto-generated quiz questions
- Learning goal tracking
- Progress metrics
- SDG 4 contextual connections
- **Safety:** Explains and teaches — never produces dishonest academic submissions

### 🧠 MindCare Mode — Mental Health & Well-being AI
- Mood and stress level summarization
- Guided reflection prompts
- Breathing exercises
- Self-care action suggestions
- Professional help suggestions when needed
- **Safety:** Crisis escalation for severe distress, self-harm mentions, or panic — includes immediate professional/emergency referral

### 💧 AquaLife Mode — Water Solutions AI *(Upgraded from AquaHealth AI)*
- Water issue categorization
- Risk level badges (Low / Moderate / High / Emergency)
- Immediate safety recommendations
- Health risk awareness cards
- Complaint and reporting guidance
- Query history tracking
- Dashboard analytics
- **Safety:** Serious symptom override (diarrhea, vomiting, fever, child illness) → Emergency escalation + doctor referral

---

## 🏗️ System Architecture

```
User Input
    │
    ▼
Frontend (Next.js / React / Tailwind)
    │
    ▼
POST /api/sdg-agent  ◄── Single unified AI route
    │
    ├── mode: "education"  →  lib/educationLogic.ts  →  data/educationDataset.ts
    ├── mode: "wellbeing"  →  lib/wellbeingLogic.ts  →  data/wellbeingDataset.ts
    └── mode: "water"      →  lib/waterRiskScoring.ts → data/waterDataset.ts
    │
    ▼
Structured JSON Response
    │
    ▼
RecommendationCard (mode-specific rendering)
    │
    ▼
Dashboard Analytics (Recharts)
```

---

## 🤖 AI Agent Process Flow

```
1. Define Purpose & Scope
2. System Prompt Design
3. Choose LLM (LM Arena / fallback logic)
4. Tools & Integrations
5. Memory Systems
6. Orchestration
7. User Interface
8. Testing & Evals
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | Next.js 14 (App Router) |
| Language | TypeScript |
| Styling | Tailwind CSS |
| Charts | Recharts |
| Icons | Lucide React |
| Backend | Next.js API Routes |
| AI Routing | Custom fallback logic + LM Arena placeholder |
| Data | Local mock datasets |
| Deployment | Lovable Cloud / Vercel-ready |

---

## 🎨 Design System

The UI uses a **premium red, black, and gradient identity** — approximately 40% light, never fully dark or fully bright.

| Token | Value |
|-------|-------|
| Primary Red | `#EF233C` |
| Deep Red | `#B00020` |
| Black | `#0B0B0F` |
| Charcoal | `#17171F` |
| Soft Light | `#F8F7F4` |
| Muted Gray | `#E5E7EB` |
| Gradient 1 | `#EF233C → #7F1DFF` |
| Gradient 2 | `#0B0B0F → #EF233C` |
| Accent Pink | `#FF4D6D` |
| Accent Violet | `#7F1DFF` |

---

## 📂 Project Structure

```
sage-sdg-ai/
├── app/
│   ├── api/
│   │   └── sdg-agent/        # Unified AI route (POST)
│   ├── dashboard/
│   │   ├── user/             # User dashboard with AIChatBox
│   │   ├── admin/            # Admin dashboard
│   │   └── client/           # Client dashboard
│   ├── roadmap/              # Roadmap + Agent Process Flow
│   └── demo/                 # Demo page
├── components/
│   ├── AIChatBox.tsx         # 3-mode selector + fetch logic
│   ├── RecommendationCard.tsx # Mode-specific response renderer
│   └── AgentProcessFlow.tsx  # 8-step AI agent diagram
├── data/
│   ├── educationDataset.ts
│   ├── wellbeingDataset.ts
│   ├── waterDataset.ts
│   ├── mockAnalytics.ts
│   └── demoQueries.ts
├── lib/
│   ├── sdgAgent.ts
│   ├── educationLogic.ts
│   ├── wellbeingLogic.ts
│   └── waterRiskScoring.ts
├── .env.example
├── README.md
└── FINAL_REPORT.md
```

---

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- npm or yarn

### Installation

```bash
# Clone the repository
git clone https://github.com/bhattizain2005-ux/Sage-SDG-AI.git
cd Sage-SDG-AI

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env.local
# Edit .env.local with your keys (optional — fallback logic works without them)

# Run locally
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Build for Production

```bash
npm run build
npm start
```

---

## 🔐 Environment Variables

```env
# Optional — app works with fallback logic if not provided
LM_ARENA_API_KEY=your_lm_arena_api_key_here
LM_ARENA_API_URL=your_lm_arena_endpoint_here
```

> ⚠️ Never commit real API keys. Use `.env.local` (already in `.gitignore`).

---

## 🧪 API Reference

### POST `/api/sdg-agent`

**Request body:**
```json
{
  "mode": "education" | "wellbeing" | "water",
  "message": "string",
  "category": "optional string",
  "symptoms": "optional string",
  "location": "optional string",
  "urgency": "optional string"
}
```

**Education response:**
```json
{
  "topic_summary": "...",
  "simple_explanation": "...",
  "learning_goal": "...",
  "recommended_activity": "...",
  "quiz_question": "...",
  "progress_metric": "...",
  "sdg_connection": "..."
}
```

**Well-being response:**
```json
{
  "mood_stress_summary": "...",
  "reflection_prompt": "...",
  "breathing_exercise": "...",
  "self_care_action": "...",
  "safety_note": "...",
  "professional_help_suggestion": "...",
  "disclaimer": "..."
}
```

**Water response:**
```json
{
  "issue_summary": "...",
  "possible_cause": "...",
  "risk_level": "Low | Moderate | High | Emergency",
  "immediate_safety_steps": "...",
  "health_risk_awareness": "...",
  "complaint_report_suggestion": "...",
  "disclaimer": "..."
}
```

---

## ⚠️ Safety & Ethics

### MindCare Mode
- Does **not** diagnose mental illness
- Does **not** prescribe medication
- Does **not** replace a therapist, doctor, or emergency service
- Triggers crisis escalation for: self-harm, suicide, severe distress, abuse, panic, or danger

### AquaLife Mode
- Does **not** diagnose disease
- Does **not** prescribe medicine
- Triggers Emergency risk override for: diarrhea, vomiting, fever, dehydration, illness in children, or multiple people sick

> **AquaLife Disclaimer:** AquaLife AI provides general water safety and health-risk awareness only. It does not provide medical diagnosis, treatment, or professional health advice. For serious symptoms such as severe diarrhea, vomiting, fever, dehydration, or illness in children, contact a qualified doctor or local health center immediately.

### Learn Mode
- Supports learning, not academic dishonesty
- Explains, guides, quizzes, and teaches

---

## 📊 Dashboards

| Dashboard | Audience | Features |
|-----------|----------|----------|
| User Dashboard | Students / General users | AIChatBox, query history, mode responses |
| Admin Dashboard | Platform administrators | Usage analytics, module metrics, charts |
| Client Dashboard | Organizations / Partners | SDG insights, impact metrics |

---

## 🗺️ Roadmap & Future Improvements

- [ ] Real LM Arena / LLM API integration
- [ ] User authentication (Auth.js / Clerk)
- [ ] Persistent database (PostgreSQL / Supabase)
- [ ] PDF report export
- [ ] Real Kaggle dataset publication
- [ ] Organization/multi-tenant accounts
- [ ] More SDG modules (SDG 1, 2, 7, 13...)
- [ ] Mobile app (React Native)
- [ ] Multi-language support

---

## 🏛️ Project History

```
AquaHealth AI  ──►  AquaLife Mode  ──►  Sage SDG AI
(SDG 6 prototype)   (water module)      (mega-agent platform)
```

This project started as **AquaHealth AI**, a Clean Water and Public Health Risk Awareness agent for SDG 6 and SDG 3. It was expanded into **Sage SDG AI** — a full mega-agent platform. The original water module lives on as **AquaLife Mode**.

---

## 👤 Author

**Zain Bhatti**
University AI Project — Portfolio Build

- 🔗 Live: [cloud-sparkle-ninja.lovable.app](https://cloud-sparkle-ninja.lovable.app/)
- 🐙 GitHub: [github.com/bhattizain2005-ux/Sage-SDG-AI](https://github.com/bhattizain2005-ux/Sage-SDG-AI)

---

## 📄 License

This project is for educational and portfolio purposes.

---

*Sage SDG AI · University presentation build · Safety-first fallback logic included. Not a substitute for professional medical, mental-health, or public-health advice.*
