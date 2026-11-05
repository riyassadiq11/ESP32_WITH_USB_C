# ESP32_WITH_USB_C (ALTIUM DESIGNER) 

## 📖 Project Overview
A custom 4-layer development board built around the ESP32-S3-MINI microcontroller, featuring modern USB-C connectivity and built-in USB-to-UART bridging. This project serves as a compact, fully featured prototyping platform designed with strict impedance control for high-speed data integrity. 

## 🛠️ Hardware Architecture & Circuit Blocks

The hardware design is broken down into several key sub-circuits:

* **Microcontroller:** Powered by the **ESP32-S3-MINI** module, providing robust Wi-Fi/Bluetooth capabilities and plenty of GPIO].
* **Power Management:** 
  * Integrates an TL1963A-33DCYR 5V-to-3.3V linear voltage regulator (LDO).
  * Includes dedicated 5V and 3V3 power selection headers for flexible power routing.
* **USB Interface & UART:** 
  * Features a modern USB-C connector with proper CC-pin pull-down resistors for host recognition and ESD protection diodes for hot-plug safety.
  * Utilizes an FTDI-series USB-to-UART bridge IC to handle reliable serial communication with the ESP32.
* **User Interface & Breakouts:**
  * Dual 24-pin headers expose the ESP32's GPIOs for easy breadboarding and peripheral connection.
  * Includes a dedicated Power LED (Green) and a programmable User LED (Red) tied to GPIO2.
  * Hardware boot and reset buttons are included for easy flashing and rebooting.

## 📏 PCB Layout & Specifications

This board was designed with a focus on signal integrity, utilizing a 4-layer stackup to ensure a solid return path and proper impedance matching for the USB data lines.

* **Board Dimensions:** 68.58 mm x 25.4 mm
* **Layer Stackup (4 Layers):**
  * **Top Layer:** Signal
  * **Inner Layer 1:** Signal
  * **Inner Layer 2:** Solid GND Plane (for signal return and thermal relief)
  * **Bottom Layer:** Signal
* **Impedance Control:**
  * **Single-Ended (50 Ω):** 6 mil trace width.
  * **Differential Pairs (90 Ω):** 6.03 mil trace width with 8 mil spacing (specifically calculated for USB data lines).

## 🧠 My Learning Journey

This project marks my transition into advanced PCB design. It is my first time using **Altium Designer**, and the experience allowed me to level up my hardware engineering skills significantly. 

**Key Takeaways from this project:**
1. **Component Library Management:** I successfully learned how to create custom schematic symbols and design accurate PCB footprints from scratch based on component datasheets.
2. **The Role of 0-Ohm Resistors:** I learned the practical applications of 0-ohm resistors. In this design, I used them strategically on the USB data lines to allow for hardware configuration, signal routing flexibility, and bridge isolation during testing.
3. **Advanced Design Rules:** I mastered the Altium Design Rule Check (DRC) system. Beyond just basic graphical menus, I learned how to modify and enforce design rules using Altium's query language (code-like commands) to specifically target differential pairs and custom clearance requirements.

## 🖼️ Schematic
![Schematic](Schematic%20(Img_Pdf)/Schematic.png)

