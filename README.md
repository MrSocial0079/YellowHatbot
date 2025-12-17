# YellowHatBot – Autonomous Marking Robot (Prototype)

## Project Overview
YellowHatBot is a small-scale autonomous robot prototype designed to demonstrate **basic path-based marking** using simple hardware and Python-based control.  
The robot uses **two servos** (head and pencil) and an **ultrasonic sensor** to follow predefined paths derived from SVG files converted into grid-based JSON coordinates.  
The project focuses on feasibility, integration, and foundational robotics concepts rather than full autonomy.

---

## What This Project Does
- Executes predefined paths extracted from SVG files
- Controls a pencil/marker using a servo mechanism
- Uses ultrasonic sensing for basic obstacle detection
- Runs entirely on a Raspberry Pi 3 using Python and Jupyter notebooks

---

## What This Project Does NOT Do
- No full ROS implementation
- No sensor fusion or localization (EKF, SLAM, odometry)
- No camera-based navigation
- No closed-loop motor control
- No real-time map updates

This project is a **proof-of-concept prototype**, not an industrial system.

---

## Hardware Used
- Raspberry Pi 3
- GoPiGo robot base
- 2 Servo motors (head, pencil)
- Ultrasonic distance sensor
- 9.6V 2000 mAh battery
- microSD card (16GB+)

---

## Software Used
- Raspberry Pi OS (Raspbian)
- Python 3
- Jupyter Notebook
- BalenaEtcher (for flashing OS)

---

## Libraries Used

- **Python 3** – Core programming language  
- **Jupyter Notebook** – Interactive code execution  
- **NumPy** – Numerical calculations and arrays  
- **Matplotlib** – Data and path visualization  
- **json** – Path and coordinate storage  
- **time** – Execution delays and timing  
- **RPi.GPIO** – Raspberry Pi GPIO control  
- **gpiozero** – Simplified hardware control  
- **math** – Distance and angle calculations  
- **os** – File and directory handling  
- **sys** – System-level operations  

---

## System Architecture

### Planning Layer
- SVG file input
- Grid overlay for scaling
- Vector extraction
- Conversion to JSON path coordinates

### Control Layer
- Servo actuation logic
- Movement sequencing
- Obstacle detection using ultrasonic sensor

### Hardware Layer
- Raspberry Pi GPIO
- Servos and motors
- Ultrasonic sensor

---

## Installation & Setup Instructions

### Step 1 – Install Raspberry Pi OS
1. Download **Raspberry Pi OS (Raspbian)** image.
2. Install **BalenaEtcher** on your computer.
3. Insert microSD card.
4. In BalenaEtcher:
   - Select OS image  
   - Select SD card  
   - Flash  
5. Safely eject SD card.

---

### Step 2 – Boot Raspberry Pi 3
1. Insert SD card into Raspberry Pi.
2. Power on the Pi.
3. Complete initial setup.
4. Update system:
```bash
sudo apt update
sudo apt upgrade -y
