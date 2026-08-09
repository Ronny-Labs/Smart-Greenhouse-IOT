# TERRAVISION V1.0 - Smart Greenhouse Automation System 🌿🤖

![AI Smart Greenhouse prototype](docs/greenhouse-hero.jpg)

An automated microclimate and soil monitoring ecosystem built with Arduino Uno, real-time Bluetooth telemetry (HC-05), and environmental actuators to manage irrigation, ventilation, heating and grow lights.

---

## Quick links

- PROFORMA: [PROFORMA.md](PROFORMA.md)
- Wiring diagram: docs/circuit-diagram.png
- Code folder: code/

> Note: This is a learning project — I am still learning C++ and embedded systems. Contributions and feedback are welcome!

---

## Overview

TERRAVISION is a classroom-scale smart greenhouse prototype that monitors soil moisture, temperature & humidity, and light, and performs automated control over irrigation, ventilation, heating and supplemental lighting using an Arduino Uno and a 4-channel relay module.

---

## Embedded images & diagrams

Wiring diagram (full):

![Wiring diagram](docs/circuit-diagram.png)

Add high-resolution PDFs to docs/ if available (docs/circuit-diagram.pdf).

---

## Components (short)

- Arduino Uno
- DHT11 / SHT31 temperature & humidity sensor
- Capacitive soil moisture probe
- LDR (light sensor)
- 4-channel relay module
- 5V/12V mini submersible water pump
- 12V cooling fan
- LED grow strip
- 16x2 LCD with I2C backpack
- HC-05 Bluetooth module

---

## How to run (short)

1. Place hardware as shown in the wiring diagram.  
2. Open code/greenhouse.ino in the Arduino IDE.  
3. Edit any pin mappings or placeholders in the sketch (replace passwords with placeholders).  
4. Upload the sketch to the Arduino Uno.  
5. Use the serial monitor or a Bluetooth terminal app to read live sensor values.

---

## Repository layout

- docs/ — wiring diagrams, photos, thumbnails
- code/ — Arduino sketch(s) and supporting files (put greenhouse.ino here)
- PROFORMA.md — project proforma and write-up (already added)
- README.md — this file

---

## Add your files

When you are ready, add or upload these files to these paths:

- docs/greenhouse-hero.jpg  (prototype photo)
- docs/circuit-diagram.png  (wiring diagram)
- code/greenhouse.ino       (Arduino sketch)

I will embed images automatically when they appear at the paths above.

---

## Notes & safety

- Do not commit real Wi‑Fi passwords or API keys — use placeholders (WIFI_SSID, WIFI_PASS_PLACEHOLDER).  
- I will not modify your code files without your explicit approval.

---

## Credits

Project converted and documented by Pratyush Pallav Pathak (Ronny) — original team and credits preserved in PROFORMA.md.
