# 🏠 SafeHomeCam – AI-Based Smart Home Security System

SafeHomeCam is an **AI-powered home security system** that uses **real-time face recognition and hand gesture detection** to trigger safety actions such as alarms, SMS alerts, and emergency calls.  
It integrates **Computer Vision, Deep Learning, and IoT-based alerting** to enhance household safety.

<p align="center">
  <h4><u>Youtube Link : https://www.youtube.com/watch?v=MvPr1x2mDaw&t=19s</u></h4>
</p>


## 📌 Introduction

SafeHomeCam is an AI-based surveillance system designed to recognize **faces and hand gestures** to trigger predefined safety actions in real time.

The system combines:
- Hand gesture recognition using a CNN model  
- Face recognition for user authentication  
- Image enhancement using gamma correction and edge detection  
- Audio alerts and optional **Twilio-based SMS/call alerts**

This project demonstrates how AI can be effectively integrated into **smart home automation and security systems**.

---

## 🧪 Hypothesis

By integrating gesture recognition, face authentication, and image enhancement techniques:

- Hand gestures (Help, Call, Danger, Thumbs Up/Down) can be detected accurately  
- Unauthorized users can be detected during SafeHouse Mode  
- Edge detection and gamma correction improve recognition in low-light conditions  
- Overall home security can be enhanced through intelligent monitoring  

---

## 🎯 Objectives

- Implement real-time face and gesture recognition  
- Improve input quality using image preprocessing techniques  
- Trigger alerts for danger or unauthorized access  
- Build a scalable and intelligent home security solution  

---

## ⚙️ System Features

- 🔐 Face Recognition for authentication  
- ✋ Hand Gesture Detection (CNN-based)  
- 🏡 SafeHouse Mode (ON/OFF via gestures)  
- 🚨 Audio alarms and emergency alerts  
- 📩 SMS & 📞 Call alerts using Twilio  
- 📊 CSV-based event logging  

---

## 🧠 Model Training & Recognition

### 🔧 Tech1 – Gesture Dataset Creation
<p align="center">
  <img src="https://github.com/PrathamRajendraPednekar/SafeHomeCam/blob/main/Images/Tech1.png" width="800"/>
</p>

The hand gesture recognition model was trained using **Google Teachable Machine**.  
Multiple images for each gesture were captured under varying lighting conditions and hand orientations to improve robustness.

---

### 🔧 Tech2 – Model Export & Integration
<p align="center">
  <img src="https://github.com/PrathamRajendraPednekar/SafeHomeCam/blob/main/Images/Tech2.png" width="800"/>
</p>

The trained model was exported from **Teachable Machine** in **Keras (.h5)** format along with a labels file.  
This model is integrated into the system using **cvzone’s ClassificationModule** for real-time prediction.

---

### 👤 Face1 – Face Recognition
<p align="center">
  <img src="https://github.com/PrathamRajendraPednekar/SafeHomeCam/blob/main/Images/Face1.png" width="800"/>
</p>

The face recognition module authenticates users using the **face_recognition** library.  
Known faces are pre-encoded and compared with live webcam input.  
The system displays the detected user name, enabling secure access control for SafeHouse Mode.

---

## ✋ Gesture-Based Actions

### 🆘 Help
<p align="center">
  <img src="https://github.com/PrathamRajendraPednekar/SafeHomeCam/blob/main/Images/help.png" width="800"/>
</p>

Triggers an **audio alarm** and sends an **SMS alert** to the owner, indicating immediate assistance is required.

---

### 📞 Call
<p align="center">
  <img src="https://github.com/PrathamRajendraPednekar/SafeHomeCam/blob/main/Images/call.png" width="800"/>
</p>

Initiates an **emergency phone call** to the registered owner and sends an SMS notification.

---

### ⚠️ Danger
<h3 align="center">
  <img src="https://github.com/PrathamRajendraPednekar/SafeHomeCam/blob/main/Images/Danger.png" width="800"/>
</h3>

Triggers a **danger alert sound**, sends **SMS alerts to both owner and police**, and initiates an emergency call.

---

### 👍 Thumbs Up
<p align="center">
  <img src="https://github.com/PrathamRajendraPednekar/SafeHomeCam/blob/main/Images/Thumpus.png" width="800"/>
</p>

Activates **SafeHouse Mode** (authorized user only).  
Once enabled, unknown faces are continuously monitored.

---

### 👎 Thumbs Down
<p align="center">
  <img src="https://raw.githubusercontent.com/PrathamRajendraPednekar/SafeHomeCam/main/Images/ThumpusDown.png" width="800"/>
</p>

Deactivates **SafeHouse Mode**, restoring normal monitoring behavior.

🔐 **Access Control:**  
SafeHouse Mode **can only be turned ON or OFF by the owner (authorized person)**.  
Any gesture performed by an **unauthorized or unknown individual is ignored** and cannot change the system state.

---

### 📸 Intruder Image Capture (SafeHouse Mode)

When **SafeHouse Mode is ON**, the system actively monitors entries into the house.

- If an **unknown person** is detected:
  - 📷 The system automatically captures **5 images** of the individual
  - Images are captured at different moments to improve identification accuracy
  - ❌ **Authorized users are excluded** from image capture
- This ensures:
  - Strong privacy for trusted users
  - Reliable evidence collection for intrusions

---

### 📊 Gesture Activity Logging (`gesture_log.csv`)

All gesture-based actions are continuously recorded in a log file:

- File name: **`gesture_log.csv`**
- Logs include:
  - 🕒 **Date & time**
  - ✋ **Detected gesture**
  - ⚙️ **Action triggered**
  - 👤 **User status (authorized / unknown)**
- Useful for:
  - Daily activity monitoring
  - Security audits
  - Debugging gesture recognition

<p align="center">
  <img src="https://raw.githubusercontent.com/PrathamRajendraPednekar/SafeHomeCam/main/Images/Records.png" width="800"/>
</p>


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
