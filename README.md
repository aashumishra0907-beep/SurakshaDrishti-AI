<div align="center">

# 🛡️ SURAKSHADRISHTI AI

### AI/ML-Based Railway Crowd and Safety Monitoring System

**Transforming Traditional Railway CCTV into Intelligent Safety Monitoring**

<br>

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge\&logo=python\&logoColor=white)
![React](https://img.shields.io/badge/React-Frontend-61DAFB?style=for-the-badge\&logo=react\&logoColor=black)
![FastAPI](https://img.shields.io/badge/FastAPI-Backend-009688?style=for-the-badge\&logo=fastapi)
![YOLOv8](https://img.shields.io/badge/YOLOv8-AI%20Detection-orange?style=for-the-badge)
![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-5C3EE8?style=for-the-badge\&logo=opencv)
![SQLite](https://img.shields.io/badge/SQLite-Database-003B57?style=for-the-badge\&logo=sqlite)

<br>

**🤖 Artificial Intelligence | 👥 Crowd Monitoring | 🚨 Incident Detection | 📊 Analytics**

<br>

[Overview](#-project-overview) •
[Features](#-key-features) •
[Architecture](#-system-architecture) •
[Installation](#-installation-guide) •
[Team](#-team-trinetra)

<br>

**Repository:** [SurakshaDrishti-AI](https://github.com/aashumishra0907-beep/SurakshaDrishti-AI)

</div>

---

# 📌 1. Project Overview

**SurakshaDrishti AI** is an Artificial Intelligence and Machine Learning-based railway safety monitoring platform developed to improve railway crowd observation, incident awareness and emergency response coordination.

The project integrates Computer Vision, YOLOv8-based person detection, video processing, tracking, event analysis and a centralized web dashboard.

It is designed to process camera feeds, identify relevant monitoring events and provide operators with a centralized interface for observing railway environments.

The platform combines AI-powered monitoring with incident management capabilities, including:

* Live camera monitoring.
* AI-based person detection.
* Person tracking.
* Crowd density monitoring.
* Restricted-zone intrusion monitoring.
* Loitering detection.
* Suspicious-event awareness.
* Fall-detection prototype.
* Real-time alert management.
* SOS emergency reporting.
* Evidence and incident management.
* Authority response workflow.
* Safety analytics and reporting.

The project explores how existing railway CCTV infrastructure can be enhanced with an intelligent monitoring layer.

### 🎯 Project Mission

> To develop an AI-assisted railway safety platform that supports faster incident awareness, intelligent crowd monitoring and organized emergency response.

---

# 🚨 2. Problem Statement

Railway stations are highly dynamic public environments where thousands of passengers move through platforms, entrances, waiting areas and other public spaces.

Traditional CCTV surveillance primarily depends on human operators continuously observing multiple camera feeds.

This creates several challenges:

* Monitoring multiple cameras simultaneously is difficult.
* Crowd congestion may not be identified immediately.
* Unusual events can be overlooked.
* Incident information may be scattered across different systems.
* Emergency reporting and response coordination can be delayed.
* Reviewing historical incidents can require significant manual effort.

### 💡 Proposed Solution

SurakshaDrishti AI introduces an AI-assisted monitoring architecture that processes camera feeds and organizes relevant monitoring information through a centralized dashboard.

The system aims to:

1. Detect people in supported video streams.
2. Track detected people across frames.
3. Analyze crowd activity.
4. Monitor configured restricted areas.
5. Generate alerts for configured event conditions.
6. Store incident information.
7. Support SOS reporting.
8. Provide incident tracking and reporting.

---

# ✨ 3. Key Features

## 🤖 3.1 AI-Based Person Detection

The AI detection module uses YOLOv8 and OpenCV to process video frames.

**Capabilities:**

* Person detection.
* Bounding-box visualization.
* Frame processing.
* Detection confidence information where available.
* Integration with tracking and event-processing modules.

## 👥 3.2 Intelligent Crowd Monitoring

The crowd monitoring module analyzes detected persons within a camera view.

**Capabilities:**

* Person-count estimation.
* Crowd activity observation.
* Configurable crowd thresholds.
* Crowd-level classification.
* Identification of potentially congested areas.

Example crowd classifications:

| Crowd Level | Description                        |
| ----------- | ---------------------------------- |
| NORMAL      | Regular activity                   |
| MODERATE    | Increasing activity                |
| HIGH        | High crowd concentration           |
| CRITICAL    | Requires immediate operator review |

Actual thresholds depend on the configured monitoring environment.

## 🎯 3.3 Person Tracking

The tracking module supports monitoring detected persons across video frames.

**Capabilities:**

* Temporary tracking IDs.
* Frame-to-frame tracking.
* Movement observation.
* Tracking information for event analysis.

Tracking information can support crowd analysis, zone monitoring and time-based presence rules.

## 🚧 3.4 Intrusion Detection

The intrusion monitoring module is designed to identify people entering configured restricted areas.

**Capabilities:**

* Restricted-zone monitoring.
* Zone-based event generation.
* Camera-specific monitoring conditions.
* Incident alert integration.

## ⏱️ 3.5 Loitering Detection

The loitering module evaluates prolonged presence using configured time-based conditions.

**Capabilities:**

* Presence-duration monitoring.
* Configurable time thresholds.
* Event generation.
* Alert integration.

## 🚨 3.6 Suspicious-Event Monitoring

The event engine organizes potentially unusual monitoring conditions into reviewable events.

Possible event categories include:

* Intrusion.
* Loitering.
* Crowd alert.
* Suspected fall.
* Other configured monitoring events.

AI-generated events must always be reviewed by authorized personnel.

## 🆘 3.7 SOS Emergency Reporting

The SOS module provides an emergency reporting interface.

**Capabilities:**

* Emergency report submission.
* Incident information management.
* Location information.
* Emergency status tracking.
* Authority assignment workflow.

## 📢 3.8 Real-Time Alert Management

The alert system provides a centralized interface for monitoring generated events.

**Capabilities:**

* Alert visualization.
* Event categorization.
* Severity classification.
* Incident status tracking.
* Alert history.
* Operator review.

## 📁 3.9 Evidence Management

The system includes an evidence-management workflow for organizing information associated with monitoring events.

Possible evidence metadata includes:

* Event ID.
* Camera ID.
* Event category.
* Timestamp.
* Location.
* Severity.
* Evidence reference.
* Incident status.

## 👮 3.10 Authority Response Workflow

The application provides a structured incident-response workflow.

```text
       EVENT DETECTED
             |
             v
          PENDING
             |
             v
          ASSIGNED
             |
             v
        ACKNOWLEDGED
             |
             v
         RESPONDING
             |
             v
          RESOLVED
```

This workflow supports organized incident tracking and operator coordination.

## 📊 3.11 Analytics Dashboard

The analytics module provides access to monitoring and incident information.

**Capabilities:**

* Event statistics.
* Incident summaries.
* Historical information.
* Monitoring activity visualization.
* Safety analytics.

## 📄 3.12 Reports and Data Export

The reporting module supports exporting available event information.

Supported formats:

* JSON.
* CSV.

Reports can be used for reviewing historical monitoring information.

---

# 🖥️ 4. Application Modules

| Module              | Responsibility                         |
| ------------------- | -------------------------------------- |
| AI Engine           | Computer vision and person detection   |
| Tracking Engine     | Tracking detected persons              |
| Crowd Engine        | Crowd observation and density analysis |
| Event Engine        | Event processing and rule evaluation   |
| Alert System        | Alert generation and management        |
| SOS System          | Emergency report handling              |
| Backend             | API and application logic              |
| Database            | Persistent information storage         |
| Frontend            | Dashboard and user interaction         |
| Analytics           | Monitoring statistics and reporting    |
| Evidence Management | Incident-related evidence organization |

---

# 🏗️ 5. System Architecture

SurakshaDrishti AI follows a modular architecture connecting video processing, AI inference, backend services, persistent storage and the frontend dashboard.

```text
                 CCTV / WEBCAM
                       |
                       v
                VIDEO CAPTURE
                       |
                       v
                OPENCV PROCESSING
                       |
                       v
                 YOLOv8 ENGINE
                       |
                       v
                PERSON DETECTION
                       |
                       v
                TRACKING MODULE
                       |
          +------------+------------+
          |            |            |
          v            v            v
      CROWD        ZONE         PRESENCE
     ANALYSIS    MONITORING     MONITORING
          |            |            |
          +------------+------------+
                       |
                       v
                  EVENT ENGINE
                       |
                       v
                 FASTAPI BACKEND
                       |
              +--------+--------+
              |                 |
              v                 v
          SQLITE DB          WEBSOCKET
              |                 |
              +--------+--------+
                       |
                       v
                REACT DASHBOARD
                       |
           +-----------+-----------+
           |           |           |
           v           v           v
         ALERTS        SOS      ANALYTICS
           |           |
           +-----------+
                       |
                       v
              AUTHORITY WORKFLOW
                       |
                       v
                INCIDENT REPORTS
```

### Architecture Explanation

**1. Video Input Layer**

Receives supported webcam or camera/video input.

**2. Computer Vision Layer**

Uses OpenCV for frame processing and YOLOv8 for person detection.

**3. Tracking and Event Layer**

Processes detection information and evaluates configured monitoring conditions.

**4. Backend Layer**

FastAPI handles application requests and backend operations.

**5. Database Layer**

SQLite stores supported application and event information.

**6. Real-Time Communication Layer**

WebSocket supports real-time communication where integrated.

**7. Presentation Layer**

React provides the centralized monitoring dashboard.

---

# 🔄 6. System Workflow

The general application workflow is:

1. The application starts.
2. The backend service initializes.
3. The frontend dashboard loads.
4. The AI processing pipeline starts.
5. A supported camera or video source is connected.
6. OpenCV captures video frames.
7. YOLOv8 processes the frames.
8. Person detections are generated.
9. Tracking and configured event-processing modules analyze the results.
10. Generated events are sent to the backend.
11. Event information is stored in the database.
12. The dashboard displays available monitoring information.
13. Operators review alerts and incidents.
14. SOS and authority workflows support incident tracking.
15. Available records can be exported for reporting.

---

# 🧰 7. Technology Stack

| Technology | Purpose                             |
| ---------- | ----------------------------------- |
| Python     | Core application and AI development |
| React.js   | Frontend interface                  |
| Vite       | Frontend development environment    |
| FastAPI    | Backend API framework               |
| YOLOv8     | Person detection                    |
| OpenCV     | Video and image processing          |
| SQLite     | Database                            |
| WebSocket  | Real-time communication             |
| REST API   | Application communication           |
| JSON       | Structured data exchange            |
| CSV        | Report export                       |
| Git        | Version control                     |
| GitHub     | Source code hosting                 |

---

# 📂 8. Project Structure

The repository is organized into separate modules for AI processing, backend development, frontend development, event handling and supporting utilities.

```text
SurakshaDrishti-AI/
│
├── ai_engine/
│
├── alert_system/
│
├── backend/
│
├── configs/
│
├── data/
│
├── database/
│
├── docs/
│
├── event_engine/
│
├── frontend/
│
├── models/
│
├── pipelines/
│
├── scripts/
│
├── tests/
│
├── tracking/
│
├── utils/
│
├── .gitignore
│
├── DEMO_SCRIPT.md
├── FEATURES.md
├── FINAL_REVIEW_NOTE.html
├── README.md
├── START_FULL_SYSTEM.txt
├── TROUBLESHOOTING.md
│
├── docker-compose.yml
├── requirements.txt
│
├── start_backend.ps1
├── start_frontend.ps1
├── start_pipeline.ps1
│
└── yolov8n.pt
```

### Directory Description

| Directory       | Description                       |
| --------------- | --------------------------------- |
| `ai_engine/`    | AI and computer vision components |
| `alert_system/` | Alert processing and management   |
| `backend/`      | FastAPI backend application       |
| `configs/`      | Application configurations        |
| `data/`         | Application data                  |
| `database/`     | Database-related components       |
| `docs/`         | Project documentation             |
| `event_engine/` | Event processing logic            |
| `frontend/`     | React-based dashboard             |
| `models/`       | AI model-related assets           |
| `pipelines/`    | Video and AI processing pipelines |
| `scripts/`      | Utility and automation scripts    |
| `tests/`        | Testing components                |
| `tracking/`     | Person tracking components        |
| `utils/`        | Shared utility functions          |

---

# ⚙️ 9. Installation Guide

Follow the instructions below to configure the project locally.

## System Requirements

Recommended development environment:

| Requirement      | Software                                  |
| ---------------- | ----------------------------------------- |
| Operating System | Windows 10/11 or compatible Linux         |
| Python           | 3.10+                                     |
| Node.js          | Compatible with the frontend dependencies |
| npm              | Included with Node.js                     |
| Code Editor      | Visual Studio Code                        |
| Version Control  | Git                                       |
| Camera           | Webcam or compatible video source         |

## Step 1: Clone the Repository

```bash
git clone https://github.com/aashumishra0907-beep/SurakshaDrishti-AI.git
```

Navigate to the project directory:

```bash
cd SurakshaDrishti-AI
```

## Step 2: Create a Python Virtual Environment

```bash
python -m venv .venv
```

Activate it using PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

## Step 3: Install Python Dependencies

```bash
pip install -r requirements.txt
```

## Step 4: Install Frontend Dependencies

The frontend startup script points to the dashboard directory.

```powershell
cd frontend/dashboard
```

Install dependencies:

```bash
npm install
```

Return to the project root when needed:

```powershell
cd ../..
```

---

# ▶️ 10. Running the Application

The repository contains three PowerShell startup scripts.

* `start_backend.ps1`
* `start_frontend.ps1`
* `start_pipeline.ps1`

**Important configuration note:** The current startup scripts contain machine-specific paths. Update those paths to your local repository location before running them on another computer.

### Terminal 1: Backend

From the project root, the backend launcher uses the following application entry point:

```powershell
python -m uvicorn backend.app.main:app --host 127.0.0.1 --port 8000
```

Alternatively, after correcting the local path in the script:

```powershell
.\start_backend.ps1
```

### Terminal 2: Frontend

```powershell
cd frontend/dashboard
npm run dev
```

Alternatively, use the frontend launcher after correcting its local directory:

```powershell
.\start_frontend.ps1
```

### Terminal 3: AI Pipeline

```powershell
.\start_pipeline.ps1
```

Check the pipeline script configuration if it uses an absolute local path.

### Access the Application

Frontend:

```text
http://localhost:5173/
```

Backend:

```text
http://127.0.0.1:8000/
```

API documentation:

```text
http://127.0.0.1:8000/docs
```

Backend health endpoint:

```text
http://127.0.0.1:8000/health
```

The backend URLs above are based on the current backend launcher configuration.

---

# 🧪 11. Testing and Validation

The repository includes a `tests/` directory.

Run the available Python tests using:

```bash
python -m pytest
```

Ensure the test dependencies are installed before running the command.

### Recommended Testing Areas

| Test Area        | Validation                    |
| ---------------- | ----------------------------- |
| Backend          | Application startup           |
| Frontend         | Dashboard loading             |
| AI Engine        | Person detection              |
| Video Processing | Frame capture                 |
| Tracking         | Tracking output               |
| Event Engine     | Event generation              |
| Alert System     | Alert handling                |
| Database         | Data storage and retrieval    |
| SOS              | Emergency report submission   |
| Reporting        | CSV and JSON exports          |
| WebSocket        | Real-time event communication |

Actual performance, accuracy and reliability should be evaluated through repeatable tests.

---

# 🔐 12. Security and Privacy

SurakshaDrishti AI processes camera and monitoring information. Responsible handling of this data is essential.

Important considerations:

* Use only authorized camera feeds.
* Protect access to application data.
* Restrict access to incident records.
* Apply appropriate authentication and authorization.
* Avoid unnecessary personal-data collection.
* Establish appropriate data-retention policies.
* Review AI-generated alerts before taking action.
* Follow applicable privacy and data-protection regulations.

The current academic prototype should undergo further security and privacy validation before operational deployment.

---

# ⚠️ 13. Current Project Scope and Limitations

SurakshaDrishti AI is developed as an academic software prototype.

Its major components include AI detection, monitoring, event processing, a web dashboard, incident reporting and supporting workflows.

However, some advanced capabilities require further testing, model validation and integration.

Important limitations include:

* Detection performance depends on camera quality and environmental conditions.
* Tracking can be affected by occlusion and crowded scenes.
* Crowd estimates depend on camera perspective and detection quality.
* Zone-based alerts depend on correct configuration.
* Advanced activity recognition requires appropriate validated models.
* Large-scale multi-camera deployment requires further optimization.
* Authority workflows are application-level demonstrations and do not guarantee real-world emergency response.

The system is intended to assist human operators rather than independently make security or enforcement decisions.

---

# 🚀 14. Future Development Roadmap

Potential improvements for future versions include:

| Enhancement                 | Objective                              |
| --------------------------- | -------------------------------------- |
| Advanced Crowd Analytics    | Improve crowd monitoring               |
| Multi-Camera Management     | Support larger monitoring environments |
| Improved Tracking           | Increase tracking reliability          |
| Advanced Zone Configuration | Improve restricted-area management     |
| Fall Detection              | Improve fall-event recognition         |
| Advanced Heatmaps           | Improve spatial event visualization    |
| Role-Based Access           | Improve access management              |
| Enhanced Notifications      | Improve alert communication            |
| Cloud Deployment            | Support scalable infrastructure        |
| Advanced Analytics          | Improve historical monitoring          |
| Automated Testing           | Improve software reliability           |
| Security Enhancements       | Strengthen application protection      |

These items represent future development opportunities and are not claims of completed implementation.

---

# 📸 15. Screenshots and Demonstration

Screenshots of the actual application can be added to the repository under:

```text
docs/
└── screenshots/
    ├── dashboard.png
    ├── live-monitoring.png
    ├── alerts.png
    ├── analytics.png
    └── sos-management.png
```

### Main Dashboard

![Main Dashboard](docs/screenshots/dashboard.png)

### Live Camera Monitoring

![Live Monitoring](docs/screenshots/live-monitoring.png)

### Alert Management

![Alert Management](docs/screenshots/alerts.png)

### Analytics Dashboard

![Analytics](docs/screenshots/analytics.png)

### SOS Management

![SOS Management](docs/screenshots/sos-management.png)

*Replace these image paths with actual screenshots committed to the repository.*

---

# 📚 16. Additional Documentation

The repository contains supporting project documents.

| File                     | Description                        |
| ------------------------ | ---------------------------------- |
| `FEATURES.md`            | Detailed feature information       |
| `DEMO_SCRIPT.md`         | Project demonstration instructions |
| `TROUBLESHOOTING.md`     | Common setup and runtime issues    |
| `START_FULL_SYSTEM.txt`  | Full-system startup information    |
| `FINAL_REVIEW_NOTE.html` | Project review documentation       |

---

# 👥 17. Team TriNetra

**Developed by Team TriNetra**

| Team Member              | Responsibility                                                  |
| ------------------------ | --------------------------------------------------------------- |
| Mahesh Rana              | Team Leader, System Architect, Full Stack Developer & Presenter |
| Laxman Chaudhary         | AI/ML Module Developer                                          |
| Pradip Singh             | Backend & Database Developer                                    |
| Ashutosh Mishra          | Frontend Dashboard Developer                                    |
| Gagan Bahadur Guru Dhami | UI/UX, Branding & Presentation Designer                         |
| Sandip Sha               | Testing, Deployment & Demo Coordinator                          |
| Osama Idris Ali Mohamed  | Research & Documentation Lead                                   |

---

# 🎓 18. Academic Project Information

| Detail            | Information                                           |
| ----------------- | ----------------------------------------------------- |
| Project Name      | SurakshaDrishti AI                                    |
| Project Title     | AI/ML-Based Railway Crowd and Crime Monitoring System |
| Team Name         | TriNetra                                              |
| Institution       | Rathinam Technical Campus                             |
| Department        | Department of Computer Science and Humanities         |
| Academic Year     | 2025–2026                                             |
| Event             | YUDHISTRA Project Demo Day 2K26                       |
| Problem Reference | SIH1349 – Ministry of Railways                        |
| Domain            | Smart Automation                                      |
| Project Type      | AI/ML-Based Software Prototype                        |

---

# 🤝 19. Contributions

Suggestions, improvements and contributions are welcome.

When reporting an issue, please include:

1. A clear description of the problem.
2. Steps to reproduce the issue.
3. Expected behavior.
4. Actual behavior.
5. Relevant error messages or screenshots.

---

# 📄 20. License

No license is currently specified in this README.

Please refer to the repository's `LICENSE` file, if present, before reusing or distributing the project.

---

# ⚖️ 21. Disclaimer

SurakshaDrishti AI is an academic project and research-oriented software prototype.

It is not a certified railway security system or a replacement for trained railway personnel.

AI-generated results may contain errors and must be verified by authorized human operators.

Any real-world deployment requires appropriate authorization, operational testing, security assessment and privacy compliance.

---

<div align="center">

# 🛡️ SURAKSHADRISHTI AI

### Smarter Monitoring. Faster Awareness. Safer Railways.

**Developed with ❤️ by Team TriNetra**

**Rathinam Technical Campus | 2025–2026**

<br>

⭐ If you find this project interesting, consider starring the repository!

</div>
