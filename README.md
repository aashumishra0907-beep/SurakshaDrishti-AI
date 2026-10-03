# SurakshaDrishti AI

## AI/ML-Based Railway Crowd and Crime Monitoring System

**Turning Railway CCTV into Real-Time AI Safety Intelligence**

---

## Project Pitch

**SurakshaDrishti AI** is an AI/ML-based railway safety monitoring system that transforms CCTV/webcam feeds into an intelligent safety command center.

The system uses computer vision, object detection, tracking, crowd analysis, event detection and real-time alerts to assist railway operators in monitoring crowded and restricted areas.

It provides a centralized dashboard for:

* Live camera monitoring
* Person detection
* Person tracking
* Crowd density monitoring
* Intrusion detection
* Loitering detection
* Fall/suspicious activity detection
* SOS reporting
* Real-time alerts
* Evidence management
* Authority response workflow
* Safety analytics
* Event reports and exports

The project is designed as a working software MVP aligned with the concept of **SIH1349 - Ministry of Railways**, focusing on AI-assisted railway crowd management, safety monitoring and incident response.

---

# Why This Project Matters

Railway stations are crowded and dynamic public environments where safety incidents can occur quickly.

Traditional CCTV systems primarily record video. Human operators must continuously watch multiple screens to identify unusual events.

SurakshaDrishti AI adds an intelligent monitoring layer that can:

```text
CCTV / Webcam
      ↓
AI Detection
      ↓
Tracking
      ↓
Event Analysis
      ↓
Alert Generation
      ↓
Command Dashboard
      ↓
Authority Response
      ↓
Evidence + Reports
```

The objective is to help operators identify important events faster and organize the response workflow.

---

# Main Features

## 1. Live Camera Monitoring

The system supports live webcam/CCTV-style video feeds through the AI pipeline.

Features:

* Live video display
* Camera status
* Camera identification
* Location information
* Person detection
* Real-time event monitoring

---

## 2. AI Person Detection

The system uses **YOLOv8 and OpenCV** for computer vision-based detection.

Detected persons can be displayed with bounding boxes.

Example:

```text
Camera 01

Person 1
Person 2
Person 3
Person 4

Total Persons: 4
```

Detection results can be passed to the tracking and event-analysis modules.

---

# 3. Person Tracking

The tracking module assigns temporary IDs to detected persons.

Example:

```text
Person ID: 17

10:20:01 → Zone A
10:20:10 → Zone A
10:20:20 → Zone A
10:20:30 → Zone A
```

Tracking information can be used for:

* Loitering detection
* Zone monitoring
* Movement analysis
* Crowd analysis

---

# 4. Crowd Monitoring

The crowd monitoring module counts detected persons in each camera view.

The system can compare the current number of detected persons against configurable thresholds.

Example:

```text
People Count: 47
Configured Capacity: 60
Occupancy: 78%

Status: HIGH
```

Possible crowd states:

```text
NORMAL
MODERATE
HIGH
CRITICAL
```

Thresholds can be configured according to the monitored area.

---

# 5. Intrusion Detection

Administrators can configure restricted zones inside camera views.

Example:

```text
Camera View

+--------------------------------+
|                                |
|       NORMAL AREA              |
|                                |
|  +----------------------+      |
|  |   RESTRICTED ZONE    |      |
|  |                      |      |
|  +----------------------+      |
|                                |
+--------------------------------+
```

When a tracked person enters a restricted area, the system generates an intrusion event.

Example:

```text
INTRUSION ALERT

Camera: C02
Zone: Restricted Area
Time: 21:32:10
Severity: HIGH
Status: PENDING
```

---

# 6. Loitering Detection

The system can monitor how long a tracked person remains inside a configured area.

Example:

```text
Person ID: 17
Zone: Restricted Area
Duration: 45 seconds

LOITERING ALERT
```

The loitering threshold can be configured according to the monitored location.

---

# 7. Suspicious Activity Detection

The system provides an AI-assisted event-analysis layer for identifying potentially unusual activity.

Possible event categories include:

```text
NORMAL
SUSPICIOUS ACTIVITY
FALL SUSPECTED
FIGHT SUSPECTED
INTRUSION
LOITERING
CROWD ALERT
```

These events are treated as alerts requiring operator verification rather than automatic confirmation of a crime.

---

# 8. Fall Detection Prototype

A fall-detection module can analyze a person's body position and movement to identify possible falls.

Workflow:

```text
Person Detection
       ↓
Pose / Movement Analysis
       ↓
Fall Suspected
       ↓
Alert
       ↓
Operator Verification
       ↓
Authority Response
```

Example:

```text
FALL ALERT

Camera: C03
Location: Platform 3
Time: 21:18:42
Severity: HIGH

[View Evidence]
[Dispatch Authority]
[Mark Resolved]
```

---

