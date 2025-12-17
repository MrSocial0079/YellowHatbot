# YellowHatBot – Autonomous Marking Robot (Prototype)

## Overview
YellowHatBot is a small-scale robotics prototype that demonstrates **basic path-based marking** using simple hardware and Python control on a **Raspberry Pi 3**.  
The robot uses **two servos** (head and pencil) and an **ultrasonic sensor** to execute predefined paths derived from **SVG files converted into JSON coordinates**.  
This project focuses on **foundational robotics integration**, not full autonomy.

---

## Problem & Significance
Manual pavement and parking-lot marking is labor-intensive and inconsistent.  
This project explores whether a **low-cost robotic system** can automate simple marking tasks using minimal hardware and software complexity.

---

## Course Concepts Applied
- Coordinate mapping and spatial reasoning  
- Servo-based actuator control  
- Sensor-based obstacle detection  
- Discrete path planning (SVG → JSON)  
- Hardware–software integration  

---

## System Summary
**Hardware:** Raspberry Pi 3, GoPiGo base, 2 servos (head, pencil), ultrasonic sensor  
**Software:** Raspberry Pi OS, Python 3, Jupyter Notebook  
**Control:** Open-loop motion with timed commands and servo actuation  

---

## Libraries Used
- Python 3 – Core programming language  
- Jupyter Notebook – Interactive execution  
- NumPy – Numerical calculations  
- Matplotlib – Path visualization  
- json – Coordinate storage  
- time – Execution timing  
- RPi.GPIO – GPIO control  
- gpiozero – Hardware abstraction  
- math – Distance calculations  

---

## Implementation
Paths are designed as **SVG files**, scaled using a grid, converted into **JSON coordinate lists**, and executed sequentially.  
The pencil servo is lowered during marking and raised between segments.  
An ultrasonic sensor continuously checks for obstacles and stops motion when a threshold distance is detected.

---

## Limitations
- No ROS implementation  
- No localization, SLAM, or odometry  
- No camera-based navigation  
- Open-loop motion control  
- Static environment assumption  

---

## Results
- Successfully executed predefined marking paths  
- Reliable pencil servo control  
- Functional ultrasonic obstacle detection  
- Demonstrated end-to-end prototype operation  

---

## Future Work
- Closed-loop motor control  
- ROS-based architecture  
- Improved mechanical stability  
- Higher-performance compute platform  

---

## Team Contributions
- Path planning and SVG-to-JSON conversion  
- Hardware wiring and servo integration  
- Control logic and testing  

---

## Setup (Brief)
1. Flash Raspberry Pi OS using **BalenaEtcher**  
2. Boot Raspberry Pi 3 and update system  
3. Install Python, Jupyter, and required libraries  
4. Copy `.ipynb` files to the Pi  
5. Connect to GoPiGo Wi-Fi  
6. Run notebooks using Jupyter  

---

## References
- Raspberry Pi Documentation  
- Python Official Documentation  
- Ultrasonic Sensor Datasheets  
- Course lecture materials  
