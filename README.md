# Final-Year-Project

## 📌 Project Overview

Printed Circuit Boards are an essential part of electronic devices. Faults such as broken tracks, solder bridges, and other visible assembly defects can affect the performance and reliability of electronic products.

Traditional manual inspection is repetitive and time-consuming and can be affected by human fatigue.

This project aims to develop a low-cost automated PCB inspection system that captures a PCB image, processes it, compares it with a correct reference PCB, and provides a PASS/FAULT result.

The proposed hardware system uses a Raspberry Pi 4 and 8 MP camera, with LED lighting, LEDs, buzzer, display, and optional communication/storage modules.


## 🎯 Objectives

Automate visual PCB inspection.

Reduce repetitive manual inspection.

Detect visible PCB defects quickly and consistently.

Capture PCB images using a camera.

Process PCB images using OpenCV.

Compare an inspected PCB with a reference PCB.

Provide a clear PASS/FAIL result.

Provide visual and audio fault indication.

Build a low-cost Raspberry Pi-based inspection system.


## ✨ Features

Current Web Dashboard

📷 PCB image upload

🖼️ PCB image preview

🔍 Inspect PCB button

✅ PASS result display

❌ FAIL result display

🆔 Automatic PCB ID generation

📊 Confidence display

🕒 Date and time

📋 Inspection history

📱 Responsive web interface

Planned Hardware/AI Features

Raspberry Pi 4 integration

8 MP camera capture

OpenCV image preprocessing

Reference PCB comparison

AI-based defect detection

Green LED for PASS

Red LED for FAULT

Buzzer alarm

16×2 LCD display

PCB holder and controlled lighting

Data storage and optional remote monitoring

⚙️ Working Principle

1. System Initialization

The Raspberry Pi initializes the camera, GPIO, OpenCV, reference PCB image, display, LEDs, and buzzer.

2. PCB Placement

The PCB is placed in a fixed position below the camera. Controlled lighting helps maintain consistent image quality.

3. Image Capture

The camera captures an image of the PCB.

4. Image Preprocessing

The captured image can be processed using:

Image Capture
      ↓
Resize
      ↓
Noise Reduction
      ↓
Grayscale / Color Processing
      ↓
Image Alignment
      ↓
Reference Comparison

5. Fault Detection

The processed PCB image is compared with a correct reference PCB.

6. Final Decision

Difference < Threshold
        ↓
      PASS
        ↓
Green LED / Display

Difference > Threshold
        ↓
     FAULT
        ↓
Red LED + Buzzer / Display

💻 Current Web Prototype

The current frontend is implemented using:

HTML

CSS

JavaScript

The dashboard allows the user to upload a PCB image and preview it before inspection.

The current JavaScript uses a random demo result:

let fail = Math.random() > 0.5;

if (fail) {
    resultStatus.innerText = "FAIL";
    defect.innerText = "Broken Track";
    confidence.innerText = "95%";
} else {
    resultStatus.innerText = "PASS";
    defect.innerText = "No Defect";
    confidence.innerText = "98%";
}

This is only for testing the interface. It is not the final AI fault-detection algorithm.

🧰 Hardware Components

Component

Function

Raspberry Pi 4 Model B

Main processing unit

8 MP Camera

PCB image capture

Green LED

PASS indication

Red LED

FAULT indication

Buzzer

Fault alarm

Push Button

Starts inspection

220–330 Ω Resistors

LED current limiting

PCB Holder

Fixed PCB positioning

LED Ring Light

Consistent illumination

16×2 LCD

Result display

MicroSD Card

Software/data storage

🛠️ Technology Stack

Technology

Purpose

HTML

Web interface

CSS

Dashboard design

JavaScript

Frontend interaction

Python

Planned backend processing

OpenCV

Image processing

Raspberry Pi 4

Embedded processing

Camera

PCB image acquisition

AI / Deep Learning

Planned defect detection

GPIO

Planned LED/buzzer control

📂 Repository Structure

PCB-Fault-Detection-System/
│
├── README.md
│
├── frontend/
│   └── index.html
│
├── backend/
│   ├── inspection.py
│   ├── image_processing.py
│   └── gpio_control.py
│
├── models/
│   └── model_files/
│
├── reference_images/
│   └── reference_pcb.jpg
│
├── test_images/
│   ├── pcb_001.jpg
│   └── pcb_002.jpg
│
├── hardware/
│   ├── block_diagram.png
│   └── circuit_diagram.png
│
└── requirements.txt

🚀 How to Run the Current Web Demo

1. Clone the repository

git clone https://github.com/YOUR-USERNAME/PCB-Fault-Detection-System.git

