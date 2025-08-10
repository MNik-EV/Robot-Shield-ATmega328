# Robot Shield - ATmega328P Controller

This repository contains the design files for a  robot controller shield based on the ATmega328P microcontroller.

![Isometric board view](Images/Isometric_View_3D.png)

## ✨ Features & Specifications

* **Microcontroller:** ATmega328P running at **16MHz**.
* **Programming Interface:** **CP2102** chip with an **Auto-Reset** circuit for full Arduino IDE compatibility.
* **Protection:** Robust input protection including a PTC Resettable Fuse, TVS Diode, and reverse polarity protection.
* **Power Supply:** 12V input with regulated 5V (Buck Converter) and 3.3V (LDO) outputs.
* **Dual Battery Monitoring:**
    * Visual 10-segment bar graph display with the **LM3914**.
    * High-precision digital gauging with the **MAX17043** via I2C.
* **User Interfaces:**
    * 5 push-buttons with hardware debouncing circuits.
    * Connector for a 0.96" I2C OLED display.
    * Buzzer with a transistor driver circuit and a flyback diode.
* **Board Dimensions:** 6cm x 8cm.

##  System Architecture

!(Images/Block_Diagram.png)

---

## ⚡ Schematics

The schematic design is modular to simplify understanding and debugging. Click on any image to view it in full size.

| Power Supply System | Microcontroller (MCU) & Core |
| :---: | :---: |
| [![Power Supply Schematic](Images/Schematic_Power.png)](Images/Schematic_Power.png) | [![MCU Schematic](Images/Schematic_MCU.png)](Images/Schematic_MCU.png) |
| **CP2102 (USB-to-UART)** | **Push-Buttons** |
| [![CP2102 Schematic](Images/Schematic_CP2102.png)](Images/Schematic_CP2102.png) | [![Push-Buttons Schematic](Images/Schematic_PushButtons.png)](Images/Schematic_PushButtons.png) |
| **OLED & Buzzer Interfaces** | **Battery Fuel Gauge System** |
| [![OLED and Buzzer Schematic](Images/Schematic_OLED_Buzzer.png)](Images/Schematic_OLED_Buzzer.png) | [![Battery Gauge Schematic](Images/Schematic_BatteryGauge.png)](Images/Schematic_BatteryGauge.png) |

---

##  PCB Layout

The PCB is a two-layer design that utilizes ground planes on both layers and via stitching to reduce noise and ensure signal integrity.

| 3D Top View | 3D Bottom View |
| :---: | :---: |
| !(Images/Top_View_3D.png) | !(Images/Bottom_View_3D.png) |

| Top Layer | Bottom Layer |
| :---: | :---: |
| !(Images/PCB_Top_Layer.png) | !(Images/PCB_Bottom_Layer.png) |


## 📂 File Structure

* **/Altium_Project:** Contains the main Altium project files (`.PcbDoc`, `.SchDoc`, `.PrjPcb`).
* **/Images:** Contains all images used in this README.

##  License

This project is licensed under the **MIT License**. See the `LICENSE` file for more details.
