# Robot Shield – ATmega328P Controller

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![GitHub last commit](https://img.shields.io/github/last-commit/MNik-EV/Robot-Shield-ATmega328)](https://github.com/MNik-EV/Robot-Shield-ATmega328/commits/main)

A compact, open-source **robot controller shield** designed around the **ATmega328P** microcontroller.  
This board integrates robust power protection, dual battery monitoring, multiple user interfaces, and plug-and-play Arduino IDE compatibility.

---

## 🚀 Main Board Render

<p align="center">
  <img src="Images/Isometric_View_3D.png" width="600"/>
</p>

---

## 🖼 Additional Views

| **Top View** | **Bottom View** |
|:---:|:---:|
| <img src="Images/Top_View_3D.png" width="300"/> | <img src="Images/Bottom_View_3D.png" width="300"/> |

---

## ✨ Features & Specifications

| Feature | Description |
|:---|:---|
| **Microcontroller** | ATmega328P running at **16 MHz** |
| **Programming Interface** | CP2102 USB-to-UART with **Auto-Reset** |
| **Input Protection** | PTC Resettable Fuse, TVS Diode, Reverse Polarity Protection |
| **Power Supply** | 12 V input → 5 V (Buck Converter) + 3.3 V (LDO) |
| **Battery Monitoring** | **LM3914** LED bar graph + **MAX17043** digital fuel gauge (I²C) |
| **User Input** | 5 push-buttons with hardware debounce |
| **User Output** | 0.96" I²C OLED, buzzer with transistor driver |
| **Dimensions** | 60 mm × 80 mm |

---

## 📐 Schematics

| **Power** | **MCU** | **USB-to-UART (CP2102)** |
|:---:|:---:|:---:|
| <img src="Images/Schematic_Power.png" width="250"/> | <img src="Images/Schematic_MCU.png" width="250"/> | <img src="Images/Schematic_CP2102.png" width="250"/> |

| **Push Buttons** | **OLED & Buzzer** | **Battery Fuel Gauge** |
|:---:|:---:|:---:|
| <img src="Images/Schematic_PushButtons.png" width="250"/> | <img src="Images/Schematic_OLED_Buzzer.png" width="250"/> | <img src="Images/Schematic_BatteryGauge.png" width="250"/> |

---

## 🖥 PCB Layout

| **Top Layer** | **Bottom Layer** |
|:---:|:---:|
| <img src="Images/PCB_Top_Layer.png" width="350"/> | <img src="Images/PCB_Bottom_Layer.png" width="350"/> |
---
## 📦Robot Shield – ATmega328P Controller
 ┣ 📂Altium_Project
 ┃ ┣ 📂robotShield.PcbDoc
 ┃ ┣ 📂robotShield.PrjPcb
 ┃ ┗ 📂robotShield.SchDoc
 ┣ 📂Images
 ┣ 📜.gitignore
 ┣ 📜README.md
 ┣ 📜LICENSE
 ┗ 📜Schematics.pdf

---
