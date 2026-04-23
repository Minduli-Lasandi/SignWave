#  SignWave

> **An accessibility app for the deaf and hearing-impaired community — bridging the communication gap through ASL translations and captions.**

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)

---

##  About

SignWave is a cross-platform mobile application developed to improve media accessibility for the deaf and hearing-impaired. It translates various forms of input — text, audio, video, YouTube links, and documents — into **American Sign Language (ASL)** animations, helping bridge the communication gap between the hearing-impaired and the broader population.

🎬 [Demo Video](https://youtu.be/kYfOujJ-UBE)

---

##  Features

- 📝 Text to ASL  
- 🎙️ Audio to ASL  
- 🎬 Video to ASL  
- 📺 YouTube to ASL  
- 📄 Document (PDF) to ASL  
- 👤 User Profile & Settings  
---

##  Tech Stack

### Frontend
- **Flutter** (Dart) — Cross-platform mobile UI framework
- **Firebase** — Google Sign-In and Authentication

### Backend
- **Python + Flask** — RESTful API backend
- **AssemblyAI** — Speech-to-text conversion for audio/video inputs
- **SignMT API** — ASL translation engine (outputs `.pose` format)
- **youtube-transcript-api** — Extracts captions from YouTube videos
- **PyPDF / PDF libraries** — Text extraction from PDF documents

### Database & Hosting
- **MySQL** — User account storage (hosted on PythonAnywhere)
- **PythonAnywhere** — Backend hosting with Webhook-based CI/CD

### Dev Tools
- **Android Studio** & **VS Code** — IDEs
- **Figma** — UI/UX prototyping
- **GitHub Actions** — Continuous Integration (unit testing)
- **Git Webhooks** — Continuous Deployment to PythonAnywhere

---

## 🗂️ Project Structure

```
SDGP/
├── frontend/               # Flutter mobile app
│   ├── lib/
│   │   ├── screens/        # App screens (login, dashboard, translation pages, etc.)
│   │   └── widgets/        # Reusable UI components
│   ├── assets/images/
│   └── pubspec.yaml
│
└── signwave_api/           # Python Flask backend
    ├── app/                # Route handlers and business logic
    ├── assets/textToASL/   # ASL video assets
    ├── config.py
    ├── run.py
    └── requirements.txt
```

---

##  API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/sign-up` | Register a new user |
| POST | `/login` | Authenticate a registered user |
| GET | `/textToASL` | Submit text for ASL translation |
| GET | `/getASLVideo` | Retrieve text translation video |
| POST | `/audio-to-asl` | Upload audio file for translation |
| GET | `/download-translation-audio` | Download audio translation video |
| POST | `/upload-video` | Upload video file for translation |
| GET | `/download-translation-video` | Download video translation |
| POST | `/upload-youtube-url` | Submit YouTube URL for translation |
| GET | `/download-translation-youtube` | Download YouTube translation video |
| POST | `/document-to-asl` | Upload PDF document for translation |
| GET | `/download-translation-document` | Download document translation video |

---

##  How It Works

1. **Text/Document input** → Sent to backend → Processed via **SignMT API** → ASL animation video returned
2. **Audio input** → Uploaded to backend → Transcribed via **AssemblyAI** → Converted to ASL via SignMT → Video returned
3. **Video input** → Audio extracted → Transcribed → Converted to ASL → Video returned
4. **YouTube URL** → Captions extracted via `youtube-transcript-api` → Converted to ASL → Video returned

---

##  Getting Started

### Prerequisites

- Flutter SDK
- Python 3.x
- MySQL database
- PythonAnywhere account (or local server)
- API keys for AssemblyAI and SignMT

### Backend Setup

```bash
cd signwave_api
pip install -r requirements.txt
python run.py
```

Set up your environment variables / `config.py` with:
- Database credentials
- AssemblyAI API key
- SignMT API endpoint

### Frontend Setup

```bash
cd frontend
flutter pub get
flutter run
```

Update the API base URL in the frontend to point to your backend server.

---
## 👥 Authors

- G.W.H.A. Minduli Lasandi
- K.A. Romayle D.A. Dharmasena 
- D.A.D.M. Deshan 
- K.L.P. Hansaja
- Pathirage Chamuditha Hirushan 

**Supervisor:** Mr. Nipuna Senanayake  
**Module Leader:** Mr. Banuka Athuraliya

---
