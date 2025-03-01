---
layout: post
title: Autonomous Vehicle
image: "/img/in-project/vehicle.jpg"
tech:
  - name: "Nvidia Cuda"
    icon: "/img/tech/nvidia.jpg"
    url: "https://github.com/jetson-nano"
  - name: "OpenCV"
    icon: "/img/tech/opencv.png"
    url: "https://github.com/opencv"
  - name: "Python"
    icon: "/img/tech/python.png"
description: Built an autonomous vehicle prototype with lane following, GPS path tracking, and dynamic lane switching, displaying robotics and AI capabilities.
tags:
  - AI/ML
  - "Embedded System"
---

# Autonomous Vehicle Development with Jetson Nano and Donkey car

## Overview
In this project, we explored autonomous driving using the Jetson Nano platform. Our implementation included lane following with computer vision, GPS-guided follow laps, and dynamic lane switching using OpenCV. This project demonstrates our capability in embedded systems, robotics, and AI.

---

## Introduction
Autonomous vehicles are at the forefront of modern technology. This project focuses on building a scaled-down prototype capable of autonomous navigation using the Nvidia Jetson Nano, leveraging computer vision, GPS, and machine learning techniques.

---

## Hardware Setup
- **Microcontroller**: Nvidia Jetson Nano
- **Sensors**: USB Camera, GPS Module
- **Actuators**: Servo motor for steering, ESC for throttle
- **Other Components**: Wireless relay for emergency stop, LEDs for system feedback

**Image Slot**: Add an image showcasing the hardware assembly.

---

## Software Architecture
- **Operating System**: Ubuntu for Jetson Nano
- **Frameworks**: OpenCV, ROS2, DonkeyCar AI
- **Programming Language**: Python

**Image Slot**: Add a system diagram or architecture flowchart.

---

## Computer Vision: Lane Following
We implemented lane-following using OpenCV, detecting lane markers through edge detection and color segmentation. This module adjusts the vehicle's steering dynamically to stay within lanes.

**Steps**:
1. Preprocess the input image (grayscale conversion, Gaussian blur).
2. Apply edge detection (Canny).
3. Perform Hough Transform to identify lane lines.
4. Calculate steering angles using the detected lane position.

**Image Slot**: Add screenshots or images of lane detection in action.

---

## GPS Integration: Follow Laps
The GPS module was integrated to record and replay laps. The vehicle followed a pre-recorded path using real-time GPS data to calculate position and make course corrections.

**Steps**:
1. Record waypoints during the initial manual lap.
2. Use PID control to minimize cross-track error while following the saved path.

**Image Slot**: Include images or a map showing the recorded and replayed GPS paths.

---

## Dynamic Lane Switching
Using computer vision and real-time decision-making, the vehicle dynamically switched lanes based on lane availability.

**Key Highlights**:
- Adaptive algorithms to detect lane boundaries in varying lighting conditions.
- OpenCV pipeline integrated with the Jetson Nano's GPU for real-time processing.

**Image Slot**: Add video frames showing the lane-switching process.

---

## Challenges and Solutions
### Challenges:
1. **Limited GPU Power**: The Jetson Nano's computational capacity required optimizing our OpenCV pipeline.
2. **Noise in GPS Data**: Signal interference led to minor inaccuracies in path following.
3. **Real-Time Constraints**: Achieving low-latency processing for decision-making.

### Solutions:
1. Used GPU-accelerated OpenCV for efficient processing.
2. Implemented a Kalman filter to smooth GPS data.
3. Leveraged asynchronous programming to handle real-time inputs.

**Image Slot**: Add examples showing before-and-after optimization results.

---

## Results
Our autonomous vehicle achieved:
- Accurate lane detection and following.
- GPS path-following precision within 0.5 meters of the recorded path.
- Smooth and reliable dynamic lane switching.

**Image Slot**: Add a final demo or highlight reel image showcasing the project in action.

---

## Future Work
- Integrating LIDAR for obstacle detection.
- Enhancing GPS accuracy with RTK corrections.
- Testing on more complex environments like intersections and urban layouts.

---

## Conclusion
This project exemplifies the fusion of computer vision, embedded systems, and AI to create a functional autonomous vehicle prototype. It is a testament to the potential of accessible hardware and open-source software in solving complex engineering problems.

---

**Acknowledgments**
Special thanks to UCSD's ECE & MAE 148 team and our mentor for guidance throughout the project.

