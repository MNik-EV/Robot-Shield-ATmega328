Robot Shield - ATmega328P Controller
A comprehensive, open-source controller shield for robotics applications, built around the ATmega328P. This shield integrates robust power protection, dual battery monitoring, and multiple user interface options for building versatile robots.

🚀 Board Renders
Top View

Isometric View

Bottom View







📋 Table of Contents
Features & Specifications

System Architecture

Schematics

PCB Layout

File Structure

License

✨ Features & Specifications
Microcontroller: ATmega328P running at 16MHz.

Programming Interface: CP2102 chip with an Auto-Reset circuit for full Arduino IDE compatibility.

Protection: Robust input protection including a PTC Resettable Fuse, TVS Diode, and reverse polarity protection.

Power Supply: 12V input with regulated 5V (Buck Converter) and 3.3V (LDO) outputs.

Dual Battery Monitoring:

Visual 10-segment bar graph display with the LM3914.

High-precision digital gauging with the MAX17043 via I2C.

User Interfaces:

5 push-buttons with hardware debouncing circuits.

Connector for a 0.96" I2C OLED display.

Buzzer with a transistor driver circuit and a flyback diode.

Board Dimensions: 6cm x 8cm.

🏗️ System Architecture
<details>
<summary><strong>Click to view the detailed Block Diagram</strong></summary>

graph TD
    subgraph "External Sources"
        A[12V Battery]
        B[PC / USB Port]
    end

    subgraph "On-Board Power System"
        C{Power Supply & Protection Circuit}
        D[5V Regulated Rail]
        E[3.3V Regulated Rail]
    end

    subgraph "Robot Shield Controller"
        F(ATmega328P MCU)

        subgraph "Communication"
            G[CP2102 USB-to-UART]
        end

        subgraph "User Input"
            H[5x Push-Buttons]
        end
        
        subgraph "Battery Monitoring"
            I[MAX17043 I2C Fuel Gauge]
            J[LM3914 Visual LED Driver]
        end

        subgraph "User Feedback"
            K[OLED Display]
            L[Buzzer]
            M[10-Segment LED Bar]
        end
    end

    %% Define Power Flow
    A --> C
    C --> D & E
    D --> F & L & J
    E --> G & I & K

    %% Define Data & Control Flow
    B -- USB --> G
    G -- UART --> F
    H -- GPIO --> F
    F -- PWM --> L
    F -- I2C --> K
    F -- I2C --> I
    A -- Voltage Sense --> I & J
    J -- Drives --> M

</details>

⚡ Schematics
<details>
<summary><strong>Click to view all Schematic Modules</strong></summary>
<p align="center">
<em>Each schematic is a clickable link to the full-size image.</em>
</p>

Power Supply System

Microcontroller (MCU) & Core





CP2102 (USB-to-UART)

Push-Buttons





OLED & Buzzer Interfaces

Battery Fuel Gauge System





</details>

💻 PCB Layout
<details>
<summary><strong>Click to view PCB Layout Images</strong></summary>
<p align="center">
<em>Top and bottom copper layers of the 2-layer PCB design.</em>
</p>

Top Layer

Bottom Layer





</details>

📂 File Structure
/Altium_Project: Contains the main Altium project files (.PcbDoc, .SchDoc, .PrjPcb).

/Images: Contains all images used in this README.

📜 License
This project is licensed under the MIT License. See the LICENSE file for more details.
