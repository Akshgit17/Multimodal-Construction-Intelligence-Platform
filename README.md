# Multimodal Construction Intelligence Platform 🏗️
### Skill Wallet Capstone Project 1 • AI-Powered Decision Support System

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io)
[![Python 3.8+](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Google Gemini AI](https://img.shields.io/badge/Google%20Gemini-3.5%20Flash%20%7C%20Flash--Lite-orange.svg)](https://aistudio.google.com/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.115%2B-009688.svg)](https://fastapi.tiangolo.com/)
[![React](https://img.shields.io/badge/React-19.0-61DAFB.svg)](https://react.dev/)
[![Tailwind CSS](https://img.shields.io/badge/TailwindCSS-3.4-38B2AC.svg)](https://tailwindcss.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

An enterprise-grade, multimodal decision-support system designed to assist construction project managers, site superintendents, QA/QC engineers, and safety auditors across site safety auditing, structural crack diagnostics, project financial estimation, and real-time site weather advisory.

Powered by **Google Gemini Multimodal AI** (`gemini-3.5-flash-lite`, `gemini-3.5-flash`, `gemini-flash-latest`), with **Pollinations AI** 3D architectural visualization, benchmarked against **OSHA 1926** and Indian Standard **IS 456:2000 / NBC 2016** codes, and equipped with a **Dynamic Computer-Vision Telemetry Engine** that analyzes real image pixels (luminance, directional edge energy, and fluorescent PPE spectrums) with zero external database dependencies.

---

## 🌟 Supported Deployment Architectures

This repository supports **two full production experiences**:
1. **Streamlit Cloud Deployment (`streamlit_app.py`):** Zero-configuration, zero-database, 1-click cloud deployable on [Streamlit Community Cloud](https://share.streamlit.io).
2. **Modern Full-Stack Architecture:** Decoupled **React 19 + Vite + Tailwind CSS** frontend communicating with a high-performance **FastAPI (Python)** backend via strict JSON contracts.

---

## ⚠️ Mandatory Preliminary Engineering Disclaimer

> **PRELIMINARY AI ASSESSMENT ONLY:** All computer-vision and LLM evaluations produced by this platform are automated preliminary assessments based on visible 2D pixels and user inputs. They cannot detect subsurface stress, soil subsidence, internal rebar corrosion, or concealed structural flaws. This application does not replace mandatory physical audits by licensed structural engineers or certified safety officers (**OSHA 1926 / IS 456 / NBC**).

---

## 🚀 How to Deploy Live to the Web

### Method 1: Streamlit Community Cloud (Recommended • 100% Free • 2 Minutes)

Streamlit Community Cloud is the fastest way to make this application live with a public URL:

1. **Push your code to GitHub**:
   ```bash
   git add .
   git commit -m "Deploy Multimodal Construction Intelligence Platform"
   git push origin main
   ```
2. **Open Streamlit Community Cloud**:
   - Go to [share.streamlit.io](https://share.streamlit.io/) and log in with your GitHub account.
3. **Create New App**:
   - Click **"Create app"** ➔ **"Yup, I have an app"**.
   - **Repository:** Select your repository (e.g. `your-username/Multimodal-Construction-Intelligence-Platform`).
   - **Branch:** `main`
   - **Main file path:** `streamlit_app.py`
4. **Configure Secrets (for Live Gemini AI Inference)**:
   - Click **"Advanced settings..."** ➔ Open **"Secrets"**.
   - Paste the following TOML configuration:
     ```toml
     GEMINI_API_KEY = "your_google_gemini_api_key_here"
     AI_MODEL = "gemini-3.5-flash-lite"
     ```
     *(Get your free API key at [Google AI Studio](https://aistudio.google.com/)).*
5. **Deploy**:
   - Click **"Deploy!"**.
   - Your application will be live in 60 seconds with a shareable HTTPS URL!

> *Note: If no API key is supplied, the platform runs in **Dynamic Computer-Vision Mode**, extracting genuine pixel telemetry from any uploaded image.*

---

### Method 2: Deploying Full-Stack (FastAPI Backend + React Frontend)

#### Backend on Render / Railway:
1. Connect your GitHub repo to [Render](https://render.com) or [Railway](https://railway.app).
2. Root directory: `backend`
3. Build command: `pip install -r requirements.txt`
4. Start command: `uvicorn main:app --host 0.0.0.0 --port $PORT`
5. Environment Variables:
   - `GEMINI_API_KEY`: Your Gemini API key
   - `AI_MODEL`: `gemini-3.5-flash-lite`

#### Frontend on Vercel:
1. Connect your repo to [Vercel](https://vercel.com).
2. Root directory: `frontend`
3. Framework preset: **Vite**
4. Build command: `npm run build`
5. Output directory: `dist`
6. Add environment variable `VITE_BACKEND_URL` pointing to your deployed backend URL.

---

## 💻 Local Windows Installation & Run Guide

### Prerequisites
- **Python 3.8+** (Tested on Python 3.10, 3.11, and 3.12)
- **Node.js v18+** & **npm** *(only required if running the React + Vite frontend)*
- **Git**

---

### Option 1: Running the Streamlit Platform (Easiest)

#### Step 1: Install Python Requirements
Open PowerShell in the project directory:
```powershell
python -m pip install -r requirements.txt
```

#### Step 2: Set your Gemini API Key
Create or edit `.env` in the project root:
```ini
AI_PROVIDER=gemini
AI_MODEL=gemini-3.5-flash-lite
GEMINI_API_KEY=your_gemini_api_key_here
PORT=8000
```
*(You can also securely type your key directly into the application's sidebar at runtime).*

#### Step 3: Launch Streamlit
Double-click `run_streamlit.bat` or run:
```powershell
python -m streamlit run streamlit_app.py
```
👉 The platform will automatically open in your browser at: **`http://localhost:8501`**

---

### Option 2: Running the React + FastAPI Full-Stack App

#### Step 1: Start Backend (FastAPI)
Double-click `run_backend.bat` or run:
```powershell
cd backend
python -m pip install -r requirements.txt
python -m uvicorn main:app --host 127.0.0.1 --port 8000 --reload
```
- API Docs & Swagger UI: **`http://127.0.0.1:8000/docs`**

#### Step 2: Start Frontend (React + Vite)
In a new terminal window, double-click `run_frontend.bat` or run:
```powershell
cd frontend
npm install
npm run dev
```
- Web Application: **`http://localhost:5173`**

#### Or use the 1-Click Starter:
Double-click `start_platform.bat` to launch both backend and frontend servers simultaneously!

---

## 📸 Verified Sample Images for Testing

You can paste these direct image URLs into the app or download them to test both modules:

### 🦺 Module 1: Construction Site Safety & PPE Audit
| Image Description | Direct Image URL | What It Evaluates |
| :--- | :--- | :--- |
| **Active Jobsite Crew** | `https://images.unsplash.com/photo-1504307651254-35680f356dfd?auto=format&fit=crop&w=1200&q=80` | Multi-worker PPE detection (helmets, high-vis vests, boots, machinery safety buffer) |
| **Worker with Vest & Hard Hat** | `https://images.unsplash.com/photo-1589939705384-5185137a7f0f?auto=format&fit=crop&w=1200&q=80` | High-vis Class-2 contrast evaluation and ANSI hard hat compliance |
| **High-Rise Facade Scaffolding** | `https://images.unsplash.com/photo-1578575437130-527eed3abbec?auto=format&fit=crop&w=1200&q=80` | Elevation fall protection, scaffold guardrails & toe-boards under OSHA 1926.451 / IS 3696 |
| **Structural Steel Ironworkers** | `https://images.unsplash.com/photo-1517581177682-a085bb7ffb15?auto=format&fit=crop&w=1200&q=80` | Ironworkers at height, fall arrest lifelines, and harness tie-off compliance |

### 🔍 Module 2: Crack Diagnostics & Structural Integrity
| Defect Classification | Direct Image URL | What It Evaluates |
| :--- | :--- | :--- |
| **Severe Diagonal Shear Crack** | `https://images.unsplash.com/photo-1590381105924-c72589b9ef3f?auto=format&fit=crop&w=1200&q=80` | Diagonal ~45° shear fracture, crack width > 0.3mm, epoxy injection & CFRP wrap |
| **Deep Concrete Surface Fracture** | `https://images.unsplash.com/photo-1518709268805-4e9042af9f23?auto=format&fit=crop&w=1200&q=80` | Severe concrete flaking, rebar spalling risk, and PMM micro-concrete repairs |
| **Masonry Settlement Damage** | `https://images.unsplash.com/photo-1513694203232-719a280e022f?auto=format&fit=crop&w=1200&q=80` | Stepped masonry fracture, differential settlement, helical stainless-steel stitching |
| **Hairline Shrinkage Fissures** | `https://images.unsplash.com/photo-1563298723-dcfebaa392e3?auto=format&fit=crop&w=1200&q=80` | Sub-0.3mm non-structural plastic shrinkage cracks, elastomeric seal, and moist curing |

---

## 🏗️ Core Modules & Feature Breakdown

### 🦺 Module 1: Construction Site Safety & PPE Audit (Epic 2)
- **Multimodal Visual Inspection:** Accepts site photos (JPG/PNG/WebP) and passes them to Gemini Vision models with structured prompt engineering.
- **Dynamic Vision Fallback:** If offline or without an API key, calculates quantitative luminance, spatial edge energy, and fluorescent PPE spectral percentages to generate dynamic safety evaluations.
- **Safety Benchmarking:** Assesses compliance against **OSHA 1926** and Indian Standard **IS 456 / IS 3696**.
- **PPE Matrix:** Evaluates hard hats (ANSI Z89.1 / IS 2925), high-visibility reflective apparel, steel-toe boots, and fall protection harnesses at elevation.
- **Hazard Scoring:** Highlights elevated scaffolding drop-offs, trailing electrical cables, and missing guardrails with severity rankings (`Low`, `Medium`, `High`, `Critical`) and corrective engineering remedies.
- **Reporting:** 1-click downloadable JSON audit documents for site safety logs.

### 🔍 Module 2: Crack Diagnostics & Structural Integrity (Epic 2)
- **Forensic Defect Classification:** Identifies defect morphology:
  - *Hairline Plastic Shrinkage* (<0.3 mm non-structural drying)
  - *Differential Foundation Settlement* (subgrade consolidation)
  - *Structural Shear Fractures* (45° principal tensile stress)
  - *Concrete Spalling & Delamination* (rebar oxidation & rust expansion)
  - *Flexural Tension Cracks* (tensile face live-load overstressing)
- **Crack Width Estimation:** Computes surface crack opening in millimeters against allowable crack thresholds (0.30 mm under IS 456 / ACI 224R).
- **Engineering Remedies:** Recommends ASTM C881 low-viscosity epoxy pressure injection, polyurethane water-stop grouting, or carbon-fiber reinforced polymer (CFRP) composite jackets.

### 📊 Module 3: Project Planning & Real Estate Valuation (Epic 3)
- **Dynamic Parameter Inputs:** Structure type (High-Rise, Commercial IT Complex, Industrial PEB, Villa), built-up area (Sq.Ft.), location tier (Tier 1 Metro, Tier 2 City, Tier 3), and milestone completion slider (0–100%).
- **Financial Analytics:**
  - Total project budget in INR (₹ Lakhs & Crores)
  - Capital expenditure incurred to date
  - Monthly cash-flow burn rate
  - Market asset valuation based on location tier premiums and completed milestones
- **Raw Material Forecasting (BoQ):**
  - Grade 53/43 Cement (50kg bags & metric tonnes)
  - TMT Reinforcing Steel (Fe 500D in metric tonnes)
  - Graded Coarse & Fine Aggregates (CFT)
  - Batching & Curing Water Requirements (kL)
- **Critical Path Method (CPM) Schedule:** Phased timeline breakdown (Substructure, RCC Frames, MEP & Glazing, Handover).
- **3D Architectural Rendering:** Integrates **Pollinations AI** to dynamically synthesize photorealistic 3D conceptual architectural renderings based on selected structural parameters.

### 💬 Module 4: Daily Site Assistant & Weather-Aware Advisory (Epic 5)
- **Real-Time Weather Sliders:** Adjust temperature (°C), wind gusts (km/h), rainfall (mm/h), and humidity (%).
- **Dynamic Weather Safety Protocols:**
  - *High Wind (> 45 km/h):* Mandatory OSHA 1926.1431 suspension of tower crane hoisting, jib weathervaning, and evacuation of high scaffolds.
  - *Heavy Monsoon Rain:* Foundation excavation shoring checks, immediate halting of exterior concrete pours, and IP65/GFCI electrical de-energization.
  - *Extreme Heat (> 38°C):* Hot weather concreting protocols (ACI 305R), chilled batch water, double wet burlap moist curing, and OSHA worker hydration cycles.
  - *Normal Weather:* Standard daily QA/QC checklists and morning 5-minute Toolbox Talks.
- **Conversational Decision Support:** Multi-turn interactive chatbot powered by Gemini 3.5 Flash (with offline fallback covering IS 456, OSHA, curing timelines, slump tolerances, and rebar lap rules).

---

## 📁 Repository Structure

```
Multimodal-Construction-Intelligence-Platform/
├── .streamlit/
│   ├── config.toml           # Sleek dark theme tokens for Streamlit
│   └── secrets.toml.example  # Template for Streamlit Cloud secrets
├── backend/
│   ├── .env.example          # Template environment file
│   ├── requirements.txt      # FastAPI, uvicorn, requests dependencies
│   ├── main.py               # FastAPI REST endpoints & health check
│   ├── gemini_service.py     # Gemini Multimodal API client & model sequence
│   └── mock_data.py          # Dynamic vision analysis & reference data
├── frontend/
│   ├── package.json          # React 19, Vite, Tailwind dependencies
│   ├── vite.config.js        # Vite config with backend proxy
│   ├── tailwind.config.js    # Tailwind CSS configuration
│   └── src/
│       ├── App.jsx           # Main React component
│       └── components/       # UI components for all 4 modules
├── app.py                    # Top-level gateway forwarder
├── streamlit_app.py          # Complete standalone Streamlit Application
├── requirements.txt          # Root Python dependencies for Streamlit Cloud
├── run_streamlit.bat         # 1-Click Streamlit runner for Windows
├── run_backend.bat           # 1-Click FastAPI runner for Windows
├── run_frontend.bat          # 1-Click React frontend runner for Windows
├── start_platform.bat        # 1-Click starter for full-stack mode
├── .gitignore                # Protects secrets & node_modules
└── README.md                 # Complete platform documentation
```

---

## 🔌 API Endpoints (FastAPI Backend)

| Method | Endpoint | Description | Request Format |
|---|---|---|---|
| `GET` | `/api/health` | Health & mode check | None |
| `POST` | `/api/safety-analysis` | Site safety & PPE audit | `multipart/form-data` (`file`) |
| `POST` | `/api/crack-analysis` | Wall & concrete crack forensics | `multipart/form-data` (`file`) |
| `POST` | `/api/project-planning` | Phased schedule & BoQ estimation | JSON (`project_type`, `budget`, `duration_months`, `location`) |
| `POST` | `/api/assistant` | Technical engineering advisory | JSON (`message`, `context`) |

---

## 🛠️ Tech Stack & Dependencies

- **Frontend (Streamlit):** Python Streamlit, Altair, Pillow
- **Frontend (Full-Stack):** React 19, Vite, JavaScript, Tailwind CSS, Lucide Icons
- **Backend:** FastAPI, Uvicorn, Python-dotenv, Requests, Httpx
- **Generative AI:** Google Gemini Multimodal Flash REST API (`gemini-3.5-flash-lite`, `gemini-3.5-flash`, `gemini-flash-latest`)
- **Architectural 3D Engine:** Pollinations AI Generative Vision API
- **Codes & Standards:** OSHA 1926, IS 456:2000, IS 3696, NBC 2016, ACI 224R / 305R

---

## 📄 License
This project is developed as part of the **Skill Wallet Capstone Project** and is licensed under the MIT License.
