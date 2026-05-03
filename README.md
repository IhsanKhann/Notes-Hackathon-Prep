# 🚢 CargoSense — Hackathon Repository

> **AI-powered shipment intelligence for Pakistani importers.**  
> Built with FastAPI · Gemini AI · Vertex AI · Google Cloud Run · Streamlit

---

## 👋 Welcome, Teammates!

This repository contains everything you need to get started — study guides, architecture diagrams, demo code, and individual role guides. Read this README carefully **before** opening anything else.

---

## 👥 Team & Roles

| Name | Role | Key Responsibility |
|------|------|--------------------|
| **Ihsan** | Repo Owner & Organizer | Repository setup, coordination |
| **Ehsan** | Integration Lead | FastAPI backend, Gemini AI agent, function calling |
| **Ali** | Cloud Infrastructure Lead | Docker, GCP, Cloud Run, CI/CD |
| **Tahreem** | Frontend Lead | Streamlit UI, user experience |

---

## 📁 Repository Contents — What's What

Here is a breakdown of every file in this repo and what it is for:

### 📄 Individual Role Guides (`.docx` files)
These are detailed, hour-by-hour guides for each team member. **Start with your own.**

| File | For Who | What's Inside |
|------|---------|---------------|
| `Ehsan_Part.docx` | Ehsan | FastAPI + Gemini agent setup, hackathon day plan |
| `Ali_Part.docx` | Ali | GCP setup, Dockerfile, GitHub Actions, deployment |
| `Tehreem_Part.docx` | Tahreem | Streamlit UI guide, frontend integration |
| `Overall_Flow_and_Plan.docx` | Everyone | Overall architecture, unified API contract, team plan |
| `hackathon_roadmap.docx` | Everyone | Timeline and milestones for hackathon day |

### 🌐 Study Notes (`.html` files)
These are reference notes in HTML format. **You must download them first** to view them properly — they will not render correctly in the GitHub browser preview.

| File | Topic |
|------|-------|
| `FastApi-Backend-Notes.html` | FastAPI backend concepts and patterns |
| `gemini_api_guide.html` | Gemini API — how to send messages, function calling, multi-turn chat |
| `vertex_ai_guide.html` | Vertex AI SDK — production-grade Gemini usage on GCP |
| `Phase_4-cloud-Notes.html` | Cloud infrastructure notes — Cloud Run, Secret Manager, Docker |

> **How to open HTML files:**  
> Download the file → open it with your browser (double-click or drag into Chrome/Firefox)

