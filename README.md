# 🎙️ Prepwise — AI-Powered Mock Interview Platform

Prepwise is a full-stack web application that helps users prepare for job interviews through realistic, AI-driven voice interviews. Users can generate role-specific interview questions, take a live voice interview with an AI agent, and receive detailed, structured feedback on their performance.

This project was built as a hands-on way to learn how to integrate real-time voice AI agents with a modern Next.js stack — covering authentication, serverless backend logic, LLM-powered content generation, and structured AI feedback scoring.

---

## 🚀 Live Project

- **GitHub Repository:** [ai_mock_interviews](https://github.com/adrianhajdin/ai_mock_interviews) *(replace with your own repo link)*
- **Live Demo:** Not deployed yet

---

## ⚙️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Next.js (App Router), React, TypeScript |
| Styling | Tailwind CSS, shadcn/ui |
| Voice AI | Vapi AI Voice Agents |
| LLM | Google Gemini |
| Auth & Database | Firebase (Authentication + Firestore) |
| Validation | Zod |

---

## 🔋 Key Features

- **🔐 Authentication** — Secure sign-up / sign-in with email and password via Firebase Auth.
- **🧠 AI-Generated Interviews** — Generates tailored interview questions based on job role, experience level, tech stack, and interview type (technical / behavioral / mixed), using Google Gemini.
- **🎤 Live Voice Interviews** — Conducts the actual interview through a real-time voice agent (Vapi), simulating a natural conversational interview experience.
- **📝 Real-Time Transcripts** — Captures and displays the full conversation transcript as the interview progresses.
- **📊 AI-Powered Feedback** — After the interview, an LLM analyzes the transcript and scores the candidate across five categories:
  - Communication Skills
  - Technical Knowledge
  - Problem-Solving
  - Cultural & Role Fit
  - Confidence & Clarity
- **📈 Dashboard** — Central hub to view past interviews, scores, and retake any interview.
- **📱 Fully Responsive** — Works seamlessly across desktop, tablet, and mobile devices.

---

## 🧩 How It Works

1. **Create an Interview** — The user specifies a role, seniority level, tech stack, and question focus (technical/behavioral). Gemini generates a list of relevant interview questions.
2. **Take the Interview** — A Vapi voice agent reads out the questions and conducts a live, two-way voice conversation with the user, just like a real interviewer.
3. **Get Feedback** — Once the interview ends, the full transcript is sent to an LLM, which generates a structured, category-wise performance evaluation along with strengths and areas for improvement.
4. **Track Progress** — All interviews and feedback are saved to the user's dashboard for future reference.

---

## 🛠️ Getting Started Locally

### Prerequisites
- [Node.js](https://nodejs.org/en)
- [npm](https://www.npmjs.com/)
- [Git](https://git-scm.com/)
- A [Firebase](https://firebase.google.com/) project (Auth + Firestore enabled)
- A [Vapi AI](https://vapi.ai/) account
- A Google Generative AI (Gemini) API key

### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/ai_mock_interviews.git
cd ai_mock_interviews
```

### 2. Install dependencies
```bash
npm install
```

### 3. Set up environment variables
Create a `.env.local` file in the project root:

```env
NEXT_PUBLIC_VAPI_WEB_TOKEN=
NEXT_PUBLIC_VAPI_WORKFLOW_ID=

GOOGLE_GENERATIVE_AI_API_KEY=

NEXT_PUBLIC_BASE_URL=

NEXT_PUBLIC_FIREBASE_API_KEY=
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=
NEXT_PUBLIC_FIREBASE_PROJECT_ID=
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=
NEXT_PUBLIC_FIREBASE_APP_ID=

FIREBASE_PROJECT_ID=
FIREBASE_CLIENT_EMAIL=
FIREBASE_PRIVATE_KEY=
```

### 4. Run the development server
```bash
npm run dev
```

Visit **http://localhost:3000** in your browser.

---

## 📂 Project Structure (high level)

```
ai_mock_interviews/
├── app/
│   ├── (auth)/             # Sign in / sign up pages
│   ├── (root)/             # Dashboard, interview, feedback pages
│   └── api/vapi/generate/  # Question generation API route
├── components/             # Reusable UI components
├── constants/              # Static mappings & dummy data
├── firebase/                # Firebase client/admin config
├── lib/
│   ├── actions/            # Server actions (feedback generation, etc.)
│   └── utils.ts
└── public/                 # Static assets, icons, images
```

---

## 🎯 What I Learned

- Integrating real-time voice AI agents (Vapi) into a web app
- Designing prompts for an LLM to generate structured, parseable output (JSON-formatted questions, multi-category scored feedback)
- Building authentication and data flows with Firebase
- Working with Next.js App Router, server actions, and TypeScript in a production-style codebase
- Component architecture and styling with Tailwind CSS + shadcn/ui

---

## 🙏 Acknowledgements

This project was built by following the tutorial by [JavaScript Mastery](https://www.youtube.com/@javascriptmastery/videos). It was completed as a personal learning project to gain hands-on experience with voice AI integration and modern full-stack development patterns.
