# Smart Greenhouse Monitoring & Automation System (IoT) 🌿📡

This repository contains the full network topology design, automated decision-logic configurations, and technical documentation for an **IoT-based Smart Greenhouse Monitoring System**. The project was modeled and simulated using **Cisco Packet Tracer** to achieve full environmental automation, safety management, and remote cloud telemetry.

---

## 📌 Project Overview
Traditional agricultural greenhouses require continuous manual supervision. This engineering project transforms manual management into a fully automated, energy-efficient IoT ecosystem. 

The system continuously senses micro-climate parameters (Temperature, Humidity, $\text{CO}_2$ concentration, Soil Moisture), monitors safety conditions (Fire/Smoke detection, RFID Access Control), and automatically triggers precise actuation responses based on predefined threshold rules.

---

## ⚙️ System Architecture & Subsystems

The smart greenhouse integrates eight core functional IoT modules:

1. **Temperature Control System:** Uses temperature sensors and thermostats to trigger air heating or cooling units dynamically.
2. **Humidity Management System:** Monitors relative air humidity and activates automated humidifiers when levels drop below thresholds.
3. **Soil Moisture & Automated Irrigation:** Tracks soil water levels and triggers high-efficiency lawn sprinklers when soil moisture is deficient.
4. **$\text{CO}_2$ Detection & Ventilation:** Monitors carbon dioxide levels and operates variable-speed exhaust fans (Low/High) to optimize plant growth conditions.
5. **Fire Safety & Hazard System:** Detects smoke/fire, instantly sounding security sirens and engaging overhead fire sprinklers.
6. **Smart RFID Access & Intrusion Security:** Integrates RFID card authentication, motion detectors, webcams, and automated door locks.
7. **Smart Lighting System:** Automatically controls greenhouse illumination based on door access states and user overrides via mobile interface.
8. **Solar Power Supply Subsystem:** Photovoltaic solar panels, power meters, and storage batteries provide clean power to all IoT sensors and actuators.

---

## 🌐 Network Topology & IP Addressing Scheme

The network uses a centralized router/switch backbone linked to an **IoT Server**, **DNS Server**, and **Central Office Server**, allowing full remote monitoring via a Smartphone interface over cellular/cloud gateways.

| Server / Device | IPv4 Address | Subnet Mask | Default Gateway | Function |
| :--- | :--- | :--- | :--- | :--- |
| **ISP Router** | `192.168.1.1` / `192.168.2.1` | `255.255.255.0` | — | Core Routing Backbone |
| **Central Office Server** | `192.168.1.6` | `255.255.255.0` | `192.168.1.1` | Cellular / Cloud Gateway |
| **DNS Server** | `192.168.2.2` | `255.255.255.0` | `192.168.2.1` | Domain Name Resolution |
| **IoT Server** | `192.168.2.3` | `255.255.255.0` | `192.168.2.1` | IoT Rules Engine & Telemetry |

---

## 🤖 Automated Decision Logic (Sample Rules)

* **Irrigation Control:** If `Soil Moisture <= 12.7 cm` $\rightarrow$ Turn Sprinklers **ON**. If `Soil Moisture >= 20.3 cm` $\rightarrow$ Turn Sprinklers **OFF**.
* **Thermostat Control:** If `Temperature >= 20.0°C` $\rightarrow$ Set Thermostats to **Cooling**. If `Temperature <= 0.0°C` $\rightarrow$ Set Thermostats to **Heating**.
* **$\text{CO}_2$ Exhaust Control:** If `$\text{CO}_2$ Level >= 2` $\rightarrow$ Set Fan to **High**. If `$\text{CO}_2$ Level <= 0.01` $\rightarrow$ Turn Fan **OFF**.
* **Security & Access:** Valid `RFID (ID=1001)` $\rightarrow$ Unlock Door, Activate Lights, Silence Siren. Invalid RFID + Motion $\rightarrow$ Trigger Alarm Siren & Lock Door.

---

## 💻 Software & Simulation Tools
* **Simulation Environment:** Cisco Packet Tracer 8.x
* **Network Protocols:** IP/DHCP, DNS, Cellular/Coaxial Infrastructure, IoT HTTP Telemetry

---

 Al-Baraa Amir Al-Zofi
* **Institution:** Department of Mechatronics, Faculty of Engineering & Technology, Al-Rasheed Smart University
* **Supervision:** Eng. Saeed Al-Sama'i