# 9. Weapon Detection Module

The system architecture supports a separate object-detection model for detecting potentially prohibited objects.

Workflow:

```text
Camera
   ↓
Object Detection
   ↓
Potential Prohibited Object
   ↓
High Priority Alert
   ↓
Evidence Capture
   ↓
Operator Verification
```

Weapon detection should be treated as a prototype AI capability and must be evaluated using an appropriate trained model and dataset before real-world deployment.

---

# 10. Real-Time Alert System

The alert engine converts detected events into dashboard alerts.

Example:

```text
HIGH PRIORITY

INTRUSION DETECTED
Camera: C02
Time: 21:32:10
Zone: Platform Restricted Area
```

Alerts can have different severity levels:

```text
LOW
MEDIUM
HIGH
CRITICAL
```

Operators can:

* View alert
* Acknowledge alert
* Assign authority
* Update status
* View evidence
* Resolve incident

---

# 11. Automatic Evidence Management

When an important event occurs, the system can store event information and associated evidence.

Stored information may include:

```text
Event ID
Camera ID
Event Type
Severity
Timestamp
Location
Confidence
Evidence Path
Status
```

Example:

```text
Incident #1042

Type: Intrusion
Camera: C02
Time: 21:32:10
Severity: HIGH

Evidence:
incident_1042.jpg

Status:
ASSIGNED
```

---

# 12. SOS Emergency System

The SOS module allows an operator or passenger to create an emergency report.

Example:

```text
SOS REPORT

Location: Platform 2
Incident Type: Medical Emergency
Description: Passenger requires assistance
Time: 21:35:12

[Submit SOS]
```

The SOS event can be sent to the command dashboard and assigned to an authority.

---

# 13. Authority Response Workflow

The system provides a structured incident-response workflow.

```text
DETECTED
    ↓
PENDING
    ↓
ASSIGNED
    ↓
ACKNOWLEDGED
    ↓
RESPONDING
    ↓
RESOLVED
```

Example:

```text
Incident #1042

✓ Detected
✓ Assigned
✓ Acknowledged
✓ Responding
✓ Resolved
```

The system can record timestamps for each response stage.

---

# 14. Command Center Dashboard

The React dashboard provides a centralized view of the railway safety system.

Example:

```text
+------------------------------------------------+
|             SURAKSHADRISHTI AI                 |
+------------------------------------------------+

+----------+----------+----------+---------------+
| Cameras  | Persons  | Alerts   | Critical      |
|    12    |   184    |    27    |      3        |
+----------+----------+----------+---------------+

LIVE CAMERAS

+----------------+    +----------------+
| CAMERA 01      |    | CAMERA 02      |
|                |    |                |
| Person  Person |    | Person Person  |
|                |    |                |
| 34 Persons     |    | 18 Persons     |
+----------------+    +----------------+

RECENT ALERTS

🔴 Intrusion        21:32
🟠 Loitering        21:29
🟡 Crowd Alert      21:26
🔴 Fall Alert       21:21
```

---

# 15. Camera Management

The administrator can manage connected cameras.

Example:

```text
CAMERA MANAGEMENT

Camera ID    Location       Status

C01          Platform 1     ONLINE
C02          Platform 2     ONLINE
C03          Entrance       OFFLINE
C04          Parking        ONLINE
```

Camera management can include:

* Add camera
* Remove camera
* Enable camera
* Disable camera
* Set location
* Set crowd capacity
* Configure restricted zones

---

# 16. User Roles

The system supports role-based access.

### ADMIN

* Manage users
* Manage cameras
* Configure zones
* View all incidents
* Manage system settings

### OPERATOR

* Monitor cameras
* View alerts
* Handle incidents
* Create SOS reports

### AUTHORITY

* View assigned incidents
* Acknowledge incidents
* Update response status
* Resolve incidents

### VIEWER

* Read-only dashboard access

---

# 17. Privacy and Security

Because the project processes surveillance video, privacy and security are important design considerations.

Planned safeguards include:

* Role-based access control
* Evidence access logging
* Data retention policies
* Optional identity/face masking
* Secure authentication
* Controlled evidence access
* Automatic deletion of expired records

The prototype does not claim to provide complete legal or production-grade privacy compliance.

---

# 18. Safety Heatmap

The analytics module can visualize locations with higher numbers of events.

Example:

```text
             STATION MAP

        PLATFORM 1 🔴
              |
              |
ENTRANCE 🟡 --+-- PLATFORM 2 🔴
              |
              |
          FOOD AREA 🟢

🔴 High Activity
🟡 Medium Activity
🟢 Low Activity
```

The heatmap can be generated using stored event and camera-location information.

---

# 19. Analytics Dashboard

The system provides event statistics.

Example:

```text
DAILY SAFETY ANALYTICS

Total Events:       184
Intrusion:           42
Loitering:           51
Crowd Alerts:        63
SOS:                 12
Other:               16
```

