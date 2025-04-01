Home-Security-System
MPCA college project using PIR, temperature, and LDR sensors. Detects motion, tracks temperature, and measures light intensity. Built with Arduino for real-time environmental monitoring.
---

Smart Home Security & Environmental Monitoring System 
This project, developed for the MPCA college course, integrates four PIR sensors, one LDR sensor, and one temperature sensor to create a robust home security and environmental monitoring system. Built using an ESP8266 microcontroller, the system leverages Wi-Fi connectivity to interface with the Blynk IoT platform for real-time data visualization and alerts. Approximately 30 wires were used to connect the hardware components, including an active buzzer that activates upon motion detection.  

Project Overview  
The system monitors motion in four directions—front, back, left, and right—using four PIR sensors, measures ambient light intensity with an LDR sensor, and tracks temperature with a single temperature sensor. Data is transmitted to the Blynk Cloud, where it’s displayed on a custom web dashboard. An active buzzer provides audible alerts when motion is detected, enhancing security functionality. This project showcases sensor integration, IoT connectivity, and practical hardware implementation.

Hardware Components  
- 4 PIR Sensors: Detect motion in four zones (front, back, left, right).  
- 1 LDR Sensor: Measures light intensity for environmental awareness.  
- 1 Temperature Sensor**: Monitors ambient temperature.  
- ESP8266: Wi-Fi-enabled microcontroller for data processing and transmission.  
- Active Buzzer: Emits sound on motion detection.  
- Wires: Approximately 30 wires for connections.  

 Steps to Connect and Implement  
1. Setup Blynk Web Dashboard
   - Create a free account on Blynk Cloud.  
   - Click "New Template" and configure:  
     - Template Name: Home Security  
     - Hardware: ESP8266  
     - Connection: Wi-Fi  
   - In the **Datastreams** section, create:  
     - PIR Front (Virtual Pin V1, Integer)  
     - PIR Back (Virtual Pin V2, Integer)  
     - PIR Left (Virtual Pin V3, Integer)  
     - PIR Right (Virtual Pin V4, Integer)  
     - LDR Sensor (Virtual Pin V5, Integer)  
     - Temperature (Virtual Pin V6, Float)  
   - Go to Web Dashboard, click "Add Widget," and add:  
     - 4 LED Indicators (for PIR motion status)  
     - Gauge Widget (for LDR Sensor)  
     - Gauge Widget (for Temperature)  
     - Notifications Widget  
   - Save and retrieve the Blynk Auth Token (sent via email).  

2. Hardware Setup
   - Connect the four PIR sensors, LDR, temperature sensor, and active buzzer to the ESP8266 using ~30 wires.  
   - Program the ESP8266 to read sensor data and trigger the buzzer on motion detection.  

3. **Software Integration**  
   - Use the Blynk Auth Token in the ESP8266 code to link the hardware to the Blynk Cloud.  
   - Map sensor outputs to the respective virtual pins for real-time dashboard updates.  

Features  
- Motion detection across four zones with audible alerts via the buzzer.  
- Real-time light intensity and temperature monitoring.  
- Remote access and notifications through the Blynk web dashboard.  

This project demonstrates practical applications of IoT and sensor-based systems, suitable for home security and environmental monitoring scenarios.
