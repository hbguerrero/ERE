# ERE – Reactive Fuzzy Row-Following Robot for Plantain Crops

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)]()
[![ROS 2](https://img.shields.io/badge/ROS2-Jazzy-22314E.svg)]()
[![License](https://img.shields.io/badge/License-MIT-green.svg)]()

This repository contains the research and implementation of a **low-cost tracked robot** designed for **reactive fuzzy row following in plantain crops**.  
The system integrates **ROS 2 (Raspberry Pi 5)** for perception and supervision with **ESP32** microcontrollers for low-level motor control.

> **Paper:** *Reactive Fuzzy Control and Field Validation of a Low-Cost Autonomous Tracked Robot for Plantain Crop Row Following*  
> **Keywords:** agricultural robotics, fuzzy control, ROS 2, ESP32, LiDAR, plantain crops

---

## 🎥 Videos

A full playlist with field experiments, laboratory tests, and control demonstrations is available on YouTube:

🔗 **[Plantain Crop Robot – YouTube Playlist](https://www.youtube.com/playlist?list=PLrb4Ia3jTb1fGVidyRJrpKlKpQCu3HL8m)**

---

## 📸 Field Pictures

<p align="center">
  <img src="docs/img/robot_field_side.jpg" alt="Tracked robot side view in plantain crop" width="45%"/>
  <img src="docs/img/robot_field_front.jpg" alt="Front view of the robot navigating between rows" width="45%"/>
</p>

---

## 🧭 Project Overview

The **ERE robot** (Experimental Robotic Equipment) was designed for *in-field autonomous navigation* between plantain crop rows.  
It performs lateral distance estimation using a **YDLidar X2** and heading correction from a **BNO055 IMU**, feeding a **Mamdani-type fuzzy controller** that computes angular velocities for both tracks.

- **Architecture:** ROS 2 nodes on Raspberry Pi 5 communicate with an ESP32 running a PI controller and PWM actuation.  
- **Control Strategy:** Reactive fuzzy control with dead-zone compensation and velocity saturation (±12 V).  
- **Field Tests:** Conducted in real crop rows (spacing ≈ 3 m) under different canopy densities.

---

## 📂 Repository Layout