Analytics can be filtered by:

* Date
* Camera
* Location
* Event type
* Severity
* Status

---

# 20. Reports and Export

The system supports event and incident reporting.

Available formats:

```text
JSON
CSV
```

Reports can contain:

```text
Event ID
Timestamp
Camera
Location
Event Type
Severity
Status
Response Time
Evidence
```

Example:

```text
Daily Report

Date: 03-10-2026

Total Events: 184
Resolved: 167
Pending: 8
Critical: 3
```

---

# 21. Database

The system uses SQLite for local prototype storage.

The database structure can include:

```text
users
cameras
zones
events
evidence
alerts
sos_reports
authority_assignments
event_history
system_logs
```

The architecture can later be migrated to PostgreSQL or another production database.

---

# 22. Technology Stack

| Layer                   | Technology               |
| ----------------------- | ------------------------ |
| Frontend                | React + Vite             |
| Backend                 | FastAPI                  |
| AI/ML                   | Python                   |
| Computer Vision         | OpenCV                   |
| Object Detection        | YOLOv8                   |
| Tracking                | Tracking module          |
| Database                | SQLite                   |
| Real-Time Communication | WebSocket                |
| Reports                 | JSON / CSV               |
| Version Control         | Git + GitHub             |
| Deployment              | Localhost / Docker-ready |

---

# 23. System Architecture

```text
                  CCTV / WEBCAM
                       |
                       ↓
               OPENCV FRAME CAPTURE
                       |
                       ↓
                YOLOv8 DETECTION
                       |
                       ↓
                PERSON TRACKING
                       |
        +--------------+--------------+
        |              |              |
        ↓              ↓              ↓
   CROWD ENGINE   ZONE ENGINE    BEHAVIOR ENGINE
        |              |              |
        ↓              ↓              ↓
     Density       Intrusion      Loitering
                    Detection     Fall/Suspicious
        +--------------+--------------+
                       |
                       ↓
                  EVENT ENGINE
                       |
                       ↓
                  FASTAPI BACKEND
                       |
             +---------+---------+
             |                   |
             ↓                   ↓
          DATABASE           WEBSOCKET
             |                   |
             +---------+---------+
                       |
                       ↓
               REACT DASHBOARD
                       |
       +---------------+---------------+
       |               |               |
       ↓               ↓               ↓
     ALERTS           SOS          AUTHORITY
                                     RESPONSE
                       |
                       ↓
                  REPORTS / ANALYTICS
```

---

# 24. Project Workflow

```text
1. User logs into the dashboard.

2. Camera feed is started.

3. OpenCV captures video frames.

4. YOLOv8 processes the frames.

5. Persons/objects are detected.

6. Tracking assigns temporary IDs.

7. Crowd and zone engines analyze the scene.

8. Event engine generates alerts.

9. FastAPI receives and stores the event.

10. WebSocket sends the alert to the dashboard.

11. Operator reviews the alert.

12. Evidence is displayed.

13. Authority can be assigned.

14. Response status is updated.

15. Incident is resolved.

16. Event remains available for analytics and reports.
```

---

# 25. API Structure

Example FastAPI endpoints:

```text
POST   /auth/login

GET    /cameras
POST   /cameras
PUT    /cameras/{id}
DELETE /cameras/{id}

GET    /events
GET    /events/{id}
POST   /events

GET    /alerts
PUT    /alerts/{id}/acknowledge

POST   /sos
GET    /sos

GET    /dispatch
POST   /dispatch
PUT    /dispatch/{id}

GET    /analytics

GET    /reports/daily
GET    /reports/monthly

WebSocket:
 /ws/alerts
 /ws/camera
```

---

# 26. Project Folder Structure

```text
SurakshaDrishti-AI/
│
├── backend/
│   ├── main.py
│   ├── database.py
│   ├── models/
│   ├── schemas/
│   ├── routes/
│   ├── services/
│   └── websocket/
│
├── ai/
│   ├── detection/
│   ├── tracking/
│   ├── crowd/
│   ├── intrusion/
│   ├── loitering/
│   ├── fall/
│   ├── behavior/
│   └── models/
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   └── dashboard/
│   └── package.json
│
├── database/
│
├── evidence/
│
├── tests/
│
├── docs/
│
├── .env.example
├── requirements.txt
├── Dockerfile
├── docker-compose.yml
└── README.md
```

---

# 27. Run Commands

Run the following PowerShell commands from the project root:

```powershell
.\start_backend.ps1
```

```powershell
.\start.frontend.ps1
```

```powershell
.\start.pipeline.ps1
```

Recommended order:

