# StudyOne — Student Learning & Productivity OS

StudyOne is a modern student learning platform: **Study smarter. Build momentum. Every single day.**

## Quick Fix for PowerShell script execution error

If you see `npm : File ... npm.ps1 cannot be loaded because running scripts is disabled on this system`, run this command in PowerShell:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```

Or run `npm` via CMD:
```cmd
cmd /c npm install
cmd /c npm run dev
```

---

## Features

- **Landing Page**: Modern hero section, features, course showcase, notes generator highlight, testmonial, FAQ.
- **Smart Study Notes Generator**: Client-side generator producing full structured revision notes (Definition, Key Concepts, Example, Viva, Exam questions) without external AI API dependency.
- **Interactive Courses & Curriculum**: Real-time topic checklists with progress tracking.
- **Coding Practice Workspace**: Problem lists, difficulty filters, and interactive code runner simulator.
- **Interactive Quiz Engine**: MCQ questions, countdown timer, navigator, instant scoring, score history.
- **Tasks & Timeline Planner**: Priority filtering (High/Med/Low), due dates, and study session calendar.
- **Pomodoro Focus Timer**: Focus (25m), Short Break (5m), Long Break (15m) with session counters and time accumulator.
- **Progress & Gamification**: Level & XP progress, streak counter, trophy achievements, leaderboard.
- **Authentication**: JWT + bcrypt + Express backend with automatic LocalStorage fallback mode if database is offline.

---

## Running the Application

### 1. Frontend Web App

```bash
# Set PowerShell policy for current window if needed
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass

npm install
npm run dev
```

### 2. Backend Server (Optional - MySQL)

```bash
# Run Express backend server on port 5000
npm run start:server
```

To connect to a live MySQL instance, update [.env](./.env) with your MySQL credentials (`DB_USER`, `DB_PASSWORD`, `DB_NAME`) and import [server/schema.sql](./server/schema.sql).
If MySQL is not configured, the frontend seamlessly operates in LocalStorage fallback mode.
