# 🐾 Allowance Buddy — Bucks, the Money-Wise AI Robot Dog

**🏫 Marshall AI Association (MAIA) — Finance Department, USC**  
**Role: ML Engineer (Computer Vision & Pose Estimation)**  
**Duration: January 2026 – May 2026**

---

> *"Little by little, your savings get bigger."*  
> Making finance and chores fun and easy for kids 7+

---

## 📌 Project Overview

Allowance Buddy is an AI-powered financial literacy companion for children aged 7+, built around **Bucks** — a robotic AI dog that sits in the classroom, engages with students, rewards good behavior with virtual currency, and teaches real money management through play.

Financial habits start forming at **7 years old** (Cambridge Research), yet most personal finance education in the US happens after age 16 — nine years too late. Allowance Buddy bridges that gap through hardware, software, and a physical book series that grow with the child.

**Organisation:** Marshall AI Association (MAIA) — Finance Department, USC  
**Team:** Vanya Shrivastava (Team Lead), Mason Zimmerman (Hardware), Oma Tasie-Amadi (ML Engineer), Samya Puri (ML Engineer), Rodrigo Sepúlveda Sagaseta (Business Analyst), Rohan Patel (Backend Engineer)

---

## 🧠 My Technical Contributions

### 1. Pose Data Collection & Manufacturing
- Led data collection efforts across the team, capturing body landmark data for **20+ pose classes** including sweeping, wiping table, reading, picking up items, folding clothes, carrying laundry, making bed, idle standing, and more
- Engineered the data collection pipeline using MediaPipe to capture and save individual CSV files per person per pose
- Generated synthetic data to supplement team-collected samples and increase model robustness across varying body proportions

### 2. Pose Classification Model Training (MediaPipe)
- Trained a deep neural network on **10,000+ normalized MediaPipe landmark coordinates** to classify real-time poses
- Used normalized body keypoints so that person size and distance from camera don't affect accuracy
- Key challenge: variations in how different people naturally move and position their bodies create noise in coordinate outputs — addressed through expanded data collection and augmentation
- Model outputs feed directly into the Context Fusion Engine to identify child actions in real time

### 3. Mobile App UI (iOS)
- Designed and developed user-facing screens for the React Native iOS app
- Built the Kids Portal including bank balance display, daily chores checklist, day streak tracker and rewards
- Contributed to the Parent and Teacher portal interfaces showing progress dashboards and activity feeds

---

## 🐾 How Bucks Works
Camera & Sensors (Raspberry Pi)
→
Perception: YOLO (Object Detection) + MediaPipe (Pose Estimation)
→
Context Fusion Engine (Pose + Object = Action)
→
Feedback: ElevenLabs Voice Agent + iPad/iPhone App + Hardware (Motor Controls, LED Strip, Bark)

**When a child completes a chore:**
1. Bucks sees the action in real time via the vision pipeline
2. The Context Fusion Engine identifies the behavior
3. Bucks responds — wagging tail, barking, LED lights, and a voice response via ElevenLabs
4. Virtual currency is deposited to the child's in-app bank balance
5. Parents and teachers see updates on their portal dashboard in real time

---

## 📱 iOS App — Three Portals

**Kids Portal:** Bank balance, daily chores checklist, day streak, unlocked lessons  
**Parent Portal:** Award system setup, progress monitoring, investing simulation controls  
**Teacher Portal:** Class overview, lesson completion rates, recent activity, assignments

---

## 📖 Physical Book Series

Bucks comes with **Book 1: Beginner** — financial lessons and activities to supplement the in-app experience. Books 2 (Intermediate) and 3 (Advanced) unlock as the child progresses, each shipped with a mystery physical prize (dog collar, bones, accessories).

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| Object Detection | YOLOv8n (Ultralytics) |
| Pose Estimation | MediaPipe (Google) |
| Inference Engine | Context Fusion (Rule-based + ML classifier) |
| Voice Agent | ElevenLabs |
| Mobile App | React Native (Expo Go) |
| Backend / Database | Supabase |
| Hardware | Raspberry Pi 5 + AI Hat |
| Deployment Target | ESP32 S3 (~$2.14 vs $150+ Pi — 45% cost reduction) |

---

## 🏗 Repository Structure
allowancebuddy/
├── app/mobile/          # iOS React Native app (Kids, Parent, Teacher portals)
├── services/
│   ├── vision/          # CV pipeline: YOLO + MediaPipe + Context Fusion
│   ├── backend/         # API, auth, accounts, transaction logs
│   └── finance-engine/  # Allowance rules, deductions, investing simulations
├── hardware/
│   └── rpi/             # Raspberry Pi firmware, camera, motor controls
├── data/                # Pose collection CSVs, sample events, simulations
├── packages/            # Shared types, UI components, utilities
├── infra/               # Docker, CI/CD
└── docs/                # Architecture, API contracts, product vision

---

## 📊 Market Opportunity

| Metric | Value |
|---|---|
| US Elementary Schools | 70,000+ |
| US Elementary Classrooms | 1.5 Million+ |
| K-12 EdTech Market | $295 Billion (growing 13% annually) |
| School Spend Per Student/Year | $17,700+ |

*Source: NCES, Dimension Market Research, Education Data Initiative 2025*

---

## 💰 Business Model

| Revenue Stream | Price |
|---|---|
| Hardware (robot dog + onboarding kit) | $699 one-time per classroom |
| SaaS (dashboard, lessons, behavior analytics) | $29/month per teacher |
| District License (50 classrooms, custom analytics) | $15K+/year |

---

## 🌍 Social Impact

Bucks is partnering with the **Iberoamerican Technology Foundation** to bring financial literacy to underserved communities in Mexico. For every two classroom units deployed in the US, one is funded in a Mexican school that couldn't otherwise afford it.

Wealthy schools are nearly **3x more likely** to require a personal finance class than low-income schools (Next Gen Personal Finance, 2024). Bucks is built to close that gap.

---

## 📈 Traction

- ✅ Pilot program at **Little Tokyo Library, Los Angeles** — 20+ children
- ✅ Demoed at **MAIA Demo Day (May 2026)** in front of guests including Alan Du (Microsoft), Gagan Bajaj (Google), Kenny Nguyen (OpenAI), Geoffrey Garrett (Dean of USC Marshall), and Dan Wadhwani (USC Marshall)
- ✅ Customer discovery survey conducted with guardians on how they teach kids about money, pain points, and child engagement

---

## 🔗 Resources

- [Demo Day Slide Deck](https://drive.google.com/file/d/1W4J84HKuVrkDCdBZSD4MjIHa5POmrI24/view?usp=sharing)
- [Main Portfolio Hub](https://github.com/omatasie/oma_tasie_portfolio)

---

*Developed by Oma Tasie-Amadi and Team @ USC Marshall AI Association.*  
*Because every Penny matters — and so does every Buck. 🐾*
