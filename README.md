
# Data-Driven Vehicle Control Using CAN Protocol

## Project Overview

This embedded systems project demonstrates **data-driven vehicle control** via the **CAN (Controller Area Network) protocol**. The system involves real-time monitoring and control tasks such as engine temperature display, reverse alert, and window glass operation—simulated through LEDs—across multiple interconnected microcontroller nodes.

---

## Features

- 🚗 **Engine Temperature Display** using DS18B20 sensor
- 🛑 **Reverse Alert System** using GP2D12 proximity sensor
- 🪟 **Window Glass Control** using switch inputs and LED indicators
- 🔁 **CAN-Based Communication** between all functional nodes
- 📟 LCD Display for real-time feedback
- 🔔 Audible and visual alerts

---

## System Architecture

The project consists of **three nodes** connected over a CAN Bus:

### 1. Main Node
- Reads and displays engine temperature
- Sends control commands to Window Glass Node
- Receives reverse alerts from Reverse Alert Node
- Uses external interrupts to detect switch presses

### 2. Window Glass Control Node
- Receives commands from Main Node
- Simulates window movement with LEDs

### 3. Reverse Alert Node
- Reads distance using GP2D12 sensor
- Sends reverse alert signal (logic 1 or 0) to Main Node based on object proximity

---

## Hardware Requirements

- **LPC2129** Microcontroller
- **CAN Transceivers** (MCP2551)
- **DS18B20** Temperature Sensor
- **GP2D12** Infrared Proximity Sensor
- **LCD Display**
- **Switches** (SW, SW1, SW2)
- **LEDs** (for simulation)
- **USB to UART Converter**

---

## Software Requirements

- **Embedded C**
- **Keil uVision (Keil-C Compiler)**
- **Flash Magic** (for flashing code to MCU)

---

## Implementation Steps

1. **LCD Testing**: Display constants (char, string, integer).
2. **ADC Testing**: Read voltage from a potentiometer.
3. **Distance Measurement**: Interface and display data from GP2D12 sensor.
4. **Interrupts**: Test with increment logic and LCD output.
5. **Temperature Sensor**: Interface DS18B20 and show engine temperature.
6. **CAN Protocol**: Test basic CAN communication.
7. **Final Node Integration**:
   - **Main Node**: Read temperature, send window control, receive reverse alerts.
   - **Window Glass Node**: Light up LEDs based on control count.
   - **Reverse Alert Node**: Alert based on object distance.

---

## CAN Protocol Summary

- **MCP2551** used for CAN transceiving
- **CANH / CANL** lines interconnect all nodes
- Controlled messaging between nodes for synchronized operation

---

## How to Run

1. Program each microcontroller with its respective node code.
2. Power up all nodes and establish CAN connections.
3. Use switches and sensors to test each feature.
4. Observe the LED, LCD, and buzzer responses.

---

## Final Notes

If all modules function as expected and data exchange over CAN is successful, your project is complete!

**✨ Good luck and happy debugging! ✨**
