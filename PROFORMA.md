# Project Proforma — TERRAVISION

**Project title:** TERRAVISION — An AI-Assisted Closed-Loop Intelligent Sustainable Farming Ecosystem

**Sub-theme:** Sustainable Agriculture (CBSE / RBVP Guidelines)

**Contributing students:**
- Team Leader / Lead Presenter: Ganesh Kharga
- Team Members: Debadutta Roy, Pratyush Pallav Pathak, Krishna Prasad, Zubaida Tabassum, Anmol Shah, Deep Das, Darshana Kalita

**Guiding Teacher:** Mrs. Neetu Shaw

**School:** Jawahar Navodaya Vidyalaya (JNV), Rangia, Kamrup, Assam

**Type of exhibit:** Working model

**Space / dark room:** Recommended 1.5 m × 1.5 m; dark room required for LDR & LED grow light demonstration

---

## 13. Brief summary

TERRAVISION is an autonomous, eco-friendly smart farming prototype designed to address pressing agricultural challenges through precision automation and closed-loop resource management. Developed specifically to aid small and medium-scale rural farmers, the system continuously monitors vital environmental parameters — including soil moisture, ambient micro-climate temperature, relative humidity, and solar illuminance — using specialized electronic sensors.

Driven by an embedded microcontroller running threshold-based decision logic, TERRAVISION automatically executes targeted micro-drip irrigation, micro-climate ventilation, thermal regulation, and supplemental Photosynthetically Active Radiation (PAR) lighting. The system integrates rainwater harvesting, multi-stage greywater filtration, and organic composting for closed-loop nutrient recycling, with live telemetry broadcast to a Bluetooth smartphone application.

---

## 14. Detailed write-up

### Introduction

Agriculture is the backbone of the Indian economy, yet traditional farming faces severe threats from climate change, groundwater depletion, erratic weather, topsoil degradation, and high labour costs. TERRAVISION demonstrates how rural smallholders can adopt scalable, eco-friendly automation to maximise crop yield, build resilience against extreme micro-climates, and conserve natural resources.

### Purpose of the Model

- Water Conservation: Eliminate agricultural water waste via sensor-driven closed-loop micro-drip irrigation.
- Micro-Climate Automation: Automate greenhouse temperature, relative humidity, and light levels to shield crops from heatwaves and overnight frosts.
- Resource Optimization: Demonstrate closed-loop recycling through rainwater harvesting, greywater filtration, and organic composting.
- Rural Accessibility: Design a low-cost technology stack suitable for smallholders using off-the-shelf electronics.
- Real-Time Telemetry: Provide farmers with accessible wireless monitoring tools via a custom smartphone interface.

### Scientific Principles

1. Soil Moisture Dynamics & Dielectric Sensing: Measure Volumetric Water Content (VWC) using electrical resistance/capacitance to prevent underwatering and root rot.
2. Micro-Climate Psychrometrics: Monitor humidity and temperature to compute Vapor Pressure Deficit (VPD) and mitigate fungal disease risk.
3. Thermal Radiation & Resistive Heating: Use a resistive thermal element as a bench-top substitute for 12V PTC heating to demonstrate frost mitigation.
4. PAR & Photo-Transduction: Use LDRs to trigger supplementary LED grow spectra during low ambient PAR.
5. Embedded Hysteresis Control: Implement decision logic in the microcontroller to switch relays cleanly and avoid mechanical chatter.
6. Opto-Isolated Electromechanical Switching: Control high-power AC/DC loads via low-voltage logic using relay modules.
7. Hydrological & Biochemical Recycling: Combine gravity sand/carbon filtration and aerobic composting for nutrient recycling.

### Materials Used

**Electronics & Embedded Hardware**
- Arduino Uno (ATmega328P)
- SHT31 / DHT11 Temperature & Humidity sensor (depending on availability)
- Capacitive Soil Moisture Probe
- PAR LDR Probe
- HC-05 Bluetooth Module
- 16x2 LCD with I2C interface
- 4-channel opto-isolated relay module (5V)
- 5V/12V mini submersible water pump
- 12V DC cooling fan
- LED grow light strip (12V)
- Regulated power supply (12V / 5V DC)
- Misc: jumper wires, breadboard, terminal blocks, connectors

**Model & Structural Materials**
- High-density foam board / sunboard base
- Transparent acrylic sheeting (greenhouse canopy)
- Plastic water reservoirs & tubing
- Micro-tubing & drip emitters
- Gravel / sand / activated carbon filter column
- Aerated compost module and miniature crop bed

### Construction & System Architecture

The system architecture uses sensors (soil moisture, temperature/humidity, LDR) as inputs to the Arduino Uno MCU. The MCU runs a closed-loop feedback control implementing hysteresis thresholds and drives a multi-channel relay module to control irrigation pump, grow lights, heating element and exhaust fan. Telemetry is broadcast via an HC-05 Bluetooth module to a companion smartphone app.

(See the converted wiring diagram in docs/circuit-diagram.png for full pin and power distribution.)

### Integrated Control Logic Sequence

1. Hydration Loop: When root-zone VWC drops below the calibrated threshold (~30%), the MCU energises the irrigation pump via relay to deliver targeted drip irrigation.
2. Thermal Regulation Loop: If ambient temperature drops below a low threshold (~18°C), the MCU enables the heating element to raise greenhouse temperature (used for frost simulation in the model).
3. Ventilation & Humidity Loop: When temperature exceeds ~35°C or relative humidity rises above ~85%, MCU activates exhaust fan to prevent heat shock and fungal rot.
4. Photoperiod Loop: If ambient light falls below LDR threshold during daytime hours, MCU activates LED grow lights to maintain photosynthetic activity.
5. Recycling & Telemetry: Greywater passes through gravel/sand/carbon filters into the main tank; sensor values are logged to LCD and streamed over Bluetooth.

---

## Applications

- Precision agriculture & commercial polyhouses
- Rural smallholder climate defense
- Urban rooftop & kitchen gardening
- High-value floriculture & seedling nurseries

## Advantages

- Reduces freshwater consumption (project estimates up to 50%)
- Protects crops from extreme frosts and heatwaves
- Demand-driven automation reduces energy and water waste
- Low setup cost for a prototype model

## Future scope

- Upgrade thermal radiator to under-bed PTC heating
- Integrate AI/ML machine vision (ESP32-CAM) for disease detection
- Solar PV + battery integration for 100% off-grid operation
- ESP32 / SIM800L cellular cloud IoT integration
- Automated NPK fertigation using solenoid dosing

---

## Conclusion

TERRAVISION demonstrates how affordable embedded electronics, precision automation, and ecological practices can be unified into a sustainable agricultural framework. By replacing wasteful conventional methods with automated micro-climate control, targeted irrigation, greywater recycling, and wireless monitoring, TERRAVISION offers a practical, scalable, and economically viable solution for smallholder farmers.