```text
1. Start Backend
2. Start Frontend
3. Start AI Pipeline
4. Open Dashboard
5. Start Camera
6. Demonstrate Person Detection
7. Demonstrate Crowd Monitoring
8. Demonstrate Intrusion/Loitering Alert
9. Demonstrate SOS
10. Demonstrate Authority Workflow
11. Show Evidence
12. Export Report
```

---

# 28. Complete Demo Scenario

A complete demonstration can follow this scenario:

```text
Camera 02 is monitoring Platform 2.

        ↓

AI detects multiple people.

        ↓

Crowd engine calculates the current density.

        ↓

A person enters a configured restricted zone.

        ↓

Tracking identifies the person's movement.

        ↓

Intrusion event is generated.

        ↓

Evidence is captured.

        ↓

WebSocket sends the alert to the dashboard.

        ↓

Operator receives HIGH priority alert.

        ↓

Operator acknowledges the incident.

        ↓

Authority is assigned.

        ↓

Authority changes status to RESPONDING.

        ↓

Incident is resolved.

        ↓

Event is stored in the database.

        ↓

Analytics are automatically updated.

        ↓

Incident appears in the exported report.
```

---

# 29. Current MVP Status

SurakshaDrishti AI is developed as a working software prototype.

### Core Components

* Login/Auth
* Live camera feed
* Person detection
* Alert system
* React command dashboard
* SOS reporting
* Authority workflow
* SQLite storage
* JSON/CSV reporting
* WebSocket communication

### Advanced Prototype Components

* Person tracking
* Crowd analysis
* Restricted-zone monitoring
* Loitering detection
* Safety heatmap
* Evidence management
* Event analytics

### Further Development

The following capabilities require additional datasets, model training, testing and validation before production deployment:

* Advanced weapon detection
* Robust fight detection
* Advanced fall detection
* Large-scale multi-camera deployment
* Production cloud infrastructure
* High-accuracy crowd-density estimation
* Advanced behavioral analysis

---

# 30. Future Scope

Future versions can include:

* Multi-camera railway station integration
* Edge AI processing
* GPU-based inference
* Advanced crowd prediction
* Improved pose-based activity detection
* Better tracking across cameras
* Production-grade databases
* Docker and cloud deployment
* Mobile authority application
* SMS/email/push notifications
* Advanced analytics
* Model monitoring
* Automated system health monitoring
* Stronger privacy controls

---

# 31. Team TriNetra

| Member                   | Role                                                            |
| ------------------------ | --------------------------------------------------------------- |
| Mahesh Rana              | Team Leader, System Architect, Full Stack Developer & Presenter |
| Laxman Chaudhary         | AI/ML Module Developer                                          |
| Pradip Singh             | Backend & Database Developer                                    |
| Ashutosh Mishra          | Frontend Dashboard Developer                                    |
| Gagan Bahadur Guru Dhami | UI/UX, Branding & Presentation Designer                         |
| Sandip Sha               | Testing, Deployment & Demo Coordinator                          |
| Osama Idris Ali Mohamed  | Research & Documentation Lead                                   |

---

# 32. Project Identity

| Detail            | Value                                                                      |
| ----------------- | -------------------------------------------------------------------------- |
| Project Title     | SurakshaDrishti AI - AI/ML-Based Railway Crowd and Crime Monitoring System |
| Team              | TriNetra                                                                   |
| College           | Rathinam Technical Campus                                                  |
| Department        | Department of Computer Science and Humanities                              |
| Academic Year     | 2025-2026                                                                  |
| Event             | YUDHISTRA Project Demo Day 2K26                                            |
| Problem Reference | SIH1349 - Ministry of Railways                                             |
| Domain            | Smart Automation                                                           |
| Type              | Software                                                                   |

---

# 33. Project Objective

The primary objective of SurakshaDrishti AI is to demonstrate how existing railway CCTV infrastructure can be enhanced with AI-assisted monitoring.

The system combines:

```text
Computer Vision
+
Object Detection
+
Tracking
+
Crowd Analysis
+
Event Detection
+
Real-Time Communication
+
Incident Management
+
Analytics
```

into one centralized railway safety monitoring platform.

---

# 34. Final Project Vision

```text
                 SURAKSHADRISHTI AI

                    Railway CCTV
                         ↓
                  AI Vision Layer
                         ↓
                Intelligent Analysis
                         ↓
                Real-Time Detection
                         ↓
                  Alert Generation
                         ↓
                Command Dashboard
                         ↓
                Human Verification
                         ↓
                Authority Response
                         ↓
                  Incident Resolution
                         ↓
                Analytics & Reports
```

SurakshaDrishti AI aims to demonstrate a practical AI-assisted approach to railway safety monitoring by converting conventional video surveillance into a structured, real-time safety intelligence workflow.

---

## Team TriNetra

**SurakshaDrishti AI**

*AI/ML-Based Railway Crowd and Crime Monitoring System*

**Rathinam Technical Campus**
**Academic Year 2025-2026**
