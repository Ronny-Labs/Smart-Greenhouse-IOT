# AI Smart Greenhouse - Wiring Diagram & Circuit Overview

## Circuit Diagram (Block Diagram)

This diagram illustrates the complete system architecture and component interconnections for the AI Smart Greenhouse.

### Click to view full diagram:
[![AI Smart Greenhouse Wiring Diagram - Circuit Diagram](./circuit-diagram-full.png)](./circuit-diagram-full.png)

---

## System Architecture Overview

### **Microcontroller Core**
- **Arduino UNO** — Main processing unit that orchestrates all sensor readings and actuator controls

### **Input Sensors**
1. **DHT11** (Temperature & Humidity Sensor) — Monitors ambient greenhouse conditions
2. **Soil Moisture Sensor** — Capacitive soil probe for precise moisture detection
3. **LDR (Light Sensor)** — Measures light intensity for grow light optimization

### **Output Actuators (via Relay Module)**
1. **Relay 1** — Controls the **5V Water Pump** for automated irrigation
2. **Relay 2** — Controls the **12V DC Fan** for ventilation and temperature control
3. **Relay 3** — Controls the **LED Grow Light** for photosynthesis optimization
4. **Relay 4** — Available for additional actuator expansion

### **Data Display & Communication**
- **16x2 LCD Display (with I2C)** — Real-time display of sensor readings and system status
- **HC-05 Bluetooth Module** — Wireless telemetry for remote monitoring via mobile app

### **Power Supply**
- **12V/2A Power Supply** — Main power source for relays and high-current devices
- **5V Step-down** — Powers Arduino UNO, sensors, and low-current components

### **Water Management System**
- **Rainwater Collection Tank** — Sustainable water source
- **Water Pump (5V)** — Controlled irrigation delivery
- **Drip Irrigation Pipes** — Precise water distribution to soil

---

## Signal Flow

```
┌──────────────────────────────────────────────────────────────┐
│                    SENSOR INPUTS                             │
│  ┌─────────┬──────────────┬──────────────┬─────────────┐    │
│  │ DHT11   │ Soil Moisture│ LDR Sensor   │ Other I/O   │    │
│  └────┬────┴──────┬───────┴──────┬───────┴─────┬───────┘    │
│       │           │              │             │            │
│       └───────────┴──────────────┴─────────────┘            │
│                      │                                       │
│                      ▼                                       │
│            ┌──────────────────┐                             │
│            │   ARDUINO UNO    │                             │
│            │  (Brain/Logic)   │                             │
│            └────────┬─────────┘                             │
│                     │                                       │
│     ┌───────────────┼───────────────┐                       │
│     │               │               │                       │
│     ▼               ▼               ▼                       │
│  ┌────────────┐  ┌─────────┐  ┌──��───────────────┐        │
│  │ LCD 16x2   │  │ HC-05   │  │  4-CH Relay Mod  │        │
│  │ (I2C)      │  │(BT Tx)  │  │  ┌────┬────┬─────┤        │
│  └────────────┘  └─────────┘  │  │ R1 │ R2 │ R3  │ R4    │
│                                  └────┴────┴─────┘        │
│                                   │    │    │    │         │
│     ┌─────────────────────────────┼────┼────┼────┘         │
│     │                             │    │    │              │
│     ▼                             ▼    ▼    ▼              │
│  ┌──────────┐              ┌────────────────────┐         │
│  │  12V PSU │              │  ACTUATORS & LOAD  │         │
│  │ (2A)     │─────────────│ ┌────┬──────┬────┐ │         │
│  └──────────┘              │ │Pump│ Fan │ LED│ │         │
│                             │ └────┴──────┴────┘ │         │
│                             └────────────────────┘         │
└──────────────────────────────────────────────────────────────┘
```

---

## Component Connections Summary

| Component | Connection | Pin/Protocol | Notes |
|-----------|-----------|--------------|-------|
| **DHT11** | Arduino | Analog/Digital | Temperature & Humidity |
| **Soil Moisture** | Arduino ADC | A0-A3 | Capacitive probe |
| **LDR** | Arduino ADC | Analog pin | Light intensity |
| **LCD 16x2** | Arduino | I2C (SDA/SCL) | Address: 0x27 |
| **HC-05 BT** | Arduino | Serial (RX/TX) | Wireless monitoring |
| **Relay Module** | Arduino | Digital pins | 4-channel relay |
| **Water Pump** | Relay 1 | 12V DC | ~5V logic signal |
| **DC Fan** | Relay 2 | 12V DC | ~5V logic signal |
| **LED Grow Light** | Relay 3 | 12V DC | ~5V logic signal |
| **Power Supply** | System | 12V/2A | Main power rails |

---

## Features Enabled by This Wiring

✅ **Automatic Irrigation** — Soil moisture-based water pump control  
✅ **Temperature Control** — DHT11 + fan relay for climate management  
✅ **Grow Light Automation** — LDR-based LED light scheduling  
✅ **Remote Monitoring** — Real-time data via Bluetooth (HC-05)  
✅ **LCD Dashboard** — On-site status display  
✅ **Sustainable** — Rainwater harvesting integration  
✅ **Eco-Friendly** — Efficient resource management  

---

## Safety & Best Practices

⚠️ **Power Management**
- Always use a regulated 12V/2A PSU for relay loads
- Never exceed Arduino pin current limits (40mA max per pin)
- Use relay module to isolate high-current devices from Arduino

⚠️ **Water Safety**
- Use submersible pump rated for continuous operation
- Install water-level cutoff to prevent pump dry-run
- Drain system if not in use for extended periods

⚠️ **Electrical Safety**
- Wear safety glasses when working with high-voltage components
- Verify polarity before powering on
- Use proper cable gauges for power distribution

---

## Further Documentation

- See **PROFORMA.md** for project history and team credits
- See **README.md** for project overview
- See **/code** folder for Arduino sketches and firmware

---

**Last Updated:** 2026-08-14  
**Model:** AI Smart Greenhouse v1.0 (TERRAVISION)  
**Status:** Science Exhibition Ready ✓
