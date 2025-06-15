# 🖱️ Virtual Mouse using Hand Gestures 🖐️

A computer vision-based project that allows you to control your mouse cursor using just your hand gestures. With the help of a webcam, this system detects your hand movements and translates them into real-time mouse actions like moving the cursor and clicking — completely touch-free!

This project utilizes **MediaPipe** for accurate hand landmark detection and **OpenCV** for image processing, alongside **Autopy** for mouse control on screen.

---

## 📌 Project Overview

- **Objective:** Create a virtual mouse interface using hand gestures.
- **Control Logic:**
  - Move mouse pointer using **index finger**.
  - Perform **left-click** by pinching **index and middle fingers**.
- **Technologies Used:** Python, OpenCV, MediaPipe, NumPy, Autopy.

---

## 🧠 How It Works

1. The webcam captures video frames.
2. MediaPipe detects your hand and returns 21 landmarks.
3. Finger tips (landmarks 8 and 12) are tracked to identify gestures.
4. Cursor movement is mapped to your index finger.
5. When index and middle fingertips are close together, a click is triggered.

---

## 🧾 Features

- Real-time hand tracking
- Smooth cursor control
- Gesture-based clicking
- Custom hand detection module
- Lightweight and easy to use

---

## 🗂️ Project Structure

├── HandTrackingModule.py # Handles hand detection & gesture logic

├── VirtualMouse.py # Main virtual mouse application

├── README.md # Project documentation

## 🧩 Module Descriptions
### 🔹 HandTrackingModule.py

This file defines the HandDetector class with:

findHands(img): Detect and draw hands in the frame.

findPosition(img): Get list of hand landmark positions and bounding box.

fingersUp(): Detect which fingers are raised.

findDistance(p1, p2, img): Compute distance between two landmarks (e.g., index and middle finger).

### 🔹 VirtualMouse.py

This is the main application file. It:

Captures webcam feed

Uses HandDetector to track finger landmarks

Maps hand positions to screen resolution

Detects gestures for mouse movement and clicking

Smoothens cursor to avoid jittery motion

### Gesture Logic:
| Gesture              | Action     |
| -------------------- | ---------- |
| Index up             | Move mouse |
| Index + Middle pinch | Left click |


---

## 🧰 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Maheswara23/volume-control-hand-gesture.git
   cd volume-control-hand-gesture

2. Install   required libraries:
   ```bash
   pip install opencv-python mediapipe pycaw comtypes numpy

3. Run the Project
   ```bash
   python VolumeHandControl.py
