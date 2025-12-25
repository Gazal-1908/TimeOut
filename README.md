# ⏰ TimeOut — Focus & Study App

A comprehensive productivity platform for students and educators with focus tracking, real-time collaboration, and behavioral analytics.

Status: ✅ Ready

![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![Version](https://img.shields.io/badge/version-2.0.0-blue)
![React](https://img.shields.io/badge/React-18.3.1-61DAFB?logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5.6.2-3178C6?logo=typescript)
![Firebase](https://img.shields.io/badge/Firebase-Latest-FFCA28?logo=firebase)

---

## Overview

TimeOut is a full-featured student productivity and classroom management system designed to improve focus, track progress, and facilitate collaborative learning. Built with React and Firebase, it provides students and teachers with powerful tools to maximize learning effectiveness through behavioral science and real-time analytics.

Key differentiators:
- Token-based reward economy (Focus Points) that incentivizes productive study habits
- Digital Detox system with fullscreen enforcement and app restriction concepts
- Real-time collaborative study rooms with synchronized timers
- Teacher dashboards with live student monitoring and analytics
- AI-ready schedule templates and automated planning concepts
- Comprehensive analytics tracking focus patterns, streaks, and productivity scores
  
---

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- npm 9+ (or yarn/pnpm)
- Git
- Optional (for full setup): Firebase CLI (`npm i -g firebase-tools`)

## 🎯 Features

### ✅ Working (Out-of-the-box)
- Focus Timer (Pomodoro, Deep Work, Breaks) with local persistence
- Beautiful, responsive UI (green theme, glassmorphism)
- Demo Mode: runs immediately without external setup
- Session history (local)
- Basic analytics (local/demo)

### 🎭 Demo/Interactive UI
- Group Study: virtual rooms, timer sync (simulated)
- Digital Detox: analytics views with generated data
- Community: achievements and leaderboards with sample data
- Camera verification UI (simulated)

### ☁️ Full Features (with Backend)
- Real Authentication (Clerk + Firebase)
- Cloud Sync (Firestore persistence)
- Live Group Sessions (real-time rooms)
- Real Analytics (usage tracking & insights)
- Callable Functions for Digital Detox, Tokens, Rooms, Schedule

---

## 🛠 Tech Stack

### Frontend
- React 18 + TypeScript
- Vite (fast dev/build)
- Tailwind CSS + shadcn/ui
- React Router DOM
- Lucide React (icons)
- React Hook Form + Zod
- date-fns

### Backend (Optional)
- Firebase Cloud Functions (Node.js 18)
- Firebase Auth, Firestore, Storage
- Express.js endpoints (as needed)
- Clerk webhooks for user sync

---

## 🏗 Project Structure

```
TimeOut/
├── TimeOut Frontend/           # React frontend application
│   ├── src/
│   │   ├── components/
│   │   │   ├── auth/           # Authentication components
│   │   │   ├── dashboard/      # Dashboard views
│   │   │   │   └── tabs/       # Dashboard tab components
│   │   │   ├── layout/         # Layout components
│   │   │   ├── tokens/         # Token system UI
│   │   │   └── ui/             # shadcn UI components
│   │   ├── contexts/           # React Context providers
│   │   ├── hooks/              # Custom React hooks
│   │   ├── config/             # Firebase & app config
│   │   ├── lib/                # Utility functions
│   │   ├── pages/              # Page components
│   │   └── utils/              # Helpers
│   ├── public/                 # Static assets
│   └── package.json
│
├── TimeOut Backend/            # Firebase backend
│   ├── functions/
│   │   ├── src/
│   │   │   ├── callable/
│   │   │   │   ├── digitalDetox.ts
│   │   │   │   ├── rooms.ts
│   │   │   │   ├── schedule.ts
│   │   │   │   ├── tokens.ts
│   │   │   │   └── users.ts
│   │   │   ├── types/
│   │   │   ├── config/
│   │   │   └── index.ts
│   │   └── package.json
│   ├── firebase.json
│   ├── firestore.rules
│   └── storage.rules
│
├── scripts/
│   ├── setup.ps1
│   ├── setup.sh
│   ├── deploy-config.ps1
│   └── deploy-config.sh
│
└── docs/
    ├── BACKEND_INTEGRATION_SUMMARY.md
    ├── DEPLOYMENT_GUIDE.md
    ├── SETUP_GUIDE.md
    ├── TOKEN_REWARD_SYSTEM_DESIGN.md
    └── VERCEL_DEPLOYMENT_GUIDE.md
```

---

## 🎮 Usage

### Study Timer
1) Set duration (25/50 custom)
2) Choose subject
3) Start session
4) Take breaks between sessions
5) Progress tracked in history