### 🗂️ Architecture Diagrams (`.drawio` files)
Visual diagrams made in [draw.io](https://app.diagrams.net). Open them at [app.diagrams.net](https://app.diagrams.net) — click **File → Open from → Device**.

| File | What it Shows |
|------|--------------|
| `AgenticAiPrep.drawio` | Python virtual environment setup, venv activation/deactivation workflow |
| `BackendAndCloud.drawio` | How the FastAPI backend and GCP Cloud infrastructure interact |

### 💻 Demo Code (`.zip` file)
| File | What's Inside |
|------|--------------|
| `Demo_agent_code.zip` | A working demo of the agent — extract and run locally |

---

## 🚀 Getting Started — Step by Step (For Complete Beginners)

### Step 1: Get the Repository on Your Machine

**Option A — Clone with Git (Recommended)**
```bash
git clone https://github.com/IhsanKhann/YOUR-REPO-NAME.git
cd YOUR-REPO-NAME
```

**Option B — Download as ZIP**
1. Click the green **`<> Code`** button on GitHub (top right of the file list)
2. Click **"Download ZIP"**
3. Extract the ZIP to a folder on your computer

---

### Step 2: Open the Diagrams (Get the Big Picture First)

1. Go to [app.diagrams.net](https://app.diagrams.net) in your browser
2. Click **File → Open from → Device**
3. Open `AgenticAiPrep.drawio` — this shows the environment setup workflow
4. Open `BackendAndCloud.drawio` — this shows how the full system connects

---

### Step 3: Read Your Role Guide

Open the `.docx` file for your role in Microsoft Word or Google Docs. Read it fully before writing any code.

- 📘 [YouTube: FastAPI Crash Course] (https://youtu.be/tLKKmouUams?si=eOW5XuLPbwBUCwzY)
- 📘 [YouTube: FastAPi Hindi Course] https://youtu.be/foGklduxhM0?si=9xL-XZjyxdsO1Ykz
- 📘 [YouTube: GCP course ] https://youtu.be/jpno8FSqpc8?si=cMwiJgkZ27NCvTw7
- cover only the following areas: 1:08:32 => 1:32:56, 1:38:01 => 3:00:02, 4:20:01 => 5:44:01
- 📘 [YouTube: Streamlit Tutorial] https://youtu.be/yKTEC1Y5bEQ?si=JY0VlJ-jjXao1pmk
- 📘 [Gemini API Python ] https://youtube.com/playlist?list=PLll2u-uqtmZO9EJ6FM0NnrQgJCUWrhytg&si=jdu4vI_dwR2QbyR-
- 📘 [Vertex AI Python ] https://youtu.be/bPtKnDIVEsg?si=jbUxKicZUxFXUZ9y

---

### Step 4: Extract and Run the Demo Code

This gets the demo project running on your local machine so you can see what the finished product looks like.

#### 4.1 — Extract the ZIP
1. Right-click `Demo_agent_code.zip` → **Extract All** (Windows) or double-click (Mac)
2. After extraction you will see a folder called `app/`
3. Navigate into it:
```bash
cd app
```

#### 4.2 — Set Up the Python Virtual Environment

> ⚠️ Always do this from the **root of the `app/` folder** — where `requirements.txt` lives.

```bash
# Create the virtual environment
python -m venv venv
```

**Activate the virtual environment:**

| OS | Command |
|----|---------|
| Windows (CMD) | `venv\Scripts\activate` |
| Windows (PowerShell) | `venv\Scripts\Activate.ps1` |
| Mac / Linux | `source venv/bin/activate` |

You will know it worked when you see `(venv)` at the start of your terminal line.

#### 4.3 — Install Dependencies

```bash
pip install -r requirements.txt
```

> If you later add a new package with `pip install something`, always run this after to save it:
> ```bash
> pip freeze > requirements.txt
> ```

#### 4.4 — Set Up Environment Variables

Create a `.env` file in the `app/` folder (copy the `.env.example` if it exists):

```
GEMINI_API_KEY=your_key_here
NEWS_API_KEY=your_key_here
EXCHANGE_RATE_API_KEY=your_key_here
GOOGLE_CLOUD_PROJECT=your_gcp_project_id
VERTEX_LOCATION=us-central1
```

> **Where to get API keys:**
> - Gemini API Key → [aistudio.google.com](https://aistudio.google.com) ← *Ask Ehsan*
> - NewsAPI Key → [newsapi.org](https://newsapi.org) ← *Ask Ehsan*
> - GCP Project ID → [console.cloud.google.com](https://console.cloud.google.com) ← *Ask Ali*

---

### Step 5: Run the App (Two Terminals Required)

You need **two separate terminal windows** open at the same time.

#### Terminal 1 — Backend (FastAPI)
```bash
# Make sure venv is activated first!
cd app
uvicorn main:app --reload --port 8000
```
✅ Done when you see: `Uvicorn running on http://127.0.0.1:8000`

#### Terminal 2 — Frontend (Streamlit)
```bash
# Make sure venv is activated here too!
cd app
streamlit run streamlit_app.py
```
✅ Done when your browser opens automatically at `http://localhost:8501`

> If the browser does not open automatically, go to `http://localhost:8501` manually.

---

## 🧪 Quick Test — Is Everything Working?

Once both terminals are running, open a new terminal and run:

```bash
curl -X POST http://localhost:8000/chat \
  -H "Content-Type: application/json" \
  -d '{"message": "What is the risk of shipping through Hormuz?"}'
```

You should get a JSON response back with a risk analysis. If you do — everything is working! 🎉

---

## 🗺️ Overall Architecture

```
User (Browser)
      │
      ▼
Streamlit UI (Port 8501)
      │  HTTP POST /chat
      ▼
FastAPI Backend (Port 8000)
      │
      ▼
Gemini AI Agent (Vertex AI)
      │
   ┌──┴──────────────────┐
   ▼          ▼           ▼
news_tool  duty_tool  route_tool
(NewsAPI)  (HS Codes)  (Routes)
```

In production, the FastAPI backend runs on **Google Cloud Run** (deployed by Ali), and all API keys are stored securely in **GCP Secret Manager**.

---

## ⚠️ Common Problems & Fixes

| Problem | Fix |
|---------|-----|
| `ModuleNotFoundError` | Virtual environment is not activated — run `source venv/bin/activate` |
| `uvicorn: command not found` | Run `pip install -r requirements.txt` again |
| `.env not found` or missing key errors | Create your `.env` file as shown in Step 4.4 |
| Streamlit does not connect to backend | Make sure Terminal 1 (backend) is running first |
| HTML files show raw code in GitHub | Download the file, then open locally in your browser |
| `.drawio` file opens as XML | Open at [app.diagrams.net](https://app.diagrams.net) instead |

---

## 📬 Team Communication

> 📱 Primary communication: **WhatsApp group**  
> 🐛 If stuck: Post your **error message + what you already tried** — do not wait more than 20 minutes before asking!

---

## 📅 Hackathon Day Cheatsheet

| Hour | Ehsan | Ali | Tahreem |
|------|-------|-----|---------|
| 0–1 | Set up agent.py + Vertex AI | Verify GCP + build Dockerfile | Set up Streamlit skeleton |
| 1–2 | Write /chat endpoint | Push image to Artifact Registry | Connect UI to /chat endpoint |
| 2–4 | Build all 3 tools (news, duty, route) | Deploy to Cloud Run | Polish UI, add loading states |
| 4–5 | Integration sync | Wire secrets in Secret Manager | Full end-to-end test |
| 5–7 | Polish system prompt | Set up GitHub Actions | Demo run-throughs |
| 7–8 | Rehearse technical talking points | Prepare GCP Console for judges | Rehearse demo flow |

---

*CargoSense Hackathon · May 2026 · Built with ❤️ in Pakistan*
