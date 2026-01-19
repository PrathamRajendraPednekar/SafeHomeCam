# SafeHomeCam

**SafeHomeCam** is an AI-based home security system that uses real-time face recognition and hand gesture detection to enhance safety. It triggers alarms, SMS alerts, and emergency calls using computer vision, deep learning, and IoT-based automation.

---

## Table of Contents
1. [Introduction](#introduction)
2. [Hypothesis](#hypothesis)
3. [Objectives](#objectives)
4. [Technologies Used](#technologies-used)
5. [Procedure](#procedure)
6. [How to Run](#how-to-run)


---

## Introduction
SafeHomeCam is an AI-based home security system designed to recognize faces and hand gestures to trigger specific safety actions. It combines computer vision, deep learning, and IoT alerting mechanisms to ensure home safety and real-time responsiveness.

The system features:  
- **Hand gesture recognition** via a trained CNN model.  
- **Face recognition** for user authentication.  
- **Edge detection and image enhancement** for clear input.  
- **Audio alerts** and **Twilio integration** for message/call alerts.

This project demonstrates how artificial intelligence can be integrated into home automation systems for real-time surveillance, access control, and alert generation.

---

## Hypothesis
By integrating gesture and face recognition modules with edge detection and safety automation, it is hypothesized that:  

- The system can accurately recognize hand gestures (Help, Call, Danger, Thumbs Up/Down).  
- Unauthorized users will be detected and trigger alarms during SafeHouse Mode.  
- Edge-enhancement and contrast techniques will improve detection accuracy in varied lighting conditions.  
- Overall, SafeHomeCam will enhance home safety through a reliable and intelligent camera-based monitoring system.

---

## Objectives
- Implement real-time gesture and face recognition using OpenCV and cvzone.  
- Enhance camera input using Gamma correction and edge detection.  
- Activate audio and alert mechanisms on recognizing danger gestures or unknown faces.  
- Design a scalable, easy-to-use safety system for smart homes.

---

## Technologies Used


  numpy==1.26.4
  mediapipe==0.10.14
  tensorflow==2.15.0
  cvzone==1.6.1
  opencv-contrib-python==4.9.0.80
  playsound
  twilio

## Procedure
1. Setup Environment
    - Install dependencies using pip:
        - pip install -r requirements.txt
    - Ensure your webcam is connected and ready.

2. Face Recognition
    - Capture and encode known user faces.
    - Compare live faces with stored encodings.
    - Unknown faces trigger alerts during SafeHouse Mode.

3. Hand Gesture Detection
    - Detect hands using cvzone’s HandDetector.
    - Preprocess images: grayscale, gamma correction, contrast stretching, edge detection.
    - Classify gestures using the pre-trained CNN model.

4. SafeHouse Mode
    - Activate with Thumbs Up, deactivate with Thumbs Down (owner only).
    - Alerts triggered for Help, Call, Danger gestures.

5. Alert Mechanism
    - Play audio alerts (alarm.mp3, siren.mp3, Danger.wav).
    - Optionally send SMS/call via Twilio API.

## How to Run

1. Clone the repository:
    - git clone https://github.com/PrathamRajendraPednekar/SafeHomeCam.git
    - cd SafeHomeCam


2. Install all required dependencies:
    - pip install -r requirements.txt


3. Add known user faces to the faces directory (or wherever the face data is stored).

4. Run the main program:
    - python main.py


5. Interact with the system using hand gestures and watch for real-time alerts.
    - Thumbs Up → Activate SafeHouse Mode
    - Thumbs Down → Deactivate SafeHouse Mode (owner only)
    - Help / Call / Danger gestures → Trigger alerts

6. Optional: Configure Twilio credentials in your code to enable SMS/call notifications.









