# 🛡️ SafeHood - Community Safety & GBV Response App

**SafeHood** is an AI-ready, community-powered mobile and backend system that enables vulnerable people—especially **women and children in high-risk townships**—to **trigger silent alerts**, stream **real-time location**, and enable **community patrol response** using modern technology.

Built for speed, safety, and scale, SafeHood is focused on fighting **gender-based violence (GBV)** through digital tools that empower users in the most underserved and unsafe environments.

---

## 📍 Use Case: Digital Safety for Vulnerable Communities

In high-crime, low-response areas like Soweto, people often face life-threatening danger with **no reliable way to call for help**. SafeHood turns your smartphone into a **digital panic button**, especially for **women and children walking alone, trapped in unsafe homes, or under threat**.

---

## 💡 Core Features

| Feature | Description |
|--------|-------------|
| 🔕 **Silent SOS** | Triple-press power button to silently trigger an emergency |
| 📡 **Live GPS Streaming** | Real-time location shared with community patrols |
| 🗣️ **Voice & Photo Capture** | Record audio or image evidence during or after incidents |
| 📶 **Offline SMS Backup** | Alert sent via SMS when internet is unavailable |
| 👥 **Community Responders** | Trusted neighbors, patrols, or private security firms receive alerts |
| 💬 **Dispatcher Chat** | Users can optionally chat with responders (via app or SMS) |
| 🔒 **Tamper-Proof Reporting** | Evidence stored securely and signed to ensure integrity |

---

## 🧠 Tech Stack Overview

| Layer | Tech | Purpose |
|-------|------|---------|
| Frontend | React Native (Bare Workflow) | Native access to device hardware (power button, GPS, media) |
| Backend | Django + PostgreSQL | Auth, alerts, user roles, audit logs |
| Real-Time | Django Channels + Redis | WebSocket system for alerts and patrol dispatch |
| Media | S3 via Django-Storages | Secure storage of sensitive files |
| Offline Comm | Africa’s Talking / Twilio | Panic via SMS or automated voice |
| DevOps | Docker + GitHub Actions + AWS/Render | CI/CD pipelines and cloud-ready deployment |
| AI Layer (future) | Python ML + REST API | Risk scoring, predictive patrols, NLP triggers |

---

## 📁 Folder Structure

```bash
SafeHood/
├── backend-api/                # Django backend
│   ├── alerts/                # Models and views for incidents
│   ├── dispatch/              # Responder assignment and live tracking
│   ├── media/                 # Handling uploads and evidence
│   ├── settings/              # Django settings modules
│   └── users/                 # Auth, roles, permissions
│
├── mobile-app/                # React Native app
│   ├── android/               # Android platform config
│   ├── ios/                   # iOS platform config
│   ├── src/                   
│   │   ├── components/        # Shared UI components
│   │   ├── screens/           # App screens (SOS, home, alerts, profile)
│   │   └── services/          # GPS, media, notification utilities
│   └── App.js                 # Entry point with SafeHood branding
│
├── docker-compose.yml         # Development & test container stack
├── .github/workflows/         # GitHub Actions CI/CD pipelines
└── README.md
````

---

## 🛠️ Dev Setup Instructions

### 🧱 Prerequisites

* Node.js & Yarn
* Python 3.11+
* Docker & Docker Compose
* Android Studio or Xcode

### 🚀 Quickstart (Dev Mode)

```bash
# 1. Clone project
git clone https://github.com/your-org/safehood.git
cd safehood

# 2. Start backend
docker-compose up --build

# 3. Install mobile deps
cd mobile-app
yarn install

# 4. Run the app
npx react-native run-android   # or run-ios
```

---

## 🐳 Docker Usage

The app ships with full containerization for backend services:

| Service          | Port   | Description            |
| ---------------- | ------ | ---------------------- |
| Django Backend   | `8000` | REST & WebSocket API   |
| PostgreSQL       | `5432` | Persistent DB          |
| Redis            | `6379` | WebSocket worker queue |
| (Optional) NGINX | `80`   | Reverse proxy for prod |

```bash
# Start everything
docker-compose up
```

---

## 🧪 Deployment Strategy

| Environment | Platform          | Purpose                                 |
| ----------- | ----------------- | --------------------------------------- |
| Dev         | Docker Compose    | Local containerized development         |
| Staging     | Render / AWS EC2  | Public-facing pilot instance            |
| Prod        | AWS ECS / Fargate | Full scale deployment with autoscaling  |
| CI/CD       | GitHub Actions    | Build, test, and deploy pipelines       |
| Monitoring  | Sentry + Logs     | Bug/error tracking for mobile + backend |

---

## 🔐 Security & GBV-Aware Architecture

* AES-256 encryption for all media and data at rest
* HTTPS + JWT for user auth and secure session flow
* Role-based responder system to avoid misuse
* Privacy-first SMS fallback (no content shown)
* Enforced audit logging for all alert handling

> SafeHood is POPIA/GDPR-aligned and puts **victim dignity and data sovereignty first**.

---

## 🌍 Future AI Capabilities

* 🧠 Risk classification based on historic data and context
* 🚨 Predictive dispatch (heatmap-driven patrols)
* 🗣️ Voice recognition for hands-free SOS (“Help me”, “Save me”)
* 📊 Community safety dashboards for local leaders

---

## 🤝 Integrations

* ADT/Chubb Private Security APIs (REST)
* Local SAPS Dispatch Systems (Webhook)
* Emergency Medical Services (e.g., Netcare)
* Telecoms (for no-data SMS relay partnerships)

---

## 💬 Pitch Summary (For Stakeholders)

> A girl walking home in Alexandra taps her power button three times. In 3 seconds, her GPS is sent to local SafeHood responders, a voice clip uploads automatically, and her family receives a ping. Whether or not she has airtime, whether or not she can speak — **SafeHood hears her**.
>
> This is not just an app. It’s a **resistance tool** against violence, a **neighborhood watch system in your pocket**, and a **lifeline** for our most vulnerable. Built by township-born engineers. Designed to protect our people.
>
> **We are done watching. SafeHood is here to act.**

---

## ✍️ Contributors

| Name            | Role                            |
| --------------- | ------------------------------- |
| **Gift Ndlala** | Tech Architect, Developer, Idea Founder      |


Open to NGO, corporate, or civic partnerships.

---

## 📜 License

This project is MIT Licensed. Free to use, fork, remix — especially in humanitarian contexts.

---

## 📎 Supporting Docs (WIP)

* System Architecture Diagram
* GBV Responder Protocols
* Safety Impact Metrics
* NGO/Government Partner Deck

---


