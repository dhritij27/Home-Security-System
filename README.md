Home-Security-System
MPCA college project using PIR, temperature, and LDR sensors. Detects motion, tracks temperature, and measures light intensity. Built with Arduino for real-time environmental monitoring.
---

Smart Home Security & Environmental Monitoring System 
This project, developed for the MPCA college course, integrates four PIR sensors, one LDR sensor, and one temperature sensor to create a robust home security and environmental monitoring system. Built using an ESP8266 microcontroller, the system leverages Wi-Fi connectivity to interface with the Blynk IoT platform for real-time data visualization and alerts. Approximately 30 wires were used to connect the hardware components, including an active buzzer that activates upon motion detection.  

Below is a README file tailored for your GitHub repository based on the details you provided. It’s structured for clarity and includes all the specifics about your MPCA project.

---

# Smart Home Security & Environmental Monitoring System

This repository contains the code, setup instructions, and documentation for a hardware project developed as part of the MPCA college course. The system integrates **four PIR sensors**, **one LDR sensor**, and **one temperature sensor** with an **ESP8266 microcontroller** to provide real-time home security and environmental monitoring. An **active buzzer** alerts users to motion, and data is visualized via the **Blynk IoT platform**.

## Project Overview

The system monitors motion in four zones (front, back, left, right) using four PIR sensors, measures ambient light with an LDR sensor, and tracks temperature with a temperature sensor. Connected via Wi-Fi through the ESP8266, it sends data to a custom Blynk dashboard. Approximately **30 wires** tie the components together, and an active buzzer sounds when motion is detected.

## Hardware Components

- **4 PIR Sensors**: Detect motion in four directions (front, back, left, right).  
- **1 LDR Sensor**: Measures ambient light intensity.  
- **1 Temperature Sensor**: Monitors room temperature.  
- **ESP8266**: Wi-Fi-enabled microcontroller for processing and connectivity.  
- **Active Buzzer**: Sounds an alert on motion detection.  
- **Wires**: ~30 wires for connections.

## Features

- Motion detection across four zones with audible buzzer alerts.  
- Real-time light intensity and temperature tracking.  
- Remote monitoring and notifications via Blynk dashboard.

## Setup Instructions

### 1. Configure Blynk Web Dashboard
- Create a free account on [Blynk Cloud](https://blynk.io/).  
- Click **"New Template"** and set:  
  - **Template Name**: Home Security  
  - **Hardware**: ESP8266  
  - **Connection**: Wi-Fi  
- In **Datastreams**, create:  
  - **PIR Front** (Virtual Pin V1, Type: Integer)  
  - **PIR Back** (Virtual Pin V2, Type: Integer)  
  - **PIR Left** (Virtual Pin V3, Type: Integer)  
  - **PIR Right** (Virtual Pin V4, Type: Integer)  
  - **LDR Sensor** (Virtual Pin V5, Type: Integer)  
  - **Temperature** (Virtual Pin V6, Type: Float)  
- Go to **Web Dashboard**, click **"Add Widget"**, and add:  
  - 4 LED Indicators (for PIR motion status)  
  - Gauge Widget (for LDR Sensor)  
  - Gauge Widget (for Temperature)  
  - Notifications Widget  
- Click **Save** and note the **Blynk Auth Token** (sent via email).

### 2. Hardware Assembly
- Connect the four PIR sensors, LDR sensor, temperature sensor, and active buzzer to the ESP8266 using ~30 wires.  
- Ensure proper pin mapping (refer to the code for pin assignments).  

### 3. Software Setup
- Install the [Blynk Library](https://github.com/blynkkk/blynk-library) for Arduino IDE.  
- Update the code with your **Blynk Auth Token**, Wi-Fi SSID, and password.  
- Program the ESP8266 to:  
  - Read sensor data.  
  - Trigger the buzzer on motion detection.  
  - Send data to Blynk virtual pins (V1-V6).

## Installation

1. Clone this repository:  
   ```bash
   git clone <repository-url>
   ```
2. Open the `.ino` file in Arduino IDE.  
3. Upload the code to your ESP8266 after connecting the hardware.  
4. Monitor the system via the Blynk dashboard.

## Usage

- Power the ESP8266 to start monitoring.  
- Check the Blynk dashboard for real-time updates:  
  - LED indicators light up when motion is detected.  
  - Gauges display light and temperature values.  
  - Notifications alert you to motion events.  
- The buzzer will sound whenever a PIR sensor detects movement.

## Contributing

This is a college project, but feel free to fork and adapt it! Submit pull requests or open issues for suggestions.

## License

This project is licensed under the [https://www.apache.org/licenses/LICENSE-2.0](Apache 2.0 License)

---

