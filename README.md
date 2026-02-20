<<<<<<< HEAD
# Real-Time-Road-Anomaly-Detection-
3- Real-Time Road Anomaly Detection from Dashcam Footage on Raspberry Pi
=======
# 🚧 Offline Real-Time Pothole Detection System  
### ARM-Based Edge AI Deployment using YOLOv8

---

## 📌 Problem Statement

Develop a fully offline, real-time pothole detection system that runs entirely on ARM-based embedded hardware without any cloud dependency.

The system should:

- Capture live road video
- Detect potholes in real time
- Operate completely offline
- Run efficiently on Raspberry Pi
- Be portable and low-cost

---

## 🧠 Project Overview

This project implements a real-time pothole detection system using the YOLOv8 deep learning model deployed on a Raspberry Pi (ARM architecture).

The system:

- Captures live road footage using a USB camera  
- Processes frames locally using YOLOv8  
- Detects potholes with bounding boxes  
- Displays annotated output on HDMI monitor  
- Runs 100% offline (no cloud APIs)

This demonstrates that modern AI models can be deployed on resource-constrained embedded systems for intelligent transportation applications.

---

## 🏗 System Architecture

```
USB Camera
     ↓
Frame Capture (OpenCV)
     ↓
YOLOv8 Inference Engine
     ↓
Bounding Box Detection
     ↓
Non-Maximum Suppression
     ↓
HDMI Display Output
```

---

## 🖥 Hardware Requirements

- Raspberry Pi 4 / Raspberry Pi 5  
- MicroSD Card (32GB recommended)  
- USB Webcam / Dashcam  
- HDMI Monitor  
- 5V 3A Power Supply  
- Optional: Cooling fan or heatsink  

---

## 💻 Software Stack

- Python 3.10+  
- Raspberry Pi OS (Bullseye / Bookworm)  
- Ultralytics YOLOv8  
- OpenCV  
- PyTorch (CPU version)  
- NumPy  

---

## 📂 Project Structure

```
offline-pothole-detection/
│
├── main.py
├── requirements.txt
├── model/
│   └── best.pt
├── utils/
├── results/
└── README.md
```

---

## ⚙️ Setup & Installation

### 1️⃣ Update the System

```bash
sudo apt update
sudo apt upgrade -y
```

### 2️⃣ Install System Dependencies

```bash
sudo apt install -y python3-pip python3-dev
```

### 3️⃣ Install Python Libraries

```bash
pip3 install -r requirements.txt
```

`requirements.txt` should include:

```
ultralytics
opencv-python
torch
numpy
```

---

### 4️⃣ Download / Place YOLO Model

Download your pretrained pothole detection model (`best.pt`).

Place it inside:

```
offline-pothole-detection/model/
```

Make sure the model path inside `main.py` matches the filename.

---

### 5️⃣ Verify Camera Detection

Check if camera is detected:

```bash
ls /dev/video*
```

Test camera:

```bash
ffplay /dev/video0
```

---

### 6️⃣ Run the Detection System

```bash
python3 main.py
```

The system will:

- Capture live video  
- Detect potholes  
- Draw bounding boxes  
- Display output in real time  

---

## 🔍 Detection Pipeline

1. Frame captured using OpenCV  
2. Frame resized and preprocessed  
3. YOLOv8 performs inference  
4. Bounding boxes predicted  
5. Confidence filtering applied  
6. Non-Maximum Suppression removes overlaps  
7. Annotated frame displayed  

---

## 🧠 AI Model Details

Model Used: **YOLOv8n (Nano Version)**

Why YOLOv8n?

- Lightweight architecture  
- Optimized for CPU inference  
- Lower RAM usage  
- Suitable for ARM-based deployment  

YOLO performs object detection in a single forward pass, making it suitable for real-time applications.

---

## 📊 Performance (Raspberry Pi 4 - CPU)

- Inference Time: 200–500 ms per frame  
- Frame Rate: 2–5 FPS  
- CPU Usage: High during inference  
- RAM Usage: Moderate  

Performance depends on:

- Input resolution  
- Model size  
- Background processes  

---

## 🔐 Offline & Privacy

- No cloud processing  
- No external API calls  
- No internet required during operation  
- All inference done locally  

This makes it suitable for:

- Highways  
- Rural deployments  
- Smart city edge systems  
- Secure environments  

---

## 🚀 Applications

- Municipal road inspection vehicles  
- Smart transportation monitoring  
- Infrastructure maintenance systems  
- Autonomous vehicle assistance  
- Smart city analytics  

---

## 🔮 Future Improvements

- GPS integration for pothole mapping  
- Multi-class road damage detection  
- Cloud dashboard integration  
- Hardware acceleration (Coral TPU)  
- Real-time alert notification system  

---

## 📜 License

MIT License

---

## 👨‍💻 Author

**Kishore Prabhakaran**  
B.E. Electronics and Communication Engineering  
Sri Shakthi Institute of Engineering and Technology
>>>>>>> 2e4bd26460da5d86c6b4dce4928a08b14bf87ef4
