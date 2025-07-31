# 🏭 MOVEMENT-DETECTION-ON-CONVEYOR-BELT

<p align="justify">
  <em>NOTE: During my experience in the mining sector, I participated in the development of a visual inspection system using machine vision to detect movement in conveyor belts. Out of respect for confidentiality, no images or technical details of the actual system are shown. The documentation presented here is a simulated version developed by me for demonstration purposes.</em>
</p>

<p align="justify">
This project implements an image processing pipeline to **detect vertical motion** in conveyor belt systems using a video feed or a sequence of images. The primary goal is to determine whether a conveyor belt is **moving in the correct vertical direction** (upward or downward), which is especially useful in mining, logistics, and industrial automation scenarios where belts must operate in predefined patterns.

Unlike traditional monitoring systems that require physical sensors (encoders, proximity sensors, etc.), this solution is **completely vision-based** and relies only on a standard video camera and real-time frame analysis.
</p>

---

## 🎯 Objective

The algorithm is designed to:

- 🧭 **Identify vertical motion** in conveyor belts from video or image sequences.
- 🚫 **Filter out lateral or stationary movement**, focusing only on vertical direction changes.
- 📊 **Provide insights** that could help in fault detection, operational verification, or automation processes.

By eliminating the need for additional hardware, this approach lowers the cost and complexity of conveyor monitoring systems.

---

## 🧠 Key Features

- 🎥 **Camera-Based Motion Detection**  
  Detects movement patterns directly from video frames without needing specialized equipment.

- ⬆️ **Vertical Direction Isolation**  
  Uses motion vector analysis (via optical flow or difference frames) to isolate only vertical displacement.

- 🧮 **Frame-to-Frame Motion Estimation**  
  Applies techniques like dense optical flow or contour tracking to estimate movement.

- ⚙️ **Real-Time or Batch Mode**  
  Can run live from a camera or process stored video/image sequences.

- 💡 **Lightweight and Adaptable**  
  Suitable for Raspberry Pi, Jetson Nano, or other edge computing devices in industrial settings.

- 📦 **Optional Alerts and Logging**  
  Designed to be extended with alert triggers or performance logs.

---

## 🛠️ Technologies Used

- `Python 3.10`
- `OpenCV`
- `NumPy` 
- `Matplotlib` 
- `argparse`

---

## 🧠 How Does It Work?

The algorithm follows a structured, image-based approach to detect vertical movement on a conveyor belt. Here's a breakdown of the main stages:

1. **Video Input**  
   The system processes a video of the conveyor belt.

2. **Frame Analysis**  
   Each frame is converted to grayscale and prepared for motion detection.

3. **Motion Detection**  
   The algorithm compares frames to detect movement.

4. **Vertical Filtering**  
   Only vertical motion (up/down) is analyzed. Horizontal movement is ignored.

5. **Result Classification**  
   If vertical movement is detected consistently, it is labeled as "Moving Vertically"; otherwise, it is flagged as stationary or irregular.

6. **Visual Output**  
   Results are saved with annotations for easy review.

<div align="center">
  <img src="https://github.com/user-attachments/assets/b9adc71b-e551-4497-ba4c-34a2c210bf21" alt="OCR Output Sample" width="500"/>
  <p><em>This image shows how the algorithm works.</em></p>
</div>

> *The algorithm works without physical sensors and is ideal for low-cost monitoring using just a camera.*

---

## 📊 Impact

Implementing this movement detection system offers several key benefits in industrial environments:

- ⚙️ **Improved Process Control**  
  Allows real-time verification of conveyor belt movement to detect unexpected stops or jams.

- ⏱️ **Reduced Downtime**  
  Early detection of movement issues helps prevent prolonged interruptions and costly delays.

- 🧯 **Enhanced Safety**  
  Reduces the need for manual inspections in high-risk areas by providing continuous visual monitoring.

- 💰 **Low-Cost Integration**  
  The system uses only camera input and lightweight algorithms, making it scalable and easy to implement without modifying existing infrastructure.

> This tool supports more efficient operations by offering a simple and effective way to ensure materials are flowing as expected in automated production lines.

