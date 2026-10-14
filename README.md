# ☀️ Active Dual-Axis Solar Tracking System

## 📌 Overview
An automated, closed-loop mechatronic system designed to maximize photovoltaic energy capture. This project utilizes an active dual-axis tracking architecture to continuously align solar panels with peak solar irradiation, resulting in a **>30% increase in electricity production efficiency** compared to fixed-angle stationary panels.

## ⚙️ Hardware Architecture
The system relies on a differential light-sensing array feeding into a programmable logic controller (PLC) / microcontroller to drive multi-axis movement.
* **Sensors:** 4x Light Dependent Resistor (LDR) array (Top/Bottom, Left/Right differentials)
* **Actuation:** 2x Stepper Motors for Pan (Yaw) and Tilt (Pitch) axes
* **Control:** Closed-loop feedback via PLC / Microcontroller
* **Power Delivery:** Electromagnetic relay modules

## 💻 Control Logic 
The core tracking logic is written in **C++**. It continuously samples analog signals from the LDR sensor array, calculates vertical and horizontal light differentials, and applies a deadband filter to prevent motor jitter during minor environmental light fluctuations (e.g., passing clouds). 

*See `solar_tracker_firmware.cpp` for the bare-metal control implementation.*

## 📊 Key Results & Performance
* **Dynamic Tracking:** Successfully implemented continuous East-to-West daily tracking and seasonal elevation adjustments.
* **Efficiency Gains:** Validated the theoretical maximum power per unit area, capturing significantly more energy throughout the day than static PV counterparts.
* **System Stability:** Minimized mechanical wear and power draw by utilizing optimized threshold-based movement logic.

---
*Note: This repository contains the modernized control logic and architectural overview of a physical mechatronics project.*
