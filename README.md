# Flow-State: AI-Powered Focus & Productivity Suite

[![Python](https://img.shields.io/badge/Python-3.9+-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![OpenCV](https://img.shields.io/badge/OpenCV-Computer_Vision-5C3EE8?logo=opencv)](https://opencv.org/)
[![MediaPipe](https://img.shields.io/badge/MediaPipe-Face_Landmarks-007FFF)](https://developers.google.com/mediapipe)

**Flow-State** is a multi-layered desktop productivity and deep-work enforcement tool. It combines real-time computer vision webcam tracking with host-level website blocking, binaural audio, and anti-cheating background monitors to guarantee uninterrupted focus sessions.

---

## ⚡ Key Highlights

### 👁️ Computer Vision Monitoring (MediaPipe + OpenCV)
- **Sleep & Drowsiness Detection**: Tracks eye aspect ratio (EAR) via facial landmarks to flag drowsiness.
- **Posture Correction**: Alerts when slouching or drifting out of ergonomic posture.
- **Distraction Alerts**: Flags when user turns away or leaves the workspace.

### 🛡️ Iron Dome Website Blocker
- Modifies host-level DNS routing (`hosts` file) during active focus blocks to completely isolate distracting websites.
- Restores standard DNS access automatically once session or rest intervals conclude.

### 🔒 "No-Escape" Ghost Supervisor
- Runs a companion background supervisor process (`ghost_blocker.py`) that monitors and prevents users from prematurely killing focus sessions through task manager.

### 🧠 Brainwave Audio Engine
- Built-in sound generator supporting Gamma, Beta, and Alpha frequencies to stimulate cognitive flow states during work periods.

### ⏱️ Integrated Pomodoro System
- Configurable work, short-break, and long-break cycles with audio notifications.

---

## 📁 Project Structure

```
Flow-State/
├── assets/                  # Audio wave files (Alpha, Beta, Gamma) & icons
├── face_landmarker.task     # Pre-trained MediaPipe face landmark model
├── audio_engine.py          # Sound playback & wave synthesizers
├── config.py                # Global settings, paths, and constants
├── ghost_blocker.py         # Anti-tamper supervisor daemon
├── iron_dome.py             # Hosts file manager & website blocking engine
├── vision_engine.py         # MediaPipe & OpenCV landmark processing
└── main.py                  # Primary application entry point & GUI/CLI
```

---

## 🛠️ Prerequisites & Setup

### 1. Requirements
- Python 3.9 or higher
- Webcam / Camera for vision tracking
- Administrator privileges (required for `iron_dome.py` hosts manipulation)

### 2. Installation
```bash
git clone https://github.com/ShunyaPulse/Flow-State.git
cd Flow-State
pip install opencv-python mediapipe pygame numpy
```

### 3. Running Flow-State
Launch the application with administrative privileges:
```bash
python main.py
```
