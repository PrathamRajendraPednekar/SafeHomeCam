# SafeHomeCam

**SafeHomeCam** is an AI-based home security system that uses real-time face recognition and hand gesture detection to enhance safety. It triggers alarms, SMS alerts, and emergency calls using computer vision, deep learning, and IoT-based automation.

---

## Table of Contents
1. [Introduction](#introduction)
2. [Hypothesis](#hypothesis)
3. [Objectives](#objectives)
4. [Technologies Used](#technologies-used)
5. [Procedure](#procedure)
6. [Discussion](#discussion)
7. [Conclusion](#conclusion)
8. [Future Scope](#future-scope)
9. [References](#references)

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
```text
numpy==1.26.4
mediapipe==0.10.14
tensorflow==2.15.0
cvzone==1.6.1
opencv-contrib-python==4.9.0.80
playsound
twilio
face_recognition
pyttsx3
