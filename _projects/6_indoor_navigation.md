---
layout: post
title: Indoor Navigation System
image: "/img/in-project/navigation_car.jpg"
tech:
  - name: "JavaScript"
    icon: "/img/tech/javascript.png"
  - name: "Python"
    icon: "/img/tech/python.png"
description: Created a real-time indoor navigation system in 24 hours, integrating experimental Wi-Fi signal platforms with a Python server and JavaScript interface. 1st Place Winner at HARD Hack 2023.
tags:
  - "Embedded System"
---

# Indoor Navigation System with Wi-Fi Signal Integration

## Overview
During HARD Hack 2023, a 24-hour IEEE hackathon, we developed a real-time indoor navigation system utilizing an experimental Wi-Fi signal platform (WiROS). The system combines a Python server for signal processing and JavaScript for visualization, offering a practical solution for indoor navigation and delivery. Our project earned the 1st Place Award for its innovation and functionality.

---

## Introduction
Indoor navigation is a challenging domain due to the lack of GPS signal reliability indoors. Our solution addresses this by leveraging Wi-Fi signals for triangulation and location tracking. The system provides accurate real-time navigation for indoor environments, with a user-friendly graphical interface for seamless operation.

---

## Hardware and Software Setup
- **Hardware**:
  - Raspberry Pi for server-side processing.
  - Experimental Wi-Fi signal platform (WiROS) for signal broadcasting and triangulation.

- **Software**:
  - **Python**: Signal processing and triangulation algorithm implementation.
  - **JavaScript**: Visualization of transmitter and receiver locations on a graphical interface.

![Image of Navgiation Car](/img/in-project/navigation_car.jpg)

---

## Key Features
### 1. Real-Time Indoor Navigation
- Triangulates user location using Wi-Fi signal strength and real-time processing.
- Delivers precise and dynamic location updates for seamless indoor navigation.

### 2. Signal Processing with Python
- Developed a Python server to handle Wi-Fi signal data and compute triangulated locations.
- Integrated with the experimental WiROS platform for signal strength data.

### 3. Visual Interface with JavaScript
- Built a graphical interface in JavaScript to represent the indoor map.
- Real-time visualization of transmitter and receiver locations for easy navigation.

---

## Challenges and Solutions
### Challenges:
1. **Accuracy in Signal Triangulation**: Wi-Fi signal variability posed challenges for consistent location accuracy.
2. **Real-Time Processing**: Ensuring low-latency signal processing on Raspberry Pi hardware.
3. **Graphical Interface Development**: Designing an intuitive and responsive interface within the hackathon time frame.

### Solutions:
1. Applied signal averaging techniques and optimized algorithms for stable triangulation.
2. Leveraged Python’s efficient libraries for signal processing to achieve low-latency performance.
3. Simplified interface design with clear visual indicators for transmitters and receivers.


---

## Results
- Achieved accurate real-time indoor navigation with Wi-Fi signals.
- Developed a responsive graphical interface for intuitive navigation.
- Delivered a working prototype within 24 hours, showcasing reliability and practical implementation.

---

## Achievements
- **1st Place Winner**: HARD Hack 2023, IEEE.
- Recognized for innovation in leveraging experimental Wi-Fi signal platforms and real-time processing for indoor navigation.

---

## Future Work
- Enhancing signal triangulation accuracy with machine learning algorithms.
- Expanding the platform to support multi-floor indoor navigation.
- Integrating additional sensors for hybrid signal-based navigation.

---

## Conclusion
This project demonstrates the potential of Wi-Fi-based solutions for addressing the challenges of indoor navigation. Winning 1st Place at HARD Hack 2023 reflects the innovation, teamwork, and practicality of our approach, paving the way for further advancements in navigation technologies.

---

**Acknowledgments**
Special thanks to the IEEE HARD Hack 2023 organizers and our team members for their dedication and collaboration during this intense 24-hour challenge.
