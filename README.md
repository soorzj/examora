<a name="top"></a>

<img width="2048" height="381" alt="unnamed (8ss)" src="https://github.com/user-attachments/assets/e8170aca-3b45-4b5f-90ba-a999b4c5a511" />
<p></p>


[![HTML](https://img.shields.io/badge/HTML-5-E34F26?logo=html5&logoColor=white)](#)
[![CSS](https://img.shields.io/badge/CSS-3-1572B6?logo=css3&logoColor=white)](#)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?logo=javascript&logoColor=black)](#)

[![Pages](https://img.shields.io/badge/pages-8_interconnected-00d4ff)](#-pages)
[![Tests](https://img.shields.io/badge/test_cases-17_passing-10b981)](#-testing)
[![Version](https://img.shields.io/badge/version-v1.0_prototype-f59e0b)](#-version-control)
[![Status](https://img.shields.io/badge/status-prototype-orange)](#)

[![Team](https://img.shields.io/badge/team-E--SATAS-7c3aed)](#-team--e-satas)
[![Exams](https://img.shields.io/badge/exams_covered-10-7c3aed)](#-exams-covered)
[![License](https://img.shields.io/badge/license-academic-blue)](#-license)

> **Examora** is a student-first competitive exam registration portal that transforms raw student data into correctly formatted applications for India's top competitive examinations — eliminating repeated form-filling, reducing errors, and ensuring no student misses an opportunity due to administrative complexity.

---

## Table of Contents

- [About the Project](#-about-the-project)
- [Live Demo](#-live-demo)
- [Pages](#-pages)
- [Exams Covered](#-exams-covered)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Data Architecture](#-data-architecture)
- [Pricing Model](#-pricing-model)
- [Testing](#-testing)
- [Known Limitations](#-known-limitations)
- [Roadmap](#-roadmap)
- [Team — E-SATAS](#-team--e-satas)
- [Version Control](#-version-control)
- [License](#-license)

---

## 🚀 About the Project

Indian students applying for multiple competitive exams must navigate up to 10 different portals, each with its own data format, document specifications, eligibility criteria, and submission deadlines. This results in repeated work, high error rates, missed deadlines, and unnecessary stress — particularly for first-generation exam takers who lack institutional guidance.

**Examora** solves this by accepting a student's raw personal and academic data once, then automatically structuring it into the precise format required by each respective exam authority. One profile. Ten exams. Zero repeated form-filling.

This repository contains the **v1.0 prototype** — a fully functional, 8-page client-side web application developed by Team E-SATAS for Module 3 (Prototype Development) of our academic program.

---

## 🌐 Live Demo

👉 **[Live link here — add your GitHub Pages URL]**

---

## 📄 Pages

| Page | File | Description |
|:--|:--|:--|
| Homepage | [index.html](source_file/index.html) | Hero, animated stats, platform overview |
| Login / Sign Up | [auth.html](source_file/auth.html)  | Email/password auth, password strength meter, session management |
| Exam Selection | [exams.html](source_file/exams.html)  | 10 exam cards with category filters and per-exam accent themes |
| Registration Form | [form.html](source_file/form.html)  | Dynamic per-exam form engine with document upload and data save |
| Pricing | [pricing.html](source_file/pricing.html)  | Four-tier plan cards with simulated payment flow |
| Support | [support.html](source_file/support.html)  | Ticket system, FAQ accordion, ticket status lookup |
| Team | [creators.html](source_file/creators.html)  | E-SATAS member cards with roles and bios |
| Logout | [logout.html](source_file/logout.html)  | Session clear, contact info, 10-second auto-redirect |

---

## 📚 Exams Covered

| Exam | Category |
|:--|:--|
| JEE (Joint Entrance Examination) | Engineering |
| NEET | Medical |
| GATE | Engineering PG |
| UPSC CSE | Civil Services |
| CAT | Management |
| IBPS PO / SBI PO | Banking |
| CLAT | Law |
| NDA | Defence |
| SSC CGL | Government |
| CUET-UG | Central Universities |

---

## ✨ Features

- **Dynamic Form Engine** — A single central `EXAMS` config object renders exam-specific fields (e.g., PCM marks for JEE, wing preference for NDA, PCB for NEET) for all 10 exams without duplicate code
- **Intelligent Data Structuring** — Submitted data is organised into `personalInfo`, `academicInfo`, `examSpecificInfo`, and `documents`, then saved as both structured JSON and a formatted `.txt`-style record with a unique reference ID
- **Local Document Storage** — Uploaded photos, marksheets, and certificates are converted to Base64 via the FileReader API and stored alongside the registration record (5MB limit per file with validation)
- **Authentication System** — Email/password login and signup with real-time password strength validation (8+ chars, uppercase, number, symbol), persistent localStorage sessions, and clean logout
- **Exam Category Filters** — Filter exam cards by Engineering, Medical, Management, Civil Services, Banking, Law, Defence, and Government
- **Four-Tier Pricing Paywall** — Free / ₹250 / ₹500 / ₹800 plans with a simulated payment modal supporting UPI, Card, and Net Banking
- **Support Ticketing System** — Submit tickets with priority levels (Low/Medium/High/Critical), auto-generated ticket IDs, localStorage persistence, and a ticket status lookup tool
- **Real-time Progress Bar** — Form completion percentage calculated live across all input types
- **Animated Homepage Stats** — IntersectionObserver-triggered counters for key platform metrics
- **Responsive Design** — CSS Grid with `auto-fill` and `minmax()` — adapts from 375px mobile to 1440px desktop without JavaScript
- **Zero Dependencies** — All CSS and JavaScript embedded per-page; no npm, no build step, no external scripts

---

## 🛠 Tech Stack

| Layer | Technology |
|:--|:--|
| Markup | HTML5 (semantic, 8 interconnected pages) |
| Styling | CSS3 — custom properties, grid, flexbox, keyframe animations |
| Behaviour | Vanilla JavaScript ES6+ — Canvas API, FileReader API, IntersectionObserver |
| Fonts | Syne (headings) + DM Sans (body) via Google Fonts |
| Data Persistence | Browser `localStorage` — JSON records + Base64 document blobs |
| File Handling | `FileReader` API — converts uploads to Data URLs, stored locally |
| Routing | Standard HTML anchor navigation + URL query strings (`?exam=jee`) |
| External Dependencies | None |

---

## 📁 Project Structure

```
examora/
├── index.html        # Homepage — hero, stats, platform overview
├── auth.html         # Login / Sign Up — validation, session management
├── exams.html        # Exam selection — 10 cards, category filter bar
├── form.html         # Registration form engine — all 10 exams, doc upload
├── pricing.html      # Pricing — four tiers, payment modal
├── support.html      # Support — ticket form, FAQ accordion, lookup
├── creators.html     # Team — E-SATAS member cards
└── logout.html       # Logout — session clear, auto-redirect
```

---

## 🏁 Getting Started

No build step. No npm install. Just clone and open.

```bash
# Clone the repository
git clone https://github.com/[your-username]/examora.git

# Navigate into the folder
cd examora

# Open in browser
open index.html
```

For a local dev server (recommended — avoids browser security restrictions on file uploads):

```bash
# Python 3
python -m http.server 8000

# Then visit
http://localhost:8000
```

> **Note:** The app uses `localStorage` for all data. Clearing browser storage will reset user accounts and saved registrations.

---

## 🗄 Data Architecture

Each submitted registration is saved to `localStorage` under the key `student_examKey` as a structured JSON record:

```json
{
  "refId": "EXM-1234567890-JEE",
  "exam": "JEE Main",
  "examKey": "jee",
  "submittedAt": "2025-04-05T10:30:00.000Z",
  "student": { "id": 1712300000000, "name": "Arjun Sharma", "email": "arjun@example.com" },
  "personalInfo": {
    "fullname": "Arjun Sharma", "dob": "2006-05-12", "gender": "Male",
    "category": "General", "aadhaar": "XXXX-XXXX-XXXX", "mobile": "+91 98765 43210",
    "father": "Rajesh Sharma", "mother": "Priya Sharma", "state": "Kerala", "pin": "695014"
  },
  "academicInfo": { "class10Board": "CBSE", "class10Percent": "94.2", "pcmMarks": "285/300" },
  "examSpecificInfo": { "attemptNumber": "1", "preferredLanguage": "English" },
  "documents": { "photo": { "name": "photo.jpg", "size": "245KB", "data": "data:image/jpeg;base64,..." } }
}
```

A plain-text `.txt`-style formatted version is saved simultaneously under `student_examKey_txt_REFID` — structured like a traditional registration printout.

---

## 💳 Pricing Model

| Plan | Price | Exams | Features |
|:--|:--|:--|:--|
| Free Explorer | ₹0 | 1 exam | Basic form fill, PDF download |
| Student Starter | ₹250 | 3 exams | All Free features + document storage |
| Exam Ready | ₹500 | 7 exams | All Starter features + priority support, mentor Q&A |
| All Access | ₹800 | All 10 exams | All features + dedicated counsellor, AI suggestions |

> **Limited-time offer:** First 5,000 students get 40% off all paid plans.

Payments are simulated in the prototype with a 1.8-second processing delay. Production integration planned via Razorpay.

---

## 🧪 Testing

**17 test cases — all passing.** Key cases:

| Test | Expected | Status |
|:--|:--|:--|
| New user signup with all fields | Account saved; session created; redirect to exams | ✅ Pass |
| Login with wrong password | Error alert; no session created | ✅ Pass |
| Exam filter — Engineering only | Only JEE and GATE visible | ✅ Pass |
| Register without login | Redirect to auth.html | ✅ Pass |
| Form submit with empty required field | Field highlighted; submit blocked | ✅ Pass |
| Upload file > 5MB | Alert shown; file rejected | ✅ Pass |
| Successful form submission | Success screen; refId generated; data saved | ✅ Pass |
| Select Free plan | Plan saved; redirect to exams; no payment modal | ✅ Pass |
| Complete UPI payment | Processing delay; success modal; plan saved | ✅ Pass |
| Submit support ticket | Ticket ID generated; saved; success banner | ✅ Pass |
| Logout and revisit protected page | Redirect to auth.html immediately | ✅ Pass |

Full test plan documented in the [Prototype Development Report](examora_prototype_report.pdf).

---

## ⚠️ Known Limitations

These are documented, expected prototype constraints with planned production resolutions:

| Limitation | Production Resolution |
|:--|:--|
| Passwords stored in plain text in localStorage | bcrypt / Argon2 server-side hashing |
| Data is device-bound (localStorage only) | MongoDB Atlas / Firebase Firestore cloud database |
| Document storage capped at ~5–10MB (browser) | AWS S3 / Firebase Storage |
| No real payment processing | Razorpay / PayU / CCAvenue gateway integration |
| No email notifications | Node.js + Nodemailer / SendGrid |
| No admin dashboard | Web panel for E-SATAS to manage submissions and tickets |

---

## 🗺 Roadmap

- [x] **v1.0** — Full 8-page prototype with auth, dynamic forms, doc upload, pricing, ticketing
- [ ] **Phase 2** — Node.js + Express backend, MongoDB Atlas, bcrypt auth, JWT sessions
- [ ] **Phase 3** — Razorpay payment gateway, automated receipt generation
- [ ] **Phase 4** — AI-assisted data formatter (auto-correct name casing, Aadhaar format, dates)
- [ ] **Phase 5** — Admin dashboard for submissions, ticket management, revenue tracking
- [ ] **Phase 6** — React Native / Flutter mobile app with deadline push notifications

**Scale Target:** 5,000 students in Year 1 · 50,000 users by Year 2

---

## 👥 Team — E-SATAS

| Name | Role |
|:--|:--|
| **Sooraj Krishna S** | Team Leader — project vision, coordination, final review |
| **Tawfiq Kabeer** | Project Coordinator — milestone tracking, activity sequencing |
| **Evan Paul Jacob** | Finance Navigator — pricing model, budget, revenue planning |
| **Anna Roy** | Product Analyst & UX Strategist — usability evaluation, UX improvements |
| **Alby Benoy** | Future Scope Planner — limitation analysis, enhancement roadmap |
| **Mohammed Thufail** | Content & Communication Lead — copy, presentations, awareness |
| **Subin S** | Promotion Head — outreach strategy, student community awareness |

---

## 📋 Version Control

| Version | Description |
|:--|:--|
| **v1.0** *(current)* | Complete 8-page prototype — all features functional, 17/17 tests passing |
| v0.9 | 7 pages without `pricing.html`; Google Drive document storage; placeholder creator names |

**Changes in v1.0:**
- Google Drive replaced with local Base64 document storage (zero external dependency)
- `pricing.html` added to all navbars and footers
- Creator cards updated with real E-SATAS names, roles, and bios
- Dynamic `EXAMS` config object introduced — replaced static common fields with per-exam field rendering

Git branching (`main` / `dev` / `feature-x`) planned for production phase.

---

## 📃 License

This project was developed as an academic prototype for Module 3 — Prototype Development. All rights reserved by Team E-SATAS · Examora · 2025.

---

<p align="center">Built with frustration, fixed with code · Team E-SATAS · Examora · 2025</p>

[Back to top](#top)
