# Smart-GreenhousE-IOT
my class 10 science exhibition greenhouse model arduino code
# TERRAVISION V1.0 - Smart Greenhouse Automation System 🌿🤖

An automated microclimate and soil monitoring ecosystem built with Arduino Uno, real-time wireless Bluetooth telemetry, and dynamic environmental actuators.

## 🚀 Key Features
* **Automated Irrigation:** Dual-threshold soil moisture sensing for automatic watering.
* **Climate Ventilation:** Temperature and humidity threshold monitoring driving forced-air ventilation.
* **Light Automation:** Adaptive grow lighting triggered by ambient Light Dependent Resistor (LDR) values.
* **Hydro Management & Safety:** Tank level detection with safety refill logic and buzzer alert integration.
* **Dual Monitoring:** Local 16x2 I2C LCD dashboard + live Bluetooth data streaming.

## 📌 Pinout Connections
| Module / Sensor | Arduino Pin |
| :--- | :--- |
| DHT11 Sensor | Digital Pin 2 |
| Active Buzzer | Digital Pin 7 |
| Relay 1 (Irrigation Pump) | Digital Pin 8 |
| Relay 2 (LED Grow Light) | Digital Pin 9 |
| Relay 3 (Refill Pump) | Digital Pin 10 |
| Relay 4 (Cooling Fan) | Digital Pin 11 |
| HC-05 Bluetooth (TX/RX) | Digital Pins 12, 13 |
| Soil Moisture Sensor | Analog Pin A0 |
| Light Sensor (LDR) | Analog Pin A1 |
| Water Level Sensor | Analog Pin A2 |
| TDS Water Quality Sensor | Analog Pin A3 |
