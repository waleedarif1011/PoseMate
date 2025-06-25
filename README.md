# 🏋️‍♂️ PoseMate: Trigonometric Pose Estimation & Correction

> "AI-powered feedback for your fitness form!"

---

## 📑 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Demo](#demo)
- [Setup & Installation](#setup--installation)
- [Usage](#usage)
- [How it Works](#how-it-works)
  - [Plank](#plank)
  - [Squat](#squat)
  - [Shoulder Press](#shoulder-press)
- [Credits](#credits)

---

## 📝 Overview
PoseMate uses [MediaPipe](https://google.github.io/mediapipe/) and [OpenCV](https://opencv.org/) to detect body landmarks and compute joint angles for real-time posture correction in fitness exercises. It provides instant feedback and guidance to help you perfect your form for planks, squats, and shoulder presses.

> **Quote:**
> "Good form is the foundation of safe and effective exercise. PoseMate helps you get it right!"



## ✨ Features
- Real-time pose estimation using your webcam or video files
- Automatic detection of key body landmarks
- Angle calculation for major joints
- Instant feedback and correction cues
- Exercise-specific logic for Plank, Squat, and Shoulder Press
- Visual overlays and repetition counting

---

## 🎬 Demo
Demo videos and images are available in the `demos/` folder:

- `demos/Plank/plank.mp4`, `plank_correct.jpg`, `plank_wrong.jpg`
- `demos/Squat/squat.mp4`
- `demos/ShoulderPress/shoulderPressV.mp4`

> "Try running the notebooks with these demo files for a quick start!"

---

## ⚙️ Setup & Installation

> **Requirements:** Python 3.7+

Install the required libraries:
```bash
pip install opencv-python mediapipe numpy
```

---

## 🚀 Usage
You can run each exercise notebook independently:

### 1. Plank
- Open `Plank.ipynb` or `trignometic-pose-estimation-and-correction/Plank.ipynb`.
- Run all cells to:
  - Detect pose from webcam or video
  - Calculate angles for shoulder, elbow, hip, and ankle
  - Get real-time feedback on your plank form

### 2. Squat
- Open `Squat.ipynb`.
- Run all cells to:
  - Analyze squat video (e.g., `demos/Squat/squat.mp4`)
  - Track knee, hip, ankle, and trunk angles
  - Count repetitions and display correction cues

### 3. Shoulder Press
- Open `ShoulderPress.ipynb`.
- Run all cells to:
  - Detect shoulder press state (up/down)
  - Calculate elbow and shoulder angles
  - Get feedback for both states and count reps

---

## 🧠 How it Works

### Plank
- **Key Angles:**
  - Shoulder: 65°–95°
  - Elbow: 70°–100°
  - Hip: 135°–175°
  - Ankle: 70°–120°
- **Logic:**
  - Uses MediaPipe to extract landmarks
  - Calculates angles using trigonometry
  - Provides feedback if angles are out of range

### Squat
- **Key Angles:**
  - Ankle: 105°–120°
  - Hip: >60°
  - Trunk: Upright
  - Knee: 45°–75°
- **Logic:**
  - Tracks joint angles frame-by-frame
  - Counts reps based on knee angle transitions
  - Displays correction messages for improper form

### Shoulder Press
- **States:**
  - **State 1 (Lower):**
    - Elbow: 55°–75°
    - Shoulder: 85°–105°
  - **State 2 (Upper):**
    - Elbow: 125°–140°
    - Shoulder: 145°–165°
- **Logic:**
  - Detects state transitions
  - Counts repetitions
  - Provides cues for initial position and movement

---

## 🙏 Credits
- [MediaPipe](https://google.github.io/mediapipe/) for pose estimation
- [OpenCV](https://opencv.org/) for image processing
- Developed by the PoseMate team

> "Feel free to contribute or raise issues to improve PoseMate!"

