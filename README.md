# Drowsiness & Yawn Detection System

A real-time computer vision system that detects driver drowsiness and yawning using facial landmarks, Eye Aspect Ratio (EAR), and Mouth Aspect Ratio (MAR).

The system uses a webcam to continuously monitor the user's eyes and mouth. When prolonged eye closure or yawning is detected, an audio alert is triggered.

---

## Features

- Real-time webcam-based monitoring
- Face detection using Dlib
- 68-point facial landmark detection
- Eye Aspect Ratio (EAR) based drowsiness detection
- Mouth Aspect Ratio (MAR) based yawn detection
- Consecutive-frame analysis to reduce false alerts
- Real-time EAR and MAR display
- Audio alerts for drowsiness and yawning
- OpenCV-based visualization
- Real-time processing

---

## Technologies Used

- Python
- OpenCV
- Dlib
- NumPy
- SciPy
- Imutils
- Pygame
- Jupyter Notebook

---

## How It Works

### 1. Face Detection

The system captures video frames from the webcam and converts them to grayscale.

Dlib's frontal face detector is used to detect the face in each frame.

### 2. Facial Landmark Detection

Dlib's 68-point facial landmark predictor identifies important facial points around the eyes and mouth.

These landmarks are used to calculate the Eye Aspect Ratio (EAR) and Mouth Aspect Ratio (MAR).

### 3. Drowsiness Detection

The Eye Aspect Ratio (EAR) is used to measure the degree of eye openness.

The formula is:

```text
EAR = (A + B) / (2 × C)
