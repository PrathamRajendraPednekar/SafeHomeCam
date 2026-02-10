# 🏠 SafeHomeCam – AI-Based Smart Home Security System

SafeHomeCam is an **AI-powered smart home security system** that uses **real-time face recognition and hand gesture detection** to trigger safety actions such as alarms, SMS alerts, and emergency calls.  
It integrates **Computer Vision, Deep Learning, and IoT-based alerting** to enhance household safety.

<img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
<p align="center">
  <h4>🎥 YouTube Demo: https://www.youtube.com/watch?v=MvPr1x2mDaw&t=19s</h4>
</p>

---

## 📑 Table of Contents

- [📌 Introduction](#-introduction)
- [🧪 Hypothesis](#-hypothesis)
- [🎯 Objectives](#-objectives)
- [⚙️ System Features](#️-system-features)
- [🧠 Model Training & Recognition](#-model-training--recognition)
  - [🔧 Tech1 – Gesture Dataset Creation](#-tech1--gesture-dataset-creation)
  - [🔧 Tech2 – Model Export & Integration](#-tech2--model-export--integration)
  - [👤 Face1 – Face Recognition](#-face1--face-recognition)
- [✋ Gesture-Based Actions](#-gesture-based-actions)
  - [🆘 Help](#-help)
  - [📞 Call](#-call)
  - [⚠️ Danger](#️-danger)
  - [👍 Thumbs Up](#-thumbs-up)
  - [👎 Thumbs Down](#-thumbs-down)
- [📸 Intruder Image Capture (SafeHouse Mode)](#-intruder-image-capture-safehouse-mode)
- [📊 Gesture Activity Logging](#-gesture-activity-logging-gesture_logcsv)
- [🧰 Technologies Used](#-technologies-used)
- [🛠 Installation & Setup](#-installation--setup)

---

## 📌 Introduction

SafeHomeCam is an AI-based surveillance system designed to recognize **faces and hand gestures** in real time to trigger predefined safety actions.

The system integrates:
- Hand gesture recognition using a CNN-based model  
- Face recognition for secure user authentication  
- Image enhancement using gamma correction and edge detection  
- Audio alerts and **Twilio-based SMS & call alerts**

This project demonstrates the practical integration of **AI and computer vision** in smart home security systems.

---

## 🧪 Hypothesis

By integrating gesture recognition, face authentication, and image enhancement techniques:

- Hand gestures (Help, Call, Danger, Thumbs Up/Down) can be detected accurately  
- Unauthorized users can be identified during SafeHouse Mode  
- Image preprocessing improves recognition in low-light conditions  
- Overall home security can be enhanced through intelligent monitoring  

---

## 🎯 Objectives

- Implement real-time face and hand gesture recognition  
- Enhance video input using image preprocessing techniques  
- Trigger alerts for danger and unauthorized access  
- Develop a scalable and intelligent smart home security solution  

---

## ⚙️ System Features

- 🔐 Face recognition for authentication  
- ✋ CNN-based hand gesture detection  
- 🏡 SafeHouse Mode (gesture-controlled)  
- 🚨 Audio alarms for emergency events  
- 📩 SMS & 📞 Call alerts using Twilio API  
- 📊 CSV-based gesture and activity logging  

---

## 🧠 Model Training & Recognition

### 🔧 Tech1 – Gesture Dataset Creation

<p align="center">
  <img src="https://github.com/PrathamRajendraPednekar/SafeHomeCam/blob/main/Images/Tech1.png" width="800"/>
</p>

The hand gesture model was trained using **Google Teachable Machine**.  
Images were captured under various lighting conditions and orientations to ensure robustness.

---

### 🔧 Tech2 – Model Export & Integration

<p align="center">
  <img src="https://github.com/PrathamRajendraPednekar/SafeHomeCam/blob/main/Images/Tech2.png" width="800"/>
</p>

The trained model was exported in **Keras (.h5)** format along with label files and integrated using **cvzone’s ClassificationModule** for real-time predictions.

---

### 👤 Face1 – Face Recognition

<p align="center">
  <img src="https://github.com/PrathamRajendraPednekar/SafeHomeCam/blob/main/Images/Face1.png" width="800"/>
</p>

Face authentication is implemented using the **face_recognition** library.  
Authorized faces are pre-encoded and matched with live webcam input to control system access.

---

## ✋ Gesture-Based Actions

### 🆘 Help

<p align="center">
  <img src="https://github.com/PrathamRajendraPednekar/SafeHomeCam/blob/main/Images/help.png" width="800"/>
</p>

- Triggers an **audio alarm**
- Sends an **SMS alert** to the owner requesting immediate help

---

### 📞 Call

<p align="center">
  <img src="https://github.com/PrathamRajendraPednekar/SafeHomeCam/blob/main/Images/call.png" width="800"/>
</p>

- Initiates an **emergency phone call**
- Sends an SMS notification to the owner

---

### ⚠️ Danger

<p align="center">
  <img src="https://github.com/PrathamRajendraPednekar/SafeHomeCam/blob/main/Images/Danger.png" width="800"/>
</p>

- Plays a danger alert sound  
- Sends SMS alerts to **owner and police**  
- Initiates an emergency call  

---

### 👍 Thumbs Up

<p align="center">
  <img src="https://github.com/PrathamRajendraPednekar/SafeHomeCam/blob/main/Images/Thumpus.png" width="800"/>
</p>

- Activates **SafeHouse Mode**
- Works **only for authorized users**
- Enables continuous monitoring of unknown faces

---

### 👎 Thumbs Down

<p align="center">
  <img src="https://raw.githubusercontent.com/PrathamRajendraPednekar/SafeHomeCam/main/Images/ThumpusDown.png" width="800"/>
</p>

- Deactivates **SafeHouse Mode**
- Restores normal monitoring behavior

🔐 **Access Control:**  
SafeHouse Mode can **only be enabled or disabled by the authorized owner**.  
Gestures from **unauthorized or unknown users are ignored**.

---

## 📸 Intruder Image Capture (SafeHouse Mode)

When SafeHouse Mode is **ON**:

- If an **unknown person** is detected:
  - 📷 Automatically captures **5 images**
  - Images are taken at different moments
  - ❌ Authorized users are excluded
- Ensures privacy protection and strong evidence collection

---

## 📊 Gesture Activity Logging (`gesture_log.csv`)

All system activities are logged in a CSV file:

- 🕒 Date & time  
- ✋ Detected gesture  
- ⚙️ Action triggered  
- 👤 User status (authorized / unknown)

<p align="center">
  <img src="https://raw.githubusercontent.com/PrathamRajendraPednekar/SafeHomeCam/main/Images/Records.png" width="800"/>
</p>

---

## 🧰 Technologies Used

- Python  
- OpenCV  
- cvzone  
- MediaPipe  
- TensorFlow / Keras  
- NumPy  
- face_recognition  
- Twilio API  

---

## 🛠 Installation & Setup

```bash
git clone https://github.com/PrathamRajendraPednekar/SafeHomeCam.git
cd SafeHomeCam
pip install -r requirements.txt