2. Enter the project directory

cd PCB-Fault-Detection-System

3. Open the frontend

Open:

frontend/index.html

in your browser.

4. Test the dashboard

Click Choose PCB Image.

Select a PCB image.

The image will appear on the dashboard.

Click Inspect PCB.

The demo will display PASS or FAIL.

🤖 Future AI Implementation

The planned final system will replace the random demo result with an actual computer-vision/AI pipeline.

Camera Image
     ↓
Preprocessing
     ↓
Image Alignment
     ↓
AI / OpenCV Detection
     ↓
Defect Classification
     ↓
Confidence Score
     ↓
PASS / FAIL
     ↓
LED + Buzzer + Display

Possible defect classes include:

Broken Track

Solder Bridge

Missing Component

Wrong Component

Component Misalignment

Other visible defects depending on the dataset

Final defect classes will depend on the dataset and trained model used in the implementation.

📈 Development Roadmap

Create PCB inspection dashboard

Implement PCB image upload

Implement image preview

Implement demo PASS/FAIL result

Add PCB ID and inspection time

Add inspection history

Connect Raspberry Pi 4

Connect 8 MP camera

Implement OpenCV preprocessing

Implement reference PCB comparison

Build PCB defect dataset

Train/evaluate AI model

Connect GPIO LEDs

Connect buzzer

Add LCD display

Add real-time inspection

Add data logging

Add optional cloud/web monitoring

📊 Project Status

Module

Status

Web Dashboard

✅ Completed

Image Upload

✅ Completed

Image Preview

✅ Completed

Demo Inspection

✅ Completed

PCB ID

✅ Completed

Inspection History

✅ Completed

Raspberry Pi

🔄 Planned

Camera

🔄 Planned

OpenCV

🔄 Planned

Reference Comparison

🔄 Planned

AI Detection

🔄 Planned

GPIO

🔄 Planned

LCD

🔄 Planned

Buzzer

🔄 Planned

Cloud Monitoring

🔄 Future

📚 Literature Survey

The project presentation references research related to automated PCB inspection and deep-learning-based PCB defect detection.

Automatic PCB Inspection Algorithms: A Survey

M. Moganti, F. Ercal, C. H. Dagli, and S. Tsunekawa

"Automatic PCB Inspection Algorithms: A Survey"

Computer Vision and Image Understanding, Vol. 63, No. 2, pp. 287–313, 1996.

DOI: 10.1006/cviu.1996.0020

Defect Detection of Printed Circuit Board Assembly Based on YOLOv5

Minghui Shen et al.

"Defect Detection of Printed Circuit Board Assembly Based on YOLOv5"

Scientific Reports, 2024.

👥 Project Team

Priyadarshini College of Engineering, Nagpur
Department of Electronics and Telecommunication Engineering
Session: 2026–2027

Roll No.

Team Member

130

Chetan Kanoje

136

Kundan Wadibhasme

151

Yash Motharkar

155

Prajwal Agashe

158

Sakshi Suryawanshi

Project Guide

Dr. (Mrs.) S.P. Washimkar

📷 Project Screenshots

Add your actual dashboard screenshot here:

![PCB Fault Detection Dashboard](images/dashboard.png)

Recommended GitHub images:

images/
├── dashboard.png
├── block-diagram.png
├── circuit-diagram.png
└── hardware-setup.jpg

🔮 Future Scope

The system can be extended with:

Real-time camera inspection

Deep-learning-based defect classification

Automatic defect localization

Conveyor-based automatic PCB feeding

Production-line integration

Inspection database

Cloud data storage

Remote monitoring

Mobile/web notifications

Automatic inspection reports

⚠️ Current Limitations

The current GitHub version is primarily a frontend prototype.

The current web interface does not yet perform real PCB defect detection. The inspection result is simulated using JavaScript.

The complete system will require:

Raspberry Pi hardware

Camera integration

Controlled lighting

OpenCV processing

Reference image comparison and/or trained AI model

GPIO hardware control

A suitable PCB image dataset

📖 References

M. Moganti, F. Ercal, C. H. Dagli, and S. Tsunekawa, Automatic PCB Inspection Algorithms: A Survey, Computer Vision and Image Understanding, 1996.

Raspberry Pi 4 Model B official specifications.

Raspberry Pi documentation.

OpenCV documentation.

Minghui Shen et al., Defect Detection of Printed Circuit Board Assembly Based on YOLOv5, Scientific Reports, 2024.

⭐ Acknowledgement

This project is developed as an academic project by the Department of Electronics and Telecommunication Engineering, Priyadarshini College of Engineering, Nagpur.
