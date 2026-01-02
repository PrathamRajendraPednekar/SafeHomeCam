# SafeHomeCam
🔐 Project Overview

SafeHomeCam is an AI-powered smart home security system that uses computer vision, deep learning, and real-time alert mechanisms to enhance home safety.
The system recognizes hand gestures and faces through a live camera feed to trigger predefined security actions such as alarms, SMS alerts, emergency calls, and SafeHouse mode activation.

It combines:

Hand gesture recognition using a trained CNN model

Face recognition for authentication and intrusion detection

Image enhancement techniques for improved accuracy

Real-time audio alerts and Twilio-based SMS/call notifications

🚀 Key Features

✅ Real-time Hand Gesture Recognition

Help

Call

Danger

Thumbs Up (Enable SafeHouse Mode)

Thumbs Down (Disable SafeHouse Mode)

✅ Face Recognition & Authentication

Recognizes authorized users

Detects unknown faces during SafeHouse Mode

✅ SafeHouse Mode

Activated only by authorized user

Triggers siren, captures images, and sends alerts on intrusion

✅ Alert System

Alarm & siren sounds

SMS notifications

Emergency calls using Twilio API

✅ Image Enhancement Pipeline

Grayscale conversion

Gamma correction

Contrast stretching

Edge detection (Canny)

✅ Event Logging

Gesture and face events stored in CSV with timestamps

🧠 Technologies Used

Python

OpenCV

cvzone

TensorFlow / Keras

MediaPipe

face_recognition

Twilio API

NumPy

Playsound

📂 Project Structure
SafeHomeCam/
│
├── Main.py
├── requirements.txt
├── gesture_log.csv
│
├── Data/
│   └── faces/
│       ├── Pratham/
│       ├── Mheet/
│       └── Others/
│
├── Model/
│   ├── keras_model.h5
│   └── labels.txt
│
├── Captured_Frames/
│   └── Unknown_*.jpg
│
├── alarm.wav
├── Danger.wav
└── siren.mp3

⚙️ Installation & Setup
1️⃣ Clone the Repository
git clone https://github.com/your-username/SafeHomeCam.git
cd SafeHomeCam

2️⃣ Install Dependencies
pip install -r requirements.txt

3️⃣ Setup Face Data

Add authorized user images inside:

Data/faces/<Person_Name>/

4️⃣ Setup Twilio

Update the following in Main.py:

account_sid = "YOUR_TWILIO_SID"
auth_token = "YOUR_TWILIO_AUTH_TOKEN"
twilio_number = "+1XXXXXXXXXX"
owner_number = "+91XXXXXXXXXX"

5️⃣ Run the Project
python Main.py


Press Q to exit.

🧪 Working Logic

Camera captures live video

Hand gestures are detected and classified using CNN

Face recognition runs in parallel

Gesture must be held for 3 seconds to avoid false triggers

SafeHouse Mode controls intrusion detection

Alerts are triggered based on detected gesture or face

📊 Test Results
Test Case	Input	System Response
Known Face + Thumbs Up	Gesture held	SafeHouse Mode ON
Unknown Face + SafeHouse Mode	3 sec detection	Siren + Alerts
Help Gesture	Detected	Alarm Sound
Call Gesture	Detected	SMS + Call
Thumbs Down + Owner Face	Detected	SafeHouse Mode OFF
📈 Advantages

High accuracy due to image enhancement

Prevents false alerts using gesture-hold mechanism

Works in low-light conditions

Modular and scalable architecture

🔮 Future Scope

Mobile application for live monitoring

Cloud-based storage and analytics

Advanced CNN models for better accuracy

Object detection for suspicious activity

Integration with smart locks and IoT devices
