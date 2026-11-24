# Zyro — Cross-Platform AI Voice Agent (Mobile & PC)

Zyro is a full-stack **Progressive Web App (PWA)** + **FastAPI** AI voice assistant that runs natively on **Windows, macOS, Linux, Android, and iOS** without needing separate native codebases.

## Features
- **Hands-Free Voice Loop:** Real-time Speech-to-Text (STT) + Text-to-Speech (TTS) with optional Auto-Listen mode.
- **Mobile & PC Adaptive UI:** Installable as an app on Android/iOS ("Add to Home Screen") and Desktop Chrome/Edge; supports **Spacebar** push-to-talk on PC.
- **Live Audio Visualizer:** Dynamic reactive orb powered by Web Audio API.
- **Flexible AI Brain:** Supports **Google Gemini (`gemini-2.5-flash`)**, **OpenAI (`gpt-4o-mini`)**, and includes a **built-in offline/local smart fallback** so it works immediately out of the box.

## Quick Start (Local PC & Mobile Testing)
1. **Install Python dependencies:**
   ```bash
   cd backend
   pip install -r requirements.txt
   ```
2. **Configure API Key (Optional):**
   ```bash
   cp ../.env.example ../.env
   # Add GEMINI_API_KEY or OPENAI_API_KEY inside .env
   ```
3. **Run Zyro:**
   ```bash
   uvicorn server:app --host 0.0.0.0 --port 8000
   ```
4. **Open on PC & Mobile:**
   - **PC:** Visit `http://localhost:8000`
   - **Mobile (same Wi-Fi):** Visit `http://<YOUR_PC_LOCAL_IP>:8000` (Note: Mobile browsers require HTTPS for microphone access over LAN; deploy to Render/Railway/Vercel or use `ngrok http 8000` for instant HTTPS on mobile).
