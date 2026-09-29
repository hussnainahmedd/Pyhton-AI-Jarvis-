<div align="center">

# 🤖 Python AI Jarvis

### _"Good evening, sir. What shall we work on today?"_

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Google Gemini](https://img.shields.io/badge/Google%20Gemini-Live%20API-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://ai.google.dev/)
[![PyQt6](https://img.shields.io/badge/PyQt6-41CD52?style=for-the-badge&logo=qt&logoColor=white)](https://pypi.org/project/PyQt6/)
[![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge&logo=playwright&logoColor=white)](https://playwright.dev/)

</div>

---

A voice-first desktop AI assistant powered by **Google Gemini's Live API**. It can hear you, see your screen and webcam, remember context across sessions, and actually *do things* on your computer — opening apps, automating the browser, searching the web, managing files — through 17 action modules and an autonomous agent mode. I set this up and customized it as my own always-on desktop companion.

## ✨ Features

- **Real-time voice conversation** — Gemini Live API with 16kHz mic input / 24kHz speaker output via `sounddevice`
- **Visual awareness** — screen capture and webcam analysis ("what's on my screen?")
- **Full computer control** — open any app, mouse/keyboard automation (`PyAutoGUI`), system settings (volume, brightness, WiFi, dark mode)
- **Browser automation** — navigate, click, type and fill forms across Chrome, Edge, Firefox and more (`Playwright`)
- **Web search & media** — DuckDuckGo search, YouTube playback/summaries, weather reports, flight search
- **Productivity tools** — reminders, WhatsApp/Telegram messaging automation, PDF/code/image analysis, Steam/Epic game updates
- **Autonomous agent mode** — multi-step planning (`planner`) → execution (`executor`) → intelligent error recovery → task queue
- **Persistent memory** — JSON-backed long-term memory of your identity, preferences and projects, auto-trimmed and injected into every prompt
- **PyQt6 desktop UI** — dark Iron-Man-inspired theme with chat view, voice controls and drag-and-drop file uploads

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| AI engine | Google Gemini Live API (`gemini-2.5-flash-native-audio-preview`) |
| Desktop UI | PyQt6 |
| Audio | `sounddevice` (16kHz in / 24kHz out) |
| Browser automation | `playwright` |
| OS automation | `pyautogui`, `pygetwindow`, `psutil` |
| Vision | `mss`, `opencv-python`, `pillow` |
| Search | `duckduckgo-search`, `beautifulsoup4`, `requests` |
| Memory | JSON persistence with thread-safe manager |

## 🚀 Run it

```bash
# 1. Clone
git clone https://github.com/hussnainahmedd/Pyhton-AI-Jarvis-.git
cd Pyhton-AI-Jarvis-/python

# 2. Automated setup (installs requirements.txt + Playwright browsers)
python setup.py

# 3. Add your free Gemini API key
#    Create config/api_keys.json:
#    { "gemini_api_key": "YOUR_GEMINI_API_KEY_HERE" }
#    Get one free at https://aistudio.google.com/apikey

# 4. Launch Jarvis
python main.py
```

> [!NOTE]
> Works best on **Windows 10/11** — several modules (`comtypes`, `pycaw`, `win10toast`, `pywinauto`) are Windows-only. You also need a working microphone for voice mode. `setup.py` runs `pip install -r requirements.txt` and `playwright install` for you.

## ⚡ Action Modules

| Module | What it does |
|---|---|
| `open_app` | Launch any application by name |
| `browser_control` | Full browser automation — navigate, click, type, forms |
| `computer_control` | Low-level mouse/keyboard automation |
| `computer_settings` | Volume, brightness, WiFi, dark mode, power controls |
| `desktop` | Wallpaper, desktop files and window management |
| `web_search` | DuckDuckGo-powered web search |
| `youtube_video` | Play, summarize and fetch info on YouTube videos |
| `screen_processor` | Screen + webcam vision via Gemini |
| `file_controller` / `file_processor` | File CRUD, search, PDF/code/image analysis |
| `send_message` | WhatsApp/Telegram messaging automation |
| `reminder` | Scheduled reminders |
| `weather_report` | Real-time weather by city |
| `flight_finder` | Search and compare flight deals |
| `game_updater` | Steam/Epic Games update manager |
| `dev_agent` / `code_helper` | AI code generation, analysis and debugging |

## 🖼️ Preview

![Python AI Jarvis preview](assets/hero.webp)

## 🙏 Credits

Built on top of the open-source [MARK XXXIX project by FatihMakes](https://www.youtube.com/@FatihMakes) — customized and extended as my own desktop assistant.

---

<div align="center">

Built by [Hussnain Ahmad](https://github.com/hussnainahmedd) — a CS undergrad learning by building.

</div>