### Group Study
- Browse and join public rooms or create a private one
- Participant limits and visibility controls
- Synchronized timers
- Optional camera check-ins (demo)

### Digital Detox
- Set app restriction rules (concept/UI)
- Start focus with fullscreen enforcement (concept/UI)
- View usage analytics and recommendations

### Students
- Create account and select “Student”
- Build weekly schedule and use templates
- Start focus sessions and earn Focus Points
- Join study groups
- Track progress and streaks

### Teachers
- Create account and select “Teacher”
- Create classes and start live sessions
- Monitor student states and connections
- Share resources
- View class analytics and engagement

---

## 💰 Token System (Focus Points)

Earning:
- 25-minute session: 25 FP
- 50-minute deep work: 60 FP
- 7-day streak: 300 FP bonus
- Group session participation: 15–40 FP
- Share template: 50 FP (+10 FP per use)

Spending:
- Shop: Themes, Avatar frames, Features, Badges
- Items have rarity (Common→Legendary)
- Purchase logs recorded

---

## 📈 Performance

Frontend:
- Code splitting via dynamic imports
- Image lazy loading and sizing
- Tree-shaking with Vite
- Optional service worker for offline support

Backend:
- Minimized cold starts
- Client-side caching of Firestore data
- Batched writes and composite indexes
- Basic rate limiting concepts for callable functions

---

## 🔒 Security

- Clerk + Firebase Auth for secure user management
- Verification on all backend calls (full setup)
- Webhook signature validation (Clerk)
- Firestore/Storage rules for least-privilege access
- HTTPS-only communication
- No secrets in client code
- Input validation and XSS protection via React

---

## 🤝 Contributing

1) Fork the repository
2) Create a feature branch: `git checkout -b feat/amazing-feature`
3) Follow code style (ESLint + Prettier)
4) Write tests
5) Update docs
6) Open a Pull Request

Standards:
- TypeScript strict mode
- ESLint enforced
- Prettier formatting
- Conventional Commits
- Component-level docs where applicable

Areas to contribute:
- Mobile app (React Native)
- i18n
- New token shop content
- Schedule template marketplace
- Analytics visualizations
- Calendar integrations
- Browser extension for blocking
- Desktop app (Electron)

---

## 🗺 Roadmap

- v2.1 (Q1 2025): Mobile app, offline mode, voice commands, calendar integration, teacher analytics
- v2.2 (Q2 2025): AI recommendations, habits, goals, social challenges, custom sounds
- v2.3 (Q3 2025): Browser extension, Electron desktop, institutional reporting, i18n, theme toggle

Long-term:
- LMS integrations (Canvas, Moodle)
- Institutional dashboards
- Public API
- ML-driven personalized plans
- Virtual study spaces with spatial audio

---

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

Third-party licenses:
- React (MIT)
- Firebase (Apache 2.0)
- Tailwind CSS (MIT)
- shadcn/ui (MIT)
- Lucide Icons (ISC)
- date-fns (MIT)

---

## 🙏 Acknowledgments

Technologies:
- React Team
- Firebase Team
- Vercel
- Clerk
- shadcn

Design inspiration:
- TickTick
- Notion
- Forest
- Toggl

Community:
- Contributors, beta testers, students, and educators who shaped the feature set

---

## 📬 Contact

- Maintainer: Gazal Pancholi
- Email: gazalpancholi2005@gmail.com

Built with focus, designed for productivity, powered by community.
