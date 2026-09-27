# FitBuddy — AI Fitness Plan Generator

Classy neon/corporate FastAPI college project.

## Features
- Responsive neon UI for mobile, laptop and desktop
- Profile form → AI workout plan → nutrition/recovery tip
- Feedback loop to revise the workout plan
- SQLite persistence
- Admin dashboard
- Gemini integration with safe local fallback when no API key is configured

## Run on Windows

```powershell
cd C:\Users\YOUR_NAME\Documents\fitbuddy
python -m pip install -r requirements.txt
python -m uvicorn app.main:app --reload
```

If PowerShell blocks activation, you can use the venv interpreter directly:
```powershell
venv\Scripts\python -m pip install -r requirements.txt
venv\Scripts\python -m uvicorn app.main:app --reload
```

Open http://127.0.0.1:8000

## Gemini
Copy `.env.example` to `.env` and add your Gemini API key. Without a key, FitBuddy still runs using its built-in fallback generator.

## Main routes
- `/` — user form
- `/generate-workout` — generate and save plan
- `/submit-feedback` — revise plan
- `/view-all-users` — admin dashboard
- `/health` — health check
