# VisionVox

VisionVox is an AI-powered assistive technology project designed to enhance accessibility for visually impaired and speech-impaired individuals. The system combines Computer Vision, Gesture Recognition, Face Recognition, Object Detection, and Voice Feedback to provide real-time assistance.
Using a camera and AI models, VisionVox can detect obstacles, recognize hand gestures, identify known faces, provide voice guidance, and send emergency alerts to caregivers.
This project was developed as an educational and social-impact solution demonstrating the practical application of Artificial Intelligence in accessibility and healthcare.

---

##  Features :

- **Smart Navigation Assistance** – Real-time obstacle detection with voice alerts.
- **Gesture-to-Voice Communication** – Recognises hand gestures and converts them into speech.
- **Face Recognition** – Identifies known faces and announces them aloud.
- **Voice Assistance** – Text-to-speech output for all alerts and confirmations.
- **Emergency Alert System** – Sends instant WhatsApp notifications to caregivers.
- **Dashboard & Activity Monitoring** – Web dashboard to track usage and events.
- **Report Generation** – Generates PDF reports of detected activities.

---

##  System Architecture :

```text
Camera Input
      │
      ▼
Computer Vision Module
      │
 ┌────┴────┐
 │         │
 ▼         ▼
Object   Gesture
Detection Recognition
 │         │
 ▼         ▼
Voice    Gesture-to-
Alerts   Speech Output
 │
 ▼
Face Recognition
 │
 ▼
Dashboard & Database
 │
 ▼
WhatsApp Alerts
```

---

##  Technologies Used :

### Frontend
- HTML5
- CSS3
- JavaScript

### Backend
- Python
- Flask
- Flask-CORS

### Artificial Intelligence & Computer Vision
- OpenCV
- MediaPipe
- YOLOv8
- Face Recognition (dlib)
- Dlib

### Database
- MySQL

### Voice Processing
- pyttsx3
- gTTS
- Pygame

### Communication Services
- Twilio WhatsApp API

### Reporting
- ReportLab

---

##  Project Structure :

```text
VisionVox/
│
├── backend/
│   ├── app.py
│   ├── requirements.txt
│   ├── yolov8n.pt
│   ├── gesture_recognizer.task
│   ├── known_face.npy
│   └── known_face_name.txt
│
├── frontend/
│   ├── index.html
│   ├── dashboard.html
│   ├── gestures.html
│   ├── activity.html
│   ├── comm.html
│   ├── face_lock.html
│   │
│   ├── css/
│   │   └── style.css
│   │
│   ├── js/
│   │   ├── app.js
│   │   ├── main.js
│   │   ├── dashboard.js
│   │   └── service-worker.js
│   │
│   └── static/
│       ├── icon-192.png
│       └── icon-512.png
│
└── README.md
```

---

##  Installation :

### 1. Clone Repository

```bash
git clone https://github.com/yourusername/VisionVox.git
cd VisionVox
```

### 2. Create Virtual Environment

```bash
python -m venv venv
```

**Windows**
```bash
venv\Scripts\activate
```

**Linux / macOS**
```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r backend/requirements.txt
```

### 4. Configure MySQL Database

Create a database named:

```sql
CREATE DATABASE visionvox;
```

Update database credentials in `backend/app.py`:

```python
DB_CONFIG = {
    "host": "127.0.0.1",
    "port": 3306,
    "database": "visionvox",
    "user": "root",
    "password": "your_password"
}
```

### 5. Configure Twilio

Replace the following values with your credentials (in `backend/app.py`):

```python
TWILIO_SID = "YOUR_TWILIO_SID"
TWILIO_TOKEN = "YOUR_TWILIO_TOKEN"
TWILIO_FROM = "YOUR_TWILIO_NUMBER"
TWILIO_TO = "CAREGIVER_NUMBER"
```

### 6. Run the Application

```bash
cd backend
python app.py
```

Then open your browser and go to:

```text
http://localhost:5000
```

---

##  Main Modules :

| Module | Description |
|--------|-------------|
| **Navigation Module** | Detects obstacles (people, chairs, doors, stairs) and provides audio warnings with direction (left/right/front). |
| **Gesture Recognition Module** | Recognises hand gestures (thumbs-up, peace, fist, palm) and converts them into spoken phrases. |
| **Face Recognition Module** | Identifies known individuals from a pre‑registered dataset and announces their name. |
| **Alert Module** | Sends emergency WhatsApp notifications (e.g., fall detection, panic gesture) using Twilio. |
| **Dashboard Module** | Displays live activity logs, statistics, and generates PDF reports for caregivers. |

---

##  Applications :

- Assistive technology for visually impaired individuals
- Communication aid for speech-impaired users
- Smart healthcare systems
- Elderly care solutions
- Accessibility research projects
- AI and Computer Vision learning projects

---

##  Future Enhancements :

- Mobile application integration (iOS/Android)
- GPS-based outdoor navigation with route planning
- Cloud database integration for remote monitoring
- Smart wearable device integration (smart glasses, smartwatch)
- Real-time caregiver monitoring app

---
