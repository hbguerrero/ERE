# Reactive Fuzzy Row-Following Robot for Plantain Crops

This repository contains the **source code, ROS 2 nodes, ESP32 firmware, and experimental datasets** for a low-cost tracked robot performing **reactive fuzzy logic–based row following** in plantain crops.

---

## 📸 Field Pictures

<p align="center">
  <img src="docs/img/robot_field_side.jpg" alt="Robot side view in plantain field" width="45%"/>
  <img src="docs/img/robot_field_front.jpg" alt="Robot front view in plantain row" width="45%"/>
</p>

## 🎥 Demo Video

[Watch on YouTube](https://www.youtube.com/watch?v=u4LEPf4ucak&list=PLrb4Ia3jTb1fGVidyRJrpKlKpQCu3HL8m)

<p align="center">
  <a href="https://www.youtube.com/watch?v=u4LEPf4ucak&list=PLrb4Ia3jTb1fGVidyRJrpKlKpQCu3HL8m" target="_blank">
    <img src="https://img.youtube.com/vi/u4LEPf4ucak/hqdefault.jpg" alt="YouTube demo thumbnail" width="60%"/>
  </a>
</p>

## 📂 Repository Structure (actual)

| Path | Description |
|---|---|
| **`ROS2nodes/`** | ROS 2 Python nodes: LiDAR reading, wall-following (fuzzy), serial bridge to ESP32 (`lidarReadings.py`, `wallFollower.py`, `esp32_serial_bridge.py`). |
| **`esp32/`** | ESP32 firmware: `main.cpp` (PI control + dead-zone compensation + PWM), `platformio.ini`. |
| **`testes/CSV_ROBOT/`** | Experimental datasets (CSV) collected in field/park campaigns. Each subfolder is one experiment (e.g., `PruebaCampo2-cono160-setpoint1metro-distanciacultivo1metro/`, `prueba1_parque/`, etc.). **Contains `plotar.py`** for plotting. |
| **`docs/img/`** | Images used in the README (you should place `robot_field_side.jpg` and `robot_field_front.jpg` here). |

> Note: folders like `firmware/`, `ros2/`, or `data/` mentioned elsewhere are **not** present here. Use the paths above.

---

## 🧭 Quick Start (Plotting)

1) Go to the plotting script folder:
```bash
cd testes/CSV_ROBOT
```
## Using `plotar.py` (step-by-step guide)

`plotar.py` creates the plots from your experiment data in a chosen folder.

### 1) Requirements
Only once, install Python packages:
```bash
python3 -m venv .venv && source .venv/bin/activate
pip install numpy pandas matplotlib
```
---

## 🧩 Selecting a Different Experiment Folder (for `plotar.py`)

Each experiment folder inside `testes/CSV_ROBOT/` contains its own set of CSV files.  
The script `plotar.py` only plots **one experiment at a time**, based on the folder name defined in its configuration.

To change which dataset is plotted, follow these steps:

1️⃣ **Open a terminal and go to the script folder**
```bash
cd testes/CSV_ROBOT
```
